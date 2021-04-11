---
description: 本主題說明如何在您的應用程式中 (IDNs) 來使用國際化功能變數名稱。
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: '處理國際化功能變數名稱 (IDNs) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193691"
---
# <a name="handling-internationalized-domain-names-idns"></a>處理國際化功能變數名稱 (IDNs) 

本主題說明如何在您的應用程式中 (IDNs) 來使用國際化功能變數名稱。 IDNs 是由網路工作群組 [RFC 3490 所指定：在應用程式中將功能變數名稱國際化 (IDNA) ](http://www.faqs.org/rfcs/rfc3490.html)。 在此草稿標準之前，IDNs 限制為不含變音符號的拉丁字元。 IDNA 可讓 IDNs 包含含有發音符號的拉丁字元，以及來自非拉丁腳本的字元，例如斯拉夫文、阿拉伯文和中文。 標準也會建立將 IDNs 對應至僅限 ASCII 功能變數名稱的規則。 因此，IDNA 問題可以在用戶端上處理，而不需要任何功能變數名稱伺服器 (DNS) 變更。

> [!Caution]  
> RFC 3490 引進了許多與使用 IDNs 相關的安全性問題。 如需詳細資訊，請參閱安全性考慮的相關章節 [：國際功能](security-considerations--international-features.md)。

 

> [!Note]  
> IDNA 目前是以 Unicode 3.2 為基礎。

 

## <a name="nls-api-functions-for-handling-idns"></a>處理 IDNs 的 NLS API 函式

NLS 包含下列轉換函式，可讓您的應用程式用來將 IDN 轉換成不同的標記法。 如需使用這些函數的範例，請參閱 [NLS：國際化功能變數名稱 (IDN) 轉換範例](nls--internationalized-domain-name--idn--conversion-sample.md)。

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii)。 將 IDN 轉換成 Punycode。
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode)。 執行將 IDN 轉換成 ASCII 名稱的 NamePrep 部分。 此函數會建立字串的標準 Unicode 標記法。
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode)。 將 Punycode 字串轉換為一般 UTF-16 字串。

NLS 也會定義數個 API 函式，可用來減輕一些 IDN 技術所呈現的安全性風險。 在 Windows Vista 和更新版本上，下列函式是用來驗證指定的 IDN 中的字元是否完全取自與特定地區設定或地區設定相關聯的腳本。 如需使用這些函數的範例，請參閱 [NLS：國際化功能變數名稱 (IDN) 緩和範例](nls--internationalized-domain-name--idn--mitigation-sample.md)。

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)。 提供特定字串中所使用的腳本清單。
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)、 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)。 取出地區設定資訊。 使用 *LCType* 設定為 [LOCALE \_ SSCRIPTS](locale-sscripts.md) 的函式，可提供一般用於特定地區設定的腳本清單。
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)。 比較腳本清單。 若要針對多個地區設定進行驗證，應用程式可以對 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) 或 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) 和 [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)進行多個呼叫。

針對在 Windows XP 與 Windows Server 2003 上執行的應用程式， [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)、 [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)和 [**DownlevelVerifyScripts**](downlevelverifyscripts.md) 等函式對上述的函式扮演類似的角色，以降低安全性風險。 [MSDN 下載中心](https://www.microsoft.com/?ref=go)提供「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載。

## <a name="handle-unicode-strings"></a>處理 Unicode 字串

IDNA 支援將 Unicode 字串轉換成合法的主機名稱標籤，但包含某些禁止字元的字串除外，例如控制字元、私用區域的字元 (PUA) 和 like。 您的應用程式可以使用 IDN \_ use \_ STD3 \_ ASCII 規則旗標搭配 \_ 數個 NLS 轉換函式，來強制函式在遇到字母、數位或連字號-減號 (-) 字元以外的 ascii 字元，或者字串開頭或結尾為連字號-減號字元時失敗。 這些字元一律禁止在功能變數名稱中使用，並在草稿標準中保持禁止。

## <a name="handle-unassigned-code-points"></a>處理未指派的程式碼點

IDNs 不能包含未指派的程式碼點。 因此，未與 Unicode 3.2 ( 「指派」 ) 字元相關聯的程式碼點也不會定義 IDN 對應，即使在某些轉換函式中，[IDN \_ 允許 \_ 未指派] 旗標可讓它們對應至 Punycode 也一樣。 您可以在 [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html)中尋找未指派的程式碼點清單。

> [!Caution]  
> 如果您的應用程式將未指派的程式碼點編碼為 Punycode，則產生的功能變數名稱應該是不合法的。 如果較新版本的 IDNA 讓這些名稱合法，或如果應用程式篩選掉不合法的字元來嘗試建立合法的功能變數名稱，安全性可能會受到危害。

 

通訊協定識別碼和命名實體中使用的預存字串中不允許未指派的程式碼點，例如數位憑證和 DNS 功能變數名稱部分中的名稱。 不過，查詢字串中允許使用程式碼點，例如，用來比對預存識別碼的使用者輸入的數位憑證授權單位單位和 DNS 查閱名稱。

> [!Caution]  
> 雖然查詢字串可以使用未指派的程式碼點，但您不應該在應用程式中使用它們。 即使是使用者提供的查詢字串，也會帶來「詐騙」攻擊的風險。 在這種類型的攻擊中，不道德的主機網站會將使用者從想要存取的網站，重設為另一個可能提供機密資訊給協力廠商的網站。 例如，從內送電子郵件複製字串，可能會出現與在瀏覽器中按一下連結相同的風險。

 

## <a name="convert-domain-names-to-ascii-names"></a>將功能變數名稱轉換成 ASCII 名稱

您的應用程式可以使用 [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) 函數和某些緩和函式，將 IDNs 轉換為 ASCII。

> [!Caution]  
> 因為具有非常不同之二進位表示的字串可以與相同的比較，所以此函式可能會引發特定的安全性考慮。 如需詳細資訊，請參閱安全性考慮中的比較函數討論 [：國際化功能](security-considerations--international-features.md)。

 

## <a name="examples"></a>範例

[NLS：國際化功能變數名稱 (idn) 轉換範例](nls--internationalized-domain-name--idn--conversion-sample.md) 示範如何使用 idn 轉換函數。 [NLS：國際化功能變數名稱 (IDN) 緩和範例](nls--internationalized-domain-name--idn--mitigation-sample.md) 示範如何使用 idn 緩和功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[安全性考慮：國際功能](security-considerations--international-features.md)
</dt> </dl>

 

 



