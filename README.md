# Overtone Explorer

![Overtone Explorer](thumbnail.png)

**Open it: https://leonardoperugia09-cyber.github.io/overtone-explorer/**

An interactive simulation of black-hole ringdown. It asks one question: **can the 221
overtone be detected in noisy data, and why?**

- **Controls:** remnant mass and spin; overtone amplitude, phase and SNR; fit start time,
  SNR convention and noise draw; four scenario presets and a reset.
- **Main plot:** simulated noisy data, the true signal, and one-mode and two-mode
  least-squares fits to the current noise draw.
- **Results:** the Fisher-matrix significance of the overtone, a one-mode vs two-mode fit
  comparison with Δχ², the bias that ignoring the overtone puts on the fundamental's
  damping time, and the reasons behind the verdict.
- **Supporting analysis:** the two modes drawn separately, significance and bias against fit
  start time, and a 50-draw noisy-data experiment.
- **A 5-step guided tour** and a "How it works" section. The tour restores your settings
  when it ends.

Colour code: blue = 220 fundamental, orange = 221 overtone, violet dashed = one-mode fit,
cyan dotted = two-mode fit.

## Files

- `index.html`: the interface (layout, charts, tour).
- `physics.js`: all physics and numerics. It has the Berti, Cardoso & Will (2006)
  quasinormal-mode fits, the damped-sinusoid models, the Fisher matrix, the
  Levenberg–Marquardt fitter and the noise generator. It matches the Ringdown Lab Python
  code to better than 0.01%.

No build step and no dependencies. Open `index.html` in a browser, or serve the folder.

## Limitations

All data are simulated: white Gaussian noise, one detector, an exact two-mode signal from
a known peak time. The Δχ² threshold (15.70) was calibrated for the project default only.
The significance Z is a best-case Fisher forecast, not proof that an overtone exists.

Part of the Ringdown Lab TKS Focus Project by Leonardo Perugia, 2026.

## License

MIT © 2026 Leonardo Perugia
