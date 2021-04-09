---
description: 提供者會執行密碼編譯演算法、產生金鑰、提供金鑰儲存，以及驗證使用者。 提供者可在硬體、軟體或兩者中執行。
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: 瞭解密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944806"
---
# <a name="understanding-cryptographic-providers"></a>瞭解密碼編譯提供者

在密碼編譯 API 中引進的密碼編譯提供者概念 ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) ，而且在 [*密碼編譯 api：新一代*](/windows/desktop/SecGloss/c-gly) (CNG) 是在 Microsoft 作業系統上安全地執行密碼編譯功能的核心。 這兩個 Sdk 用來建立許多應用程式，並由其他 Sdk 在內部呼叫。 例如，Active Directory 憑證服務和憑證註冊 API 依賴 CryptoAPI 和 CNG。

一般而言，提供者會執行密碼編譯演算法、產生金鑰、提供金鑰儲存，以及驗證使用者。 提供者可在硬體、軟體或兩者中執行。 使用 CryptoAPI 或 CNG 所建立的應用程式無法改變提供者所建立的金鑰，也無法改變密碼編譯演算法的執行。 Microsoft 所建立的多個提供者會與作業系統一起散發。 其他提供者已由協力廠商建立和散發。

下列主題強調與 CryptoAPI 相關聯的提供者之間的差異，以及與 CNG 相關聯的提供者。 一般而言，本檔會參考提供者，而不需要參考與其相關聯的 SDK，請注意關聯性。

-   [CryptoAPI 密碼編譯服務提供者](cryptoapi-cryptographic-service-providers.md)
-   [CNG 密碼編譯演算法提供者](cng-cryptographic-algorithm-providers.md)
-   [CNG 金鑰儲存提供者](cng-key-storage-providers.md)
-   [列舉已安裝的提供者](enumerating-installed-providers.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用憑證註冊 API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
