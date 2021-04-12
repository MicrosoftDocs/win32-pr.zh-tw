---
description: 不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者分開 (Ksp) 。
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: CNG 金鑰儲存提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386096"
---
# <a name="cng-key-storage-providers"></a>CNG 金鑰儲存提供者

不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者分開 (Ksp) 。 Ksp 可以用來建立、刪除、匯出、匯入、開啟和儲存金鑰。 根據執行的不同，它們也可以用於非對稱式加密、秘密合約和簽署。 從 Windows Vista 和 Windows Server 2008 開始，Microsoft 會安裝下列 Ksp。 廠商可以建立和安裝其他提供者。

## <a name="microsoft-software-key-storage-provider"></a>Microsoft 軟體金鑰儲存提供者

支援軟體金鑰建立和儲存，以及下列演算法。



| 演算法                                          | 目的                           | 金鑰長度 (bits)                  |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                 | 秘密合約和金鑰交換 | 512至4096以64位遞增  |
|  (DSA) 的數位簽章演算法                  | 簽章                        | 512至1024以64位遞增  |
|  (ECDH) 的橢圓曲線 Diffie-Hellman               | 秘密合約和金鑰交換 | P256、P384、P521                  |
|  (ECDSA) 的橢圓曲線數位簽章演算法 | 簽章                        | P256、P384、P521                  |
| RSA                                                | 非對稱式加密和簽署 | 512至16384以64位遞增 |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Microsoft 智慧卡金鑰儲存提供者

支援智慧卡金鑰建立和儲存，以及下列演算法。



| 演算法                                          | 目的                           | 金鑰長度 (bits)                  |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                 | 秘密合約和金鑰交換 | 512至4096以64位遞增  |
|  (ECDH) 的橢圓曲線 Diffie-Hellman               | 秘密合約和金鑰交換 | P256、P384、P521                  |
|  (ECDSA) 的橢圓曲線數位簽章演算法 | 簽章                        | P256、P384、P521                  |
| RSA                                                | 非對稱式加密和簽署 | 512至16384以64位遞增 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CNG 演算法識別碼**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[CNG 金鑰儲存功能](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[瞭解密碼編譯提供者](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
