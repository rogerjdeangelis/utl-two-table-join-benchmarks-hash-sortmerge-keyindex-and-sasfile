# utl-two-table-join-benchmarks-hash-sortmerge-keyindex-and-sasfile
Two table join benchmarks hash sortmerge keyindex and sasfile 

    Two table join benchmarks hash sortmerge keyindex and sasfile                                                         
                                                                                                                          
    Very rough guide for joining two tables.                                                                              
                                                                                                                          
    By ChrisNZ                                                                                                            
    https://communities.sas.com/t5/user/viewprofilepage/user-id/16961                                                     
                                                                                                                          
    github                                                                                                                
    http://tinyurl.com/y2qn23j6                                                                                           
    https://github.com/rogerjdeangelis/utl-two-table-join-benchmarks-hash-sortmerge-keyindex-and-sasfile                  
                                                                                                                          
                                                                                                                          
    For detail see                                                                                                        
    http://tinyurl.com/yynt464e                                                                                           
    https://communities.sas.com/t5/SAS-Communities-Library/Study-on-the-best-method-to-join-two-tables/ta-p/406434        
                                                                                                                          
                                                                                                                          
    A lot depends on locality of reference and the size of memory.                                                        
                                                                                                                          
                                                                                                                          
      +----------+---------------------------------------------------------+                                              
      |          |                                                         |                                              
      |          |            TIME IN SECONDS FOR FASTEST METHODS          |                                              
      |Columns   |                                                         |                                              
      |Retrieved |               Percent of Rows Retrieved                 |                                              
      |          |                                                         |                                              
      +----------+----------+-----------+---------+--------+--------+------+                                              
      |          |      1%  |      5%   |   10%   |   20%  |   50%  | 100% |                                              
      |----------+----------+-----------+---------+--------+--------+------+                                              
      |          |INDEX KEY |     SASFILE KEY INDEX        |     HASH      |                                              
      |    1     |--------  |     -----------------        |     ----      |                                              
      |          |     47   |    53        53        58    |  65      73   |                                              
      |----------|          |                              |               |                                              
      |    5     |          |                              |               |                                              
      |          |     46   |    52        55        59    |  66      77   |                                              
      |----------|          |                              |               |                                              
      |    10    |          |                              |               |                                              
      |          |     48   |    58        60        66    |  69      80   |                                              
      |----------|          +-----------+------------------+               |                                              
      |    20    |                      |                                  |                                              
      |          |     49        59     |  64        69       71      82   |                                              
      |----------|                      |                                  |                                              
      |    30    |                      |                                  |                                              
      |          |     48         57    |  63        66       72      82   |                                              
      |----------|                      |                                  |                                              
      |    40    |                      |                                  |                                              
      |          |     47         56    |  64        67       75      89   |                                              
      |----------|                      +------------------+---------------+                                              
      |          |                                         |  SORT MERGEE  |                                              
      |    50    |                                         |  -----------  |                                              
      |          |     47         56        68       92    |  105     110  |                                              
      |          |                                         |               |                                              
      +----------+-----------------------------------------+---------------+                                              
                                                                                                                          
                                                                                                                          
