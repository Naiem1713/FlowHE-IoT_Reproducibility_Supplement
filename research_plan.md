# FlowHE-IoT Research Plan

## Objective

Develop a traffic- and resource-aware CKKS framework for binary IoT intrusion monitoring that jointly selects the feature count, CKKS profile, and SIMD batch size.

## Datasets

- Primary: Edge-IIoTset
- External validation: IoT-23

## Main encrypted model

Plaintext-trained Logistic Regression with encrypted linear-score inference:

`z = w^T x + b`

The trusted client decrypts the score and applies the final threshold.

## Main experiments

1. Plaintext model and feature-selection benchmark
2. Standard CKKS baseline
3. Feature-reduced CKKS
4. Feature-reduced packed CKKS
5. Validated CKKS profile search
6. Low/normal/burst traffic evaluation
7. Tiny/low/gateway resource profiles
8. Energy, latency, memory, and ciphertext-size analysis
9. Component ablation
10. IoT-23 external validation

## Reproducibility

- Seeds: 42, 123, 2024, 3407, 7777
- Five warm-up runs
- At least 30 measured runs per HE configuration
- Mean, standard deviation, 95% confidence interval
- p50, p95, p99 latency
- Dataset hashes and split manifests
- Raw benchmark traces retained
