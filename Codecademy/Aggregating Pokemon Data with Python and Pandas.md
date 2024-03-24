[[Aggregating Pokemon Data with Python and Pandas]]style="color: #1f00a8; background-color: #1f00a8"#ff00bb#a600ff#fb00ff#ff00d5#ff00ff#06abcd#972fff#ff0099![INSIGHTS](https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/INSIGHTS.png)


![albert-lee-author-photo.jpg?w=908](https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/albert-lee-author-photo.jpg?w=908)By [Albert Lee](https://www.codecademy.com/resources/blog/author/albert-lee/)

Most of the time, high-level decision-makers require aggregated data. For example, to understand sales trends, business analysts need to aggregate individual sales transactions by month, quarter, or fiscal year. Data aggregation is a key skill that can drive value for many organizations.

![image6](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image6.jpg)

Supermarket sales aggregated by category  

[Pokémon](https://en.wikipedia.org/wiki/Pok%C3%A9mon) is a video game where creatures (known as Pokémon) of different types battle each other for glory. To commemorate the release of the newest Pokémon games for the Nintendo Switch ([Let’s Go Pikachu and Let’s Go Eevee](https://www.youtube.com/watch?v=BSL7l2Ie_NY)), we will aggregate and analyze Pokémon data in order to answer the following questions:

1. **How many Pokémon of each type are there?**
2. **Which Pokémon type is the most powerful?**

First, we will complete our analysis using spreadsheets because spreadsheets are the most widely used tool for data analysis. However, **Python programming provides more flexible and more scalable analysis options than spreadsheets**, so we will complete the analysis using Python and the Pandas library.

## Starting with spreadsheets
Let’s start with a dataset of all Pokémon from [Pokémon Database](https://pokemondb.net/pokedex/all). To follow along, download the data [here](https://raw.githubusercontent.com/albemlee/pokemon_data/master/all_pokemon.csv) (_right click and select "Save As…"_).

We will use [Google Sheets](https://www.codecademy.com/resources/blog/aggregating-pokemon-data-python-pandas/sheets.google.com), a free spreadsheet application, for our analysis. Regardless of the specific spreadsheet tool you use, the underlying concepts will be the same. Below is a preview of the data.

![image1](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image1.png)

Each row represents a single Pokémon  

Each Pokémon belongs to one or two **types**, and certain types are strong against other types. For example, Charizard is a flying, fire-breathing lizard, so it is both `flying` and `fire` types, and it is weak against `water` types.

Pokémon that belong to two types occupy two rows in our spreadsheet. In addition, every Pokémon has multiple stats to determine how it performs in battle. A description of each stat can be found in the [Pokémon Database](https://pokemondb.net/pokedex). For example, Blastoise has a higher defense stat than Charizard, so it will better withstand physical attacks. For our analysis, we will look at the type with the highest number for each stat.

A pivot table is a tool designed specifically to aggregate data, and it will be the easiest way to aggregate Pokémon by type in our spreadsheet. To create a pivot table, select your data, and select the Pivot Table option. Since we are aggregating by Pokémon type, we will add “Type” to rows in the pivot table options.

![image5](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image5.jpg)

The resulting pivot table has a row for each unique type  

Right now, our pivot table is blank, and we need to add values to it. Since we want to count the number of unique Pokémon in each type, we would add it to values in our pivot table options.

![image4](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image4.jpg)  
![image5](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image5.jpg)

We are counting the number of unique Pokémon names for each type  

Since there is no type that is definitively the “strongest”, we will look at the strongest type for each stat. This would be useful for Pokémon players who are building balanced teams with both offensive;y- and defensively-inclined Pokémon. To see which type has the highest median values for each stat, we will add additional options to values in the pivot table options.

![image10](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image10.jpg)

Calculating the median of each stat for each type  

At this point, we can see our results in the pivot table:

![image2](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image2.png)

The highest values in each column are highlighted in green, and lowest values are highlighted in yellow  

Here are some interesting observations from this initial analysis:

- There are a lot of `water`-type Pokémon and very few `ice`-type Pokémon. Clearly, most Pokémon aren’t living in winter conditions! 🌴
- `Dragon`-type Pokémon seem to be the strongest while `bug`-type Pokémon are the weakest. 🐉 > 🐞
- `Fairy`-type Pokémon have low attack. Guess we don’t have to worry about being attacked by the tooth fairy. 🧚
- `Steel`-type Pokémon have the strongest defense. Does the aluminum industry have something to say about that? 🤔
- [ ] - [ ] 
- `Rocks` are slow. Even the `ground` and `grass` are faster…🗿
## Now to Python
Spreadsheets are great, and we were able to glean some fun insights from our pivot table analysis. However, **using [Python with the Pandas library](https://www.codecademy.com/learn/data-processing-pandas?utm_source=ccblog&utm_medium=blog&utm_campaign=publication&utm_content=Pokemon) is far superior to spreadsheet analysis.**

Writing code with Pandas is significantly quicker than interacting with a spreadsheet’s GUI interface (did you see all of those screenshots above?).

To aggregate data with Pandas, you will need to complete the following steps:

1. **Import the Pandas library**
2. **Upload your data to a Pandas DataFrame**
3. **Complete the aggregation**

For our Pokémon analysis, our commented code and output are below:

![image8](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image8.png)  
![image3](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image3.png)

Unlike the spreadsheet analysis, there are no intermediate steps when aggregating data with Python and Pandas.
## Modifying our analysis
The dataset we used contained all Pokémon. However, only a subset of Pokémon are available in each "Let’s Go" game. Download the data with only the subset [here](https://raw.githubusercontent.com/albemlee/pokemon_data/master/letsgo_pokemon.csv) (right click and select "_Save As…_").

To aggregate this new data with spreadsheets, we would have to repeat all of the manual steps involved in making a pivot table. However, with Python, we only need to modify a single line of code:

![image9](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image9.png)  
![image7](https://www.codecademy.com/resources/blog/wp-content/uploads/2018/12/image7.png)

We only needed to change one line of code to modify our analysis  

When only Pokémon available in "Let’s Go Pikachu" and "Let’s Go Eevee" are included, `Dragon`-type Pokémon still have the highest overall stats. However, they do not dominate as much as they did before in each of the stats, and overall, the stats are distributed more evenly across types.


## What’s next
High-level decision makers often require analysts to make minor adjustments to view data in a slightly different format. In these cases, Python will save significantly more time when compared to traditional spreadsheet analysis.

I’d encourage you to try analyzing the data yourself. Below are other modifications you can apply to our Pokémon analysis:

- Include only final evolved Pokémon
- Exclude legendary Pokémon that are ineligible for Pokémon competitions

To learn more about data wrangling with Python and Pandas, take a look at Codecademy’s [Data Analysis with Pandas](https://www.codecademy.com/learn/data-processing-pandas?utm_source=ccblog&utm_medium=blog&utm_campaign=publication&utm_content=Pokemon) course.


12/7-Organizations-Helping-Girls---Women-Build-Careers-in-Tech-1.jpg?w=1024)](https://www.codecademy.com/resources/blog/7-organizations-helping-girls-women-build-careers-in-tech/)

[Get Inspired](https://www.codecademy.com/resources/blog/category/get-inspired/)



# [8 Organizations Helping Girls & Women Build Careers in Tech](https://www.codecademy.com/resources/blog/7-organizations-helping-girls-women-build-careers-in-tech/)
03/05/2024

**7 minutes**

By Jacob Johnson

There’s a gender gap in tech — but it’s getting smaller thanks to organizations like these.

[![Pride-Day_R1_Blog2.webp?w=1024](https://www.codecademy.com/resources/blog/wp-content/uploads/2023/05/Pride-Day_R1_Blog2.webp?w=1024)](https://www.codecademy.com/resources/blog/python-code-challenges-lgbtq-pride/)

[Learning Tips](https://www.codecademy.com/resources/blog/category/learning-tips/)



# [8 Python Code Challenges to Try During Pride](https://www.codecademy.com/resources/blog/python-code-challenges-lgbtq-pride/)
06/01/2023

**4 minutes**

By Cory Stieg

Celebrate Pride with these bite-sized Python coding challenges.

[![what-is-open-source-1.png?w=1024](https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/what-is-open-source-1.png?w=1024)](https://www.codecademy.com/resources/blog/what-is-open-source/)

[Learning Tips](https://www.codecademy.com/resources/blog/category/learning-tips/)



# [What Is Open Source?](https://www.codecademy.com/resources/blog/what-is-open-source/)
09/22/2022

**8 minutes**

By Codecademy Team

Learn why developers and companies love open source software and how to start contributing to open-source projects.

[![How-Does-the-Internet-Work-.png?w=1024](https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/How-Does-the-Internet-Work-.png?w=1024)](https://www.codecademy.com/resources/blog/how-does-the-internet-work/)

[Learning Tips](https://www.codecademy.com/resources/blog/category/learning-tips/)



# [How Does the Internet Work?](https://www.codecademy.com/resources/blog/how-does-the-internet-work/)
07/28/2022

By Codecademy Team

Check out this wonderful explanation of how the Internet works. Discover our courses that provide you with the skills you need to design cyber solutions.

[![professional-benefits-learning-to-code.png?w=1024](https://www.codecademy.com/resources/blog/wp-content/uploads/2022/12/professional-benefits-learning-to-code.png?w=1024)](https://www.codecademy.com/resources/blog/what-boosting-retention-looks-like-during-the-great-resignation/)

[Business](https://www.codecademy.com/resources/blog/category/business/)



# [What Boosting Retention Looks Like During “The Great Resignation”](https://www.codecademy.com/resources/blog/what-boosting-retention-looks-like-during-the-great-resignation/)
10/21/2021

By Warren Lawless


[![Instagram Post](https://scontent-iad3-2.cdninstagram.com/v/t51.29350-15/432112774_1132033474592137_5888032542713156760_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=18de74&_nc_ohc=ClMRMcgFApAAX9VMuui&_nc_ht=scontent-iad3-2.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfCWf3XyRpjqktV2ni2Pwc8vDTuDWtMe-MHN_EEfns_UbA&oe=65F91CDE)](https://www.instagram.com/p/C4YVDWkOQyb/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/431979871_1617101139107636_1532223639909243218_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=18de74&_nc_ohc=UcAGvU38Hv4AX-SxSEd&_nc_oc=AQkJac_s0EZR0mCXzmLS4klw_2jfqcZ0sxNTN4mrd4o6dn6NuNvA5fxBCWO5Idm_7Lo&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfAAIRz8rlqAhyVzBRdO7YExBY4x6odA6p5B9sdUv7Gtug&oe=65F8F03C)](https://www.instagram.com/p/C4RDhFYRCXa/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/431954683_454691146885584_6339648388255410914_n.heic?stp=dst-jpg&_nc_cat=110&ccb=1-7&_nc_sid=18de74&_nc_ohc=dyaAne-6dswAX_5h0ZL&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfArQnCV0kMv14-ce2nsakrXy6VtDKedwMHGhbaha-eIyA&oe=65FA4DA7)](https://www.instagram.com/p/C4OJe6JrPmx/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/431749721_3232420880395635_654768753733608189_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=18de74&_nc_ohc=aWbzOF820PwAX80G3lK&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBggZDs_X_eSsN63hJJELd8Fc61VTwfM97rCTnK67ZzmQ&oe=65F9AF9B)](https://www.instagram.com/p/C4LmjeSMw8L/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/431715582_318943031160216_6635180724602602596_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=18de74&_nc_ohc=yKNWZ2t3HZwAX-55_0Z&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBOw0JJRSxfUu9Z-b64hL_oVy1b_OwIsDvDY3nrrvDqQw&oe=65FA1AC5)](https://www.instagram.com/p/C4JFxGZsJF9/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/431535386_737447548365932_8667382953321994390_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=18de74&_nc_ohc=4Nb7gET_AwkAX8sCoe8&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBlnqphz-bMgxhg4TGCbnojb0mAAweFIOK_0F7RHVtn7w&oe=65F9E94C)](https://www.instagram.com/reel/C4GZtVjOSaB/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/430335103_631950762396577_7969932595876133364_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=18de74&_nc_ohc=OjzI2DLZVh8AX8uRDUr&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBVQ516RavEOJOVOZqy-ELOHl_qRB-_4Yq9IS9xXjVgmQ&oe=65F9A09B)](https://www.instagram.com/reel/C3-2IG0uw1T/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/430367636_446777397914890_273174304617012477_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=18de74&_nc_ohc=ez5CRyHSBZoAX-LW4yv&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfDHPzzMscvroDrtX6oy9cUM-K0bxue7DGiJPfRz0qo4AQ&oe=65FAA1EC)](https://www.instagram.com/p/C38EyQ_u9Y-/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/430619446_1103168614051496_6767101658075651727_n.heic?stp=dst-jpg&_nc_cat=110&ccb=1-7&_nc_sid=18de74&_nc_ohc=fxYWlp-IeboAX9L7xax&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBsqA_S0qzwdIVztHwWzOELLgOImvIRq7yptaQVDtspvQ&oe=65F95562)](https://www.instagram.com/p/C35kdERuyHl/)

[![Instagram Post](https://scontent-iad3-2.cdninstagram.com/v/t51.29350-15/430103309_411030934670227_9173306435543831790_n.heic?stp=dst-jpg&_nc_cat=105&ccb=1-7&_nc_sid=18de74&_nc_ohc=6nHerUlrJ-4AX-jo2RN&_nc_ht=scontent-iad3-2.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfDyv8ZnhfxHcxsXCqxOCCTcPItcMGkEIEo13OO-7AUhEQ&oe=65F9ABA0)](https://www.instagram.com/p/C327sfJOKue/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/429571590_399519376003150_8865579862667511406_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=18de74&_nc_ohc=qcbCwa87HE8AX-Z6RaT&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfAsqWXzOx0zb8zuxjv94lu9uF65k8XEUiPN3YvspsR-8Q&oe=65F9872B)](https://www.instagram.com/p/C31CMNVOsmJ/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/429838919_249749771521113_4362841570985751839_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=18de74&_nc_ohc=_lD6oPKUGtoAX-NCjVU&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfB4to_XUx4jC9kVUvFCyxsTSu65XZGXwCxxzLk-mmgvgw&oe=65F9419E)](https://www.instagram.com/reel/C30XlteOEEO/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/429504896_926943348783950_2826750948784456895_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=18de74&_nc_ohc=wf2NwMc1gE0AX_zR7Cr&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfDZ74sukX1U5xHMwWfX922iT60qV_gP4HZDro7a4r1sgA&oe=65F91A82)](https://www.instagram.com/p/C3viSRgsV8A/)

[![Instagram Post](https://scontent-iad3-2.cdninstagram.com/v/t51.29350-15/429568964_1337316713618182_8930860658213623688_n.heic?stp=dst-jpg&_nc_cat=100&ccb=1-7&_nc_sid=18de74&_nc_ohc=7O1r8-9G8U0AX_I0J5G&_nc_ht=scontent-iad3-2.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfADAH_NDqOB-xMaNzVXD-ZjoqCVLueQuxQVYTn1Y2exEg&oe=65F9C1CC)](https://www.instagram.com/p/C3s3oL_OeJ3/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/429074981_360729233538255_317460788718103032_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=18de74&_nc_ohc=AoXipIjgmU4AX-zcATV&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBh64WDmJAkAXkiFZccaNloYu1SA88gi2uU61E5kA6TFA&oe=65F9E0C9)](https://www.instagram.com/p/C3nxm2iO0VX/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/429231598_1088691592456683_5437793012965362993_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=18de74&_nc_ohc=gYcHy6dx0b8AX_P731n&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfD_KUjnixHqgQztp21cdE3cOoCfu4qypkmZfBxnCyqRbw&oe=65F965BF)](https://www.instagram.com/p/C3lCvC7OBpb/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.2885-15/427927976_1531662467680004_2506766048730543920_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=18de74&_nc_ohc=DtyMzPLCDVIAX9CE7zn&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfBf8n-FtN_NH3MEqJJQFi_BMZJ5nDr_kN0lAMmtXe9iCA&oe=65F9626A)](https://www.instagram.com/p/C3a9w4eu73d/)

[![Instagram Post](https://scontent-iad3-1.cdninstagram.com/v/t51.29350-15/427840207_705142588466642_7748775616570335555_n.heic?stp=dst-jpg&_nc_cat=104&ccb=1-7&_nc_sid=18de74&_nc_ohc=lj0Z_dFEyAYAX8A0xdU&_nc_ht=scontent-iad3-1.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfAxEoNyegvr-GgbtCot4UAlG-A9th96eROEYHpABBC7_g&oe=65FA82F7)](https://www.instagram.com/p/C3YEMmCuBDo/)

[![Instagram Post](https://scontent-iad3-2.cdninstagram.com/v/t51.2885-15/427129223_420355697080294_878503512055433580_n.jpg?_nc_cat=100&ccb=1-7&_nc_sid=18de74&_nc_ohc=6mOml8QQh6sAX-_jrxG&_nc_ht=scontent-iad3-2.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfAdh_j17Dd1DEPqpmllVvnp_7EaWDhYFEGDJ5ChLU6wqg&oe=65F8D7ED)](https://www.instagram.com/p/C3ViHFkREVW/)

[![Instagram Post](https://scontent-iad3-2.cdninstagram.com/v/t51.2885-15/426825274_2512626778920595_7306758713456076628_n.jpg?_nc_cat=100&ccb=1-7&_nc_sid=18de74&_nc_ohc=8ItX4gy7ev0AX9kYAET&_nc_oc=AQkkAUjvVo-QsUxTkxGP4hOOiupiNYlQs7qAU8VWem_pilMk1ImV0r3DqYln47POkvY&_nc_ht=scontent-iad3-2.cdninstagram.com&edm=AM6HXa8EAAAA&oh=00_AfCOdGgFs6aoBFnLECF3hINpNATM95uj9_KyBdkOqAsTjg&oe=65F9C7DE)](https://www.instagram.com/p/C3S4tzxO9aZ/)


## Find a plan that fits your goals
- [Explore plans](https://www.codecademy.com/pricing?utm_source=ccblog&utm_medium=ccblog&utm_content=blogsignupbar)


## Company
- [About](https://www.codecademy.com/about)
- [Careers](https://www.codecademy.com/about/careers)
- [Affiliates](https://www.codecademy.com/pages/codecademy-affiliate-program)

- [](https://twitter.com/Codecademy)
- [](https://codecademy.com/users/redirect?redirect_url=https://www.facebook.com/groups/codecademy.community)
- [](https://instagram.com/codecademy)
- [](https://www.youtube.com/@codecademy)
- [](https://www.tiktok.com/@codecademy)


## Resources
- [Articles](https://www.codecademy.com/articles)
- [Blog](https://www.codecademy.com/resources/blog)
- [Cheatsheets](https://www.codecademy.com/resources/cheatsheets/all)
- [Code challenges](https://www.codecademy.com/code-challenges)
- [Docs](https://www.codecademy.com/resources/docs)
- [Projects](https://www.codecademy.com/projects)
- [Videos](https://www.codecademy.com/resources/videos)
- [Workspaces](https://www.codecademy.com/pages/workspaces)


## Support
- [Help Center](https://help.codecademy.com/)


## Plans
- [For individuals](https://www.codecademy.com/pages/paid-plans)
- [For students](https://www.codecademy.com/student-center)
- [For teams](https://www.codecademy.com/business)
- [Discounts](https://www.codecademy.com/pages/codecademy-discount-codes)


## Community
- [Chapters](https://community.codecademy.com/chapters)
- [Code Crew](https://try.codecademy.com/code-crew/)
- [Discord](https://discord.com/invite/codecademy)
- [Events](https://www.codecademy.com/events)
- [Forums](https://discuss.codecademy.com/)
- [Learner Stories](https://www.codecademy.com/resources/blog/category/learner-stories)
- [Student Beans](https://connect.studentbeans.com/v4/hosted/codecademy/US)


## Subjects
- [AI](https://www.codecademy.com/catalog/subject/artificial-intelligence)
- [Cloud Computing](https://www.codecademy.com/catalog/subject/cloud-computing)
- [Code Foundations](https://www.codecademy.com/catalog/subject/code-foundations)
- [Computer Science](https://www.codecademy.com/catalog/subject/computer-science)
- [Cybersecurity](https://www.codecademy.com/catalog/subject/cybersecurity)
- [Data Analytics](https://www.codecademy.com/catalog/subject/data-analytics)
- [Data Science](https://www.codecademy.com/catalog/subject/data-science)
- [Data Visualization](https://www.codecademy.com/catalog/subject/data-visualization)
- [Developer Tools](https://www.codecademy.com/catalog/subject/developer-tools)
- [DevOps](https://www.codecademy.com/catalog/subject/devops)
- [Game Development](https://www.codecademy.com/catalog/subject/game-development)
- [IT](https://www.codecademy.com/catalog/subject/information-technology)
- [Machine Learning](https://www.codecademy.com/catalog/subject/machine-learning)
- [Math](https://www.codecademy.com/catalog/subject/math)
- [Mobile Development](https://www.codecademy.com/catalog/subject/mobile-development)
- [Web Design](https://www.codecademy.com/catalog/subject/web-design)
- [Web Development](https://www.codecademy.com/catalog/subject/web-development)


## Languages
- [Bash](https://www.codecademy.com/catalog/language/bash)
- [C](https://www.codecademy.com/catalog/language/c)
- [C++](https://www.codecademy.com/catalog/language/c-plus-plus)
- [C#](https://www.codecademy.com/catalog/language/c-sharp)
- [Go](https://www.codecademy.com/catalog/language/go)
- [HTML & CSS](https://www.codecademy.com/catalog/language/html-css)
- [Java](https://www.codecademy.com/catalog/language/java)
- [JavaScript](https://www.codecademy.com/catalog/language/javascript)
- [Kotlin](https://www.codecademy.com/catalog/language/kotlin)
- [PHP](https://www.codecademy.com/catalog/language/php)
- [Python](https://www.codecademy.com/catalog/language/python)
- [R](https://www.codecademy.com/catalog/language/r)
- [Ruby](https://www.codecademy.com/catalog/language/ruby)
- [SQL](https://www.codecademy.com/catalog/language/sql)
- [Swift](https://www.codecademy.com/catalog/language/swift)


## Career building
- [Career paths](https://www.codecademy.com/catalog/all)
- [Career center](https://www.codecademy.com/career-center)
- [Interview prep](https://www.codecademy.com/pages/interview-prep)
- [Professional certification](https://www.codecademy.com/pages/pro-certifications)
- [Compare to bootcamps](https://try.codecademy.com/bootcamps)
- —
- [Full Catalog](https://www.codecademy.com/catalog/all)
- [Beta Content](https://www.codecademy.com/catalog/subject/beta)
- [Roadmap](https://trello.com/b/vAgDXtT6/codecademy-releases-roadmap)


## Mobile
- [![Download on the App Store](https://www.codecademy.com/resources/blog/wp-content/themes/favsolution/assets/images/app-store.svg)](https://itunes.apple.com/us/app/codecademy-go/id1376029326)
- [![Get it on Google Play](https://www.codecademy.com/resources/blog/wp-content/themes/favsolution/assets/images/google-play.png)](https://play.google.com/store/apps/details?id=com.ryzac.codecademygo)

- [Privacy Policy](https://www.codecademy.com/policy)
 - [Cookie Policy](https://www.codecademy.com/cookie-policy)
 - [Do Not Sell My Personal Information](https://privacy.codecademy.com/?_gl=1*m4g8qs*_ga*NDIxOTMxNDMyOS4xNjY4NTM2MDM0*_ga_3LRZM6TM9L*MTY3MTY0NTc3MC4yOS4xLjE2NzE2NDU3ODYuNDQuMC4w)
 - [Terms](https://www.codecademy.com/terms)

Made with ❤️ in NYC © 2024 Codecademy
