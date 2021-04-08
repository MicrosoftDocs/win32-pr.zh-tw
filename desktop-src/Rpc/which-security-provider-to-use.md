---
title: 要使用的安全性提供者
description: 所有其他專案都相等，請使用 RPC \_ c \_ 驗證 \_ GSS \_ KERBEROS 或 rpc \_ c \_ 驗證 \_ GSS \_ NEGOTIATE。
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673247"
---
# <a name="which-security-provider-to-use"></a>要使用的安全性提供者

所有其他專案都相等，請使用 RPC \_ c \_ 驗證 \_ GSS \_ KERBEROS 或 rpc \_ c \_ 驗證 \_ GSS \_ NEGOTIATE。 每個都提供最具擴充性且安全的服務。 如果您在 \_ 伺服器上使用 RPC C \_ 驗證 \_ GSS \_ NEGOTIATE，這會允許下層用戶端（例如 NTLM 用戶端）連接到您的伺服器。 如果不想要的話，請將選擇限制為 \_ \_ 僅限 RPC C 驗證 \_ GSS \_ KERBEROS，或呼叫 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) 來判斷用戶端所使用的安全性提供者，並使用 NTLM 來拒絕用戶端的存取。 建立用戶端所使用之安全性提供者的慣用方法是 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 函式。

 

 




