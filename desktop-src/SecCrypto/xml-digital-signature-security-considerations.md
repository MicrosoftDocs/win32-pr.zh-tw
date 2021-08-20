---
description: 簽署和驗證 XML 數位簽章的應用程式應該根據下列最佳作法來撰寫，以避免阻斷服務攻擊、資料遺失，以及洩漏私用資訊。
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: XML 數位簽章安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4c66304d454d97a5583aab8458d98fd2a38208ff7b302a9139747787d10eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970442"
---
# <a name="xml-digital-signature-security-considerations"></a>XML 數位簽章安全性考慮

簽署和驗證 XML 數位簽章的應用程式應該根據下列最佳作法來撰寫，以避免阻斷服務攻擊、資料遺失，以及洩漏私用資訊。 下列清單提供一般指引;不過，我們鼓勵開發人員針對其應用程式執行額外的安全性分析，並查看 W3C 所發行的最新數位簽章最佳作法。

-   [確認簽署金鑰的信任](#verify-trust-of-the-signing-key)
-   [先確認簽署金鑰並驗證 SignedInfo，然後驗證參考](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [使用所需的一組最基本的標準化演算法和轉換](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [確定目標 Uri 指向預期範圍內的目的地](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [確認應用程式所使用的資料是由簽章驗證](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [遵循最佳的密碼編譯作法](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>確認簽署金鑰的信任

確認簽署金鑰是受信任的，方法是確認已簽署的訊息中包含對應的 [*x.509*](../secgloss/x-gly.md) 憑證 (和憑證鏈) 。 或者，您可以用頻外方式建立簽署金鑰的信任，例如系統管理員設定一組受信任的金鑰，或透過安全通道查詢受信任服務的應用程式。

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>先確認簽署金鑰並驗證 SignedInfo，然後驗證參考

驗證參考之前，請先確認簽署金鑰和 **SignedInfo** 元素完整性的信任。 同樣地，應用程式應該先驗證 **資訊清單** 專案，再解析 **資訊清單** 專案中包含的參考。 **Reference** 元素允許指定目標 uri、轉換和標準化演算法。 如果未經過驗證，這些欄位可能會用來建立拒絕服務、資料遺失或其他攻擊。

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>使用所需的一組最基本的標準化演算法和轉換

XSLT 和 XPATH 不應使用於未驗證的元素中，例如 **KeyInfo**。 如果應用程式需要使用 XPath，請將一組 XPATH 運算式限制為只允許使用上階或本身軸的運算式，而且不會計算元素的字串值。 根據預設，CryptXML 支援一組有限的標準化演算法 (查看 [XML 數位簽章密碼編譯演算法](xml-digital-signature-cryptographic-algorithms.md) 中支援的 uri) 。 開發人員可以在其應用程式中執行其他轉換或正常化演算法來使用。 不過，使用複雜的演算法可能會導致阻絕服務攻擊或破壞簽章的否認性特性。 在應用程式需要轉換的情況下，將每個參考可指定的轉換數目限制為應用程式所需的最高數目。 這種作法會根據過度使用的轉換，減少阻斷服務的攻擊。

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>確定目標 Uri 指向預期範圍內的目的地

應用程式應該將目標 Uri 限制為應用程式所需的最小範圍。 例如，Uri 可能預期會指向相同檔中的目的地、特定目標目錄中的檔案，或特定 DNS 網域內的網路位置。 攻擊者設定為指向預期網域以外的 Uri 可能會導致應用程式取出惡意內容、傳送惡意 HTTP 要求 (可能包含查詢字串) ，或導致應用程式向惡意伺服器驗證。

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>確認應用程式所使用的資料是由簽章驗證

如果應用程式驗證簽署金鑰和 **SignedInfo** 和 **參考** 元素，但應用程式取用簽章未參考的重要資料，則簽章不會提供有意義的保護。 簽章的語義意義可能會根據簽章在檔內的位置而有所不同。 建議應用程式檢查檔中簽章的位置。 此外，請檢查參考資料和專案名稱的位置，以減少替代和包裝攻擊。

## <a name="follow-best-cryptographic-practices"></a>遵循最佳的密碼編譯作法

當發現新的攻擊，且有更多運算能力可供使用時，密碼編譯演算法會變得較弱。 請勿將密碼編譯演算法識別碼或金鑰大小硬的編碼到您的應用程式中。 如需最佳密碼編譯作法的完整清單，請參閱 Michael Howard 和 Steve Lipner *《安全性開發生命 (週期* 中的《 SDL 基本密碼編譯標準》（美國華盛頓州的《 Microsoft，2006) ，251–258》）。

其他最佳作法可在 W3C 網站上找到： https://www.w3.org 。

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
