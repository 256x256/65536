# [Linux][Chromium] mousemove to out of the window left or top with mousedown, X or Y coords get 65536.

Chromium-based browsers on my Ubuntu,
mousemove to out of the window left or top with mousedown,
X coordinate or Y coordinate are large value(s) close to 65536.

Is there anyone in the same situation? Tell me how to solve it.

[screen record](https://256x256.github.io/65536/65536.webm)

## Occurrence condition

1. Mousedown on content area (No logging without mousedown @ to out of the window)
2. To out of the window left or top (No problems @ to right or bottom)

## Results

Chromium run with "--disable-extensions"

### Abnormal (get large value)

- Chromium 86.0.4240.111 snap (on Ubuntu 20.04)
- Chromium 86.0.4240.75 (on Ubuntu 18.04)
- [Microsoft Edge](https://www.microsoftedgeinsider.com/) 88.0.680.1 dev (on Ubuntu 18.04)

### Normal (get valid value)

- Firefox 82.0 snap (on Ubuntu 20.04)
- Firefox 82.0 (on Ubuntu 18.04)
- Chrome 86.0.4240.111 (on Windows 10)

## Checked environment

- Ubuntu 20.04.1
  - 64 bit
  - only the core of the system + lxqt-core + openbox + sddm (x11)
- Ubuntu 18.04.5
  - 64 bit
  - Lubuntu minimal installation (x11)

## Verification

[verification site](https://256x256.github.io/65536/)

[verification code](https://github.com/256x256/65536/)

or simply

```javascript
addEventListener('mousemove', console.log)
```
