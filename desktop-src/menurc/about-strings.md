---
title: 關於字串
description: 本主題討論字串函數。
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- 資源，字串
- 字串
- 字串函數 (string functions)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966851"
---
# <a name="about-strings"></a>關於字串

字串函式提供應用程式複製、比較、排序、格式化和轉換字元字串的方法，以及用來判斷字串中每個字元之字元類型的方法。 如果執行應用程式的作業系統支援這些字元集，則所有字串函數都支援單位元組、雙位元組和 Unicode 字元集。

**安全性警告：** 不當使用字串函式可能會導致您的應用程式發生安全性問題。 這通常牽涉到緩衝區溢位，這可能會對您的應用程式造成阻絕服務攻擊，或從攻擊者插入可執行程式碼。 >strsafe.h 函式可讓您更安全地處理字串，建議您為應用程式提供更好的安全性。 如需這些函式的詳細資訊，請參閱 [使用 >strsafe.h .H 函數](strsafe-ovw.md)。

本節將討論下列主題。

-   [與 C Run-Time 字串函數的比較](#comparison-with-c-run-time-string-functions)
-   [字串資源](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>與 C Run-Time 字串函數的比較

許多字串函式會從標準 C 執行時間 (CRT) 程式庫複製或增強熟悉的字串函式。 許多增強功能可讓字串函數使用 Unicode 或擴充字元集。 下表顯示 CRT 函式、支援 Unicode 的 Windows 函式 (，與 CRT 函數) 和 >strsafe.h 函式不同。



| CRT 字串函數                                       | Windows String 函數    | >strsafe.h 函式                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | 沒有對等的函式 ()                                                                                                                                                                                                                                                                                                                                                                                   |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

例如， **strlen** 函式一律會傳回字串中的位元組數目，但 [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) 函數會傳回 **TCHAR** 值的數目，這是指 ANSI 版本的函數或 Unicode 版本的 **WCHAR** 值的位元組數。

下列字串函數與標準 C 函式（例如 **tolower** 和 **toupper** ）不同，因為它們會在字元集中的任何字元上運作。 例如，藉由使用 [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera) 函式，應用程式可以將大寫 U 轉換成變音符 (Ü) 為小寫 (Ü) 。 如需字元集的詳細資訊，請參閱 [單一位元組字元集](/windows/desktop/Intl/single-byte-character-sets)。



| 函式                               | 描述                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | 將字元或字串轉換為小寫。  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | 將字元字串轉換成小寫。     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | 移至字串中的下一個字元。      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | 移至字串中的前一個字元。 |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | 將字元或字串轉換為大寫。  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | 將字串轉換為大寫。               |



 

下列字串函式會根據使用者所選取之語言的語義來決定字元。 這些函式是 Unicode 啟用的功能。



| 函式                                         | 描述                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | 判斷字元是否為字母。   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | 判斷字元是否為英數位元。 |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | 判斷字元是否為小寫。    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | 判斷字元是否為大寫。    |



 

下表顯示 standard C 執行時間 (CRT) 函數的 Unicode 擴充功能。 如先前所述，>strsafe.h 函式可讓您更安全地處理字串，因此建議您為應用程式提供更好的安全性。



| 標準 CRT 函數                                       | String 函數                | >strsafe.h 函式                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>字串資源

在資源中維護字元字串的應用程式可以最少的努力轉譯成新的語言。 您可以直接轉譯資源檔中的字串並重新連結應用程式，而不是搜尋來源模組中的字串。 此外，使用字串資源可簡化從相同原始程式檔建立 Unicode 和非 Unicode 版應用程式的程式。

[**Loadstring 時**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)函式會從應用程式的可執行檔載入字串資源。 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)函式會載入字串資源，並解釋可能內嵌在字串中的格式化選項。

二進位格式的資源會以 Unicode 格式儲存。 載入資源時，應用程式可以使用 Unicode 版本的資源函式 ([**LoadStringW**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)，例如) ，以 unicode 資料的形式取得資源。

16位字串資源的長度上限為255個字元。 若為32位字串資源，65535個字元是最大長度。

 

 