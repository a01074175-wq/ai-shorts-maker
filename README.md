

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Shorts Maker</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background: #090d18;
  color: white;
  min-height: 100vh;
}

header {
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #263149;
}

.logo {
  font-size: 21px;
  font-weight: bold;
  color: #a78bfa;
}

.logo span {
  color: white;
}

main {
  width: 92%;
  max-width: 650px;
  margin: 35px auto;
}

.hero {
  text-align: center;
  margin-bottom: 30px;
}

.hero h1 {
  font-size: 32px;
  margin-bottom: 12px;
}

.hero h1 span {
  color: #a78bfa;
}

.hero p {
  color: #9ca3af;
  line-height: 1.6;
}

.panel {
  background: #151c2e;
  border: 1px solid #29344d;
  border-radius: 17px;
  padding: 20px;
  margin-bottom: 20px;
}

.upload {
  border: 2px dashed #6654bb;
  border-radius: 13px;
  padding: 35px 15px;
  text-align: center;
  cursor: pointer;
  background: #1b2140;
}

.upload .icon {
  font-size: 42px;
  margin-bottom: 12px;
}

.upload h3 {
  margin-bottom: 9px;
}

.upload p {
  color: #a5adc0;
  font-size: 13px;
  margin-top: 5px;
}

input[type=file] {
  display: none;
}

video {
  width: 100%;
  max-height: 350px;
  margin-top: 18px;
  border-radius: 12px;
  background: black;
}

.file-info {
  margin-top: 12px;
  color: #c4b5fd;
  font-size: 13px;
  overflow-wrap: anywhere;
}

label {
  display: block;
  margin: 18px 0 9px;
  font-weight: bold;
  font-size: 14px;
}

select {
  width: 100%;
  padding: 14px;
  border-radius: 9px;
  background: #0e1526;
  border: 1px solid #35415c;
  color: white;
  font-size: 15px;
}

