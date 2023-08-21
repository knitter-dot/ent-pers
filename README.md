**Entirely Personal: A Deep Dive into 3D Scanning, Remeshing, and Knitting**

**Introduction**

The design world is vast and ever-evolving, with new technologies and methodologies constantly emerging. In this journal, we delve into a specific project that seeks to explore and understand some of these cutting-edge techniques. This project, while multifaceted, is organized into three distinct work packages, each with its unique focus and objectives.

The **first package** is dedicated to the technological assessment at AMFI. Here, the goal is to evaluate and contrast the two available technologies to pinpoint the optimal scan settings that would yield the best results. This phase is crucial as it sets the foundation for the subsequent stages, ensuring that the data acquired is of the highest quality.

Moving on, the **second package** delves into the world of remeshing. This phase is all about exploring various approaches to remeshing strategies. Remeshing, in the context of this project, is pivotal as it determines how the scanned data is processed and prepared for the final phase.

The **third and final package** bridges the gap between design and production. It revolves around the sampling and iteration process, specifically between the Rhino/Grasshopper environment and the native 3D knitting software, namely Stoll’s M1plus and Shima Seiki’s Apex. The design truly comes to life in this phase, transforming from digital data into tangible knitted structures.

In the pages of this journal, I will keep the sum of all the experiences done during this research.

-----
May 12, 2022 \_ 3D Scan Technologies: Initial Assessment

- Began assessment of various 3D scan technologies.
- Initial focus on Scanlounge V2.5 by Scanlogics, using photogrammetry technology.
- Noted high-resolution outputs and clean data, but lack of raw data (point clouds) is a concern.

Considerations:

- The Scanlounge V2.5 shows immense promise due to its high-resolution and clean output. The technology seems to be advanced, but the lack of raw data is a significant limitation. This could affect the flexibility and control we have over the data processing stage.

Next Steps:

- Investigate the possibilities of using an iPad for scanning.
- Compare TrueDepth and Lidar applications on the iPad.

![](/imgs/Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.001.png)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.002.jpeg)

Technology: Photogrammetry

Max. resolution: 0.1 mm

244 cameras of 8 MP each

8 projectors with light textures to help photogrammetry

Price:  $ 60,500

Source: 

<https://www.aniwaa.com/product/3d-scanners/scanologics-scanlounge/>

<https://www.scanologics.com/>




-----
May 16, 2022 \_ 3D Scan Technologies: iPad Scanning

- Conducted experiments with iPad scanning, achieving a max resolution of 0.5mm-1mm.
- Observed that TrueDepth and Lidar technologies are time-consuming and sensitive to micro-movements.
- Lidar is better for environments, TrueDepth has a denser grid that works better with smaller items.

Considerations:

- The iPad, being a more accessible and cost-effective tool, presents a compelling case. However, the time it takes to capture a scan and the sensitivity to micro-movements could lead to less reliable data. The resolution is also notably lower than the Scanlounge V2.5.

Next Steps:

- Analyze and compare the results of Scanlogics' photogrammetry and iPad scanning.
- Decide on the technology to proceed with for further experiments.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.003.png)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.004.png)

PRO:

- A cheap tool to realize good outputs.
- many app and software possibilities.
- availability of lot of outputs and raw data
- enough good resolution for body scan purpose.

CONS:

- need to post-produce mesh.
- True depth and Lidar technologies needs more time to get a scan, allowing mistakes due micro-movements.

Source: <https://www.researchgate.net/publication/350729997_Comparison_of_iPad_ProR's_LiDAR_and_TrueDepth_Capabilities_with_an_Industrial_3D_Scanning_Solution>



-----
May 18, 2022 \_ 3D Scan Technologies: Comparison

- After comparing the available technologies at Amfi,  we decided to use photogrammetry with the Scanalounge
- we took several elbows scan to use as topology test for the exploration

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.005.png)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.006.png)

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.007.png)

-----
Jun 12, 2022 \_ Remeshing: Initial Approach

- Began work on remeshing the output from the scanner to create knitting instructions.
- Initial attempts with Anemone in Rhinoceros Grasshopper, based on Carnegie Mellon's Textile Lab research.
- Faced challenges in generating reliable knitting instructions due to complex topology.

Considerations:

- The remeshing process is proving to be a significant challenge. The initial mesh is complex, and translating this into knitting instructions is not straightforward. The Anemone plugin in Grasshopper is powerful but may require a more sophisticated approach to handle the complexity of garment shapes.

Next Steps:

- Explore alternative remeshing methods, including circle packing and Cockatoo plugin.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.008.png)

-----
Jun 15, 2022 \_ Remeshing: Circle Packing and Cockatoo

- Conducted experiments with circle packing algorithm; faced issues with data loss and ordering.
- Started working with Cockatoo, a Grasshopper plugin; promising initial results.
- Cockatoo appears to be the most reliable approach for our purposes.

