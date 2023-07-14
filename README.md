# invisement.github.io
A blog about software development, cloud engineering, and project management

# AWS vs GCP vs Azure
Ali Khosro,
July 2023

I have experience working with two popular cloud solutions: GCP and AWS. While my proficiency and hands-on experience lean more towards GCP, I have also managed teams exclusively working on AWS for large enterprise companies, primarily focusing on API development and analytics.

I believe that comparing cloud providers solely based on "on-paper" numbers found in common articles can be unhelpful, lacking in insight, and often misleading. Many authors of such articles have not engaged in serious hands-on work and instead provide superficial information based on simple "hello world" programs or catalog descriptions, as well as claims and financial reports. It is best to disregard such wasteful and misleading comparisons when making software selections.

While it is true that the choice of cloud provider ultimately depends on specific circumstances, I will refrain from offering generic advice like "it depends." Instead, let's delve into the comparisons. In the following analysis, I primarily compare AWS to GCP because of my familiarity with these two platforms, but it is worth noting that Azure often falls in the middle-ground between GCP and AWS, incorporating elements from both.

### Where does AWS appear to excel?

1. AWS boasts a longer tenure.

   In many cases, a longer presence signifies greater maturity, fewer bugs, and a larger pool of available resources when encountering challenges.

2. AWS offers a wider range of products and services.

   As of the current time, AWS provides nearly 200 product offerings, while GCP offers around 100. Furthermore, AWS tends to release new products at a faster pace than GCP.

3. AWS operates more data centers worldwide.

   This factor holds particular significance if your application has a presence in countries like China, where Google is technically absent from the market.

4. AWS delivers exceptional customer service for ticket resolution.

   Amazon's commitment to customer service is ingrained in their DNA.

5. AWS provides extensive documentation.

   However, this does not necessarily imply that it is more helpful. In fact, AWS documentation can often be more confusing compared to GCP's documentation.

6. AWS does not face the same brand reputation challenges as Google (and possibly Microsoft).

   I hold no biases against Google, Microsoft, Apple, or Amazon. Nevertheless, it is worth noting that certain individuals hold strong opinions against one or another. Additionally, Google is sometimes associated with abandoning projects midway and appears to have a tendency to chase after the next big shiny thing. On the other hand, Amazon faces fewer problems in these regards.

7. Finding data engineers proficient in AWS is generally easier than finding those skilled in GCP.

   Locating experienced and cost-effective engineers who possess AWS expertise and can work on the AWS platform should not pose significant difficulties.

Honestly,

> None of the aforementioned advantages are truly crucial.

Regarding points 1, 2, and 3: longevity, extensive offerings, and numerous data centers often hold little importance or provide little advantage. GCP's smaller product portfolio is a result of their focused development, organization, and thoughtful integration. Practically any application can be easily implemented on GCP. A notable example is workflow management: GCP provides Pub/Sub (a clear pub-sub mechanism) and EventArc (for event-driven architecture) which seamlessly integrate into the ecosystem and are highly intuitive. AWS, on the other hand, offers a handful of products that are quite similar to one another but fail to perform the task effectively. External third-party solutions become necessary to adequately manage workflow on AWS.

As for points 4 and 5, GCP's products are inherently more intuitive, requiring less extensive documentation. In fact, GCP's tutorials and guidance panels are more helpful and concise, without the confusion often encountered in AWS documentation. Similarly, GCP's customer service engineers are seldom needed due to the platform's intuitive nature and concise documentation.

Regarding point 6, I find the criticism, that might be true for other Google products, aimed at GCP to be unfounded. GCP is a well-established, profitable, and stable product within Google, and it is not prone to cancellation or abandonment like some of Google's consumer-oriented projects. In fact, developers often hold a more positive perception of Google due to its strong presence in the open-source community (surpassing that of Amazon or any other company) and its advanced technologies.