button {
  width: 100%;
  padding: 16px;
  margin-top: 22px;
  border: none;
  border-radius: 10px;
  background: linear-gradient(90deg,#7354e8,#a855f7);
  color: white;
  font-size: 16px;
  font-weight: bold;
  cursor: pointer;
}

button:disabled {
  opacity: .5;
  cursor: not-allowed;
}

.status {
  color: #a5adc0;
  font-size: 13px;
  margin-top: 15px;
  text-align: center;
  line-height: 1.6;
}

.features {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
}

.feature {
  background: #151c2e;
  border: 1px solid #29344d;
  border-radius: 12px;
  padding: 16px;
  font-size: 14px;
}

.feature p {
  color: #9ca3af;
  margin-top: 7px;
  font-size: 12px;
}

.voice-title {
  color: #c4b5fd;
  font-size: 21px;
}

.voice-note {
  background: #0e1526;
  border: 1px solid #35415c;
  border-radius: 10px;
  padding: 13px;
  margin-top: 15px;
  color: #a5adc0;
  font-size: 12px;
  line-height: 1.6;
}

footer {
  text-align: center;
  color: #7e899e;
  padding: 25px;
  font-size: 12px;
}

@media(max-width:380px) {
  .hero h1 {
    font-size: 26px;
  }
}
</style>
</head>

<body>

<header>
  <div class="logo">AI <span>SHORTS MAKER</span></div>
  <div>✦ AI</div>
</header>

<main>

<section class="hero">
  <h1>Long Video to <span>Shorts</span></h1>
  <p>Upload your video and prepare for AI-powered Shorts.</p>
</section>

<!-- VIDEO UPLOAD -->

<section class="panel">

  <h2>📁 Video Upload</h2>

  <label>Upload Your Video</label>

  <label class="upload" for="videoFile">
    <div class="icon">☁️</div>
    <h3>Choose Video File</h3>
    <p>Tap here to select a video from your phone</p>
    <p>MP4, MOV, WEBM (browser supported formats)</p>
  </label>

  <input type="file" id="videoFile" accept="video/*">

  <video id="preview" controls hidden></video>

  <div class="file-info" id="fileInfo">
    No video selected
  </div>

  <label for="caption">Caption Language</label>

  <select id="caption">
    <option value="both">English + Hindi</option>
    <option value="english">English</option>
    <option value="hindi">Hindi</option>
  </select>

  <label for="duration">Short Video Duration</label>

  <select id="duration">
    <option value="60">60 Seconds</option>
    <option value="75">75 Seconds</option>
    <option value="90" selected>90 Seconds</option>
  </select>

  <label for="format">Video Format</label>

  <select id="format">
    <option value="9:16">Vertical 9:16</option>
  </select>

  <button id="startBtn" disabled>
    AI Shorts Processing (Coming Soon)
  </button>

  <div class="status" id="status">
    Upload and preview are ready.
    AI cutting and caption engine will be connected later.
  </div>

</section>

<!-- AI VOICE CHANGER -->

<section class="panel" id="voiceStudio">

  <h2 class="voice-title">🎙️ AI Voice Studio</h2>

  <p style="color:#9ca3af;margin-top:10px">
    Transform your video audio using different AI voices.
  </p>

  <label for="aiVoice">Select AI Voice</label>

  <select id="aiVoice">
    <option value="male-natural">Male Natural</option>
    <option value="female-natural">Female Natural</option>
    <option value="male-deep">Male Deep</option>
    <option value="female-soft">Female Soft</option>
    <option value="ai-narrator">AI Narrator</option>
  </select>

  <label for="voiceMode">Voice Conversion Mode</label>

  <select id="voiceMode">
    <option value="live">Real-time AI Voice Conversion</option>
    <option value="export">Convert and Export Video</option>
  </select>

  <label for="voiceSpeed">Voice Speed</label>

  <select id="voiceSpeed">
    <option value="0.9">Slow</option>
    <option value="1" selected>Normal</option>
    <option value="1.1">Fast</option>
  </select>

  <button id="voiceBtn" type="button">
    Connect AI Voice Engine
  </button>

  <div class="status" id="voiceStatus">
    AI Voice Engine is waiting for backend integration.
  </div>

  <div class="voice-note">
    Note: Voice selection is ready. Actual AI voice conversion
    requires a separate AI model and processing backend.
  </div>

</section>

<!-- FEATURES -->

<section class="features">

  <div class="feature">
    <h3>✂️ Auto Cutting</h3>
    <p>AI video moment detection.</p>
  </div>

  <div class="feature">
    <h3>💬 AI Captions</h3>
    <p>English and Hindi subtitles.</p>
  </div>

  <div class="feature">
    <h3>📱 9:16 Format</h3>
    <p>Vertical Shorts videos.</p>
  </div>

  <div class="feature">
    <h3>🎙️ AI Voice</h3>
    <p>Multiple synthetic voices.</p>
  </div>

  <div class="feature">
    <h3>⚡ AI Editing</h3>
    <p>Automatic video editing.</p>
  </div>

  <div class="feature">
    <h3>⬇️ Download</h3>
    <p>Download finished Shorts.</p>
  </div>

</section>

</main>

<footer>
  AI Shorts Maker © 2026 | Made for Creators
</footer>

<script>

// VIDEO UPLOAD

const input = document.getElementById("videoFile");
const preview = document.getElementById("preview");
const fileInfo = document.getElementById("fileInfo");
const startBtn = document.getElementById("startBtn");

let currentURL = null;

input.addEventListener("change", function() {

  const file = this.files[0];

  if (!file) return;

  if (!file.type.startsWith("video/")) {
    fileInfo.textContent = "Please select a valid video.";
    return;
  }

  if (currentURL) {
    URL.revokeObjectURL(currentURL);
  }

  currentURL = URL.createObjectURL(file);

  preview.src = currentURL;
  preview.hidden = false;

  fileInfo.textContent =
    "Selected: " + file.name +
    " | Size: " +
    (file.size / (1024 * 1024)).toFixed(2) + " MB";

  startBtn.disabled = true;

  preview.onloadedmetadata = function() {

    const mins = Math.floor(preview.duration / 60);
    const secs = Math.floor(preview.duration % 60);

    fileInfo.textContent +=
      " | Length: " + mins + "m " + secs + "s";

    startBtn.disabled = false;

    startBtn.textContent =
      "AI Shorts Processing (Coming Soon)";
  };

  preview.onerror = function() {
    fileInfo.textContent =
      "Unable to preview this video format.";
    startBtn.disabled = true;
  };

});

// AI SHORTS BUTTON

startBtn.addEventListener("click", function() {

  document.getElementById("status").textContent =
    "AI cutting engine is not connected yet. This feature will be added in Phase 2.";

});

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
    URL.revokeObjectURL(currentURL);
  }

});

</script>

</body>
</html>

< 