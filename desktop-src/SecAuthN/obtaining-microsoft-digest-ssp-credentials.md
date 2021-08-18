---
description: Microsoft Digest 需要使用者認證;用戶端和伺服器都必須顯示有效的認證，才能建立訊息交換的安全性內容。 認證控制碼可用來取得和出示認證。
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: 取得 Microsoft Digest 的 SSP 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17889331453f009d0d19b7b834e9a4b1301636ec41ef73e6557f79419b461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921277"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a>取得 Microsoft Digest 的 SSP 認證

Microsoft Digest 需要使用者 [*認證*](../secgloss/c-gly.md) ;用戶端和伺服器都必須顯示有效的認證，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。 認證控制碼可用來取得和出示認證。

因為認證控制碼是用來儲存設定資訊，所以相同的控制碼無法同時用於用戶端和伺服器端作業。 這表示支援用戶端和伺服器連線的應用程式必須至少取得兩個認證控制碼。

若要取得 Microsoft Digest 所需認證的控制碼，請呼叫 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) 函數。

下列 C 語言範例示範如何取得認證。

-   [取得預設摘要認證](obtaining-default-digest-credentials.md)
-   [取得替代的摘要認證](obtaining-alternate-digest-credentials.md)

 

 
