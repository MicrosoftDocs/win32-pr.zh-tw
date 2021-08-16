---
description: 某些應用程式（例如 microsoft Active Directory、microsoft Exchange 和 microsoft Access）會維護依 (名稱編制索引的地區設定和語言字串的可排序資料庫) 以及其相關聯的排序加權。
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: 處理應用程式中的排序
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 73c7ca897cb5f83e5a073205341f8b0d0f96ff2d0a9d4c7144a914cd5c96c44d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822688"
---
# <a name="handling-sorting-in-your-applications"></a>處理應用程式中的排序

某些應用程式（例如 microsoft Active Directory、microsoft Exchange 和 microsoft Access）會維護依 (名稱編制索引的地區設定和語言字串的可排序資料庫) 以及其相關聯的排序加權。

[排序](sorting.md) 對於自己的地區設定中的使用者來說通常是直覺的。 但是，應用程式開發人員可能不太直覺化。 本主題討論在應用程式中處理排序的考慮。 排序可以是語言或序數 (非語言) 。

## <a name="sorting-functions"></a>排序函數

您可以在應用程式中使用各種排序功能：

-   NLS 字串比較函數。 範例包括 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 和 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)、 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)、 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)、 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)、 [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)和 [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal)。 請參閱 [安全性考慮：](security-considerations--international-features.md) 與字串比較函式相關之安全性問題討論的國際功能。
-   在內部呼叫字串比較函數的包裝函式。 最常見的函式為 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) 和 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)，其會呼叫 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)。

排序函式通常會依字元評估字串字元。 不過，許多語言都有多個字元的元素，例如傳統西班牙文中的兩個字元組 "CH"。 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 和 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) 會使用應用程式提供的地區設定識別碼或名稱來識別多字元元素。 相反地， [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)和 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 會使用使用者的地區設定。

另一個範例是越南文，其中包含多個兩個字元的元素，例如有效的大寫字母、標題案例和小寫形式的 "GI" （分別為 "GI、" Gi "和" gi "）。 其中任何一種形式都會視為單一排序專案，而且如果忽略大小寫，則會比較為相等。 不過，由於 "gI" 不是有效的單一元素，因此 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)和 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 會將 "gi" 視為兩個不同的元素。

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)、 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)、 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)、 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)、 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)和 [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)等函數全都預設為使用「文字排序」技術。 對於這種類型的排序，除了連字號和單引號以外的所有標點符號和其他非英數位元，都在任何英數位元之前。 連字號和單引號的處理方式與其他非英數位元不同，以確保文字（例如「共同作業」和「共同作業」）在已排序的清單中保持在一起。

應用程式可以藉由指定 SORT STRINGSORT 旗標，從排序函數要求「字串排序」技術，而不是文字排序 \_ 。 字串排序會將連字號和單引號視為與任何其他非英數位元一樣。 它們在排序次序中的位置是在英數位元之前。

下表比較文字排序的結果與字串排序的結果。 

| 文字排序 | 字串排序 |
|-----------|-------------|
| 坯    | 帳單      |
| 條例 草案     | 坯      |
| 帳單    | 條例 草案       |
| 無法    | 不能       |
| 不能      | 無法      |
| 不能     | 不能        |
| con       | 共同作業       |
| 庫 珀      | con         |
| 共同作業     | 庫 珀        |



 

## <a name="sort-strings-linguistically"></a>以語言排序字串

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)和 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)函數會針對語言相等進行測試。 您的應用程式應該使用這些函式搭配正確的地區設定，以進行語言排序字串。

> [!Note]  
> 為了與 Unicode 相容，應用程式應該偏好 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) 或 unicode 版本的 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)。 偏好 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) 的另一個原因是，因為互通性的緣故，Microsoft 正針對新地區設定使用地區設定名稱，而非地區設定識別碼。 只有在 Windows Vista 和更新版本上執行的任何應用程式，都應該使用 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)。

 

