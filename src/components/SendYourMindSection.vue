<script setup>

const womenModal = () => {
   const isOpen = document.querySelector("#women-modal");
   isOpen.showModal();
}

const menModal = () => {
   const isOpen = document.querySelector("#men-modal");
   isOpen.showModal();
}

const modalClose = (_name, event) => {
   const targetModal = document.querySelector(_name);
   let rect = event.target.getBoundingClientRect();

   if (rect.left > event.clientX ||
       rect.right < event.clientX ||
       rect.top > event.clientY ||
       rect.bottom < event.clientY
   ) {
     targetModal.close();
   }
}

const copyButton = (person, val) => {
  if (typeof(navigator.clipboard)=='undefined') {
    var textArea = document.createElement("textarea");
    textArea.value = val;
    textArea.style.position="fixed";  //avoid scrolling to bottom
    document.body.appendChild(textArea);
    textArea.focus();
    textArea.select();
    document.body.removeChild(textArea)
    return;
  }
  navigator.clipboard.writeText(val);

  const el = document.querySelector("#"+person);
  el.innerHTML = "복사되었습니다.";
  el.enabled = false;
  el.style.background = "#000000"
  el.style.color = "#FFFFFF"
  setTimeout(() => {
    el.innerHTML = "계좌번호 복사하기";
    el.style.background = "#efefef"
    el.style.color = "#202121"
    el.enabled = true;
  }, 4000);
}

const closeModal = (name) => {
  const targetModal = document.querySelector("#"+name);
  targetModal.close();
}
</script>

<template>
  <section id="sendyourmind-section">
    <h1 style="font-size: 20px;">마음을 전해주실 곳</h1>
    <p style="padding-top: 20px;">"신랑신부에게 축하의 마음을 전해주세요"</p>
    <p style="padding-top: 20px;">
      <button class="modal-button" @click="menModal">신랑측 계좌번호</button>
    </p>
    <p style="padding-top: 20px;">
      <button class="modal-button" @click="womenModal">신부측 계좌번호</button>
    </p>
    <dialog id="men-modal" @click="modalClose('#men-modal', $event)">
      <div class="dialog-header">
        <h1>🤵🏽 신랑측 마음 전하실 곳</h1>
      </div>
      <div class="dialog-body">
        <div class="dialog-body-unit">
          <p class="name">신랑 : 김도령</p>
          <p class="number">국민은행 77130201501464</p>
          <p>
            <button class="copy-button" id="men_person" @click="copyButton('men_person', '국민은행 77130201501464')">계좌번호 복사하기</button>
          </p>
        </div>
        <div class="divide"></div>
        <div class="dialog-body-unit">
          <p class="name">신랑 아버지: 김종수</p>
          <p class="number">우체국 50126202062303</p>
          <p>
            <button class="copy-button" id="mem_father_person" @click="copyButton('mem_father_person', '우체국 50126202062303')">계좌번호 복사하기</button>
          </p>
        </div>
        <div class="divide"></div>
        <div class="dialog-body-unit">
          <p class="name">신랑 어머니: 강정희</p>
          <p class="number">농협 65303752086505</p>
          <p>
            <button class="copy-button" id="mem_mother_person" @click="copyButton('mem_mother_person', '농협 65303752086505')">계좌번호 복사하기</button>
          </p>
        </div>
      </div>
      <div class="divide"></div>
      <div class="dialog-footer">
        <p style="padding-top: 10px">
          <button @click="closeModal('men-modal')">나가기</button>
        </p>
      </div>
    </dialog>
    <dialog id="women-modal" @click="modalClose('#women-modal', $event)">
      <div class="dialog-header">
        <h1>👰🏻신부측 마음 전하실 곳</h1>
      </div>
      <div class="dialog-body">
        <div class="dialog-body-unit">
          <p class="name">신부 : 강유민</p>
          <p class="number">국민은행 77130201501464</p>
          <p>
            <button class="copy-button" id="women_person" @click="copyButton('women_person', '국민은행 77130201501464')">계좌번호 복사하기</button>
          </p>
        </div>
        <div class="divide"></div>
        <div class="dialog-body-unit">
          <p class="name">신부 아버지: 강희구</p>
          <p class="number">농협 3511278276423</p>
          <p>
            <button class="copy-button" id="women_father_person" @click="copyButton('women_father_person', '농협 3511278276423')">계좌번호 복사하기</button>
          </p>
        </div>
        <div class="divide"></div>
        <div class="dialog-body-unit">
          <p class="name">신부 어머니: 신지윤</p>
          <p class="number">신협 132094642299</p>
          <p>
            <button class="copy-button" id="women_mother_person" @click="copyButton('women_mother_person', '신협 132094642299')">계좌번호 복사하기</button>
          </p>
        </div>
      </div>
      <div class="divide"></div>
      <div class="dialog-footer">
        <p style="padding-top: 10px">
          <button @click="closeModal('women-modal')">나가기</button>
        </p>
      </div>
    </dialog>
  </section>
</template>
<style scoped>
  #sendyourmind-section {
    padding-top: 50px;
    padding-bottom: 100px;
    text-align: center;
  }
  .modal-button {
    cursor: pointer;
    font-size: 20px;
    border-radius: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 50px;
    padding-right: 50px;
    color: #202121;
  }
  .modal-button:active {
    background-color: #e5e4e4;
  }
  .divide {
    margin-top: 10px;
    border-top: 1px solid #bbb;
  }
  dialog {
    border: none !important;
    border-radius: calc(5px * var(--ratio));
    box-shadow: 0 0 #0000, 0 0 #0000, 0 25px 50px -12px rgba(0, 0, 0, 0.25);
    padding: 1.6rem;
    max-width: 480px;
  }
  .dialog-header h1 {
    margin: 1rem 0 0.5rem;
    font-size: 30px;
    font-weight: 900;
  }
  dialog .dialog-header {
    width: 100%;
    display: flex;
    justify-content: space-between;
  }
  dialog .dialog-body {
    text-align: left;
  }
  .dialog-body p {
    padding-top: 10px;
    font-size: 20px;
  }
  .dialog-body .dialog-body-unit {
    margin: 20px;
  }
  .dialog-body .dialog-body-unit .name{
    font-weight: bold;
  }
  .dialog-body .dialog-body-unit .number{
    font-weight: lighter;
  }
  .dialog-body .dialog-body-unit .copy-button {
    width: 100%;
    border-radius: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 50px;
    padding-right: 50px;
    color: #202121;
  }
  .copy-button:active {
    background-color: #e5e4e4;
  }
  .dialog-footer button {
    font-weight: bold;
    font-size: 20px;
    width: 100%;
    border-radius: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 50px;
    padding-right: 50px;
    background: #D0E7F7;
  }
</style>
