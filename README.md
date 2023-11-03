# 15.093_optimization_methods

## Datasets
- Nike manufacturing data: https://manufacturingmap.nikeinc.com/#
    - Aggregate by Region (Field: Region)
    - Most important fields: Factory Name, Factory Type, Product Type, Region, and Total Workers
    - Simple model aggregation: Group by region - sum total workers
    -  Need to link workers to output
- Nike 10K report: https://www.sec.gov/ix?doc=/Archives/edgar/data/320187/000032018723000039/nke-20230531.htm#i8dbf0fa99ce247278aa0e00c038ec4d0_73
     - Have revenue by footware, equipment, apperal
     - Translate revenue to sales based on average price of top 10 selling items in each category
     - Breakdown of revenue by region and category in regions
     - Cost of sales is reported --> not broken down by labor vs raw material vs shipping vs inventory
- Shipping Cost --> need to obtain
    - cost for shipping container from region to region
    - how much can ship per container --> estimate cost per item to ship

- Time period
    - workers grow with revenue proportionally
    - 10 year period: 2013 - 2023
 
- To Do
   - Virginia:
         - Get 10K data
         - Determine cost sales split
   - Jason:
         - Set up initial (simple model)
         - Shipping Cost
## Meeting 11/3
 - Product: shoes only
 - Need to do:
        - Average price: go to Nike website and average top 10 best sellers
- Cost : C_ijt = 1/3 * (cost of sales)
- Shipping Cost: $0.10 - $0.50 per pair of shoes
      - Once we have sale price of shoes, test inventory vs shipping costs with above assumptions - Virginia
- Supply: Max number of shoes a factory can reduce
        - Number of shoes told * 1.1-1.3 --> divide between factories depending on workers - Virginia
- To Do:
  - Get datasets needed for model - Virginia
  - Read in data to Julia - Virginia
  - Pre-processing - Virginia
  - Start writing constraints - Jason

