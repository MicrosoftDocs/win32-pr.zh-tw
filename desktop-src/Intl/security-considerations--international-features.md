---
description: 本主題提供與國際支援功能相關之安全性考慮的相關資訊。
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 安全性考慮：國際功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e61566fdf51b80a76e5c8997018f35ce421dee6dd0e1b9e290888d96576249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147041"
---
# <a name="security-considerations-international-features"></a>安全性考慮：國際功能

本主題提供與國際支援功能相關之安全性考慮的相關資訊。 您可以使用它做為起點，然後針對特定技術的安全性考慮，查看相關國際技術的檔。

本主題包含下列各節。

-   [字元轉換函式的安全性考慮](#security-considerations-for-character-conversion-functions)
-   [比較函數的安全性考慮](#security-considerations-for-comparison-functions)
-   [檔案名中字元集的安全性考慮](#security-considerations-for-character-sets-in-file-names)
-   [國際化功能變數名稱的安全性考慮](#security-considerations-for-internationalized-domain-names)
-   [ANSI 函數的安全性考慮](#security-considerations-for-ansi-functions)
-   [Unicode 正規化的安全性考慮](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>字元轉換函式的安全性考慮

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 是 Unicode 和字元集函數，最常用來轉換 ANSI 和 Unicode 之間的字元。 這些函式有可能會造成安全性風險，因為它們會以不同的方式計算輸入和輸出緩衝區的元素數目。 例如， [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 會採用以位元組計算的輸入緩衝區，並將轉換後的字元放入以 Unicode 字元調整大小的緩衝區。 當您的應用程式使用這個函式時，必須正確地調整緩衝區大小，以避免緩衝區溢位。

針對字碼頁， [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)預設為「最適合」的對應，例如1252。 不過，這種類型的對應允許相同字串的多個表示，可能會讓您的應用程式容易受到攻擊。 例如，以分音符號 ( "Ä" 的拉丁文大寫字母 A ) 可能會對應到拉丁大寫字母 A ( "A" ) ;亞洲語言的 Unicode 字元可能會對應到斜線 ( "/" ) 。 \_從安全性的觀點來看，最好不要使用 WC 的 \_ 最 \_ 適合 \_ 字元旗標。

某些字碼頁（例如，5022x (iso-2022-x) 字碼頁）本質上是不安全的，因為它們允許相同字串的多個標記法。 正確撰寫的程式碼會以 Unicode 格式執行安全性檢查，但是這些類型的字碼頁會擴充您應用程式的攻擊風險，應該盡可能避免。

## <a name="security-considerations-for-comparison-functions"></a>比較函數的安全性考慮

字串比較可能存在安全性問題。 因為所有的比較函數都稍微不同，所以一個函式可能會將兩個字串回報為相等，而另一個函式可能會將它們視為相異。 以下是您的應用程式可以用來比較字串的數個函數：

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia)。 根據地區設定的規則（不區分大小寫）比較兩個字元字串。 此函式會比較字串，方法是檢查第一個字元彼此、第二個字元互相對應，依此類推，直到找到不相等或到達字串的結尾為止。
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)。 使用與 [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia)類似的技術來比較字串。 唯一的差別在於 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) 會執行區分大小寫的字串比較。
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)、 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista 和更新版本) 。 在應用程式提供的地區設定上執行字串比較。 [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) 與 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)類似，但它會依 [地區設定名稱](locale-names.md) （而非 [地區設定識別碼](locale-identifiers.md)）來識別地區設定。 這些函式類似于 [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 和 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ，不同之處在于它們會在特定地區設定上運作，而不是在使用者選取的地區設定上運作。
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista 和更新版本的) 。 比較兩個 Unicode 字串來測試二進位相等。 除了不區分大小寫的選項之外，此函式會忽略所有非二進位 equivalences，並測試所有的程式碼點是否相等，包括未在語言 [排序](sorting.md) 配置中提供任何權數的程式碼點。 請注意，本主題中提及的其他比較函數不會測試所有程式碼點是否相等。
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)、 [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista 和更新版本) 。 在另一個 Unicode 字串中找出 Unicode 字串。 [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) 與 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)類似，不同之處在于它會依地區設定名稱（而非地區設定識別碼）識別地區設定。
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 和更新版本) 。 在另一個 Unicode 字串中尋找一個 Unicode 字串。 應用程式應該使用此函式，而不是 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) 進行所有的非語言比較。

如同 [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 和 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)， [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 會依字元評估字串字元。 不過，許多語言都有多個字元的元素，例如傳統西班牙文中的兩個字元元素 "CH"。 由於 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 會使用應用程式所提供的地區設定來識別多個字元的元素，而 [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) 和 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) 會使用執行緒地區設定，因此相同的字串可能不會比較相等。

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 會忽略未定義的字元，因此會傳回零 (，表示對許多非常相異的字串組) 的相等字串。 字串可能包含未對應到任何字元的值，或者可能包含在應用程式網域以外的字元（例如 URL 中的控制字元）。 使用此函式的應用程式應該提供錯誤處理常式和測試字串，以確保它們在使用之前都是有效的。

> [!Note]  
> 針對 Windows Vista 和更新版本， [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)類似于 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)。 這些功能的安全性問題都相同。

 

類似的安全性問題適用于進行隱含比較的函數（例如 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)）。 視所設定的旗標而定，呼叫 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) 以搜尋另一個字串中某個字串的結果可能會有很大的差異。

> [!Note]  
> 針對 Windows Vista 和更新版本， [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)類似于 [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)。 這些功能的安全性問題都相同。

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>檔案名中字元集的安全性考慮

