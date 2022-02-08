# week-1-a-barplot
Names <- c("pragna","swathi","lohitha","Nithya","bhuvana")
Rollno <- c("Y20CS093","Y20CS123","Y20CS095","Y20CS127","Y20CS130")
Gender <- c("Female","Female","Female","Female","Female")
Marks <-c(2,4,6,8,10)
Fee <-c(69400,57892,58903,69400,67390)
Section <-c("C","C","C","B","B")

rvrstudents <-data.frame(Names,Rollno,Gender,Marks,Fee,Section)
rvrstudents
write.csv(rvrstudents,"Rvr_Students.csv",row.names=F)

a <- read.csv("Rvr_Students.csv")
barplot(rvrstudents$Marks,
        xlab="Students names",
        ylab="marks",
        main="RVRJCCE",
        xlim=c(1,10),
        ylim=c(1,10),
        col=c("Lavender","Pink","Green","Yellow","Black")
        names.arg=rvrstudents$Names,
        las=2)
