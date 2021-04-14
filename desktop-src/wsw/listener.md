---
title: 接聽程式
description: 用戶端會使用接聽程式來接受來自服務的傳入通道。
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- 適用于 Windows 的接聽程式 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383325"
---
# <a name="listener"></a><span data-ttu-id="2fa8f-106">接聽程式</span><span class="sxs-lookup"><span data-stu-id="2fa8f-106">Listener</span></span>

<span data-ttu-id="2fa8f-107">用戶端會使用接聽程式來接受來自服務的傳入 [通道](channel.md) 。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="2fa8f-108">若要建立接聽程式缺少，您必須將通道類型指定為 [**WS \_ 通道 \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) 列舉值、系 [結資訊，](binding.md) 以及要接聽的 [URL](url.md) 。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="2fa8f-109">若要開始在 URL 上接聽，請呼叫 [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) 函數。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="2fa8f-110">若要接受連入通訊，請呼叫 [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="2fa8f-111">若要取消接聽程式的暫止 IO，請呼叫 [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="2fa8f-112">如需有關接聽程式之狀態轉換的詳細資訊，請參閱 WS 接聽程式 [**\_ \_ 狀態**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) 列舉。</span><span class="sxs-lookup"><span data-stu-id="2fa8f-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="2fa8f-113">下列回呼是接聽程式的一部分：</span><span class="sxs-lookup"><span data-stu-id="2fa8f-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="2fa8f-114">**WS \_ 中止接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="2fa8f-115">**WS \_ 接受 \_ 通道 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="2fa8f-116">**WS \_ 關閉接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="2fa8f-117">**接聽 \_ \_ \_ 程式回呼的 \_ WS CREATE 通道 \_**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="2fa8f-118">**WS \_ 建立接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="2fa8f-119">**WS \_ 免費接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="2fa8f-120">**WS \_ GET 接聽程式 \_ \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="2fa8f-121">**WS \_ 開啟接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="2fa8f-122">**WS \_ 重設接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="2fa8f-123">**WS \_ SET 接聽程式 \_ \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="2fa8f-124">下列列舉是接聽程式的一部分：</span><span class="sxs-lookup"><span data-stu-id="2fa8f-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="2fa8f-125">**WS \_ IP \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="2fa8f-126">**WS 接聽程式 \_ \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="2fa8f-127">**WS 接聽程式 \_ \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="2fa8f-128">下列函數是接聽程式的一部分：</span><span class="sxs-lookup"><span data-stu-id="2fa8f-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="2fa8f-129">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="2fa8f-130">**WsAcceptChannel**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="2fa8f-131">**WsCloseListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="2fa8f-132">**WsCreateListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="2fa8f-133">**WsFreeListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="2fa8f-134">**WsGetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="2fa8f-135">**WsOpenListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="2fa8f-136">**WsResetListener**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="2fa8f-137">**WsSetListenerProperty**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="2fa8f-138">下列控制碼是接聽程式的一部分：</span><span class="sxs-lookup"><span data-stu-id="2fa8f-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="2fa8f-139">WS \_ 接聽程式</span><span class="sxs-lookup"><span data-stu-id="2fa8f-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="2fa8f-140">下列結構是接聽程式的一部分：</span><span class="sxs-lookup"><span data-stu-id="2fa8f-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="2fa8f-141">**WS \_ 自訂接聽程式 \_ \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="2fa8f-142">**WS 不 \_ 允許的 \_ 使用者 \_ 代理程式 \_ 子字串**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="2fa8f-143">**WS \_ 主機 \_ 名**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="2fa8f-144">**WS 接聽程式 \_ \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="2fa8f-145">**WS 接聽程式 \_ \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="2fa8f-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