日文語言系統上使用的 Windows 字碼頁和 OEM 字元集包含日元符號 (¥) ，而不是反斜線 (\\) 。 因此，不允許使用日元字元作為 NTFS 和 FAT 檔案系統。 當將 Unicode 對應至日文語言字碼頁時，轉換函式會將反斜線 (U + 005C) 和一般 Unicode 日元符號 (U + 00A5) 轉換成這個相同的字元。 基於安全性理由，您的應用程式通常不應該在可能轉換的 Unicode 字串中允許字元 U + 00A5，以做為 FAT 的檔案名。

## <a name="security-considerations-for-internationalized-domain-names"></a>國際化功能變數名稱的安全性考慮

 (IDNs) 的國際化功能變數名稱是由網路工作群組 [RFC 3490：在應用程式中將功能變數名稱國際化 (IDNA) ](http://www.faqs.org/rfcs/rfc3490.html)。 標準引進了許多安全性問題。

代表不同腳本某些字元的字元可能會類似或甚至相同。 例如，在許多字型中，斯拉夫小寫 A ( "a" ) 與拉丁小寫 A ( "a" ) 不區分。 無法以視覺化的方式告訴 "example.com" 和 "example.com" 兩個不同的功能變數名稱，一個名稱中有一個拉丁文小寫 A，另一個則具有斯拉夫小寫 A。不道德的主機網站可使用此視覺效果，偽裝為詐騙攻擊中的另一個網站。

IDNA 允許 IDNs 的擴充字元集在特定腳本內也有詐騙潛力。 例如，連字號之間有強式非常相似-減號 ( "-" U + 002D) ，連字號 ( "—" U + 2010) 、非斷字元 ( "-" U + 2011) 、"\u2012" U + 2012 (、en 虛線) "–" U + 2013 ( 和減號) "−" U + 2212 (。

某些相容性組合會產生類似的問題。 例如，單一 Unicode 字元號碼二十 FULL STOP ( "20."、U + 249B) 轉換為 "20"。 在轉換成 Punycode 之前， (U + 0032 U + 0030 U + 002E) 于 NamePrep 步驟中。 換句話說，此組合會將句點插入句號 (full stop) 。 這類組合具有詐騙潛力。

在 IDN 中混合不同的腳本並不一定表示詐騙或欺騙意圖。 [技術報表 \# 36： Unicode 安全性考慮](https://www.unicode.org/reports/tr36/#international_domain_names) 提供數個合理 IDNs 的範例，其中包含混合的腳本，例如 XML-Документы .Com ( "Документы" 是 [檔] ) 的俄文。

詐騙攻擊不限於 IDNs。 例如，"rnicrosoft.com" 看起來很像「microsoft.com」，但它是 ASCII 名稱。 此外，可能會因為名稱損毀而發出詐騙攻擊。 在已知的品牌名稱之後新增額外的標籤，或在標示為安全的 URL 路徑中包含品牌名稱，可能會混淆新手使用者，不論是否使用 IDN。 在某些地區設定中，IDNs 是必要的，而且這些名稱的 Punycode 格式無法接受，因為它會讓名稱看起來像是很雜亂的名稱。

如需有關此處所述安全性問題的詳細資訊，以及與 IDNA 相關的許多其他問題，請參閱 [技術報表 \# 36： Unicode 安全性考慮](https://www.unicode.org/reports/tr36/#international_domain_names)。 除了詳細討論與 IDNA 相關的安全性問題之外，這份報告還提供在應用程式中處理可疑 IDNs 的建議。

## <a name="security-considerations-for-ansi-functions"></a>ANSI 函數的安全性考慮

> [!Note]  
> 建議您在全球化應用程式中使用 Unicode，尤其是新的應用程式（如果有的話）。 如果您有覆寫不使用 Unicode 的原因（例如，符合不支援 Unicode 的舊版通訊協定），則應該使用 ANSI 函數。

 

 (NLS) 函式（例如 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 和 [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)）的許多國家語言支援都有特定的 ANSI 版本，在此情況下，會分別為 **GetLocaleInfoA** 和 **GetCalendarInfoA**。 當您的應用程式使用 ANSI 版本的函式搭配 Unicode 作業系統（例如 Windows NT、Windows 2000、Windows XP 或 Windows Vista）時，此函式可能會失敗或產生未定義的結果。 如果您有充分的理由要搭配使用 ANSI 函數與這類作業系統，請確定您的應用程式所傳遞的資料對 ANSI 而言是有效的。

## <a name="security-considerations-for-unicode-normalization"></a>Unicode 正規化的安全性考慮

由於 Unicode 正規化可能會變更字串的形式，因此安全性機制或字元驗證演算法通常應該在正規化之後執行。 例如，假設應用程式具有接受檔案名的 Web 介面，但不接受路徑名稱。 全形 U + FF43 U + FF1A U + FF3C U + FF57 U + FF49 U + FF4E U + FF44 U + FF4F U + FF57 U + FF53 `(c : \ w i n d o w s)` 變更為 U + 0063 u + 001A u + 003C u + 0077 u + 0069 u + 006E u + 0064 u + 006F u + 0077 u + 0073 `(c:\windows)` WITH form KC 正規化。 如果應用程式在執行正規化之前測試是否存在冒號和反斜線字元，則結果可能是不小心的檔案存取。

雖然 Unicode 正規化是讓作業系統安全的元素，但請記住，正規化不是完整安全性原則的取代專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案名中使用的字元集](character-sets-used-in-file-names.md)
</dt> <dt>

[函數原型的慣例](conventions-for-function-prototypes.md)
</dt> <dt>

[處理應用程式中的排序](handling-sorting-in-your-applications.md)
</dt> <dt>

[處理國際化功能變數名稱 (IDNs) ](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
