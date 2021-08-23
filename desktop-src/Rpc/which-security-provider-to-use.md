---
title: 要使用的安全性提供者
description: 所有其他專案都相等，請使用 RPC \_ c \_ 驗證 \_ GSS \_ KERBEROS 或 rpc \_ c \_ 驗證 \_ GSS \_ NEGOTIATE。
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b89bdb10eb95952183b2a992fd12a668e79b0716f3c453f597d2241323c4ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010446"
---
# <a name="which-security-provider-to-use"></a>要使用的安全性提供者

所有其他專案都相等，請使用 RPC \_ c \_ 驗證 \_ GSS \_ KERBEROS 或 rpc \_ c \_ 驗證 \_ GSS \_ NEGOTIATE。 每個都提供最具擴充性且安全的服務。 如果您在 \_ 伺服器上使用 RPC C \_ 驗證 \_ GSS \_ NEGOTIATE，這會允許下層用戶端（例如 NTLM 用戶端）連接到您的伺服器。 如果不想要的話，請將選擇限制為 \_ \_ 僅限 RPC C 驗證 \_ GSS \_ KERBEROS，或呼叫 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) 來判斷用戶端所使用的安全性提供者，並使用 NTLM 來拒絕用戶端的存取。 建立用戶端所使用之安全性提供者的慣用方法是 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 函式。

 

 




