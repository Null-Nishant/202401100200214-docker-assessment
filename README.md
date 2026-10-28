# Docker & Container Security Assessment

- **Registration Number:** 202401100200214
- **Port:** 8014

## Stage 3: Image Security

### Image Size Comparison

| Image | Disk Usage |
|---|---:|
| fest-backend:0.1 | 1.61 GB |
| fest-backend:0.2 | 282 MB |

The optimized image is approximately 82.5% smaller than the original.

### Vulnerability Scanning

- **Scanner:** Trivy 0.76.0
- **Before report:** `reports/trivy-before.txt`
- **After report:** `reports/trivy-after.txt`
- **Security gate:** `trivy image --severity CRITICAL --ignore-unfixed --exit-code 1 fest-backend:0.2`
- **Result:** Passed — no CRITICAL findings detected by the security gate.

The original image scan and the final image scan are saved in the `reports/` directory.