測試語言是否相等的另一種方式是使用 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) 或 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)，一律使用文字排序。 [**Lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)函式會使用標準 IGNORECASE 旗標來呼叫 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) \_ ，而 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)則會在沒有該旗標的情況下呼叫。 如需使用包裝函式的總覽，請參閱 [**字串**](../menurc/strings.md)。

這些函式會針對所有地區設定取得語言適當的結果。 不同地區設定的使用者期望在排序行為上可能會有顯著的差異，如下列範例所示。

-   許多地區設定會將 ae 連字號 (æ) 與字母 ae 相同。 不過，冰島文 (冰島) 將它視為個別的字母，並將它放在排序次序中的 Z 之後。
-   Å) 的環形 (通常只會針對與之間的變音符號的差異進行排序。不過，瑞典文 (瑞典) 會在排序次序中的 Z 之後放置環形。

函式會嘗試嚴格驗證 Unicode 標準中定義的程式碼點是否標準方式等於相等的程式碼點字串。 例如，代表小寫 "u" 的程式碼點， (ü) ，其標準方式等於小寫 "u"，並結合了分字元 (▆) 。 不過請注意，這種標準的等價不一定可行。

幾乎所有使用 Windows 鍵盤和輸入方法編輯器輸入的資料都 (ime) 符合 Unicode 標準中所定義的 C 格式，使用 NLS unicode 正規化函式從其他平臺轉換傳入資料會提供最一致的結果，特別是針對使用藏文腳本的地區設定或新式韓文的韓文腳本。 如需 Windows Vista 和更新版本中的 unicode 正規化支援的詳細資訊，請參閱[使用 unicode 正規化來代表字串](using-unicode-normalization-to-represent-strings.md)。

當字串比較遵循使用者的語言喜好設定時，例如，當排序的 ListView 控制項的專案排序時，應用程式可以執行下列其中一項動作：

-   以使用者的地區設定呼叫 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) 或 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 。
-   呼叫 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 或 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) 來定義比較的地區設定、傳遞額外的旗標、內嵌 null 字元，或傳遞明確長度以符合字串的部分。

不論地區設定的比較結果應該一致，例如，在比較抓取的資料與預先定義的清單或內部值時，應用程式應該使用 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 或 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ，並將 *locale* 參數設定為地區設定不 \_ 變。 若為 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)，即使 mystr 為 "INLAP"，下列任一呼叫都將會相符。 在此情況下，如果目前的地區設定是越南文，則區分地區設定的 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 呼叫會失敗。

在 Windows XP 上：


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



在舊版作業系統上：


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>排序字串序數

針對序數 (非語言) 排序，您的應用程式應該一律使用 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) 函數。

> [!Note]  
> 這項功能僅適用于 Windows Vista 和更新版本。

 

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) 會比較兩個 [Unicode](unicode.md) 字串來測試二進位相等，而不是語言相等。 這類非語言字串的範例包括 NTFS 檔案名、環境變數，以及 mutex、具名管道或 mailslots 的名稱。 除了不區分大小寫的選項之外，此函式會忽略所有非二進位 equivalences。 不同于其他某些排序函式，它會測試所有的程式碼點是否相等，包括未在語言排序配置中提供任何權數的程式碼點。

下列所有語句都適用于二進位比較中的 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) ，但不適用於 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)或 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)。

-   標準方式 Unicode 中的對等序列（例如，在上述 (U +) 00e5 的拉丁小寫字母 A）和上面 (U + 0061 U + 030a) 的拉丁小寫字母 A + 組合環形之間，不相等，即使它們顯示的 ( "å" ) 相同也一樣。
-   以 Unicode 標準方式類似的字串，例如拉丁字母 SMALL 大寫字母 Y (U + 028f) 和拉丁大寫字母 Y (U + 0059) ，看起來非常類似 ( "ʏ" 和 "Y" ) 而且只有在語言資料表中有一些特殊的案例權數，才會被視為完全不同的字元。 即使應用程式將 *bIgnoreCase* 設為 **TRUE**，這些字串仍會比較不同。
-   已定義但沒有語言排序權數的程式碼點（例如零寬度的連接子 (U + 200d) ）會被視為具有其程式碼點加權。
-   在較新版本的 Unicode 中定義的程式碼片段，但目前的語言資料表中沒有權數，會被視為具有其程式碼點加權。
-   Unicode 未定義的程式碼點會被視為具有其程式碼點加權。
-   當應用程式將 *bIgnoreCase* 設為 **TRUE** 時，函式會使用作業系統 uppercasing 資料表來對應案例，而不是語言排序表中的資訊。 因此，對應與地區設定無關。

