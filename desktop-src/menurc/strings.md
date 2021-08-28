---
title: 字串
description: 本節討論字串函數。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- 資源，字串
- 字串
- 字串函數 (string functions)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478894"
---
# <a name="strings"></a>字串

本節說明字串函式，並說明如何在您的應用程式中使用這些函數。

### <a name="in-this-section"></a>本節內容



| Name                                     | 描述                                             |
|------------------------------------------|---------------------------------------------------------|
| [關於字串](about-strings.md)       | 討論字串函數。<br/>              |
| [關於 >strsafe.h。h](strsafe-ovw.md)       | 討論 >strsafe.h 中的字串函數。<br/> |
| [字串參考](string-reference.md) | 包含 API 參考。<br/>                  |



 

### <a name="string-functions"></a>字串函式




| Name | 描述 | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> | 將字元字串或單一字元轉換成小寫。 如果運算元是字元字串，則函式會就地轉換字元。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a> | 將緩衝區中的大寫字元轉換成小寫字元。 函數會就地轉換字元。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a> | 抓取字串中下一個字元的指標。 此函數可以處理由單一或多位元組字元組成的字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a> | 抓取字串中下一個字元的指標。 此函數可以處理由單一或多位元組字元組成的字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a> | 抓取字串中上一個字元的指標。 此函數可以處理由單一或多位元組字元組成的字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a> | 抓取字串中上一個字元的指標。 此函數可以處理由單一或多位元組字元組成的字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> | 將字串轉譯成 OEM 定義的字元集。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a> | 將字串中指定的字元數轉譯成 OEM 定義的字元集。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a> | 將字元字串或單一字元轉換成大寫。 如果運算元是字元字串，則函式會就地轉換字元。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> | 將緩衝區中的小寫字元轉換成大寫字元。 函數會就地轉換字元。 <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | 使用指定的地區設定，比較兩個字元字串。<blockquote>[!Note]<br />若要與 Unicode 相容，請使用 <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> 或 unicode 版本的 <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>。</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> | 使用指定的地區設定，比較兩個 Unicode (寬字元) 字串。<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a> | 地圖一個字串轉換成另一個字串，執行指定的轉換選項。 <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> | 抓取指定之來源字串中字元的字元類型資訊。 針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。 每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> | 抓取指定之來源字串中字元的字元類型資訊。 針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。 每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。 <br /> 不同于其 close <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> 和 <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a>， <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> 會透過使用 <strong>#define 的 UNICODE</strong> 參數來展現標準行為。 這是建議的函式。<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a> | 抓取指定之來源字串中字元的字元類型資訊。 針對字串中的每個字元，函數會在輸出陣列的對應16位元素中設定一或多個位。 每個位都會識別指定的字元類型，例如字元是字母、數位，或兩者都不是。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a> | 判斷字元是否為字母字元。 這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> | 判斷字元是否為字母或數位字元。 這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a> | 判斷字元是否為小寫。 這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a> | 判斷字元是否為大寫。 這項決定是根據使用者在安裝期間或透過主控台所選取之語言的語法。 <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>Loadstring 時</strong></a> | 從與指定模組相關聯的可執行檔載入字串資源、將字串複製到緩衝區，並附加終止的 Null 字元。<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a> | 將一個字串附加至另一個字串。<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a> | 比較兩個字元字串。 比較會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a> | 比較兩個字元字串。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a> | 將字串複製到緩衝區。<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a> | 從來源字串將指定的字元數複製到緩衝區。 <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | 判斷指定之字串的長度 (不包括終止的 null 字元) 。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a> | 將 OEM 定義字元集中的字串轉譯為 ANSI 或寬字元字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a> | 將字串中指定的字元數從 OEM 定義的字元集轉譯為 ANSI 或寬字元字串。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a> | 將格式化資料寫入至指定的緩衝區。<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a> | 使用引數清單的指標，將格式化資料寫入指定的緩衝區。<br /> | 




 

### <a name="strsafe-functions"></a>>Strsafe.h 函式



| Name                                             | 描述                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | 將一個字串串連至另一個字串。<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | 將一個字串串連至另一個字串。<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | 將指定的位元組數從一個字串串連到另一個字串。<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | 將指定的位元組數從一個字串串連到另一個字串。<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | 將一個字串複製到另一個字串。<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | 將一個字串複製到另一個字串。<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | 將指定的位元組數目從某個字串複製到另一個字串。<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | 將指定的位元組數目從某個字串複製到另一個字串。<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | 從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | 從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | 判斷字串是否超過指定的長度（以位元組為單位）。<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | 將格式化資料寫入指定的字串。<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | 將格式化資料寫入指定的字串。<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | 使用引數清單的指標，將格式化資料寫入指定的字串。<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | 使用引數清單的指標，將格式化資料寫入指定的字串。<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | 將一個字串串連至另一個字串。<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | 將一個字串串連至另一個字串。<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | 將指定的字元數從一個字串串連到另一個字串。<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | 將指定的字元數從一個字串串連到另一個字串。<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | 將一個字串複製到另一個字串。<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | 將一個字串複製到另一個字串。<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | 將指定的字元數從某個字串複製到另一個字串。<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | 將指定的字元數從某個字串複製到另一個字串。<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | 從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | 從 stdin 取得一行文字，最多可包含分行符號 ( ' \\ n ' ) 。<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | 判斷字串是否超過指定的長度（以字元為單位）。<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | 將格式化資料寫入指定的字串。<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | 將格式化資料寫入指定的字串。<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | 使用引數清單的指標，將格式化資料寫入指定的字串。<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | 使用引數清單的指標，將格式化資料寫入指定的字串。<br/> |



 

 

