---
parent: Architectural Decisions
nav_order: 2
---

# ADR 2: Implementing a 3-Step Action Plan for Project Transparency and Collaboration

## Context and Problem Statement

Following the comprehensive reform outlined in ADR 1, the next phase focuses on enhancing project transparency, easing contributions, and clarifying the project's direction. This involves adopting Infrastructure as Code (IaC) for transparent infrastructure configuration, standardizing on open-source/Git for change management and collaboration, and clearly defining the project's roadmap and vision to attract and retain contributors.

## Objective

To implement a 3-step action plan aimed at:
1. Increasing infrastructure transparency and simplifying contributions through IaC.
2. Enhancing change logging, review processes, and external contributions via open-source/Git standardization.
3. Providing clear motivation for both core and non-core contributors by articulating a compelling project roadmap and vision.

## Considered Options

### IaC Implementation
- **Option 1**: Adopt Terraform for its extensive provider support and strong community.
- **Option 2**: Use Ansible for its simplicity and agentless architecture.

### Open Source/Git Standardization
- **Option 1**: Standardize on GitHub for its widespread adoption and comprehensive tooling.
- **Option 2**: Use GitLab for its integrated CI/CD features and open-source licensing.

### Roadmap/Vision Clarification
- **Option 1**: Develop an interactive roadmap using tools like Roadmunk or Aha!.
- **Option 2**: Maintain a simpler, markdown-based roadmap in the project's repository for easy access and updates.

## Decision Outcome

- **IaC Implementation**: Chosen option: Terraform, for its ability to manage complex infrastructure setups with a wide range of service providers and its strong community support, which can be invaluable for troubleshooting and best practices.
- **Open Source/Git Standardization**: Chosen option: GitHub, due to its ubiquity in the open-source community, making it more likely to attract contributions and its robust ecosystem of integrations and tools that facilitate code review and collaboration.
- **Roadmap/Vision Clarification**: Chosen option: A markdown-based roadmap within the project's GitHub repository, to ensure it is easily accessible to all contributors and can be updated as part of the standard Git workflow, keeping the vision and roadmap closely aligned with actual project developments.

### Consequences

- IaC and GitHub standardization will streamline contributions and infrastructure management but require training for existing team members unfamiliar with these tools and practices.
- A markdown-based roadmap is easily accessible but may lack the dynamic features and visual appeal of dedicated roadmap software, potentially requiring more effort to keep engaging and up-to-date.

## Implementation Strategy

1. **IaC Implementation**: Begin with a pilot project to convert a small, manageable portion of the infrastructure to Terraform. Expand gradually, documenting best practices and lessons learned for wider team education.
   
2. **Open Source/Git Standardization**: Migrate existing code repositories to GitHub, if not already hosted there. Conduct workshops and provide resources on Git workflows, pull request processes, and open-source contribution guidelines.

3. **Roadmap/Vision Clarification**: Collaborate with project stakeholders to refine the project's long-term vision and immediate goals. Update the markdown roadmap accordingly and integrate it into the project's main GitHub page for visibility.

## Monitoring and Evaluation

- Success of IaC implementation will be measured by the speed and efficiency of infrastructure changes and the reduction in configuration errors.
- Open-source/Git standardization success will be evaluated based on the increase in external contributions and improvements in change tracking and code review processes.
- The effectiveness of the roadmap/vision clarification will be assessed through contributor feedback and an increase in both core and non-core project engagement.

## More Information

- For Terraform best practices, consult HashiCorp's official documentation and community forums.
- GitHub's "Building a strong community" guide offers valuable insights into managing open-source projects on the platform.
- For roadmap development, consider insights from "Product Roadmaps Relaunched" for strategies on maintaining an effective, transparent roadmap.