如需以 Unicode 標準方式對等序列以及 Unicode 中標準方式類似字串的詳細資訊，請參閱 [使用 unicode 正規化來代表字串](using-unicode-normalization-to-represent-strings.md)。

## <a name="sort-code-points"></a>排序程式代碼點

某些 Unicode 程式碼點沒有權數，例如零寬度的非加入點、U + 200c。 排序函式會刻意將不加權的程式碼點評估為相等，因為它們沒有任何權數可進行排序。 在 Windows Vista 和更新版本中，應用程式可以藉由呼叫 NLS 字串比較函式（特別是 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)），以評估常值中的所有程式碼點（例如，在密碼驗證中），來排序這些程式碼點。 在預先 Windows 的 Vista 作業系統上，應用程式應該使用 C 執行時間函數 **strcmp** 或 **wcscmp**。

當應用程式指定 hlink NONSPACE 旗標時，排序函式會忽略變音符號，例如非間距的短音符號、U + 0306 \_ 。 同樣地，當指定 hlink 符號旗標時，這些函式會忽略符號，例如等號、U + 003d \_ 。 在 Windows Vista 和更新版本中，應用程式會呼叫 [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)來評估常值（二進位）中的變音符號和符號代碼點。 在預先 Windows 的 Vista 作業系統上，應用程式應該使用 **strcmp** 或 **wcscmp**。

某些程式碼點（例如0xFFFF 和0x058b）目前不會以 Unicode 指派。 這些程式碼點不會在排序中收到任何權數，而且永遠不會傳遞至排序函數。 應用程式應該使用 [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) 來偵測資料流程中的非 Unicode 程式碼點。

> [!Note]  
> [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring)的結果可能會根據在較新版本中將字元加入至 unicode 時傳遞的 unicode 版本而有所不同，之後再加入 Windows 排序表中。 如需詳細資訊，請參閱 [使用排序版本](#use-sort-versioning)設定。

 

## <a name="sort-digits-as-numbers"></a>以數位排序數位

在 Windows 7 和更新版本中，應用程式可以使用 SORT DIGITSASNUMBERS 旗標來呼叫 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)或 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) \_ 。 此旗標支援將數位視為數位的排序，例如，"2" 之前的排序 "10"。

請注意，使用此旗標不適用於下列的十六進位數位。 <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

在此情況下，「數位」會依序排序，但使用者會感覺出不正確的十六進位清單。

## <a name="map-strings"></a>對應字串

如果未指定 LCMAP 的 SORTKEY，則應用程式會使用 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 或 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) 函數來對應字串 \_ 。 如果來源字串以 null 結束，則對應的字串會以 null 終止。

在大寫和小寫之間轉換時，此函式不保證單一字元將對應至單一字元。 例如，LCMAP \_ 小寫和 LCMAP \_ 大寫字母旗標可能會將德文 ( "ß" ) 對應至本身。 或者，LCMAP \_ 大寫旗標可能會將 "ß" 對應至 "ss"，而 LCMAP \_ 小寫旗標可能會將 "ss" 對應至 "ß"。 此行為取決於 NLS 版本。

在大寫和小寫之間轉換時，此函式對內容並不敏感。 例如，雖然 LCMAP \_ 大寫旗標正確地將希臘文小寫的 sigma ( "σ" ) 和希臘文小寫的最終 sigma ( "σ" ) 到希臘文大寫 sigma ( "σ" ) ，LCMAP \_ 小寫旗標一律會將 "σ" 對應至 "σ"，絕不會將 "σ" 對應至 ""。

