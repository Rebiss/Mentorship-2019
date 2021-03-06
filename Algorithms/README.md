# Ալգորիթմ (Algorithms).

<div>
    Ալգորիթմը ֆունկցիայի հաշվարկման որոշակի լավ սահմանված արդյունավետ մեթոդ է: 
    Քայլ առ քայլ հաշվարկային գործընթաց է։ Ավելի ճշգրիտ, ալգորիթմը ֆունկցիայի հաշվարկման որոշակի լավ սահմանված արդյունավետ մեթոդ է:
    Յուրաքանչյուր խնդիր լուծելու համար կարող են գոյություն ունենալ նպատակին հասցնող բազմաթիվ ալգորիթմներ։ Ալգորիթմների արդյունավետության մեծացումը ժամանակակից ինֆորմատիկայի խնդիրներից մեկն է։
    Ալգորիթմ իրականացնողը հիմնականում համակարգիչներն ու այլ սարքավորումներն են, սակայն ալգորիթմը պարտադիր չէ, որ կապված լինի ծրագրավորման հետ։
    Ալգորիթմների մեծ մասը նախատեսված է գործարկել որպես համակարգչային ծրագրեր։ Այնուամենայնիվ ալգորիթմներն իրականացվում են նաև այլ միջոցներով, ինչպիսիք են կենսաբանական նյարդային ցանցը (օրինակ, մարդու ուղեղը թվաբանական գործողություն կատարելիս, կամ միջատը սնունդ փնտրելիս), էլեկտրական շղթայում կամ մեխանիկական սարքում:
    Համակարգչային համակարգերում ալգորիթմը հիմնականում ծրագրավորողների կողմից մաթեմատիկական ապահովման մեջ ծրագրավորողների կողմից գրված տրամաբանության օրինակ է։ Նույնիսկ հին սարքի վրա աշխատող օպտիմալ ալգորիթմը ավելի արագ արդյունքներ կտա քան օչ օպտիմալը ավելի արագընթաց և արդյունավետ սարքավորման վրա։
</div>

![alt text](https://datascience.foundation/backend/web/uploads/blog/what-is-an-algorithm-featured12-30-2019_083310.png)

```bash
    .
    ├── Boyer–Moore–Horspool.js			    # 
    ├── Graph-Dijkstra.js			        # 
    ├── Graph-FindingCenter.js		        # 
    ├── Graph-Floyd–Warshall.js			    # 
    ├── Graph-Kruskal.js			        # 
    ├── Graph-Prima.js			            # 
    ├── Knuth–Morris–Pratt.js			    # Որոնել բառը տեքստի մեջ։
    ├── Polindrom.js			            # 
    ├── Search-Binary.js			        # Բինար որոնում։
    ├── Sort-Bubble.js			            # Պղպջակային տեսակավորում։
    ├── Sort-Insertion.js			        # Ներդրմամբ տեսակավորում։
    ├── Sort-Merge.js			            # Միաձուլման տեսակավորում։
    ├── Sort-Quick.js			            # Արագ տեսակավորում։
    ├── Sort-Selection.js			        # Ընտրության տեսակավորումը։
    ├── Sort-Odd_Even.js			        # Կենտ-զույգ տեսակավորումը
    └── ...                                 #
```
<div>
    <p>Նախագծում</p>
    <div>
        Ալգորիթմի նախագծումը վերաբերում է խնդրի լուծման և ալգորիթմների կառուցման մեթոդին կամ մաթեմատիկակական գործընթացին։ Ալգորիթմների նախագծումը գործողությունների հետազոտության շատ լուծումների տեսությունների մաս է կազմում, ինչպիսիք են դինամիկ ծրագրավորումը և բաժանիր որ տիրես ալգորիթմը։ Ալգորիթմների մշակման և իրականացման մեթոդները նաև կոչվում են ալգորիթմների նախագծման շաբլոններ։
        Ալգորիթմների մշակման կարևորագույն ասպեկտներից է ռեսուրսների One of the most important aspects of algorithm design is resource (կատարման ժամանակը, հիշողության օգտագործման ծավալը) արդյունավետությունն է։
        Ալգորիթմների մշակման բնորոշ քայլերն են`
    </div>
    <ul>
        <li>Խնդրի սահմանումը</li>
        <li>Մոդելի մշակումը</li>
        <li>Ալգորիթմի հստակեցում</li>
        <li>Ալգորիթմի մշակում</li>
        <li>Ալգորիթմի ճշգրտության ստուգում</li>
        <li>Ալգորիթմի վերլուծություն</li>
        <li>Ալգորիթմի գործարկում</li>
        <li>Ծրագրի ստուգում</li>
        <li>Փաստաթղթերի պատրաստում</li>
    </ul>
</div>

<div>
    <p> Հատկություններ </p>
    <ul>
        <li><b>Դիսկրետություն</b> – ալգորիթմը պետք է իրենից ներկայացնի պարզ քայլերի հաջորդականություն, որոնք կբերեն որևէ խնդրի լուծմանը։ Միևնույն ժամանակ, ալգորիթմի յուրաքանչյուր քայլի կատարման ժամանակը սահմանափակ է։</li>
        <li><b>Որոշվածություն </b> – ցանկացած պահի հաջորդ քայլը հստակ որոշվում է կախված համակարգի իրավիճակից։ Այսպիսով, ալգորիթմը տալիս է նույն     պատասխանը նույն սկզբնական տվյալների համար։ Հնարավոր է նաև, որ հաջորդ քայլը կախված լինի այդ պահին ընտրված պատահական թվից։</li>
        <li><b>Հասկանալի լինել</b> – ալգորիթմը պետք է ներառի միայն կատարողին հասկանալի և նրա տվյալների մեջ առկա գործողույթուններ։ </li>
        <li><b>Վերջավորություն </b>– ճիշտ տրված սկզբնական տվյալների դեպքում, ալգորիթմը պետք է վերջավոր քանակի քայլերից հետո տա ճիշտ պատասխանը։ <li>
        <li><b>Ունիվերսալություն</b>– ալգորիոմը պետք է կատարի իր ֆունկցիան ցանկացած թույլատրելի սկզբնական տվյալներ տալու դեպքում։ </li>
        <li><b>Արդյունավետություն </b>– որոշակի արդյունքների ստացում։</li>
        <li>Ալգորիթմը պարունակում է սխալներ, եթե արդյունքը սխալ է, կամ արդյունք չկա ընդհանրապես։ </li>
        <li>Ալգորիթմը չի պարունակում սխալներ, եթե տալիս է ճշմարիտ արդյունք։ </li>
    </ul>
</div>

<div> 
    <p>Հավելյալ հղումներ</p>
    <a href="https://hy.wikipedia.org/wiki/%D5%8F%D5%A5%D5%BD%D5%A1%D5%AF%D5%A1%D5%BE%D5%B8%D6%80%D5%B4%D5%A1%D5%B6_%D5%A1%D5%AC%D5%A3%D5%B8%D6%80%D5%AB%D5%A9%D5%B4">Տեսակավորման ալգորիթմ</a>
</div>