As for point 7, while it may have been a concern a few years ago, it is rapidly becoming less significant. The availability of engineers and resources for GCP has increased substantially, rapidly closing the gap. I believe this advantage will not play a major role in the near future. After all, investing in a platform is a decision with a horizon of over 10 years.

### So, where does AWS truly excel?

Based on the analysis provided above, it is evident that I would recommend GCP for most use cases. However, what are the real advantages of AWS?

> AWS offers more granularity, flexibility, and a professional appearance.

This comparison is often likened to "Android vs iOS" or "Windows vs Mac." Personally, I find the analogy of **Linux vs MacOS** most fitting. In this case, GCP can be seen as the less flexible option, but one that is thoughtfully designed around developers' needs and experiences. If you are a developer seeking a secure, scalable, and modern development environment with minimal complications and engineering work, GCP will feel like home. On the other hand, if you are a data engineer who values a high level of flexibility, granularity, transparency, and extensive documentation, you may perceive GCP as rigid and overly opinionated, and consider AWS to be more professionally oriented.

> GCP is opinionated.

GCP is known for its strong opinions. It is even more opinionated than Azure or AWS, and in comparison, more opinionated than Apple products. GCP provides default options that guide you on the recommended way to do things, allowing limited customization. Cloud engineers and data engineers often prefer and appreciate AWS for its professional nature, while holding negative sentiments towards GCP. Azure strikes a middle-ground, which is why managers and business professionals tend to gravitate towards it. Who, then, favors GCP? Developers.

For instance, with GCP, you can dive in, start developing, and deploy solutions after just a day of training, without requiring much assistance from cloud engineers. The roles are well-defined by default, allowing you to quickly spin up the desired service with minimal time wasted. GCP comes with default security measures, encryption, auto-managed services, and seamless integration with other parts of the ecosystem. While you can modify the default settings, it is often more limited compared to AWS (and possibly Azure). Nonetheless, the default settings work exceptionally well.

In contrast, AWS necessitates meticulous configuration upfront, requiring experienced data engineers to define various aspects such as granular roles, resources, access levels, domains, projects, user groups, and more. The idea is that by investing more effort into customization, it becomes more secure or superior. However, it is easy to overlook essential factors like encrypting data in transit or at rest, whereas GCP takes care of such matters by default. Nevertheless, AWS exudes a sense of professionalism with its wealth of options, demanding a deeper level of expertise.

> AWS enjoys greater friendliness and familiarity with third-party providers.

Many data engineers and system engineers come from backgrounds rooted in on-premise servers and traditional network environments. They are accustomed to relying on "a platform" that incorporates a series of third-party solution integrations. Some of these providers feel more comfortable with AWS due to its granularity, flexibility, and resemblance to on-premise servers equipped with open-source solutions. It appears that AWS has simply migrated these solutions to the cloud with minimal development or intervention. Conversely, GCP tends to handle most of these "third-party" integration solutions in-house, reducing the need for external providers. However, some engineers still seek a particular third-party solution they are familiar with, making AWS feel like home to them—a cloud-based extension of on-premise systems and open-source solutions.


## Analogies: Making Sense of the GCP, AWS, and Azure Landscape

In the end, the differences among GCP, AWS, and Azure can be likened to a comparison of three enterprise programming languages: **Java, Golang, and C#**. AWS represents the Java of the cloud world.

- **If you have a preference for Java, you will likely gravitate towards AWS.**

   Similar to Java, the AWS environment is known for its verbosity, architectural nature, abundance of abstractions, enterprise-grade solutions, professional appearance, and classic approach.

- **If you lean towards Golang, GCP is the platform for you.**

   Like Golang, GCP is opinionated, slightly unconventional, extremely simple yet elegant, offering fewer features (and consequently fewer bugs), abstracting away complexity, and boasting seamless integration. GCP, much like Golang, perceives additional features as potential pitfalls, aiming to provide a single, optimal way to achieve desired outcomes. (I, too, share the same belief that a feature is a bug in tux).

