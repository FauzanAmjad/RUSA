library(readr)
RUSA_Recovery_Fund_Totals <- read_csv("Desktop/RUSA_Recovery_Fund_Totals.csv")


## Applied & Requested Food Money
hist(RUSA_Recovery_Fund_Totals$`Food Amount:`, col="darkmagenta", main = "Money Requested for Food By Applying Students", xlab = "Money Requested", ylab = "Frequency of Applying Students");
wantedFood <- subset(RUSA_Recovery_Fund_Totals, RUSA_Recovery_Fund_Totals$`Food Amount:` > 0)

## Applied & Requested Rent Money
hist(RUSA_Recovery_Fund_Totals$`Rent Amount:`, col = "darkgreen", main = "Money Requested for Rent By Applying Students",xlab = "Money Requested", ylab = "Frequency of Applying Students")
wantedRent <- subset(RUSA_Recovery_Fund_Totals, RUSA_Recovery_Fund_Totals$`Rent Amount:` > 0);

## Applied & Requested Money for Other
hist(RUSA_Recovery_Fund_Totals$`Other:`, col = "cyan", main = "Money Requested for Other By Applying Students",xlab = "Money Requested", ylab = "Frequency of Applying Students")
wantedOther <- subset(RUSA_Recovery_Fund_Totals, RUSA_Recovery_Fund_Totals$`Other:` > 0)

## Recommended & Requested Food Money
recStudents <- subset(RUSA_Recovery_Fund_Totals, RUSA_Recovery_Fund_Totals$`Recommend/Denied` == "Recommend")
hist(recStudents$`Food Amount:`, col="darkmagenta", main = "Money Requested for Food By Recommended Students", xlab = "Money Requested", ylab = "Frequency of Recommended Students");
wantedFood1 <- subset(recStudents, recStudents$`Food Amount:` > 0)

## Recommended & Requested Rent Money
hist(recStudents$`Rent Amount:`, col = "darkgreen", main =  "Money Requested for Rent By Recommended Students", xlab = "Money Requested", ylab = "Frequency of Recommended Students")
wantedRent1 <- subset(recStudents, recStudents$`Rent Amount:` > 0)

## Recommended & Requested Money for Other
hist(recStudents$`Other:`, col = "cyan", main = "Money Requested for Other By Recommended Students",xlab = "Money Requested", ylab = "Frequency of Applying Students")
wantedOther1 <- subset(recStudents, recStudents$`Other:` > 0)