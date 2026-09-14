# Polynomial Regression Visualizer

An interactive, beginner-friendly polynomial regression visualizer. The complete application is in **task2.html**, with embedded HTML, CSS, and JavaScript and no external dependencies.

## 🚀 Live Demo

[**Open Polynomial Regression Visualizer**](https://hamnuttapat1.github.io/Data-analytics-Polynomial-regression-visaulizer/task2)

## Explore the algorithm

1. Generate linear, quadratic, wave, or random data. Add points by clicking the canvas or entering coordinates; remove them with Remove mode, right-click, or Delete selected.
2. Set the polynomial degree (1–6), learning rate (0.001–0.1), and maximum epochs.
3. Press **Step** for exactly one full-batch gradient descent update, or **Play until Convergence** to train automatically. Pause and Reset are also available.
4. Watch the fitted curve, residuals, coefficient updates, numerical example, and MSE history change together. Inspect a point to follow its calculation.

The dark interface has two independently scrolling desktop columns. Both pairs of panels match in height, including the lower controls and loss panels. Smaller screens use a stacked layout. The footer lists all four group members and **CEi KMITL**.

## Mathematics

The input is normalized as `z = x / 5`, keeping `z` in `[-1, 1]` for numerical stability. The model is `prediction = sum(beta[j] * z^j)` with `degree + 1` coefficients, initialized to zero.

Each epoch computes the mean squared error and its full-batch gradient, then updates every coefficient simultaneously using `beta[j] -= learningRate * gradient[j]`. The table displays the actual values before and after that epoch.

Training stops on near-zero loss, a small gradient, or 20 consecutive small improvements (the exact thresholds are explained on the page). A plateau is a practical stopping criterion, not proof of an exact optimum. The maximum epoch limit is reported separately from convergence.

## Run and deploy

Open `task2.html` directly in a modern browser; no installation or build is required. GitHub Pages is already configured for this repository and automatically publishes updates pushed to `main`. The live page is available at the link above.
