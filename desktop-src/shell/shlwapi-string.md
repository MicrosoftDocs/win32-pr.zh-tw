---
description: 本節說明 Windows Shell 字串處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。
title: Shell 字串處理函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d11ad956b6eab11212243232dfaf8ef341d05544
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473314"
---
# <a name="shell-string-handling-functions"></a>Shell 字串處理函式

本節說明 Windows Shell 字串處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br /> | 在兩個字元之間執行比較。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br /> | 在指定語言喜好設定時，捕獲與網站搭配使用的字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br /> | 針對兩個當地語系化字串開頭的指定字元數，執行區分大小寫的比較。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br /> | 從兩個當地語系化字串的開頭，執行指定字元數的不區分大小寫比較。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br /> | 比較兩個當地語系化字串開頭的指定字元數。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br /> | 判斷字元是否代表空格。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br /> | 當指定的文字資源以間接字串的形式提供，而該資源的 (開頭為 ' @ ' 符號的字串) 時，會將指定的文字資源解壓縮。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br /> | 在新配置的記憶體中建立字串的複本。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br /> | 將一個字串附加至另一個字串。 <br /><blockquote>[!Note]<br />請勿使用。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br /> | 將字元從某個字串複製並附加至另一個字串的結尾。 <br /><blockquote>[!Note]<br />請勿使用。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br /> | 串連兩個 Unicode 字串。 當需要重複串連至相同緩衝區時使用。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br /> | 搜尋字串中第一次出現符合指定字元的字元。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br /> | 搜尋字串中第一次出現符合指定字元的字元。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br /> | 搜尋字串中第一次出現的指定字元。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br /> | 搜尋字串中第一次出現的指定字元。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br /> | 比較兩個字串，以判斷它們是否相同。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br /> | 使用 C 執行時間 (ASCII) 定序規則來比較字串。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br /> | 比較兩個字串，以判斷它們是否相同。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br /> | 使用 C 執行時間 (ASCII) 定序規則比較兩個字串。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br /> | 比較兩個 Unicode 字串。 字串中的數位會被視為數位內容，而不是文字。 這項測試不區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br /> | 比較兩個字串開頭的指定字元數，以判斷它們是否相同。 比較會區分大小寫。 <strong>StrNCmp</strong>宏的名稱只與此函數不同。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br /> | 使用 C 執行時間 (ASCII) 定序規則，比較兩個字串開頭的指定字元數。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br /> | 比較兩個字串開頭的指定字元數，以判斷它們是否相同。 這項比較不會區分大小寫。 <strong>StrNCmpI</strong>宏的名稱只與此函數不同。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br /> | 使用 C 執行時間 (ASCII) 定序規則，比較兩個字串開頭的指定字元數。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br /> | 將一個字串複製到另一個字串。 <br /><blockquote>[!Note]<br />請勿使用。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br /> | 將指定的字元數從一個字串的開頭複製到另一個字串。<br /><blockquote>[!Note]<br />請勿使用此函數或 <strong>StrNCpy</strong> 宏。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br /> | 搜尋字串中是否有任何一組字元的第一次出現。 搜尋方法會區分大小寫，且終止的 <strong>Null</strong> 字元會包含在搜尋模式比對中。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br /> | 搜尋字串中是否有任何一組字元的第一次出現。 搜尋方法不區分大小寫，且終止的 <strong>Null</strong> 字元會包含在搜尋模式比對中。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br /> | 複製字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br /> | 根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br /> | 根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。 與一個參數類型中的 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> 不同。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br /> | 根據大小，將數值轉換為表示位元組、kb、mb 或 gb 數位的字串。 藉由提供選項以四捨五入至最接近的顯示數位，或捨棄 undisplayed 數位，來擴充 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> 。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br /> | 根據大小，將數值轉換為表示以位元組為單位的大小值（以位元組為單位，kb、mb 或 gb）表示的數位值。 與一個參數類型中的 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> 不同。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br /> | 將數值轉換成字串，表示以 kb 為單位的大小值（以 kb 為單位）。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br /> | 將時間間隔（以毫秒為單位）轉換成字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br /> | 比較兩個字串開頭的指定字元數，以判斷它們是否相等。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br /> | 將一個字串開頭的指定字元數附加至另一個字串的結尾。 <br /><blockquote>[!Note]<br />請勿使用此函數或 <strong>StrCatN</strong> 宏。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br /> | 在字串中搜尋指定緩衝區所包含的第一次出現的字元。 此搜尋不包含終止的 null 字元。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br /> | 在字串中搜尋指定字元的最後一個出現位置。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br /> | 在字串中搜尋指定字元的最後一個出現位置。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br /> | 接受包含或指向字串之<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>所傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，並以<a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>形式傳回該字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br /> | 將<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構轉換成字串，並將結果放在緩衝區中。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br /> | 採用<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，並將指標傳回至包含顯示名稱的配置字串。<br /> | 
| <a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br /> | 採用<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder：： GetDisplayNameOf</strong></a>傳回的<a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a>結構，將它轉換成字串，並將結果放在緩衝區中。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br /> | 搜尋字串中所指定子字串的最後一個出現專案。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br /> | 取得字串內子字串的長度，該字串包含指定緩衝區中包含的所有字元。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br /> | 在字串中尋找第一個出現的子字串。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br /> | 在字串中尋找第一個出現的子字串。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br /> | 將表示十進位值的字串轉換成整數。 <strong>StrToLong</strong>宏與此函數相同。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br /> | 將表示十進位或十六進位值的字串轉換成64位整數。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br /> | 將表示十進位或十六進位數位的字串轉換成整數。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br /> | 從字串中移除指定的開頭和結尾字元。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br /> | 接受可變長度的引數清單，並傳回引數的值做為 <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>樣式的格式化字串。 <br /><blockquote>[!Note]<br />請勿使用此函數。 請參閱備註以取得替代功能。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br /> | 接受引數清單，並傳回引數的值做為 <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>樣式的格式化字串。 <br /><blockquote>[!Note]<br />請勿使用此函數。 請參閱備註以取得替代功能。</blockquote><br /> | 




 

 

 
