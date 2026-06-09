# IMPB
Immune / Inflammatory, Metabolic / Cardiometabolic, Brain / Neurological / Neurodegenerative


ALz
gawk 'ARGIND==1 && FNR>1{k[$2":"$3]="NA"; next} ARGIND==2{if($1":"$2 in k) k[$1":"$2]=$3; next} ARGIND==3{if(FNR==1) print "RSID\t"$0; else print k[$2":"$3]"\t"$0}' ADGC_AFR_GRCh37.txt /scratch/negishi/hasan128/data/harmon_marry_data/dbsnp37_lookup_chr_header.tsv ADGC_AFR_GRCh37.txt > ADGC_AFR_GRCh37_with_RSID.txt
