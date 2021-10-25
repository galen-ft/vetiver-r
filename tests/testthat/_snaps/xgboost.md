# create plumber.R for xgboost

    Code
      cat(readr::read_lines(tmp), sep = "\n")
    Output
      # Generated by the vetiver package; edit with care
      
      library(pins)
      library(plumber)
      library(rapidoc)
      library(vetiver)
      
      # Packages needed to generate model predictions
      if (FALSE) {
          library(xgboost)
      }
      b <- board_folder(path = "/tmp/test")
      v <- vetiver_pin_read(b, "cars_xgb")
      
      #* @plumber
      function(pr) {
          pr %>% vetiver_pr_predict(v)
      }