根據預設，函式會將小寫 "i" 對應至大寫 "I"，即使 *Locale* 參數指定土耳其文或亞塞拜然。 若要覆寫土耳其文或亞塞拜然的這種行為，應用程式應指定 LCMAP \_ 語言 \_ 大小寫。 如果使用適當的地區設定來指定此旗標，則 "ı" (小寫的非點按 I) 是小寫形式的 "I" (大寫的非點按 I) 和 "i" (小寫的點) 是小寫形式的 "i" (大寫的點) 。

如果指定 LCMAP \_ 平假名旗標以將片假名字元對應到平假名字元，而且 \_ 未指定 LCMAP 全形字元，則 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 或 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) 只會將全形字元對應至平假名。 在此情況下，任何半形片假名字元都會放在目的字串中，且不會對應至平假名。 應用程式必須指定 LCMAP \_ 全半形，將半形片假名字元對應至平假名。 這項限制的原因是所有平假名字元都是全形字元。

如果應用程式需要從來源字串中去除字元，則可以使用標準 \_ IGNORESYMBOLS 和標準 IGNORENONSPACE 旗標集合來呼叫對應函式 \_ ，並清除所有其他旗標。 如果應用程式使用不是以 null 結束的來源字串來執行這項工作，則函式可能會傳回空字串，而不會傳回錯誤。

## <a name="create-sort-keys"></a>建立排序關鍵字

當應用程式指定 LCMAP \_ 排序程式時， [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 或 [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) 會產生排序索引鍵，也就是位元組值的二進位陣列。 排序索引鍵不是真正的字串，其值代表來源字串的排序行為，但不是有意義的顯示值。

> [!Note]  
> 函數會在產生排序索引鍵期間忽略阿拉伯文 kashida。 如果應用程式呼叫函式來建立包含阿拉伯文 kashida 之字串的排序關鍵字，此函數不會建立排序索引鍵值。

 

排序索引鍵可以包含奇數位節數目。 LCMAP \_ BYTEREV 旗標只會反轉偶數的位元組數目。 排序索引鍵中的最後一個位元組 (奇數位置) 不會反轉。 如果終止的0x00 位元組是奇數位置的位元組，它會保留在排序索引鍵中的最後一個位元組。 如果終止的0x00 位元組是一個偶數位置的位元組，它會與之前的位元組交換位置。

產生排序索引鍵時，函式會以不同于其他標點符號的方式來處理連字號和單引號，如此一來，「共同作業」和「共同作業」這類單字會在清單中保持在一起。 在英數位元之前的連字號和單引號字元以外的所有標點符號符號。 應用程式可以藉由設定 SORT STRINGSORT 旗標來變更此行為 \_ ，如 [排序函數](#sorting-functions)中所述。

在 [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp)中使用時，排序索引鍵會產生與在 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 或 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)中使用來源字串時相同的順序。 應該使用 [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) 函式，而不是 [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)，因為排序索引鍵可以有內嵌的 null 位元組。

## <a name="use-sort-versioning"></a>使用排序版本設定

[排序](sorting.md)資料表有兩個識別其版本的數位：已定義的版本和 NLS 版本。 這兩個數字都是 DWORD 值，由主要值和次要值組成。 值的第一個位元組是保留的，接下來的兩個位元組代表主要版本，而最後一個位元組代表次要版本。 以十六進位詞彙來說，此模式為0xRRMMMMmm，其中 R 等於 Reserved、M 等於主要，而 m 等於次要。 例如，次要版本為4的主要版本3會以0x304 表示。

定義的版本會識別程式碼點的所有產品，而且所有地區設定都相同。 主要版本會遞增以表示現有程式碼點的變更。 次要版本會遞增，以表示已加入程式碼點，但先前尚未變更任何現有的程式碼點。

NLS 版本是 [地區設定識別碼](locale-identifiers.md) 或 [地區設定名稱](locale-names.md)的特定版本，並且會追蹤受影響地區設定的程式碼點加權變更。 當已針對已排序的程式碼點變更加權時，主要版本會遞增。 當新的程式碼點指派權數時，次要版本會遞增，但所有其他先前可排序的程式碼點加權都會保持不變。

> [!Note]  
> 針對主要版本，會變更一或多個程式碼點，讓應用程式必須重新為所有資料重新建立索引，以便讓比較有效。 如果是次要版本，則不會移動任何專案，但會新增程式碼點。 針對此類型的版本，應用程式只需要使用先前不可排序的值來重新編制字串的索引。

 

> [!IMPORTANT]
> Windows 8 中的主要版本已變更。 在舊版 Windows 下建立的資料必須重新建立索引。

 

已定義和 NLS 版本都適用于使用 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) 或 [**LCMAPSTRINGEX**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) 函數搭配 LCMAP 分類旗標所抓取的可排序程式代碼點 \_ ，而且 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)、 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)和 [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) 函式也會使用此旗標。 如果字串中的一個或多個程式碼點是不可排序，則當該字串以參數形式傳遞給它時， [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) 函數會傳回 **FALSE** 。

