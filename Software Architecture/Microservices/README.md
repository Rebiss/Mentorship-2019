# Microservices.

<div>
    <h3> Monolit </h3>
    <p>
        Ճարտարապետական ​​ոճը, երկու կամ երեք շերտանի կառուցվածքով։ Փոքր և պարզ ծրագրերի համար այս ճարտարապետությունը հիանալի է գործում, բայց 
        եթե ցանկանում ենք մեծացնել ծրագրերը՝ դրան ավելացնելով նոր ծառայություններ(service) և տրամաբանություն: 
    <p>
<div>

```sh
User Interface
Business Logic Leyer
Data Access Leyer
DataBase
```

</div>
        Կամ ունեք մեկ այլ ծրագիր, որն աշխատում է նույն տվյալների հետ (օրինակ, բջջային(mobile) ծրագիր), ապա հավելվածի ճարտարապետությունը փոքր-ինչ կփոխվի:
<div>

```sh
User Interface (App_1)  |   User Interface (App_2)
Business Logic Leyer    |   Business Logic Leyer
Data Access Leyer       |   Data Access Leyer

                    DataBase
```

</div>
    Այսպես թե այնպես, հավելվածը մեծանում և զարգանում է և առաջանում են ճարտարապետության հետ խնդիրների՝
    <ul>
        <li>Համակարգի բարդությունը աճում է</li>
        <li>Շատ սխալներ</li>
        <li>Փոփոխությունները անհնար են դառնում</li>
        <li>Դժվար է հասկանալ, մանավանդ եթե համակարգը ՛՛սերնդեսերունդ՛՛ փոխանցվում է, տրամաբանությունը մոռացվում է, նոր մարդիկ եկան, բայց        մեկնաբանություններ ու թեստեր չկան։
        </li>
        <li>Տեխնոլոգիաները թարմացնելը դառնում է խնդիր</li>
    </ul>
    Փորձելով լուծել այս խնդիրները, հանդիպում ենք CAP-ի տեսությանը: Տեսությանը այն է, որ մենք, տեսականորեն, չենք կարող միաժամանակ ապահովել համակարգը՝
    <ul>
        <li>Համաձայնեցում( Consistency )</li>
        <li>Հասանելություն( Availability )</li>
        <li>Բաժանում( Partitioning) </li>
    </ul>
    Հետևաբար, մենք պետք է զոհաբերենք երեքից մեկը ՝ կողմ մյուս երկուսի:
    <p> CA — consistency + availability </p>
    <p> CP – consistency + partitioning </p>
    <p> AP — availability + partitioning </p>
    Այժմ, երբ մենք ծանոթ ենք CAP-ի տեսությանը, մենք հասկանում ենք, թե ինչպես կարող ենք համակարգը զարգացնել այնպես, որ այն լինի արագ, մատչելի և բաշխված: Ոչ մի կերպ!!!  Մենք միայն պետք է ընտրենք երեք հատկություններից երկուսը:
    </p>
</div>

<hr />

