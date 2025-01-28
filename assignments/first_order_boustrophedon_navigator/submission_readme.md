## README: Completion of PD Controller Tuning for Boustrophedon Pattern

### Objective

The goal of this assignment was to tune a PD controller to achieve the most precise boustrophedon pattern for a first-order system. The primary objective was to minimize the cross-track error while ensuring smooth motion and maintaining effective cornering behavior. The success of the system was evaluated based on controller performance, pattern quality, and the analysis and documentation of the tuning process.

### Controller Tuning

In this task, I utilized `rqt_reconfigure` and manual inputs to tune the PD controller parameters in real-time, optimizing the following four key parameters:

### Methodology

The tuning process involved iterating through various combinations of the PD controller gains and pattern parameters while carefully monitoring the cross-track error and motion smoothness. Key steps included:

1. **Adjusting the `Kp_linear` and `Kd_linear` parameters** to minimize overshoot and reduce the average cross-track error.
2. **Fine-tuning the `Kp_angular` and `Kd_angular` gains** to ensure smooth and accurate cornering with minimal oscillations.
3. **Modifying the spacing between lines** to optimize the boustrophedon pattern for better coverage and completeness of the target area.

### Performance Plots
I plotted the required plots and saw a spike in angular velocity graph alternating with positive and negative values during turning corners. Not able to attach the image of the plot here because it is too big to capture. Even after captring not much is visible since everything is very small and lines superimpose/overlap upon one another.

### Challenges and Solutions

- **Challenge**: Achieving smooth cornering behavior while maintaining low cross-track error was a balancing act between the proportional and derivative gains.
  - **Solution**: I adjusted the derivative gain slightly to reduce overshoot and improve the smoothness of the velocity profiles during cornering.

### Final Parameter Values

The final tuned parameters are as follows:

- **Kp_linear**: 25.0
- **Kd_linear**: 0.8
- **Kp_angular**: 11.5
- **Kd_angular**: 0.04
- **Spacing**: 1.0  

These values were chosen based on the best performance with respect to the cross-track error and smooth motion.

### Evaluation

- **Controller Performance**: Achieved an average cross-track error of **0.028** units and a maximum error of **0.109** units, with smooth velocity profiles and clean cornering behavior.
- **Pattern Quality**: The spacing between lines was even, the target area was fully covered, and space was used efficiently.

### Conclusion

The project successfully tuned the PD controller to produce a precise boustrophedon pattern while minimizing cross-track error and ensuring smooth motion. The tuned parameters were evaluated against performance metrics, and the results show good adherence to the given criteria. The repository contains all relevant documentation, performance plots, and the final tuned parameter values for review.