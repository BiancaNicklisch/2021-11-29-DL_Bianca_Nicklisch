# Aufgabe 4 Shell: Shell-Script
# Bianca Nicklisch 

sed -Ee 's/[ ]//g' 2021-11-29-Article_list_dirty.tsv > Ohne7-10.tsv

sed '15,18d' Ohne_7-10.tsv > Ohn_15-18.tsv

sed '67,69d'  Ohn_15-18.tsv > Oh_67-69.tsv

sed -Ee 's/[ISSN:]//g' Oh_67-69.tsv > Oh_ISSN.tsv

sed -Ee 's/[ssn]//g' Oh_ISSN.tsv > Oh_ssn.tsv

sed -Ee 's/[i]//g' Oh_ssn.tsv > Oh_i.tsv

sed '24,31d' Oh_i.tsv > Oh_24-31.tsv

cut -f 5,12 Oh_24-31.tsv > Oh_spalte.tsv

sed '1d' Oh_spalte.tsv > Oh_1.tsv

sort Oh_1.tsv  > Oh_sorti.tsv

uniq Oh_sorti.tsv > 2021-11-29-Dates_ISSNs.tv

