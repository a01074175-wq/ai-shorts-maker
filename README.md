

<

// AI VOICE CHANGER

const voiceBtn = document.getElementById("voiceBtn");
const voiceStatus = document.getElementById("voiceStatus");

voiceBtn.addEventListener("click", function() {

  const video = document.getElementById("videoFile").files[0];

  if (!video) {
    voiceStatus.textContent =
      "Please upload a video first.";
    return;
  }

  const selectedVoice =
    document.getElementById("aiVoice").value;

  const mode =
    document.getElementById("voiceMode").value;

  const speed =
    document.getElementById("voiceSpeed").value;

  voiceStatus.textContent =
    "Selected voice: " + selectedVoice +
    " | Mode: " + mode +
    " | Speed: " + speed +
    " | AI conversion backend is not connected yet.";

});

// CLEANUP

window.addEventListener("beforeunload", function() {

  if (currentURL) {
    URL.revok
