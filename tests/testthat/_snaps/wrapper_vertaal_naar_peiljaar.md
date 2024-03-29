# wrapper vertaal naar peiljaar op wijkniveau

    Code
      filter(df, grepl("Wageningen", gemeentenaam))
    Output
      # A tibble: 14 x 6
         wijkcode     gemeentenaam                       aanta~1 aanta~2 Gemid~3  jaar
         <chr>        <chr>                                <int>   <int>   <dbl> <dbl>
       1 "WK028900  " "Wageningen                      ~   33885    5125     1.7  2017
       2 "WK028901  " "Wageningen                      ~    4570     800     1.9  2017
       3 "WK028901  " "Wageningen                      ~    4725     440     2.3  2018
       4 "WK028902  " "Wageningen                      ~    2480       5     1.1  2018
       5 "WK028903  " "Wageningen                      ~    2750     545     2.2  2018
       6 "WK028904  " "Wageningen                      ~    2085     365     2.2  2018
       7 "WK028905  " "Wageningen                      ~    3170      35     1.4  2018
       8 "WK028906  " "Wageningen                      ~    6890    1435     1.7  2018
       9 "WK028907  " "Wageningen                      ~    5185     755     1.8  2018
      10 "WK028908  " "Wageningen                      ~    2505     560     1.6  2018
      11 "WK028909  " "Wageningen                      ~    3530     510     1.4  2018
      12 "WK028910  " "Wageningen                      ~    2520     710     1.9  2018
      13 "WK028911  " "Wageningen                      ~    1175     410     2.3  2018
      14 "WK028912  " "Wageningen                      ~    1365     385     2.1  2018
      # ... with abbreviated variable names 1: aantal_inwoners, 2: aantal_65plus,
      #   3: GemiddeldeHuishoudensgrootte_32

---

    Code
      filter(df_omgezet, grepl("Wageningen", gemeentenaam))
    Output
         gwb_code jaar aantal_inwoners aantal_65plus GemiddeldeHuishoudensgrootte_32
      1     28901 2017        4731.450    420.221218                        2.250470
      2     28901 2018        4725.000    440.000000                        2.300000
      3     28902 2017        2480.943      2.106764                        1.085815
      4     28902 2018        2480.000      5.000000                        1.100000
      5     28903 2017        2753.530    534.173181                        2.161249
      6     28903 2018        2750.000    545.000000                        2.200000
      7     28904 2018        2085.000    365.000000                        2.200000
      8     28904 2017        2086.779    359.545556                        2.172495
      9     28905 2018        3170.000     35.000000                        1.400000
      10    28905 2017        3173.439     24.453154                        1.372402
      11    28906 2017        6921.518   1338.344758                        1.584218
      12    28906 2018        6890.000   1435.000000                        1.700000
      13    28907 2018        5185.000    755.000000                        1.800000
      14    28907 2017        5198.047    714.988467                        1.725506
      15    28908 2017        2509.150    547.273581                        1.558570
      16    28908 2018        2505.000    560.000000                        1.600000
      17    28909 2017        3535.615    492.780891                        1.351131
      18    28909 2018        3530.000    510.000000                        1.400000
      19    28910 2017        2523.462    699.382214                        1.861657
      20    28910 2018        2520.000    710.000000                        1.900000
      21    28911 2018        1175.000    410.000000                        2.300000
      22    28911 2017        1175.612    408.123382                        2.283867
      23    28912 2017        1365.454    383.606834                        2.088000
      24    28912 2018        1365.000    385.000000                        2.100000
         berekend                             gemeentenaam   wijkcode
      1      TRUE Wageningen                               WK028901  
      2     FALSE Wageningen                               WK028901  
      3      TRUE Wageningen                               WK028902  
      4     FALSE Wageningen                               WK028902  
      5      TRUE Wageningen                               WK028903  
      6     FALSE Wageningen                               WK028903  
      7     FALSE Wageningen                               WK028904  
      8      TRUE Wageningen                               WK028904  
      9     FALSE Wageningen                               WK028905  
      10     TRUE Wageningen                               WK028905  
      11     TRUE Wageningen                               WK028906  
      12    FALSE Wageningen                               WK028906  
      13    FALSE Wageningen                               WK028907  
      14     TRUE Wageningen                               WK028907  
      15     TRUE Wageningen                               WK028908  
      16    FALSE Wageningen                               WK028908  
      17     TRUE Wageningen                               WK028909  
      18    FALSE Wageningen                               WK028909  
      19     TRUE Wageningen                               WK028910  
      20    FALSE Wageningen                               WK028910  
      21    FALSE Wageningen                               WK028911  
      22     TRUE Wageningen                               WK028911  
      23     TRUE Wageningen                               WK028912  
      24    FALSE Wageningen                               WK028912  

# wrapper vertaal naar peiljaar op gemeenteniveau

    Code
      filter(df, grepl("^Groningen", gemeentenaam))
    Output
      # A tibble: 2 x 6
        wijkcode     gemeentenaam                        aanta~1 aanta~2 Gemid~3  jaar
        <chr>        <chr>                                 <int>   <int>   <dbl> <dbl>
      1 "GM0014    " "Groningen                        ~  202810   25697     1.6  2018
      2 "GM0014    " "Groningen                        ~  231299   33349     1.7  2019
      # ... with abbreviated variable names 1: aantal_inwoners, 2: aantal_65plus,
      #   3: GemiddeldeHuishoudensgrootte_32

---

    Code
      filter(df_omgezet, grepl("^Groningen", gemeentenaam))
    Output
        gwb_code jaar aantal_inwoners aantal_65plus GemiddeldeHuishoudensgrootte_32
      1       14 2019          231299         33349                        1.700000
      2       14 2018          229963         32387                        1.666373
        berekend                             gemeentenaam   wijkcode
      1    FALSE Groningen                                GM0014    
      2     TRUE Groningen                                GM0014    

