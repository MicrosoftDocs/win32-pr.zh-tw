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
# <a name="which-security-provider-to-use"></a><span data-ttu-id="fe892-103">要使用的安全性提供者</span><span class="sxs-lookup"><span data-stu-id="fe892-103">Which Security Provider to Use</span></span>

<span data-ttu-id="fe892-104">所有其他專案都相等，請使用 RPC \_ c \_ 驗證 \_ GSS \_ KERBEROS 或 rpc \_ c \_ 驗證 \_ GSS \_ NEGOTIATE。</span><span class="sxs-lookup"><span data-stu-id="fe892-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="fe892-105">每個都提供最具擴充性且安全的服務。</span><span class="sxs-lookup"><span data-stu-id="fe892-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="fe892-106">如果您在 \_ 伺服器上使用 RPC C \_ 驗證 \_ GSS \_ NEGOTIATE，這會允許下層用戶端（例如 NTLM 用戶端）連接到您的伺服器。</span><span class="sxs-lookup"><span data-stu-id="fe892-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="fe892-107">如果不想要的話，請將選擇限制為 \_ \_ 僅限 RPC C 驗證 \_ GSS \_ KERBEROS，或呼叫 [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) 來判斷用戶端所使用的安全性提供者，並使用 NTLM 來拒絕用戶端的存取。</span><span class="sxs-lookup"><span data-stu-id="fe892-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="fe892-108">建立用戶端所使用之安全性提供者的慣用方法是 [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) 函式。</span><span class="sxs-lookup"><span data-stu-id="fe892-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




