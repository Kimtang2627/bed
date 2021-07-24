<template>
  <div class="chat-wrapper">
    <div class="inbox-container">
      <span>INBOX ({{ mess.length }})</span>

      <button>
        <svg
          width="12"
          height="12"
          viewBox="0 0 12 12"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M10.6665 5.33341H6.6665V1.33341C6.6665 1.1566 6.59627 0.987035 6.47124 0.86201C6.34622 0.736986 6.17665 0.666748 5.99984 0.666748C5.82303 0.666748 5.65346 0.736986 5.52843 0.86201C5.40341 0.987035 5.33317 1.1566 5.33317 1.33341V5.33341H1.33317C1.15636 5.33341 0.98679 5.40365 0.861766 5.52868C0.736742 5.6537 0.666504 5.82327 0.666504 6.00008C0.666504 6.17689 0.736742 6.34646 0.861766 6.47149C0.98679 6.59651 1.15636 6.66675 1.33317 6.66675H5.33317V10.6667C5.33317 10.8436 5.40341 11.0131 5.52843 11.1382C5.65346 11.2632 5.82303 11.3334 5.99984 11.3334C6.17665 11.3334 6.34622 11.2632 6.47124 11.1382C6.59627 11.0131 6.6665 10.8436 6.6665 10.6667V6.66675H10.6665C10.8433 6.66675 11.0129 6.59651 11.1379 6.47149C11.2629 6.34646 11.3332 6.17689 11.3332 6.00008C11.3332 5.82327 11.2629 5.6537 11.1379 5.52868C11.0129 5.40365 10.8433 5.33341 10.6665 5.33341Z"
            fill="#ED702D"
          />
        </svg>
      </button>
    </div>
    <div class="box-container flex" v-for="(me, index) in mess" :key="index">
      <div class="border flex ">
        <div :class="[mess[index].name === 'Kate Nash' ? 'pink' : 'yellow' ]" > 
          {{mess[index].message}} </div>
          <div class="name-wrapper flex">
        <div class="picture-wrapper flex">
          <!-- Profile Picture -->
         
          
          <!-- Profile Name  -->
          <div class="name-container flex">{{ mess[index].name }}</div>
        </div>

        <!-- Profile Time  -->
        <span class="time "> 7:32 pm</span>
      </div>

      <span class="message-wrapper">
        {{ mess[index].message }}
      </span>
      </div>
    
    </div>
  </div>
</template>

<script>
export default {
  name: "box",
  data() {
    return {
      mess: [
        {
          name: "Kate Nash",
          message:
            "This example when you run into someone the text line will be lklkgldkfldf;lsdfk;sdkfop3ek;ldkfopefgkegejgpoejjepokldfglsdkfgjopis "
        },
        {
          name: "Ethel Hanson",
          message:
            "This example wheomeone the text line will be lklkgldkfldf;lsdfk;sdkfop3ek;ldkfopefgkegejgpoejjepokldfglsdkfgjopis "
        },
        {
          name: "Alan Perry",
          message:
            "This example when you run into someone the text line will be lklkgldkfldf;lsdfk;sdkfop3ek;ldkfopefgkegejgpoejjepokldfglsdkfgjopis "
        },
        {
          name: "Kate Nash",
          message:
            "This example when you run into someone the text line will be lklkgldkfldf;lsdfk;sdkfop3ek;ldkfopefgkegejgpoejjepokldfglsdkfgjopis "
        }
      ]
    };
  }
};
</script>

<style lang="scss">

.chat-wrapper {

  margin-top: 1rem;
  .inbox-container {
    font-weight: 600;
    margin-bottom: 0.3125rem;
    color: #ed702d;

    justify-content: space-between;
    border-radius: 0.625rem;
    display: flex;
    align-items: center;
    margin-top: 1rem;
    background-color: #ffffff;
    width: 18rem;
    height: 2.75rem;

    span {
      padding-left: 1.5rem;
    }

    button {
      background-color: rgba($color: #ffc3a3, $alpha: 0.2);
      border: none;
      border-radius: 0.625rem;
      width: 2rem;
      height: 2rem;
      margin-right: 0.5rem;
    }
  }
  ////////// Box Container ////////////////
  // .box-container:hover{
  //   border-right: orange 3px solid ;
    
  // }
  .box-container {
    margin-bottom: 0.5rem;
    height: 7.5rem;
    justify-content: center;

    background-color: white;
    border-radius: 0.625rem;
    width: 18rem;
    flex-direction: column;
    .border:hover{
      border-right: 0.1875rem solid orange;
    }
    .border{
      justify-content: center;
      height: 95%;
      width: 100%;
      margin: 0 auto;
      overflow: hidden;
      text-align: start;
      flex-direction: column;

        .pink{
          color: pink;
        }

        .yellow{
          color: yellow;
        }
    }

   
    .message-wrapper {
      overflow: hidden;
      font-size: 0.875rem;
      width: 16rem;
      padding-left: 1.375rem;
      padding-top: 0.25rem;
      opacity: 0.4;
    }
   
    .name-wrapper {
      width: 17.5rem;
      align-items: center;
      justify-content: space-around;

      .picture-wrapper {
        width: 17.5rem;
        font-size: 1rem;
        margin-right: 1rem;
        font-weight: bold;
        flex: 2;

        align-content: center;
        //

        justify-content: space-evenly;
        align-items: center;

        .name-container {
          //  margin-right: 15px;
          width: 5.9375rem;
        }
      }

      .time {
        flex: 1;
        opacity: 0.3;
        font-size: 0.875rem;
        text-align: center;
      }
    }
  }
}
</style>
