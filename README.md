<style>

.loading-svg {
  width: 100%;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.loading-svg-animation {
  stroke-width: 1.5px;
  stroke: #f3ca9f;
  width: 100%;
  height: 100%;
  stroke-dashoffset: 100;
  stroke-dasharray: 100;
  animation: svganimation 30s ease-in-out forwards infinite;
}

.animated-svg {
  width: 300px;
  height: 200px;
  background-color: rgb(0, 0, 0);
  border-radius: 125px;
  top: 90%;
  left: 51%;
  position: fixed;
  transform: translate(-50%, -50%);
}

.traço {
  stroke-width: 0.7px;
  stroke: #e61809;
  width: 100%;
  height: 100%;
  stroke-dashoffset: 1000;
  stroke-dasharray: 1000;
  animation: svganimation 5s ease-in-out forwards infinite;
}

.maleus {
  stroke-width: 0.7px;
  stroke: #e0380e;
  width: 100%;
  height: 100%;
  stroke-dashoffset: 300;
  stroke-dasharray: 1850;
  animation: svganimation 5s ease-in-out forwards infinite;
}

.pereira {
  stroke-width: 0.8px;
  stroke: #d16c0e;
  width: 100%;
  height: 100%;
  stroke-dashoffset: 1000;
  stroke-dasharray: 1000;
  animation: svganimation 5s ease-in-out forwards infinite;
}

.barra {
  stroke-width: 1px;
  stroke: #d1a40e;
  width: 100%;
  height: 100%;
  stroke-dashoffset: 1000;
  stroke-dasharray: 1000;
  animation: svganimation 5s ease-in-out forwards infinite;
}

@keyframes svganimation {
  0% {
    stroke-dashoffset: 2000;
  }
  70% {
    stroke-dashoffset: 200;
  }
  100% {
    stroke-dashoffset: 0;
  }
}

.glow-on-hover {
  width: 310px;
  height: 210px;
  border: none;
  outline: none;
  color: #fff;
  background: #111;
  cursor: pointer;
  z-index: 0;
  border-radius: 125px;
}

.glow-on-hover:before {
  content: "";
  background: linear-gradient(
    45deg,
    #ff0000,
    #ff7300,
    #fffb00,
    #48ff00,
    #00ffd5,
    #002bff,
    #7a00ff,
    #ff00c8,
    #ff0000
  );
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 400%;
  z-index: -1;
  filter: blur(5px);
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  animation: glowing 20s linear infinite;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
  border-radius: 125px;
}

.glow-on-hover:active {
  color: #000;
}

.glow-on-hover:active:after {
  background: transparent;
}

.glow-on-hover:hover:before {
  opacity: 1;
}

.glow-on-hover:after {
  z-index: -1;
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: #111;
  left: 0;
  top: 0;
  border-radius: 125px;
}

@keyframes glowing {
  0% {
    background-position: 0 0;
  }
  50% {
    background-position: 400% 0;
  }
  100% {
    background-position: 0 0;
  }
}
  
</style>

<div id="SVG" className="animated-svg glow-on-hover">
      <svg
        width={width ? width : "300"}
        height={height ? height : "300"}
        viewBox={viewBox ? viewBox : "0 105 200 200"}
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          className="maleus"
          d="M70.56 115.746c-.005-.001-.015.002-.03.01-.394.222-.76.42-1.112.606-5.29 1.379-5.828.62-6.23 3.69-.116 1.362-.327 2.714-.394 4.08-.008 1.697-.014 3.396-.141 5.09a50.869 50.869 0 01-1.237 7.732c-.926 3.371-2.174 6.644-3.652 9.814-1.309 2.762-2.702 5.506-4.474 8.002a17.544 17.544 0 01-3.487-.541c-1.428-.467-2.858-.98-4.012-1.978-.787-.655-1.44-1.443-2.044-2.267.142-3.485.222-6.972.281-10.459.045-3.483.01-6.966.008-10.448.017-2.53.061-5.058.07-7.587 0-4.563.867-4.372-3.499-1.483-3.116 1.12-3.545.92-3.535 2.412-.228 2.774-.63 5.53-.943 8.296-.496 3.363-.779 6.744-.976 10.135-.12 2.356-.147 4.716-.16 7.074.041 1.731.412 3.402 1.205 4.94.264.4.537.793.82 1.179-.026.659-.056 1.318-.09 1.977-.267 4.512-.533 9.038-1.206 13.511-.614 3.66-1.232 7.336-2.442 10.857-1.157 3.457-2.404 6.89-3.886 10.221-.65 1.327-1.352 2.634-2.232 3.81-1.458-.006-2.92-.03-4.363-.252-1.292-.257-2.327-.692-3.15-1.77-.613-.814-1.3-1.616-1.496-2.647-.169-1.232-.247-2.452 0-3.685.248-1.378.626-2.735 1.303-3.971l-7.226 3.269c-.58 1.331-.937 2.734-1.16 4.164-.25 1.31-.077 2.6.103 3.901.242 1.152.983 2.082 1.667 3.006.918 1.18 2.078 1.82 3.497 2.202 1.678.36 3.4.367 5.107.39 1.157.076 2.267-.101 3.277-.692 7.494-4.388 5.414-2.365 8.074-5.108 1.654-1.641 2.702-3.722 3.64-5.825 1.377-3.366 2.603-6.794 3.732-10.25 1.196-3.568 1.826-7.278 2.426-10.98.329-2.506.538-5.026.701-7.549l.015.006c1.715.544 3.512.74 5.304.757 4.283-.264 8.358-2.959 10.875-6.388 1.545-2.15 2.824-4.468 3.994-6.838a273.95 273.95 0 00-.127 5.574c.004 2.94.024 5.878.04 8.816.017 3.418.016 6.836-.015 10.254-.004 2.468-.033 4.936-.041 7.404.167 1.832.249 3.677.508 5.499.12.733.226 1.47.323 2.207l6.969-3.676c-.112-.73-.232-1.458-.35-2.187-.231-1.787-.365-3.59-.496-5.386-.008-2.454-.037-4.908-.041-7.362a751.267 751.267 0 01-.021-10.236c.014-2.953.024-5.906.06-8.859.011-2.722.036-5.443.178-8.162.179-3.191.399-6.382.304-9.58.007-3.546.005-7.094-.026-10.64-.003-.204-.031-3.82-.187-3.775-.077.022-.142.038-.216.06.125-.183.251-.359.217-.366zm35.775 2.467c-.843-.06-2.468 1.63-6.924 4.296-.538 2.181-.546 4.442-.806 6.663-.3 2.187-.433 4.39-.504 6.596-.035 2.178-.043 4.355-.06 6.533-.019 1.64-.01 3.279-.007 4.918a434.88 434.88 0 00-.007 4.391c.007 1.903.024 3.807.041 5.71-.006 2.121-.01 4.242-.023 6.364-.012 1.41-.025 2.818-.032 4.227l.083.603.722-.378a69.139 69.139 0 01-1.043 3.579 9.917 9.917 0 01-1.001-.221 5.24 5.24 0 01-2.424-1.981c-.504-.96-.53-2.095-.541-3.158-.017-1.855-.021-3.71-.091-5.564-.014-.284-.015-.57-.042-.852-.01-.102.008-.258.016-.4-.115.063-.231.123-.347.185.05-.135.098-.252.129-.275.045-.034.169-.002.222.034.006-.166-.013-.295-.13-.254-7.902 2.754-6.53.971-7.572 4.533-.234 1.013-.275 2.033-.363 3.063-.74-.105-1.48-.22-2.223-.308-1.057-.144-2.05-.364-2.662-1.328-.472-.925-.241-1.978-.296-2.985-.01-1.059-.032-2.119.033-3.176.05-.494.123-.975.276-1.42 1.248-.27 2.5-.417 3.814-.259l6.423-4.667a20.293 20.293 0 00-5.724.598c-3.74 1.204-8.64 3.524-10.987 6.047-.705.948-.816 2.098-.878 3.238-.031 1.078-.01 2.157 0 3.236.004 1.287-.142 2.122.469 3.309.71 1.146 1.799 1.651 3.066 1.93 1.33.176 2.651.409 3.983.565 2.096.22 4.065-.516 5.892-1.606-.02 1.185.093 2.395.657 3.45.674 1.047 1.628 1.826 2.72 2.397 1.439.557 3 .641 4.525.715 3.385-.031 5.575-2.436 8.65-4.418.348-.224.927-2.058 1.05-2.417.868-2.78 1.53-5.622 2.257-8.443 1.086-3.401 2.198-6.79 2.92-10.29.504-2.856.676-5.755.752-8.649.095-2.284.014-4.556-.166-6.832-.2-2.212-.432-4.432-.8-6.623a463.78 463.78 0 00-1.537-6.997c-.672-2.527-.855-3.632-1.51-3.678zm-12.64 41.27l-.003.055.018-.01c.023-.012.01-.029-.014-.045zm6.326-36.965c.127.009.134.195.165.338-.044.02-.087.043-.13.064-.122.057-.169-.41-.035-.402zM56.934 154.09c.022.001-.429.302-.608.383-.07.03-.14.056-.21.079.259-.148.517-.297.778-.442a.185.185 0 01.04-.02zm63.516 3.565c-2.618.033-5.669 2.283-6.136 4.837-.264 2.17-.165 4.348-.023 6.521.18 1.403.327 2.819.604 4.206-.209.304-.43.6-.668.887-.17.205-.339.414-.508.622a6.656 6.656 0 01-2.603-1.257l-6.719 4.221c1.186.896 2.529 1.453 3.977 1.744 2.689.24 5.296-1.514 7.54-3.065.46.782 1.101 1.436 1.817 2.045.968.946 2.165 1.448 3.469 1.716 1.384.186 2.794.277 4.178.06 2.493-.862 4.27-1.517 5.554-2.27.138.594.349 1.171.671 1.723a15.629 15.629 0 002.459 2.486c.995.97 2.062 1.823 3.27 2.51 1.677.836 3.515.925 5.35.791 1.003-.133 1.992-.412 2.868-.934 2.272-1.353 3.771-2.023 4.908-2.626.087.95.509 1.764.958 2.605.575.822 1.259 1.55 1.723 2.446.436 1.329 1.087 2.56 1.768 3.776.837 1.395 1.68 2.863 3.121 3.695 6.3 1.087 8.66-4.794 10.472-8.987.816-2.154 1.568-4.328 2.17-6.545 1.322.263 2.675.338 4.021.375 1.404.002 2.784-.046 4.146.323 1.31.547 2.344 1.598 3.371 2.55 1.802 1.587 2.957 3.7 4.125 5.761 1.263 2.264 2.38 4.61 3.087 7.108.526 2.177.665 4.398.386 6.614-.327 1.593-.737 3.258-1.817 4.529a8.94 8.94 0 01-1.099 1.051c-.64.266-1.284.519-1.926.775-1.683.712-3.423 1.19-5.248 1.291-2.366-.166-3.914-2.116-5.275-3.859-1.356-1.931-2.128-4.184-2.703-6.454-.148-.685-.276-1.377-.306-2.065 1.013-.058 1.889.264 2.76.769.758.553 1.218 1.42 1.565 2.275.043.15.209.688.199.846-.007.109-.086.2-.129.3l6.34-4.07-6.212 4.952c4.778-2.995 7.961-2.166 6.714-5.903-.431-.995-.99-1.98-1.833-2.68-.944-.636-1.974-1.194-3.148-1.122-1.322-.002-2.649-.018-3.965.113-3.355.487-.697.028-7.947 4.137-.658.372-.986 1.151-1.213 1.824-.282 1.466-.059 2.923.3 4.361.68 2.342 1.53 4.66 2.928 6.68 1.474 1.902 3.104 4.007 5.585 4.512 1.903.066 3.723-.372 5.48-1.103 5.001-1.998 9.927-4.293 14.19-7.672.857-.77 1.387-1.153 2.046-2.093.993-1.415 1.381-3.182 1.684-4.849.222-2.315.07-4.629-.529-6.885-.763-2.541-1.933-4.918-3.216-7.236-1.18-2.138-2.341-4.332-4.145-6.02-1.084-1.064-2.207-2.143-3.536-2.893-.191-.059-1.108-.347-1.285-.383-.991-.204-2.013-.017-3.014-.084-1.645-.027-3.303-.064-4.916-.429-1.343-.42-2.703-.968-3.403-2.27-.503-1.165-.833-2.388-1.039-3.635-.068-.896-.127-1.792-.194-2.687-.01-.131.081-.457-.035-.394l-.042.022c-.155-.65-.722.039-2.946 1.448-3.388 1.478-4.075 1.049-4.06 2.263-.011.02-.005.047.004.076.01.316.056.728.116 1.312.072.555.157 1.107.257 1.656.155 2.457.059 4.917-.393 7.344-.555 2.717-1.374 5.366-2.36 7.956a8.31 8.31 0 00-.331-.508c-.66-1.227-1.258-2.473-1.703-3.795-.47-.892-1.095-1.665-1.714-2.456-.442-.837-.857-1.631-.84-2.611-.014-1.877-.023-3.754-.054-5.63-.029-2.413-.018-4.837-.292-7.237-.102-.505-.154-.95-.384-1.416-.021-.043-.046-.08-.069-.12.404-.3.38-.298-.026-.047-1.615-2.712-6.788 1.169-7.769 3.778-.365 1.163-.438 2.403-.552 3.61.019 1.51.043 3.02-.03 4.527-.127 1.876-.278 3.809-1.091 5.52-1.108.008-2.205-.148-3.26-.58a11.753 11.753 0 01-3.172-2.4 17.722 17.722 0 01-2.315-2.244c-.833-1.393-.804-3.026-.854-4.609-.145-3.39-.273-6.793-.808-10.15-.043-.147-.355-1.23-.729-1.917l-.098.065.088-.084c-.207-.375-.432-.628-.64-.527-3.872 1.88-6.7 1.913-7.395 5.146-.092 1.053-.086 2.116-.278 3.16-.192 1.077-.345 2.146-.248 3.247.013 1.76.016 3.525-.214 5.273l-.042.243c-1.048-.178-2.026-.528-2.813-1.304-.988-.773-1.761-1.662-2.13-2.887-.12-.348-.22-.7-.313-1.055.74-1.105 1.259-2.327 1.844-3.523.598-1.426.938-2.932.9-4.478-.197-1.3-.79-2.493-1.564-3.543-.712-.78-1.67-1.106-2.694-1.093zm15.587 1.34l.01.02c3.14-2.116 1.354-1.279-.01-.02zm-59.097-.1c-.35.202-.667.388-1.051.605-.215.121.41-.277.627-.393.14-.074.282-.142.424-.211zm38.568 3.453h.004c-.122.068-.234.132-.36.2-.083.045.13-.147.219-.176a.507.507 0 01.137-.024zm13.79.95l-.143.089c-.048.03.064-.065.144-.089zm20.476 4.315a.074.074 0 01.04.006l-.136.081c-.009.005.035-.078.096-.087zm-47.482 3.958c.13-.072-.104.07-.322.183.108-.06.215-.123.322-.183zm48.165 8.664v.055c-.16.076-.304.139-.432.185l.432-.24zM30.869 193.374c.026-.001-.54.368-.753.492-.326.191-.573.323-.851.414.492-.282.986-.566 1.554-.881a.269.269 0 01.05-.025zm142.318.227c-.001.003-.01.01-.027.02-.345.206-.674.4-.994.587.156-.157.33-.286.536-.396.128-.069.49-.229.485-.21z"
        />
        <path
          className="traço"
          d="M83.877 137.59c2.062.121 4.098.443 6.115.876 3.2.904 6.374 1.877 9.62 2.61 3.436.73 6.938 1.018 10.438 1.21 1.377.094 2.742.098 4.111-.072l6.26-4.713c-1.352.299-2.702.337-4.085.257-3.512-.094-7.028-.321-10.48-1.012-3.217-.709-6.329-1.734-9.473-2.706a40.59 40.59 0 00-6.047-1.021l-6.46 4.571z"
        />
        <path
          className="pereira"
          d="M68.473 175.126l-2.224 1.348c.45.5.195.264.775.696 1.753.886 3.712 1.027 5.651 1.073 3.488.152 6.984.116 10.464.416 2.15.245 4.826.36 6.506 1.944.192.181.328.414.492.621.494 1.3.617 2.612.309 3.98-.318 1.532-.794 3.042-1.516 4.434-1.003 1.324-.374.277.967-.004.371-.078-.648.396-.992.557-1.577.737-3.295 1.14-4.978 1.548-1.002.178-2.006.352-3.014.506a5504.442 5504.442 0 00.002-6.43v-1.512l-2.325 1.185v6.048l.003 1.012c-.614.061-1.229.106-1.846.128-3.114.112-.451-.132-2.762-.078-.324.008-.646.055-.97.082-2.175.426-2.558.67-4.859 2.103-.594.37-.88 1.015-.984 1.672.22 1.481 1.102 2.79 2.306 3.666 1.182.519 2.364.677 3.652.595l2.12-1.54c-1.297.085-2.416 0-3.63-.486-1.15-.78-2.024-2.037-2.153-3.44.117-.33.159-.512.302-.725.093-.039.186-.078.25-.095.317-.085.642-.14.964-.21.317-.033.633-.085.951-.1.933-.046 1.87.056 2.804.012a41.335 41.335 0 003.858-.392v.269c.004 1.046.006 2.092.013 3.138.003 1.666-.006 3.332-.082 4.996-.097 1.737-.196 3.493-.617 5.187l2.354-1.128c.34-1.711.454-3.465.544-5.205.077-1.672.087-3.346.099-5.02.007-.867.005-1.734.005-2.601.361-.06.722-.12 1.083-.182 3.523-.725 5.914-1.621 8.809-3.867.226-.175.32-.473.48-.71a20.213 20.213 0 001.483-4.537c.311-1.415.143-2.774-.38-4.108-.18-.228-.33-.483-.54-.684-1.735-1.663-4.452-1.802-6.693-2.057-3.473-.306-6.962-.28-10.442-.453-1.891-.067-3.81-.18-5.53-1.028-.534-.388-.302-.176-.709-.624zm36.303 17.287c-1.165.037-2.273 1.172-2.512 2.29a40.105 40.105 0 01-1.96 4.558c-.472.798-1.018 1.525-1.685 2.144a3.981 3.981 0 01-.864-.044c-.767-.11-1.5-.32-2.226-.589-.56-.242-1.077-.565-1.462-1.028.278-.197.515-.366.832-.582 1.28-1.655 2.31-3.715 2.197-5.856-.321-.93-1.049-.917-1.837-.592-1.808.998-2.915 1.547-3.993 3.141-.423.864-.57 1.825-.52 2.779.047.707.387 1.33.734 1.934-.402.07-.808.113-1.201.126-.167.006-.334-.004-.501-.006l-2.12 1.539c1.895.014 3.07-.36 4.254-1.043.395.443.899.768 1.442 1.03.736.29 1.487.515 2.266.648 1.986.3 2.636-.576 4.55-1.718 1.078-.768 1.857-1.777 2.48-2.93a52.297 52.297 0 001.681-3.888c.47.117.948.199 1.43.257.768.093 1.536.08 2.305.03.112.024.316.023.368.174.105.306-.389 1.873-.471 2.216-.378 1.444-.52 2.924-.59 4.41.004 1.411.33 2.802 1.051 4.017.561.796 1.588 1.428 2.6 1.407.189-.004.371-.074.557-.111l2.677-1.614-.791.315c.716-.39 1.409-.836 2.115-1.269.062.058.122.117.186.173a6.24 6.24 0 002.515 1.168c2.015.391 3.15-.797 4.952-1.873.385-.418.725-.862 1.035-1.324.06 1.218.237 2.43.48 3.63a8.024 8.024 0 001.658 3.373c.573.597 1.323.765 2.113.845 1.816.154 2.984-.965 4.526-1.916 1.677-2.224 2.035-4.674 2.476-7.352.103-.499.165-1.004.225-1.51.41.237.833.45 1.283.622.825.288 1.696.327 2.56.348.706.039 1.47-.629 2.146-.31.287 1.402.026 2.875-.093 4.286a94.033 94.033 0 00-.281 5.12c.05.943.078 1.9.64 2.69.605.585 1.483.662 2.286.646.547-.058 1.04-.27 1.526-.51l2.038-1.632c-.473.247-.933.497-1.465.599-.716.071-1.551.027-2.137-.433-.545-.72-.52-1.66-.584-2.526.036-1.7.107-3.399.259-5.092.127-1.444.473-3.172.015-4.565-.088-.066-.162-.158-.264-.199-.626-.252-1.364.36-1.977.4-.845-.014-1.698-.03-2.514-.275-1.006-.349-1.901-.895-2.715-1.583-.85.375-1.722.704-2.55 1.125-.168.084-.22.594-.232.678-.149 1.068-.201 2.15-.396 3.211-.39 2.332-.795 4.716-2.195 6.65-.159.02-.314.027-.453.012-.733-.05-1.453-.14-2.009-.672-.812-.922-1.348-2.042-1.63-3.237-.404-1.966-.633-3.963-.382-5.968.015-.245.039-.488.045-.733.004-.167.152-.524-.013-.5l-.152.022c.022-.05.04-.078.057-.11-.08.047-.16.092-.242.137-1.97.285-1.932.336-2.361 1.6-.62 1.765-1.389 3.494-2.639 4.895-.3.021-.597-.019-.897-.058a5.845 5.845 0 01-2.456-1.047 7.857 7.857 0 01-.64-.607c.146-.207.289-.417.43-.626.529-.793.775-1.691.9-2.623.126-.77-.186-1.475-.504-2.156-.287-.598-.35-1.405-1.156-1.426-.821.57-1.715 1.047-2.464 1.709-.168.148-.137.427-.195.644-.274 1.022-.397 2.063-.431 3.118.011.956.418 1.748.99 2.439a7.615 7.615 0 01-.965 1.11c-.273.11-.538.205-.733.238l-.65.49c-.759-.14-1.453-.481-1.885-1.14-.71-1.166-.999-2.517-.992-3.877.08-1.47.234-2.935.609-4.364.122-.487.264-.97.372-1.461.13-.594.196-1.152-.48-1.363-.761.024-1.521.116-2.286.006-.785-.078-1.569-.199-2.304-.497a1.772 1.772 0 00-.806-.163zm21.786 5.023c.04-.023.08-.043.12-.067.027-.016-.072-.008-.092.016-.008.009-.02.036-.028.051zm-21.475-4.716l-.163.096.003-.005c.037-.05.213-.123.16-.091zm-10.707 1.31c.172.059.318.198.417.462.076 1.542-.475 3.031-1.294 4.334-.227-.434-.416-.886-.442-1.384-.028-.91.125-1.83.593-2.623.18-.24.457-.524.726-.788zm20.787 2.941c.014.001.028.007.042.01-.095.052-.189.107-.285.153.055-.051.092-.132.164-.153a.229.229 0 01.08-.01zm21.177.102c.015-.003.017 0 0 .011l-.248.162c.008-.016.014-.032.023-.047.034-.053.183-.117.225-.126zm-20.1 2.087c.101.35.147.712.072 1.096-.012.08-.027.16-.042.24a3.16 3.16 0 01-.072-.66c.01-.225.024-.45.041-.676zm34.961 2.856c-.406.004-.779.052-1.037.184-.967.496-1.881 1.09-2.822 1.634-1.327 1.389-1.537 2.577-1.283 4.423.074.282.025.631.223.845.275.3.686.465 1.08.567 1.966.513 3.968-.561 5.632-1.455.434-.104 1.255-.99 1.811-.739.393.177.293 1.458.306 1.696-.019 1.802-.047 3.599.225 5.384.227.999.455 1.516 1.443 1.873 2.035.525 3.55-.83 5.265-1.82.991-.714 1.674-1.738 2.109-2.866l.126-.452-2.352 1.114-.133.427c-.343.811-.817 1.555-1.452 2.152a2.005 2.005 0 01-.14.034c-.422.08-.85.015-1.265-.057-.94-.26-1.09-.69-1.317-1.614-.29-1.771-.263-3.557-.234-5.348-.023-.53.101-1.648-.449-2.025-.617-.423-1.495.476-1.982.659-1.636.929-3.51 1.992-5.476 1.637-.335-.06-.709-.142-.944-.388-.194-.202-.14-.543-.21-.814-.158-1.46-.028-2.493.785-3.504.623-.055 1.248.01 1.866.113l2.144-1.504c-.476-.048-1.243-.163-1.919-.156zm-35.983 1.932a4.516 4.516 0 01-.045.024l.045-.024z"
        />
        <path
          className="barra"
          d="M97.585 182.637l-1.672 2.628 52.77 9.316 7.478 6.448-5.84-9.35-52.736-9.042z"
        />
      </svg>
    </div>


