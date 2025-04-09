<p align="center">
    <a href="https://www.witboost.com/">
        <img src="docs/img/witboost_logo.svg" alt="witboost" width=600 >
    </a>
</p>

Designed by [Agile Lab](https://www.agilelab.it/), Witboost is a versatile platform that addresses a wide range of sophisticated data engineering challenges. It enables businesses to discover, enhance, and productize their data, fostering the creation of automated data platforms that adhere to the highest standards of data governance. Want to know more about Witboost? Check it out [here](https://www.witboost.com) or [contact us!](https://witboost.com/contact-us)

This repository is part of our [Starter Kit](https://github.com/agile-lab-dev/witboost-starter-kit) meant to showcase Witboost integration capabilities and provide a "batteries-included" product.

# Google BigQuery Output Port Template

- [Overview](#overview)
- [Usage](#usage)

## Overview

Use this template to create an Output Port that allows you to create a view of a source table on Google Big Query

Refer to the [Witboost Starter Kit repository](https://github.com/agile-lab-dev/witboost-starter-kit) for information on the Tech Adapter that can be used to deploy components created with this template.

### What's a Template?

A Template is a tool that helps create components inside a Data Landscape. Templates help establish a standard across the organization. This standard leads to easier understanding, management and maintenance of components. Templates provide a predefined structure so that developers don't have to start from scratch each time, which leads to faster development and allows them to focus on other aspects, such as testing and business logic.

For more information, please refer to the [official documentation](https://docs.witboost.com/docs/p1_user/p6_advanced/p6_1_templates/#getting-started).

### What's an Output Port?

An Output Port refers to the interface that a Data Product on a Data Mesh uses to provide data to other components or systems within the organization. The methods of data sharing can range from APIs to file exports and database links.

## Usage

To get information on how to use this template, refer to this [document](./docs/index.md).

### Component Testing

To verify the component before deploying it along with the Data Product, this template provides two sets of CUE Policies:

- General component testing using [Google BigQuery Output Port CUE policy](./policies/outputport.cue). This policy needs to be defined inside the **Governance** section of the Witboost Platform with a selector matching the Infrastructure Template and Use Case Template of the component and applied to all three environments
- Owner roles policy testing registering both the [Development/QA CUE policy](./policies/ownerRolesDevelopmentQA.cue) defined with a selector matching the Infrastructure Template and Use Case Template of the component and applied to only development and QA environments, and the [Production CUE policy](./policies/ownerRolesProduction.cue) defined with a selector matching the Infrastructure Template and Use Case Template of the component and applied to production environment.

For more information, please refer to the [official documentation](https://docs.witboost.com/docs/p1_user/p5_managing_policies/p5_1_overview).

## License

This project is available under the [Apache License, Version 2.0](https://opensource.org/licenses/Apache-2.0); see [LICENSE](LICENSE) for full details.

## About Witboost

[Witboost](https://witboost.com/) is a cutting-edge Data Experience platform, that streamlines complex data projects across various platforms, enabling seamless data production and consumption. This unified approach empowers you to fully utilize your data without platform-specific hurdles, fostering smoother collaboration across teams.

It seamlessly blends business-relevant information, data governance processes, and IT delivery, ensuring technically sound data projects aligned with strategic objectives. Witboost facilitates data-driven decision-making while maintaining data security, ethics, and regulatory compliance.

Moreover, Witboost maximizes data potential through automation, freeing resources for strategic initiatives. Apply your data for growth, innovation and competitive advantage.

[Contact us](https://witboost.com/contact-us) or follow us on:

- [LinkedIn](https://www.linkedin.com/showcase/witboost/)
- [YouTube](https://www.youtube.com/@witboost-platform)