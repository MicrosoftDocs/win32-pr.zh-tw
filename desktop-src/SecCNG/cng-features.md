---
description: CNG 具有下列功能。
ms.assetid: 400a2b6e-6bbe-4ba4-abde-a2f625007517
title: CNG 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df40606a255adc90bd36540571979c1c34579611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991683"
---
# <a name="cng-features"></a>CNG 功能

CNG 具有下列功能。

-   [密碼編譯靈活性](#cryptographic-agility)
-   [認證與合規性](#certification-and-compliance)
-   [Suite B 支援](#suite-b-support)
-   [舊版支援](#legacy-support)
-   [核心模式支援](#kernel-mode-support)
-   [稽核](#auditing)
-   [可替換的亂數產生器](#replaceable-random-number-generators)
-   [執行緒安全性](#thread-safety)
-   [作業模式](#mode-of-operation)

## <a name="cryptographic-agility"></a>密碼編譯靈活性

CNG 的其中一個重要價值主張是密碼編譯的靈活性，有時也稱為密碼編譯 agnosticism。 不過，將通訊協定（例如 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 或 [*傳輸層安全性*](/windows/desktop/SecGloss/t-gly) (TLS) 、CMS (S/MIME) 、IPsec、Kerberos 等等）轉換成相當重要。 在 CNG 層級上，必須提供所有演算法類型的替代和可探索性 (對稱、非對稱、雜湊函式) 、亂數產生和其他公用程式函數。 通訊協定層級的變更更為重要，因為在許多情況下，通訊協定 Api 需要新增演算法選取專案和其他先前未存在的彈性選項。

CNG 是在 Windows Vista 中首次推出，其定位於取代整個 Microsoft 軟體堆疊中的 [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 現有用途。 協力廠商開發人員會發現 CNG 有許多新功能，包括：

-   新的加密設定系統，支援更佳的密碼編譯靈活性。
-   金鑰儲存體 (更精細的抽象概念，以及將儲存體與演算法作業) 分開。
-   使用長期金鑰進行作業的進程隔離。
-   可替換的亂數產生器。
-   從出口簽署限制中降低。
-   整個堆疊的安全線程。
-   核心模式密碼編譯 API。

此外，CNG 還支援所有必要的 Suite B 演算法，包括 (ECC) 的 [*橢圓曲線密碼*](/windows/desktop/SecGloss/e-gly) 編譯。 現有的 CryptoAPI 應用程式將會繼續運作，因為 CNG 變成可用。

## <a name="certification-and-compliance"></a>認證與合規性

CNG 會驗證為聯邦資訊處理標準 (FIPS) 140-2，而且是 Windows 通用準則認證的評估目標的一部分。 CNG 的設計目的是要當做 FIPS 層級2驗證系統中的元件使用。

CNG 符合一般條件需求，方法是在安全的進程中儲存和使用長時間的金鑰。

## <a name="suite-b-support"></a>Suite B 支援

CNG 的一項重要功能，就是支援 Suite B 演算法。 在2005年2月，美國政府機關 (NSA) 宣佈一組對稱式加密、非對稱式加密合約 (也稱為金鑰交換) 、數位簽章和雜湊函式，供未來的美國政府使用，稱為 *Suite B*。NSA 宣佈已通過認證的 Suite B 實施，並且將用來保護指定為最常機密、秘密和私用資訊的資訊，而這些資訊在過去已描述為敏感性但不機密。 因此，對應用程式軟體廠商和系統整合者以及 Microsoft 而言，Suite B 的支援非常重要。

所有 Suite B 的演算法都是公開已知的。 這些都是在過去與密碼編譯演算法開發相關聯的政府機密範圍之外進行開發。 在這個相同的時間範圍內，某些歐洲國家和地區也提議相同的 Suite B 需求來保護其資訊。

Suite B 密碼編譯建議在許多現有的通訊協定中使用橢圓曲線 Diffie-Hellman (ECDH) ，例如網際網路金鑰交換 (IKE，主要用於 IPsec) 、 [*傳輸層安全性*](/windows/desktop/SecGloss/t-gly) (TLS) ，以及安全 Mime (S/mime) 。

CNG 支援擴充至所有必要演算法的 Suite B： AES (所有金鑰大小) 、SHA-1 系列 (256 SHA-1、sha-1、sha-384 和 SHA-512) （雜湊演算法、ECDH 和橢圓曲線 DSA） (在 NIST 標準的質數曲線 P-256、P-384 和 P-521。 Windows Vista 隨附的 Microsoft 演算法提供者不支援二進位曲線、Koblitz 曲線、自訂質數曲線，以及橢圓曲線 Menezes-Qu-Vanstone (ECMQV) 。

## <a name="legacy-support"></a>舊版支援

CNG 可支援 [*CryptoAPI*](/windows/desktop/SecGloss/c-gly) 1.0 中目前的演算法組。 *在 CNG 1.0 中* 目前支援的每個演算法都會繼續受到 CNG 的支援。

## <a name="kernel-mode-support"></a>核心模式支援

CNG 在核心模式中支援密碼編譯。 核心和使用者模式都使用相同的 Api，以完整支援密碼編譯功能。 除了將使用 CNG 的開機程式之外，SSL/TLS 和 IPsec 都可在核心模式中運作。 並非所有的 CNG 函數都可以從核心模式中呼叫。 無法從核心模式呼叫之函式的參考主題將明確指出無法從核心模式呼叫該函式。 否則，如果呼叫端是以 **被動 \_ 層級** 的 [*IRQL*](/windows/desktop/SecGloss/i-gly)執行，則可以從核心模式呼叫所有的 CNG 函數。 此外，根據提供者的功能而定，某些核心模式的 CNG 函式可能可在 **分派 \_ 層級的 IRQL** 上呼叫。

Microsoft 核心安全性支援提供者介面 (Ksecdd.sys) 是一般用途、軟體型的密碼編譯模組，位於 Windows 的核心模式層級。 Ksecdd.sys 會以核心模式匯出驅動程式的形式執行，並透過其記載的介面，提供密碼編譯服務給核心元件。 Ksecdd.sys 不支援的內建 Microsoft 提供者演算法是 DSA。

**Windows Server 2008 和 Windows Vista：** CNG 不支援在核心模式中插入的演算法和提供者。 核心模式中唯一支援的密碼編譯演算法，是由 Microsoft 透過核心模式 CNG Api 提供的實作為。

## <a name="auditing"></a>稽核

為了符合一些通用準則需求，除了提供完整的安全性之外，在 Microsoft 軟體金鑰儲存提供者 (KSP) 中會審核 CNG 層中的許多動作。 Microsoft KSP 遵循下列指導方針，在安全性記錄中建立審核記錄：

-   金鑰和金鑰組產生失敗（包括自我測試失敗）必須經過審核。
-   必須先審核金鑰匯入和匯出。
-   必須審核金鑰損毀失敗。
-   持續性金鑰必須在寫入和讀取檔案時進行審核。
-   必須對成對的一致性檢查失敗進行審核。
-   秘密金鑰驗證失敗（如果有的話）必須經過審核，例如，3DES 金鑰的同位檢查。
-   必須審核加密、解密、雜湊、簽章、驗證、金鑰交換和亂數產生的失敗。
-   必須先審核密碼編譯自我測試。

一般而言，如果金鑰沒有名稱，則是暫時金鑰。 暫時金鑰不會保存，而且 Microsoft KSP 不會產生暫時金鑰的審核記錄。 Microsoft KSP 只會在 LSA 進程的使用者模式中產生審核記錄。 核心模式 CNG 不會產生任何審核記錄。 系統管理員必須設定稽核原則，才能從安全性記錄檔取得所有的 KSP 審核記錄。 系統管理員必須執行下列命令列來設定 Ksp 所產生的其他審核：

**auditpol/set/subcategory：「其他系統事件」/success： enable/failure： enable**

## <a name="replaceable-random-number-generators"></a>可替換的亂數產生器

CNG 提供的另一項改進，是取代預設亂數產生器 (RNG) 的能力。 在 CryptoAPI 中，可以提供替代的 RNG 做為加密服務提供者 (CSP) 的一部分，但是無法將 Microsoft 基礎 Csp 重新導向為使用其他 RNG。 CNG 可以明確指定特定的 RNG，以便在特定的呼叫中使用。

## <a name="thread-safety"></a>執行緒安全性

當從不同的執行緒呼叫時，任何同時修改相同記憶體區域 (重要) 區段的函式，都不是安全線程。

## <a name="mode-of-operation"></a>作業模式

CNG 支援五種作業模式，可透過加密 Api 與對稱式封鎖密碼搭配使用。 下表列出這些模式和其支援能力。 您可以使用 [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty)函數來設定演算法提供者的 [**BCRYPT \_ 連結 \_ 模式**](cng-property-identifiers.md)屬性，藉以變更作業模式。



| 作業模式           | BCRYPT \_ 連結 \_ 模式值 | 演算法              | 標準  |
|-----------------------------|------------------------------|-------------------------|-----------|
| ECB (電子 Codebook)    | **BCRYPT \_ 鏈 \_ 模式 \_ ECB** | 對稱式區塊密碼 | SP800-38A |
| CBC (加密區塊鏈)  | **BCRYPT \_ 鏈 \_ 模式 \_ CBC** | 對稱式區塊密碼 | SP800-38A |
| CFB (加密的意見反應)        | **BCRYPT \_ 鏈 \_ 模式 \_ CFB** | 對稱式區塊密碼 | SP800-38A |
| 具有 CBC) 的 CCM (計數器      | **BCRYPT \_ 鏈 \_ 模式 \_ CCM** | AES                     | SP800-38C |
| GCM (Galois/計數器模式)    | **BCRYPT \_ 鏈 \_ 模式 \_ GCM** | AES                     | SP800-38D |



 

> [!Note]  
> Windows Vista 中只會定義作業的 ECB、CBC 和 CFB 模式。 GCM 和 CCM 需要 Windows Vista （含 Service Pack 1） (SP1) 或 Windows Server 2008。

 

 

 
