# DjTaha


![cat image](https://github.com/tahahamdii/ShoppingCart/blob/main/party.png)

# Description : 

You can change the playsound function with this to keep it playing everytime you keydown xd
```
function playSound(e) {
  const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
  const key = document.querySelector(`div[data-key="${e.keyCode}"]`);
  if (!audio) return;

  key.classList.add('playing');
  audio.currentTime = 0;
  audio.loop = true;
  audio.play();

  let count = 1;
  const interval = setInterval(function() {
    if (count === 8) {
      clearInterval(interval);
      key.classList.remove('playing');
      audio.loop = false;
      audio.pause();
    }
    count++;
  }, audio.duration * 1000);
}

```
