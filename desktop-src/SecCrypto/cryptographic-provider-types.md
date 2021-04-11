---
description: 密碼編譯的領域很大且不斷增加。
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: 密碼編譯提供者類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e976909cec25b5194187d61d2e753eeb830c09f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690135"
---
# <a name="cryptographic-provider-types"></a>密碼編譯提供者類型

[*密碼*](../secgloss/c-gly.md)編譯的領域很大且不斷增加。 有許多不同的標準資料格式和通訊協定。 這些通常會組織成群組或系列，其中每個群組都有自己的一組資料格式以及進行作業的方式。 即使兩個系列使用相同的演算法 (例如， [*RC2*](../secgloss/r-gly.md) [*區塊加密*](../secgloss/b-gly.md)) ，它們通常會使用不同的 [*填補*](../secgloss/p-gly.md) 配置、不同的 [*金鑰長度*](../secgloss/k-gly.md)和不同的預設模式。 CryptoAPI 的設計目的是讓 CSP 提供者類型代表特定的系列。

當應用程式連接到特定類型的 CSP 時，每個 CryptoAPI 函式預設會以對應至該 CSP 類型的系列所規定的方式運作。 應用程式的提供者類型選擇會指定下列專案：



| 項目                                                                                                                                | 描述                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*金鑰交換演算法*](../secgloss/k-gly.md)                | 每個提供者類型只會指定一個金鑰交換演算法。 特定類型的每個 CSP 都必須執行此演算法。 應用程式會藉由選取適當提供者類型的 CSP，來指定要使用的金鑰交換演算法。                                                        |
| [*數位簽章演算法*](../secgloss/d-gly.md) | 每個提供者類型只會指定一個數位簽章演算法。 特定類型的每個 CSP 都必須執行此演算法。 應用程式會藉由選取適當提供者類型的 CSP，來指定要使用的數位簽章演算法。                                              |
| 金鑰 BLOB 格式                                                                                                                    | 提供類型可決定用來從 [*csp*](../secgloss/c-gly.md)匯出金鑰，以及將金鑰匯入 csp 的 [*金鑰 BLOB*](../secgloss/k-gly.md)格式。 |
| 數位簽章格式                                                                                                            | 提供者類型決定數位簽章格式。 這可確保由相同提供者類型的 csp 所產生的簽章可由相同提供者類型的任何 CSP 進行驗證。                                                                                                              |
| 工作階段金鑰衍生配置                                                                                                       | 提供者類型會決定用來從 [*雜湊*](../secgloss/h-gly.md)衍生 [*工作階段金鑰*](../secgloss/s-gly.md)的方法。                                                                                   |
| [*金鑰長度*](../secgloss/k-gly.md)                                                    | 某些提供者類型會指定 [*公開/私密金鑰*](../secgloss/p-gly.md) 組的長度和工作階段金鑰。                                                                                                               |
| 預設模式                                                                                                                       | 提供者類型通常會指定各種選項的預設模式，例如封鎖加密加密 [*模式*](../secgloss/c-gly.md) 或封鎖加密 [*填補*](../secgloss/p-gly.md) 方法。          |



 

某些先進的應用程式一次可能會連線到多個 CSP，但大部分的應用程式通常只會使用一個 CSP。

目前有許多預先定義的提供者類型。 下一節提供下列提供者類型的相關資訊：

-   [>PROV \_ RSA \_ FULL](prov-rsa-full.md)
-   [>PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [>PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [>PROV \_ RSA \_ SCHANNEL](prov-rsa-schannel.md)
-   [>PROV \_ DSS](prov-dss.md)
-   [>PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [>PROV \_ DH \_ SCHANNEL](prov-dh-schannel.md)
-   [>PROV \_ FORTEZZA](prov-fortezza.md)
-   [>PROV \_ MS \_ EXCHANGE](prov-ms-exchange.md)
-   [>PROV \_ SSL](prov-ssl.md)

雖然有些 CSP 型別可能會與其他 CSP 類型部分相容，但需要 [*交換金鑰*](../secgloss/e-gly.md) 和加密訊息的兩個或多個應用程式應該使用相同類型的 csp。

自訂的 CSP 寫入器可以定義新的提供者類型。 不過，CSP 寫入器接著會負責將新的提供者類型散發給任何使用它的應用程式的作者。 如需撰寫自訂 Csp 的詳細資訊，請參閱 [密碼編譯服務提供者](cryptographic-service-providers.md)。

 

 
