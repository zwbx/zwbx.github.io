---
layout: page
title: Robotic Vision Summer School Competition
permalink: /rvss-competition/
description: Kiola, Australia, 2024
nav: false
---

#### Overview

The [Robotic Vision Summer School (RVSS)](https://www.rvss.org.au/) is an annual program in Australia for students and researchers in robotics and computer vision. In February 2024, it was held at the [ANU Kioloa Coastal Campus](https://www.rvss.org.au/2024-venue-and-transport/) on the New South Wales south coast — a week of lectures, hands-on labs, and outdoor activities by the beach.

A main event of RVSS 2024 was the [**Need4Speed Challenge**](https://github.com/rvss-australia/RVSS_Need4Speed) — in essence, a minimal autonomous driving task. Each team must program a small mobile robot to drive along a printed track on its own: the robot uses its camera to stay on the road, recognize stop signs, and finish the course as quickly and reliably as possible. The robot platform and a basic control framework are provided in advance; the challenge is to get the full pipeline working within **three days** — collecting data, training the driving policy, and debugging the issues that show up when moving from training to real deployment.

Our team won **1st place** in this challenge. Our strategy was to find a baseline training pipeline that could run end-to-end within half a day, then iterate quickly from there. Three choices made the difference:

1. **Online data flywheel with human in the loop.** After a short round of initial data collection, we kept collecting data during deployment. When the robot made a mistake, we interrupted the run, manually labeled the episode, and discarded bad behaviors—turning deployment into an iterative data loop rather than a one-shot train-then-deploy workflow.

2. **Low latency for closed-loop control.** Time delay had an outsized effect on closed-loop driving. We used a very lightweight model and optimized network communication to keep control responsive.

3. **Dynamic inference at test time.** Most failures happened during turns, so we adjusted forward speed based on how strongly the model signaled a turn—slowing down when the turn cue was strong to reduce cornering errors.

Before this competition, my background was purely in computer vision — I had never worked on robotics. In just three days, this challenge gave me a whirlwind tour of the core problems in autonomous robot control: data collection in the real world, the gap between training and deployment, latency in closed-loop systems, and the long tail of failure cases. Looking back, it feels like a seed: many of the research questions I have pursued since then trace back, one way or another, to the small but real problems we bumped into on that little printed track.

Our code and workflow are available on GitHub: [**RVSS\_Need4Speed\_Winners**](https://github.com/zwbx/RVSS_Need4Speed_Winners). Below are a video from our final competition run and photos from the summer school.

#### Final Competition Run

<div class="rvss-video">
<video controls>
  <source src="/assets/rvss/competition-demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div>

<hr class="rvss-section-divider">

#### Photos

<div class="rvss-gallery" markdown="1">

![RVSS group photo](/assets/img/rvss/group-photo.jpg)
*RVSS group photo*

![Lecture by Richard Hartley](/assets/img/rvss/lecture-manifold-learning.jpg)
*Lecture by Richard Hartley*

![Outdoor lunch with fellow participants](/assets/img/rvss/outdoor-lunch.jpg)
*Outdoor lunch with fellow participants*

![Lunch](/assets/img/rvss/lunch-combined.jpg)
*Lunch*

![Need4Speed Challenge track map](/assets/img/rvss/track-map.jpg)
*Need4Speed Challenge track map*

![Award ceremony with the winning team](/assets/img/rvss/award-ceremony.jpg)
*Award ceremony with the winning team*

![Need4Speed Challenge Champion trophy](/assets/img/rvss/champion-trophy.jpg)
*Need4Speed Challenge Champion trophy*

![Prize book by Peter Corke](/assets/img/rvss/peter-corke-book.jpg)
*Prize: Robotics, Vision and Control by Peter Corke, awarded and signed by him*

![Campfire gathering at night](/assets/img/rvss/campfire-night.jpg)
*Campfire gathering at night*

</div>
