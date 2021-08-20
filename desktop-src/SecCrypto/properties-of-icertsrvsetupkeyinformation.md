---
description: 下列屬性是由 ICertSrvSetupKeyInformation 介面所定義。
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: ICertSrvSetupKeyInformation 的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c3e1f95a8bac8a166e5f3046a0517d4b20442c3978219753df5ed33c13c4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977145"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>ICertSrvSetupKeyInformation 的屬性

下列屬性是由 [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) 介面所定義。



| 屬性                                                                           | 描述                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**容器**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | 取得或設定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 用來產生、儲存或存取金鑰的名稱。                                                                       |
| [**Existing**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | 取得或設定值，這個值表示私密金鑰是否已存在。                                                                                                                                                                                                                       |
| [**ExistingCACertificate**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | 取得或設定已使用 [*可辨別編碼規則*](../secgloss/d-gly.md) (DER) 編碼的二進位值，也就是對應至現有金鑰的 CA 憑證的二進位值。 |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | 取得或設定雜湊演算法的名稱，此雜湊演算法用來簽署或驗證金鑰的 CA 憑證。                                                                                                                                                                                                |
| [**長度**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | 取得或設定金鑰的強度為 CSP 所支援的其中一個值。                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | 取得或設定用來產生或儲存私密金鑰的 CSP 名稱。                                                                                                                                                                                                               |



 

 

 
