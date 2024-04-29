# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Regularization paths for regression models with grouped covariates Use grpreg With (In) R Software
# Fit a group penalized regression path grpreg With (In) R Software
install.packages("readxl")
install.packages("httr")
install.packages("grpreg")
install.packages("ncvreg")
library("httr")
library("readxl")
library("grpreg")
library("ncvreg")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
github_link <- "https://github.com/timbulwidodostp/grpreg/raw/main/grpreg/grpreg.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, 
# authenticate using GITHUB_PAT
authenticate(Sys.getenv("GITHUB_PAT"), ""),
# write result to disk
write_disk(path = temp_file))
grpreg <- readxl::read_excel(temp_file)
# Estimate Regularization paths for regression models with grouped covariates Use grpreg With (In) R Software
X <- Prostate$X
y <- Prostate$y
fit <- grpreg(X, y)
select(fit, "BIC")
# Regularization paths for regression models with grouped covariates Use grpreg With (In) R Software
# Fit a group penalized regression path grpreg With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished