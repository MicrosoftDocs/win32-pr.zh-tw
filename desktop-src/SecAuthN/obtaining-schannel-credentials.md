---
description: Schannel 驗證程式需要認證;用戶端和伺服器都必須取得有效的認證，才能建立訊息交換的安全性內容。 如需示範此程式的範例，請參閱取得認證。
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: 取得 Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692932"
---
# <a name="obtaining-schannel-credentials"></a>取得 Schannel 認證

Schannel 驗證程式需要認證;用戶端和伺服器都必須取得有效的認證，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。 如需示範此程式的範例，請參閱 [取得認證](getting-a-certificate-for-schannel.md)。

您的應用程式會藉由呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函式來取得認證，此函式會將控制碼傳回給要求的認證。 因為認證控制碼是用來儲存設定資訊，所以相同的控制碼無法同時用於用戶端和伺服器端作業。 這表示支援用戶端和伺服器連線的應用程式必須至少取得兩個認證控制碼。

在 Windows XP 中，安全通道 [**認證結構會 \_**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) 指定下列各項：

-   安全性通訊協定
-   允許的密碼
-   最小和最大加密強度
-   用於驗證的 [*x.509*](../secgloss/x-gly.md) 憑證—伺服器的必要參數，除非伺服器要求用戶端驗證，否則為用戶端選用。

透過 *pAuthData* 參數) [**，將安全通道認證結構 \_ (**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred)傳遞給 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函數。 此函數會傳回建立 [*安全性內容*](../secgloss/s-gly.md)所需的認證控制碼。

如需設定搭配 Schannel 使用之加密的詳細資訊，請參閱 [指定 Schannel 密碼和加密強度](specifying-schannel-ciphers-and-cipher-strengths.md)。

如需憑證的詳細資訊，請參閱 [憑證和憑證存放區功能](../seccrypto/cryptography-functions.md)。

如需示範如何開啟 [*憑證存放區*](../secgloss/c-gly.md) 並尋找要用於 Schannel 驗證的憑證，請參閱 [取得憑證](getting-a-certificate-for-schannel.md)。

 

 