應用程式可以呼叫 [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) 或 [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) ，以取得排序資料表的已定義版本和 NLS 版本。

## <a name="index-the-database"></a>為資料庫編制索引

基於效能考慮，當編制資料庫的索引時，應用程式應該遵循此程式。

**適當地為資料庫編制索引**

1.  針對每個函式，儲存 NLS 版本、該版本的排序索引鍵，以及每個索引字串的 sortability 指示。
2.  當次要版本遞增時，會重新編制先前不可排序字串的索引。 此更新中受影響的字串應該限制為先前已傳回 **FALSE** 的 [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) 。
3.  當主要版本遞增時，會重新建立所有字串的索引，因為更新的加權可能會變更任何字串的行為。 主要版本版本非常罕見。

資料庫索引問題可能會因下列原因而發生：

-   較新的作業系統可以定義針對舊版作業系統未定義的程式碼點，進而變更排序。
-   由於語言支援中的修正，程式碼點在不同的作業系統中可能會有不同的排序加權。

為了盡可能減少在這些情況下重新編制資料庫索引的需要，應用程式可以使用 [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) 來區別定義自訂的字串，讓應用程式可以使用未定義的程式碼點來拒絕字串。 使用 [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) 或 [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) ，可讓應用程式判斷 NLS 變更是否會影響特定索引資料表所使用的地區設定。 如果變更對地區設定沒有任何影響，則應用程式不需要重新建立資料表的索引。

## <a name="examples"></a>範例

下表說明某些旗標搭配排序函數使用的效果。 在每個案例中，旗標的選取範圍會決定兩個不同的字元是否視為相等，以供排序之用。



| 字元1                                                        | 字元2                                             | 預設 | 標準 \_ IGNOREWIDTH | 標準 \_ IGNOREKANA | 標準 \_ IGNOREWIDTH \| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> U + 3042 平假名字母 A<br/>                | "ガ"<br/> U + 30A2 片假名字母 A<br/>     | 不等 | 不等           | 等於            | 等於                              |
| "ｵ"<br/> U + FF75 半形片假名字母 O<br/>       | "オ"<br/> U + 30AA 片假名字母 O<br/>     | 不等 | 等於             | 不等          | 等於                              |
| B<br/> U + FF22 全形拉丁大寫字母 B<br/> | "B"<br/> U + 0042 拉丁大寫字母 B<br/> | 不等 | 等於             | 不等          | 等於                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[排序](sorting.md)
</dt> <dt>

[正在抓取和設定地區設定資訊](retrieving-and-setting-locale-information.md)
</dt> <dt>

[使用 Unicode 正規化來代表字串](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[安全性考慮：國際功能](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
