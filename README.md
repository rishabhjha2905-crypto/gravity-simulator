# Gravity Simulator

An interactive Newtonian gravity simulation of planets orbiting a star. Set the star's mass and launch the simulation — the planets calculate their own correct orbital velocities and start orbiting immediately.

## What it shows

- **Newtonian orbits** — each planet's motion is calculated using F = GMm/r²
- **Star mass input** — type any mass in solar masses and hit Launch to restart the simulation fresh
- **Realistic star scaling** — the star's visual size follows the real stellar mass-radius relation (R ∝ M^0.8 for M < 1 solar mass, R ∝ M^0.57 for M > 1 solar mass)
- **Planet engulfment** — if the star grows large enough to engulf a planet's orbit, that planet is removed from the simulation

## The physics

Each planet's orbital velocity is calculated from scratch on every launch using:

```
v = √(GM/r)
```

This comes from setting gravitational force equal to centripetal force — the exact speed needed for a stable circular orbit at radius r around a star of mass M. This means no matter what mass you enter, the planets always start with the right velocity and never fly away.

The star's size uses the empirical stellar mass-radius relation from observational astronomy rather than a simple approximation, so the scaling is physically grounded.

## How to use it

Open `index.html` in any browser. Type a star mass in solar masses, hit **Launch Simulation**, and watch the orbits. Try increasing the mass gradually and watch the star grow and eventually swallow the inner planets.

Or visit the live version: [https://rishabhjha2905-crypto.github.io/gravity-simulator](https://rishabhjha2905-crypto.github.io/gravity-simulator)

## Built with

Plain HTML, CSS, and JavaScript — no frameworks or libraries.

## Background

Built as a side project while taking PHYS 211 and PHYS 212 at UIUC, alongside a special relativity visualizer. The goal was to make orbital mechanics interactive and physically accurate rather than just visually impressive.
