# devanagari-transliterate
Node Package to transliterate between देवनागरी (devanāgarī) and Latin script based on IAST, Harvard-Kyoto, SLP-1 &amp; ISO-15919 Standards

```
const sanskrittransliterate = require("devanagari-transliterate");

console.log('SLP >> देवनागरी : ',sanskrittransliterate("SLP","latin2devanagari","saMskfta", false));  // Expected SLP >> देवनागरी : संस्कृत
console.log('SLP >> देवनागरी : ',sanskrittransliterate("SLP","latin2devanagari","manu1\\^ maˆjnâ ja\\h na/m vâhthāˆ ma\\nu prasthaH jaV maZ", false)); // Expected SLP >> देवनागरी : मनु१॒॑  म॑ज्न॑  ज॒ह्  न꣫म्  व॑ह्था॑  म॒नु  प्रस्थः  जᳶ  मᳵ
console.log('SLP >> ISO : ', sanskrittransliterate("SLP","latin2devanagari","saMskfta", true)); // Expected SLP >> ISO :  saṁskr̥ta
console.log('SLP >> ISO : ',sanskrittransliterate("SLP","latin2devanagari","manu1\\^ maˆjnâ ja\\h na/m vâhthāˆ ma\\nu prasthaH jaV maZ", true)); // Expected SLP >> ISO : manu1̱̍ ma̍jna̍ ja̱h na꣫m va̍hthā̍ ma̱nu prasthaḥ jaᳶ maᳵ

console.log('H-K >> देवनागरी : ',sanskrittransliterate("HK","latin2devanagari","saMskRta", false)); // Expected H-K >> देवनागरी : संस्कृत
console.log('H-K >> देवनागरी : ',sanskrittransliterate("HK","latin2devanagari","anuklRp klRRmanyaplRRn", false)); // Expected H-K >> देवनागरी : अनुकॢप् अनुकलृप्  कॣमंयपॣन् कलॄमंयपलॄन्
console.log('H-K >> ISO : ',sanskrittransliterate("HK","latin2devanagari","saMskRta", true)); // Expected H-K >> ISO :  saṁskr̥ta
console.log('H-K >> ISO : ',sanskrittransliterate("HK","latin2devanagari","anuklRp klRRmanyaplRRn", true)); // Expected H-K >> ISO : anukl̥p kl̥̄manyapl̥̄n

console.log('IAST >> देवनागरी : ',sanskrittransliterate("IAST","latin2devanagari","saṃskṛta", false));  // Expected IAST >> देवनागरी : संस्कृत
console.log('IAST >> ISO : ',sanskrittransliterate("IAST","latin2devanagari","saṃskṛta", true)); // Expected IAST >> ISO :  saṁskr̥ta

console.log('ISO >> देवनागरी : ',sanskrittransliterate("ISO","latin2devanagari","samskr̥ta", false));  // Expected ISO >> देवनागरी : संस्कृत
console.log('देवनागरी >> ISO : ',sanskrittransliterate("ISO","latin2devanagari","maˆjnâ jàh nám vâhthāˆ ma̲nu", false)); // Expected देवनागरी >> म॑ज्न॑  ज॒ह्  न꣫म्  व॑ह्था॑  म॒नु

console.log('देवनागरी >> ISO : ',sanskrittransliterate("ISO","devanagari2latin","संस्कृता", false)); // Expected देवनागरी >> ISO with strict nasalisation :  samskr̥tā

```
