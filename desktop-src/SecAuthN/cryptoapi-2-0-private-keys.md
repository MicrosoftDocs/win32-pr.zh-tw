---
description: Schannel 認證會在內部表示為憑證 \_ 內容結構。
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 私密金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984556"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 私密金鑰

Schannel 認證會在內部表示為憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 結構。 Schannel 會使用[](/windows/desktop/SecGloss/p-gly)憑證的 CERT \_ key \_ >prov \_ INFO \_ \_ ID 屬性，找出與特定憑證內容相關聯的私密金鑰。 使用這個屬性，Schannel 會藉由呼叫 [**CryptAcquireCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta)函式來存取 *私密金鑰*。 如需其他詳細資訊，請參閱 [公開/私密金鑰](/windows/desktop/SecCrypto/public-private-key-pairs)組。

每個 Schannel 認證都包含一或多個私密金鑰的參考，每個私密金鑰都與特定憑證相關聯。 [*私密金鑰*](/windows/desktop/SecGloss/p-gly)的處理方式會有很大的不同，這取決於用戶端或伺服器的認證是否正確。

## <a name="client-private-keys"></a>用戶端私密金鑰

用戶端 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 是由 (CSP) 使用中的 [*密碼編譯服務提供者*](/windows/desktop/SecGloss/c-gly) 所管理。 用戶端私密金鑰通常會由 [>prov \_ rsa \_ FULL](/windows/desktop/SecCrypto/prov-rsa-full) 或 >prov rsa 簽章類型的 csp 儲存 \_ \_ 。

如果用戶端應用程式在呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)之前以手動方式進行 [**CryptAcquireCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta)呼叫，用戶端必須使用 CERT \_ KEY \_ >prov \_ 控制碼 \_ \_ 識別碼屬性，將 CSP 的控制碼系結至憑證內容。 如果 Schannel 發現此屬性集，則不會使用 CERT \_ KEY \_ >prov \_ INFO \_ \_ 屬性 ID 屬性。

## <a name="server-private-keys"></a>伺服器私密金鑰

伺服器私密金鑰是由下列其中一項 Csp 所儲存：

-   >PROV \_ RSA \_ SCHANNEL
-   >PROV \_ DH \_ SCHANNEL
-   >PROV \_ FORTEZZA CSP

CSP 的選擇取決於所選的 [*金鑰交換演算法*](/windows/desktop/SecGloss/k-gly)。 伺服器私用金鑰的類型必須是 \_ KEYEXCHANGE。

 

 