- **If C# aligns with your preferences, Azure becomes your top choice.**

   There are numerous reasons why C# enthusiasts opt for Azure. Its functionality is extensive, polished, and well-supported by a tech giant. Azure seamlessly integrates with other Microsoft products, such as Windows, Office, and SQL Server. Business managers often require minimal persuasion since they are already familiar with and utilize these Microsoft offerings. Azure can be backed by a plethora of figures and reasoning that resonate with business-minded individuals. It comfortably occupies the middle-ground, and there's nothing inherently wrong with that.

Another perspective applicable to managers and executives is to consider how you identify the tech professionals in your company: DevOps, Developers, or IT Staff?

> DevOps engineers tend to work with AWS, developers often find themselves paired with GCP, and IT staff frequently stick to Azure.

Another way to approach this analogy is by asking individuals about their roles and observing the titles they choose to introduce themselves with: developer, engineer, or otherwise. **Developers generally lean towards GCP, engineers gravitate towards AWS, and those with other titles (managers, marketers, executives, programmers) often prefer Azure**.

Regarding cost, performance, and switching costs:
---------------------------------------------------
Technical benchmarks related to cost and speed are inconclusive. Each cloud provider and their advocates claim to offer a faster and more cost-effective platform, supporting their claims with selected products, use cases, and benchmarks.

Based on my experience, I find that AWS often entails hidden costs and unexpected expenses. It also requires more maintenance costs as it necessitates a larger team of engineers to provide the professional support that developers and consumers require. In certain cases, the higher cost of professional-grade support might be justified.

In my opinion, for most applications, GCP tends to be faster (though not always) and more cost-effective in the long run, as it does not demand as much DevOps staff and has fewer hidden costs. Ultimately, I don't believe the difference is substantial, and it should not be the most significant factor to consider. The human cost, encompassing ease of use, developer time, and maintenance, holds greater importance. In this regard, GCP outshines AWS. I lack the necessary knowledge to make a judgment about Azure, but I assume it falls somewhere in the middle.

Regarding switching costs, it is true that all cloud providers strive to establish some degree of lock-in. They do so not only for profitability but also to offer more integrated services and better solutions. However, I cannot definitively say which provider presents a stronger lock-in. My intuition suggests that Microsoft might pose more challenges in this regard, while GCP should be relatively more flexible, and AWS should be the most compatible with the open source standards. Nevertheless, I do not possess sufficient information to make a definitive judgment.

## Choosing the Right Cloud Provider
First and foremost, it is important to emphasize that the similarities among these cloud providers outweigh their differences, and you will become accustomed to their way of operation. Additionally, in certain cases, it may be more advantageous to consider bare-metal solutions, third-party clouds, or stick to on-premise servers. The public cloud is not always the optimal choice.

With that said, my recommendation is that, for most use cases and future considerations, GCP is either a superior choice or at the very least, a comparable one. This is primarily because GCP is designed with the developer experience and needs in mind, and developers are often the primary users of the system if the cloud is a crucial component of your organization. However, if development is not the primary focus of your company, then AWS or Azure might be better alternatives.

Let's examine which industries are well-suited for each cloud provider:
- **GCP**: High-tech, software development, technology startups, machine learning, financials, and other industries where applications and app development (web or mobile) play a critical role in their products.
- **Azure**: Well-established, brick-and-mortar, large enterprises with extensive legacy systems and Microsoft-based technologies. This is especially true if you aim to empower business professionals to securely work remotely and on-the-go. If you are familiar with and rely on Windows, SQL Server, Office, Outlook, Visual Basic, C#, and similar Microsoft technologies, Azure will be the obvious choice.
- **AWS**: If you have a substantial team of data engineers and IT staff, AWS is well-suited to your needs. If ERP systems and large databases with constant data querying and exporting to Excel are your primary reasons for utilizing the cloud, AWS is the recommended option. If you heavily rely on open-source, third-party, or legacy systems, or use platforms like Jenkins, Spring, Airflow, and others, AWS will feel like home.
