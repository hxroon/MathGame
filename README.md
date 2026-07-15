
=SUMPRODUCT((TEXT(Table13[BUSINESS_DATE],"dd-mmm-yy")=TEXT($C10,"dd-mmm-yy"))*(TRIM(Table13[BUSINESS])=TRIM($C$2))*(TRIM(Table13[L7_SUB_BUSINESS])=TRIM($C$3))*(TRIM(Table13[PLSHEET_NAME])=TRIM($B10))*ISNUMBER(SEARCH("Estimate",Table13[ActEstState]))*IFERROR(Table13[Sum of Estimate],0))
