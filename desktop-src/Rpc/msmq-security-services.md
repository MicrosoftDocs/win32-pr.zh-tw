---
title: MSMQ 安全性服務
description: 同步 RPC 訊息可以使用 RPC 執行時間所提供的任何安全性功能。 如需詳細資訊，請參閱安全性。
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092944"
---
# <a name="msmq-security-services"></a><span data-ttu-id="c1fb7-104">MSMQ 安全性服務</span><span class="sxs-lookup"><span data-stu-id="c1fb7-104">MSMQ Security Services</span></span>

<span data-ttu-id="c1fb7-105">同步 RPC 訊息可以使用 RPC 執行時間所提供的任何安全性功能。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="c1fb7-106">如需詳細資訊，請參閱 [安全性](security.md) 。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="c1fb7-107">非同步 \[ [訊息](/windows/desktop/Midl/message) \] 呼叫無法使用 RPC 安全性，因為用戶端與伺服器之間沒有信號交換。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="c1fb7-108">事實上，伺服器可能甚至不會在呼叫時執行。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="c1fb7-109">若要存取訊息佇列服務 (MSMQ) 所提供的安全性服務，用戶端應用程式應該呼叫 [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) 來控制其對伺服器之呼叫的驗證層級和隱私權。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="c1fb7-110">伺服器應用程式可以從遠端程序呼叫內呼叫 [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) ，以判斷該呼叫的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="c1fb7-111">下表顯示 RPC 安全性常數與 MSMQ 安全性之間的對應。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="c1fb7-112">RPC 安全性層級</span><span class="sxs-lookup"><span data-stu-id="c1fb7-112">RPC security level</span></span>                | <span data-ttu-id="c1fb7-113">Description</span><span class="sxs-lookup"><span data-stu-id="c1fb7-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fb7-114">RPC \_ 驗證 \_ 層級 \_ 無</span><span class="sxs-lookup"><span data-stu-id="c1fb7-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="c1fb7-115">呼叫未經過驗證或加密。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="c1fb7-116">RPC \_ 驗證 \_ 層級的 \_ PKT \_ 完整性</span><span class="sxs-lookup"><span data-stu-id="c1fb7-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="c1fb7-117">呼叫是使用 MSMQ 安全性進行驗證。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="c1fb7-118">RPC \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權</span><span class="sxs-lookup"><span data-stu-id="c1fb7-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="c1fb7-119">呼叫會在用戶端和伺服器佇列之間傳輸時進行驗證和加密。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="c1fb7-120">伺服器也可以藉由呼叫 [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) 和設定 rpc \_ c \_ mq \_ 驗證 \_ 層級 \_ NONE、rpc \_ c \_ mq \_ 驗證 \_ 層級 \_ \_ 的 pkt 完整性和 rpc \_ c \_ mq \_ 驗證 \_ level \_ pkt \_ [**rpc \_ 原則**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) 結構中的隱私權旗標，來強制執行呼叫驗證和加密。</span><span class="sxs-lookup"><span data-stu-id="c1fb7-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 