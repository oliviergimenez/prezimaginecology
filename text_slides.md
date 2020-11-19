## Text of the slides

1. Hi everyone. My name is Olivier Gimenez. I'm a researcher at the National Centre for Scientific Research in France. I'm gonna talk about my first steps in deep learning with its application to the identification of animal species on pictures taken with camera traps. 

2. I'm working a lot on predator-prey interactions these days. These are interactions between species that structure communities or large mammals. 

3. This is joint work with Anna Chaine, Maëlis Kervellec, both first-year Master students, Vincent Miele deep learning MC, and colleagues from the French Office for Biodiversity and from hunting associations. 

The main question we're interested in is to understand how predators, preys and their environment interact.

4. To address this issues, our colleagues collect data in the natural habitat of the species we're studying, using camera traps set up in strategic places. So we don't use this kind of material, it would disappear in no time. 

5. Instead these camera traps are used. These are installed on both sides of the path used by animals, like this lynx females w/ her kittens. This methods is non-invasive, meaning that we don't have to physically capture individuals. The big issue is that we get tons of pictures which we need to annotate with species id. This is where deep learning is useful!

6. The idea is first to use annotated pictures to train models to identify species; second we may use these models to identify species on any non-annotated pictures. 

7. To make my first steps in deep learning, I used the resources available on imaginecology a website we built in our French national centre for statistical ecology. Give it a try, it's awesome. It's full of relevant and useful resources. There is an introduction to deep learning, codes, papers and data to train your models. There is also a series of tutorials that are very didactic. Kuddos to Vincent and Gaspard for an amazing work!  

8. I used the tutorial on detection of animals on camera trap images. I used Retinanet that implements a two-step approach detection and classification. You can find my peregrinations on GitHub. 

9. Before going to the results, a disclaimer: I am a beginner, and these results are only preliminary. My colleagues should not be made responsible of my errors. 

10. What are our results?

11. First, I used transfer learning on a study site in the Jura county where we had a bunch of annotated pictures. 

12. The results are pretty good. We succeed in detecting and identifying lynx individuals and its preys, chamois and roe deer, with a high level of certainty. 

13. It is also the case for other species that appear on the pictures. 

14. Then, I used my model to automatically annotate a bunch of pictures that were taken at another site, in the Ain county. The cool thing is that these pictures were also annotated, so that I could go through a step of testing of the model. 

15. We get some results that can be arranged as follows. In columns you have the species, the true positives, the false positives and the false negatives. We're doing pretty well for lynx, but we wonderfully fail at identifying its preys, with an excess of false positives for chamois, and an excess of false negatives for roe deer.

16. Took me some time to get over the frustration...

17. Then I asked myself why the results were so bad. We see several reasons why. 

18. We know for example that generalisation from a site to another one is tricky with deep learning. Traps might be different, as well as the environmental conditions, the exposition, etc... 
Another reason might be that our training dataset was to small. 
Next thing I'm gonna do is to pool both datasets in the two counties, and re-train my model. 

19. As a way to end my short talk, let me go through a few lessons I learnt along the way. 

20. Terminology is an obstacle. On the imaginecology website, you will find a glossary that might help. Also, I recommend exploring the material shared by Jennifer Hoeting, and the video of her talk at the last International Statistical Ecology Conference. The viewpoint of a statistician is useful to make the parallel with a familiar vocabulary.  

Also, I asked myself a lot of questions. 

First, about reproducibility. Training a model is like cooking with its share of improvisation. 
Second, there are legal and ethical considerations that should be raised when we analyze pictures on which our species puts itself on stage. 
Third, there is the question of the carbon footprint of deep learning as we often have to use GPUs for long periods. 
Fourth, my advice is to check out what the experts are doing. For example, there is a challenge organised by Sara Beery in which the best teams share their recipes. Talking about Sara, I warmly recommend to follow her on Twitter, as well as Mikey Tabak, both are yodas of deep learning for ecology.  

Last, the deep learning community speaks Python, therefore learning Python cannot hurt. If like me you're a heavy R user, these two books might help. 

21. Thank you for listening. 

22. Self-promotion.

