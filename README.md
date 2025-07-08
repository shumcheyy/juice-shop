# This Project from OWASP teaches  about OWASP Top 10. It provides a great hands on approach on how to find the vulnerabilities.



## My Approach for this particular project and repo is to build a Devsecops pipeline for learning purpose.

Rather than just exploring the vulnerabilities in OWASP Juice Shop, my goal is to take things a step further by building a full DevSecOps pipeline around it. This will help me not only understand how these vulnerabilities work, but also how modern teams can catch and fix them automatically as part of their development process.

### What I Plan to Do

I’ll be setting up a CI/CD pipeline using **GitHub Actions** as the backbone. At each stage of the pipeline, I’ll integrate security tools and checks that are commonly used in the industry:

- **Static Code Analysis (SAST):**  
  I’ll use tools like CodeQL, SonarQube, and Semgrep to scan the source code for vulnerabilities every time code is pushed or a pull request is opened.

- **Dependency Scanning (SCA):**  
  With Dependabot and Snyk, I’ll make sure that any third-party libraries or packages used in the project are checked for known security issues.

- **Secrets Detection:**  
  To prevent accidental leaks of sensitive information, I’ll run Trufflehog and enable GitHub’s built-in secret scanning.

- **Container Security:**  
  The application will be containerized, and I’ll use Trivy to scan the Docker images for vulnerabilities before they’re deployed.

- **Dynamic Application Security Testing (DAST):**  
  After deploying to a test environment, I’ll run automated scans with OWASP ZAP to catch vulnerabilities that only show up when the app is running.

- **Security Gates:**  
  The pipeline will be set up to block deployments if any critical security issues are found at any stage.

- **Deployment:**  
  For deployment, I’ll use Helm to manage Kubernetes manifests and deploy the app to AWS EKS (Kubernetes).

- **Notifications:**  
  Optionally, I’ll integrate Slack notifications so I get real-time updates about pipeline results and security findings.

### Why This Approach?

I want to get hands-on experience with what DevSecOps looks like in the real world. By automating security checks throughout the development lifecycle, I’ll learn how to catch issues early, reduce manual work, and build more secure software from the ground up. This project will give me practical experience with both the tools and the mindset needed for modern, security-focused development.
