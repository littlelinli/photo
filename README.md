# function upDate(previewPic) {
    // Логируем информацию о событии
    console.log("Mouse over image: ", previewPic);
    console.log("Image source: ", previewPic.src);
    console.log("Alt text: ", previewPic.alt);

    // Обновляем текст и фон div с id="image"
    let imageDiv = document.getElementById("image");
    imageDiv.style.backgroundImage = "url(" + previewPic.src + ")";
    imageDiv.innerHTML = previewPic.alt;
}

function undo() {
    // Возвращаем исходное состояние
    let imageDiv = document.getElementById("image");
    imageDiv.style.backgroundImage = "url('')";
    imageDiv.innerHTML = "Hover over an image below to display here.";
}
