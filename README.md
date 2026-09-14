// Wait until the web DOM layers are fully operational
document.addEventListener("DOMContentLoaded", function() {
    
    // Acquire tracking nodes for the modal elements
    const lightbox = document.getElementById("lightbox");
    const lightboxImg = document.getElementById("lightbox-img");
    const lightboxCaption = document.getElementById("lightbox-caption");
    const closeBtn = document.querySelector(".lightbox-close");
    
    // Select all product images optimized with the action selector class
    const clickableImages = document.querySelectorAll(".clickable-image");

    // Assign interactive click tracking across catalog photos
    clickableImages.forEach(image => {
        image.addEventListener("click", function() {
            lightbox.style.display = "flex";
            lightboxImg.src = this.src;
            lightboxCaption.textContent = this.alt;
        });
    });

    // Dismiss the photo box popup when close token indicator is tapped
    closeBtn.addEventListener("click", function() {
        lightbox.style.display = "none";
    });

    // Dismiss the photo box layer instantly if the outer backdrop area is tapped
    lightbox.addEventListener("click", function(e) {
        if (e.target === lightbox) {
            lightbox.style.display = "none";
        }
    });
});

