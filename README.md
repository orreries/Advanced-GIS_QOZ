# Qualified Opportunity Zones Assessment

## **Project Overview**

## [Story Map](https://arcg.is/18iTPH1)

This project examines the spatial relationship between mortgage activity, Qualified Opportunity Zones (QOZs), rent changes over time, and residential development indicators in California. The goal is to understand whether QOZs are positioned in areas experiencing economic investment or market shifts, and how spatial statistics reveal the dynamics of mortgage clustering and development. The analysis incorporates mortgage counts, rent values from 2010 (inflation-adjusted) and 2023, and residential building permits, alongside designated QOZ boundaries.

#### _Why California?_
California is used as the basis for examining Qualified Opportunity Zone tax incentives within this project because it elucidates the tensions shaping housing markets nationwide. It exhibits underbuilding, escalating rents, and notable economic stratification. The state offers a view of QOZs operating within areas with the highest construction volumes nationally, yet also experiencing the persistent affordability crises. They crop up in markets that are among the most regulated but also among the most expensive. This makes California a prudent frame of reference for observing mechanisms linking federal tax policy, local development patterns, and emerging displacement pressures.

The spatial patterns observable in California are not unique to the state. This includes QOZ clustering in underinvested urban cores, new development closely concentrating outside those boundaries, and affordability pressures radiating outward. California offers a clarifying lens on dynamics that operate more broadly. It showcases how tax incentives interact with market forces and regulatory constraints to shape who builds where and who can afford to stay. While the focus is on California, the underlying mechanisms provide insights applicable to communities nationwide grappling with similar policy tools and market conditions.

## **Data Sources**

- Census tracts (TIGER/ACS)
-  QOZ polygons (IRS Opportunity Zone dataset)
- Units with mortgages (tract-level aggregate)
- Median gross rent (ACS 2010 adjusted to 2023 dollars, and ACS 2023)
- Residential building permits (California and Florida)
- ArcGIS spatial statistics tools (Global Moran’s I, Local Moran’s I, Getis–Ord Gi*)

## **Research Questions**

1. Are mortgages clustered spatially in California?
2. Do QOZs overlap with mortgage clusters or outlier tracts?
3. How have rents shifted from 2010 to 2023, and how do QOZ areas fit into those patterns?
4. Are new residential building permits occurring inside QOZs or in surrounding areas?
5. Overall, does spatial evidence suggest that QOZ policy is aligned with real market activity?

## **Building Permits: California vs. Florida**

[Project info](https://github.com/orreries/Advanced-GIS_QOZ/tree/main/Lab%201)

In California, residential building permits are clustered heavily in coastal metros (Los Angeles, San Diego, the Bay Area). QOZs are usually located outside these active permit corridors, implying a disconnect between where development is happening and where incentives are offered.

In Florida, building permits are more spatially dispersed across metropolitan areas, and QOZs more frequently overlap areas with active construction. This indicates stronger alignment between QOZ placement and real development patterns in Florida than in California.

## Mortgages (Spatial Statistics)

### *Global Moran’s I (Spatial Clustering Test)*

Global Moran’s I = 0.356
z-score = 72.31
p-value < 0.000001

Mortgage activity in California is highly clustered. High mortgage tracts tend to be near other high mortgage tracts, and low-mortgage tracts cluster together as well. This confirms that local spatial analyses (Local Moran’s I and Getis–Ord Gi*) are appropriate.

### *Getis–Ord Gi* (Hot Spot Analysis)*

The Gi* hotspot map shows statistically significant concentrations of mortgage activity. Strong hotspots (95–99% confidence) occur in the San Francisco Peninsula, Silicon Valley, Oakland, and Sacramento metro area. Cold spots are found in the Central Valley, rural northern counties, and outer exurban regions.

Most QOZs do not intersect strong mortgage hotspots. Instead, they tend to lie in cold spot or not significant areas. When overlaps do occur, they are usually at lower confidence levels (around 90%). This suggests that QOZs are rarely placed in locations with strong underlying mortgage investment dynamics.

### *Local Moran’s I (Cluster and Outlier Analysis)*

The Local Moran’s I map reveals four types of spatial patterns:

- High–High clusters: Strong mortgage markets, appearing in the Bay Area, Sacramento, and Silicon Valley/San Jose.
- Low–Low clusters: Weak mortgage markets, concentrated in the Central Valley and rural northeastern California.
- High–Low outliers: Tracts with high mortgage activity despite being surrounded by low activity neighbors; these may represent localized redevelopment or early gentrification signals.
- Low–High outliers: Tracts with low mortgage activity surrounded by higher activity areas, often reflecting pockets of disinvestment.

QOZs mostly appear in Low–Low mortgage clusters, indicating that they are located in the weakest mortgage markets. A smaller number fall within High–Low or Low–High outlier tracts, suggesting uneven or emerging areas of investment or development potential.

 ## **Rent Change: 2010 to 2023** 

[Link to info and web map](https://github.com/orreries/GIS-Web-Map-Project-Lab-3-) 

Rent maps show significant increases in coastal regions such as Los Angeles, the Bay Area, and San Diego. Interior regions remain more affordable, though still rising. QOZs typically appear in lower rent tracts but often border zones where rents have increased sharply. This suggests that QOZs may be influenced by rising rent spillovers, even if the zones themselves are not currently in high rent markets.

## **Synthesis of Findings**

-  Development alignment differs by state. QOZs in Florida appear better positioned relative to new construction than those in California.
-   Mortgage activity is strongly clustered, with QOZs located mainly in low activity areas.
-   Hotspot analysis shows limited alignment between QOZ locations and regions of strong investment.
-   Localized outlier tracts point to small pockets of possible increased development.
-   Rent changes highlight rising economic pressure near many QOZ adjacent areas.

## **Interpretation for QOZ Policy**

**Strengths:**
QOZs successfully target low investment areas, consistent with their policy intent. Some tracts show emerging signs of investment that could be connected to QOZ incentives.

**Limitations:**
QOZs rarely coincide with high investment mortgage hotspots or active development regions, particularly in California. Structural constraints such as zoning and high land costs may limit the effectiveness of QOZ incentives. Market driven development pressures often bypass QOZs unless supported by additional policy measures.
