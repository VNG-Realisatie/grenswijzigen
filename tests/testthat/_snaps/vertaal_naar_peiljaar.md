# vertaal naar peiljaar

    Code
      filter(df, grepl("^289", as.character(gwb_code)))
    Output
      # A tibble: 14 x 4
         AantalInwoners_5 k_65JaarOfOuder_12  jaar gwb_code
                    <int>              <int> <dbl>    <dbl>
       1            33885               5125  2017    28900
       2             4570                800  2017    28901
       3             4725                440  2018    28901
       4             2480                  5  2018    28902
       5             2750                545  2018    28903
       6             2085                365  2018    28904
       7             3170                 35  2018    28905
       8             6890               1435  2018    28906
       9             5185                755  2018    28907
      10             2505                560  2018    28908
      11             3530                510  2018    28909
      12             2520                710  2018    28910
      13             1175                410  2018    28911
      14             1365                385  2018    28912

---

    Code
      filter(df_omgezet, grepl("^289", as.character(gwb_code)))
    Output
           AantalInwoners_5 k_65JaarOfOuder_12 jaar gwb_code berekend
      6210         3850.943           587.2929 2017    28901     TRUE
      635          1912.549           312.5852 2017    28902     TRUE
      6410         2703.195           408.8498 2017    28903     TRUE
      6510         1918.679           290.1941 2017    28904     TRUE
      6610         3611.462           579.2401 2017    28905     TRUE
      6710         8076.806          1221.5916 2017    28906     TRUE
      6810         5196.603           785.9699 2017    28907     TRUE
      6910         2969.560           450.0674 2017    28908     TRUE
      7010         3409.042           515.6069 2017    28909     TRUE
      7110         2679.029           405.2438 2017    28910     TRUE
      7210         1059.680           185.5020 2017    28911     TRUE
      7310         1067.452           182.8564 2017    28912     TRUE

