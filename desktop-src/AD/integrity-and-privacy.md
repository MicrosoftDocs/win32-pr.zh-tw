---
title: 完整性和隱私權
description: 需要相互驗證的用戶端/服務通訊必須保護它們在成功驗證之後交換的流量。
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- 完整性和隱私權 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c287956fcebc250d5324a15f88fb6a47e087fca40f68f793dd695b47e6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187102"
---
# <a name="integrity-and-privacy"></a>完整性和隱私權

需要相互驗證的用戶端/服務通訊必須保護它們在成功驗證之後交換的流量。 如果流量稍後可能被未經授權的使用者修改，則造成在初始連線至服務時進行相互驗證。 SSPI、RPC 和 COM 都提供可用於數位簽署和加密訊息的公用程式。 套用數位簽章可防止未偵測到的已修改流量，以及防止竊聽。 您可以攔截流量，但是解密流量很難阻擋大多數未經授權的使用者。

除非效能需求很嚴重，否則建議使用簽署和加密，尤其是針對系統管理功能。 即使當效能是問題時，有些客戶會選擇更嚴密的安全性，以提升效能。 在這種情況下，請以較高的安全性提供完整性和隱私權可設定選項，此選項預設和更高的效能。

RPC 用戶端可以在呼叫 [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) 函式來設定 RPC 系結的驗證資料時，指定完整性和隱私權的層級。 使用 **rpc \_ c \_ 驗證 \_ level \_ pkt \_ 完整性** 進行簽署，並使用 **rpc \_ c \_ 驗證 \_ LEVEL \_ pkt \_ 隱私權** 進行加密。 如需詳細資訊，請參閱 [RPC 應用程式中的相互驗證](mutual-authentication-in-rpc-applications.md)。

使用 SSPI 套件進行相互驗證的服務可以查詢套件，以判斷它是否支援 [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature)、 [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature)、 [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)和 [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) 功能來簽署和加密訊息。 如需詳細資訊和程式碼範例，請參閱[確保訊息 Exchange 期間的通訊完整性](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange)。

 

 