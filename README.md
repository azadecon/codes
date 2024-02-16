# codes
frequent codes to use till I learn to write them self
---
## rmdf

```{r}
library(tidyverse)
library(readxl)
library(data.table)

file.path <- "./file_folder/combined//"
file.list <- list.files(path = file.path, pattern = "*.xlsx", full.names = T)
df.list <- lapply(file.list, read_xlsx)

present_15_30 <- rbindlist(df.list, idcol = "id", fill = F)


writexl::write_xlsx(present_15_30, "./ram_mandir/combined//present_15_30.xlsx")
```