<div>
    <h3> Microservices & Service Oriented Architecture (SOA) </h3>
    <p>
        Ինչ է SOA-ն - Ծառայություններ(service) վրա հիմնված ճարտարապետություն։ ԵՎ ինչպե՞ս է SOA-ն համեմատվում Microservices ճարտարապետության հետ?: Ի վերջո, թվում է, թե SOA-ն նույնն է, բայց դա այնքան էլ այդպես չէ։ Իսկ իրականում Microservices ճարտարապետությունը SOA-ի մասնավոր դեպքն է։
    </p>
    <p>
    Microservices Architecture - ընդամենը մի շարք ավելի խիստ կանոնների և համաձայնությունների համակարգ է, թե ինչպես կառուցել նույն SOA-ն:
    </p>
    <div>
        <h3>Ի՞նչ է Microservices Architecture?</h3>
        <ul>
            <li>Փոքր (Small) - Սա նշանակում է, որ Microservices ճարտարապետության մեջ services-ը չի կարող մշակվել մեկից ավելի թիմի կողմից: Սովորաբար մեկ թիմ զարգացնում և մշակում է մոտ 5-6 services: Ավելին, յուրաքանչյուր services լուծում է մեկ բիզնես խնդիր, և մեկ մարդը ի վիճակի է այն հասկանալ: Եթե ​​ոչ, ապա ժամանակն է services բաժանել:
            </li>
            <li>Կենտրոնացած (Focused) - Սա նշանակում է, որ micro-services լուծում է միայն մեկ բիզնես խնդիր, և այն լուծում է լավ: Նման services-ը  մեկուսացված այլ services-ից:
            </li>
            <li>Թույլ կապված (Low coupled-GRASP) - Սա այն դեպքում, երբ մի services-ի փոխելը չի ​​պահանջում այլ services-ի փոխելուն: DI և IoC</li>
            <li>Խիստ համաձայնեցված (Highly cohesive) - Սա նշանակում է, որ class-ը կամ component-ը պարունակում է բոլոր անհրաժեշտ մեթոդները խնդրի լուծման համար: SOLID(SRP) 
            </li>
        </ul>
    </div>
    <div>
        <h3>Microservices-ի բնութագրերը</h3>
        <ul>
            <li>Բաժանել կոմպոնենտների(services) - Կոմպոնենտները լինում են 2 տեսակի՝ գրադարաններ և services-ներ։ Եթե կարող ենք ինչ-որ բան վերցնել և ապահով կերպով փոխարինել նոր տարբերակով, դա կոմպոնենտ(services) է։ </li>
            <li>Խմբավորում ըստ բիզնես առաջադրանքների - UI-BL-DB </li>
            <li>Services-ները բիզնեսի իմաստ ունեն</li>
            <li>Խելացի services-ներ և պարզ հաղորդակցություններ - Services-ի փոխգործակցության տարբեր տարբերակներ կան: Պատահում է, որ վերցնում ենք
            "հոսք" որը գիտի երթուղիների(routing) և բիզնեսի կանոնների մասին, և պատրաստի օբեկտները հասնում են services-ներին: Ստանում ենք շատ խելացի middleware և հիմար(անիմաստ) endpoint-ներ։ Որը իրականում Antipattern է։
            </li>
            <li>Ապակենտրոնացված կառավարում</li>
            <li>Տվյալների ապակենտրոնացված կառավարում - Սա նշանակում է որ յուրաքանչյուր Services ունի միայն իր սեփական տվյալների բազան։ Միակ դեպքը, երբ տարբեր Services-ներ կարող են օգտագործել նույն տվյալների բազան, այն դեպքն է երբ Services-ը մյուսի ճշգրիտ պատճեն է: Տվյալների բազանները միմյանց հետ չեն փոխազդում։</li>
            <li>Տեղակայման և մոնիտորինգի ավտոմատացում - CI/CD, ELK stack, Monitoring tools, ...</li>
            <li>Design for failure (Chaos Monkey) - Մինչ Microservices-ի կառուցելը մենք պետք է ենթադրեք, որ մեր services-ները չեն աշխատում: Այլ կերպ ասած, մեր services-ները պետք է պատրաստ լինեն այն բանին, որ կարող են պատասխան չըստանալ, եթե որոշ տվյալներ է ակնկալվում: Այսպիսով, մենք պետք է պատրաստ լինենք այդպիսի իրավիճակի, որ ինչ-որ բան կարող է մեզ համար չաշխատել: Սա անհրաժեշտ է համակարգի հուսալիությունը գնահատելու համար:
            </li>
        </ul>
    </div>
    <div>
        <h3> Microservices-ի տարբեր տեսակներ </h3>
        <ul>
            <li>Service Discovery (RPC Style) - Service-ը գիտեն միմյանց մասին և ուղղակիորեն շփվում են իրար հետ</li>
            <li>Message Bus (Event-driven) - Publish/Subscribe Pattern դա անհրաժեշտ է, որպեսզի մի ծառայություն կարողանա մյուսին տեղեկացնել, որ իր համար ինչ-որ բան փոխվել է, որպեսզի այլ ծառայություններ կարողանան արձագանքել դրան:</li>
            <li>Hybrid - Խառը տարբերակ, երբ որոշ դեպքերում մենք օգտագործում ենք RPC, իսկ մյուսների համար` Message Bus </li>
        </ul>
    <div>
    <div>
        <h3> Microservices-ի առավելությունները և թերություններ </h3>
        <h5> Առավելությունները՝ </h5>
        <ul>
            <li>Մոդուլային հստակ բաժանում</li>
            <li>Բարձր հասանելություն</li>
            <li>Տեխնոլոգիաների բազմազանություն </li>
            <li>Անկախ տեղակայում</li>
        </ul>
        <h5> Թերությունները՝ </h5>
        <ul>
            <li>Ծրագրավորման և մշակման բարդությունը</li>
            <li>Վերջնական համաձայնեցումը</li>
            <li>Տեխնիկական աջակցության(support` DevOps) բարդություն </li>
        </ul>
    <div>
<div>