Considerations:

- Circle packing was an interesting approach, but the randomness and data loss are significant issues. Cockatoo, on the other hand, seems to offer a more structured and reliable process. It’s encouraging to see a potential path forward with this plugin.

Next Steps:

- Conduct extensive tests with Cockatoo.
- Begin integration with knitting software such as Shima Seiki's Apex or Stoll's M1plus.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.009.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.010.jpeg)

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.011.png)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.012.png)

-----
Jun 17, 2022 \_ Initial Tests

- Conducted detailed analysis of different samples knitted using our modified version of Cockatoo.
- Observed the need for post-production process standardization across all samples.
- Initial tests with “Elbow” sample highlighted issues in bitmap generation and manual corrections needed.
- Traveled to Knitwearlab in Almere to do some test

Considerations:

- The transition from digital to physical is revealing intricate nuances. The “Elbow” sample test was a learning experience; the bitmap errors were unexpected and required manual intervention. Standardizing the post-production process is emerging as a critical need.

Next Steps:

- Refine Cockatoo script for more accurate results in goring and increasing/decreasing.
- Conduct tests with larger samples, such as a full sleeve or torso.
- ![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.013.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.014.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.015.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.016.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.017.jpeg)
-----
July 5, 2022 \_ Coding and scanning

- Did other body scan to prepare the material for further test.
- Implement some extra module in Gh to add the code part to avoid the main errors.


|Gore|Increase/Decrease|
| :- | :- |
|<p>- always over two rows</p><p>- going to the left: on rows 1-2, 3-4</p><p>- going to the right: on rows 2-3, 4-1 (offset over one row compared to the left side)</p><p>- can happen over an x amount of stitches in width - no limit</p><p>- insert a tuck stitch at the end of a gore point (only on one of the two rows in height)</p>|<p>- one color for moving stitches to the left, one for moving stitches to the right</p><p>- max two increases or two decreases (one left and one right) in a row</p><p>- Increase and decrease null each other, so if you have more than one type per row removes the less one</p><p>- increase and decrease works better on the edge of the piece, otherwise leaving marks in the knit</p>|


Considerations:

- the variable are many, so we started to code the main issues; we will proceed step by step.

Next Steps:

- Develop a user interface within Rhino/Grasshopper for operator input.
- Explore methods for automatic bitmap production for specific machines.
- Consider testing with different stitch types beyond Single Jersey.
-----

July 15, 2022\_Head Sample: Navigating Gauge and Resolution

- Explored gauge and resolution using a 3D model of a human head.
- Modified the script to address double row issues and used a 9-needles/inch Stoll machine for knitting.
- Observed pronounced shape marks due to the lower gauge of 9 needles/inch, impacting both 3D topological emergence and the 2D shape.

Considerations:

- The intricate relationship between gauge, resolution, and the final knitted outcome became evident.
- The lower gauge significantly affected the visible 3D topological emergence and the 2D shape.

Next Steps:

- Further refine the script to address the challenges observed.
- Explore the balance between gauge and resolution to achieve the desired knitted outcome.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.018.jpeg)

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.019.png)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.020.jpeg)

-----
September 5, 2022\_Advancing Techniques: Elbow\_plating Sample

- Refined the Cockatoo script to incorporate color variations.
- Assigned different yarn carriers to distinct colors, enhancing the examination of short-rowing intricacies.
- Knitted the Elbow\_plating sample, showcasing the intricate plating technique.

Considerations:

- The refined approach allowed for a clearer understanding of short-rowing intricacies.
- The relationship between digital design and physical knitting became more evident.

Next Steps:

- Continue refining the script based on the insights gained.
- Explore other techniques and innovations to further enhance the knitting process.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.021.jpeg)![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.022.jpeg)

-----
September 20, 2022\_Complex Front Panel Exploration

- Used a 3D body scan to create a sleeveless sweater divided into front and back panels.
- Encountered unforeseen challenges leading to unpredictable results in both 2D shape and 3D topology.

Considerations:

- Translating complex shapes into accurate knitting instructions requires further refinement.
- The project's scope expanded due to the intricate interplay between digital geometry, knitting instructions, and physical execution nuances.

Next Steps:

- Address the challenges observed during the front panel exploration.
- Dive deeper into the relationship between digital design, knitting instructions, and physical execution.

![](Aspose.Words.bb5e59e0-5571-4607-9f43-8e014e8e0e72.023.png)

Limitation and Future Works

- The sampling process highlighted the complexities of the knitting process.
- The remeshing process faces challenges when scaling up samples.

Considerations:

- The placement of gores and increases and decreases in knitted samples appear random.
- Proprietary software like M1plus or Apex poses challenges due to their 2-dimensional architecture.

Next Steps:

- Explore strategies to reduce the randomness of the remeshing process.
- Develop tools to make the knitting process more accessible and accurate.

