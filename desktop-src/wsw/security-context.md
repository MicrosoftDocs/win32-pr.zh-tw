---
title: 安全性內容
description: 安全性內容可讓您根據 SecureConversation 來建立訊息安全性內容。
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- 安全性內容原生-Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316789"
---
# <a name="security-context"></a><span data-ttu-id="35540-106">安全性內容</span><span class="sxs-lookup"><span data-stu-id="35540-106">Security Context</span></span>

<span data-ttu-id="35540-107">安全性內容可讓您根據 SecureConversation 來建立訊息安全性內容。</span><span class="sxs-lookup"><span data-stu-id="35540-107">Security contexts enable the establishment of a message security context according to WS-SecureConversation.</span></span> <span data-ttu-id="35540-108">接著，該內容可以用來保護訊息的安全，作為單次安全性的替代方案，其中會針對每個要求傳輸認證。</span><span class="sxs-lookup"><span data-stu-id="35540-108">That context can then be used to secure messages as an alternative to one-shot security where the credentials are transmitted for every request.</span></span> <span data-ttu-id="35540-109">在交換多個訊息時，所建立的安全性內容是更有效率的訊息安全方法。</span><span class="sxs-lookup"><span data-stu-id="35540-109">The established security context is a more efficient method of securing messages when multiple messages are exchanged.</span></span>


<span data-ttu-id="35540-110">安全性內容需要有啟動程式安全性認證，用來保護內容中傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="35540-110">Security contexts require the presence of bootstrap security credentials that are used to secure the messages sent in the context.</span></span> <span data-ttu-id="35540-111">[**Ws \_ KERBEROS \_ APREQ \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)系結、 [**ws \_ XML \_ 權杖 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)系結，以及 ws 使用者 [**\_ 名稱 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)系結結構可用於此用途。</span><span class="sxs-lookup"><span data-stu-id="35540-111">The [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), [**WS\_XML\_TOKEN\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding), and [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) structures may be used for this purpose.</span></span>

<span data-ttu-id="35540-112">安全性內容是一種訊息安全性功能，而且是透過訊息安全性系結來設定。</span><span class="sxs-lookup"><span data-stu-id="35540-112">Security contexts are a message security feature and are configured by way of message security bindings.</span></span>

## <a name="client"></a><span data-ttu-id="35540-113">用戶端</span><span class="sxs-lookup"><span data-stu-id="35540-113">Client</span></span>

<span data-ttu-id="35540-114">在用戶端上，安全性內容會系結至特定通道。</span><span class="sxs-lookup"><span data-stu-id="35540-114">On the client side, the security context is tied to a particular channel.</span></span> <span data-ttu-id="35540-115">它是使用 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)系結來設定。</span><span class="sxs-lookup"><span data-stu-id="35540-115">It is configured using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding).</span></span> <span data-ttu-id="35540-116">內容的行為和存留期是由通道所決定。</span><span class="sxs-lookup"><span data-stu-id="35540-116">Behavior and lifetime of the context are determined by the channel.</span></span> <span data-ttu-id="35540-117">在通道上傳送第一個訊息時，就會建立安全性內容。</span><span class="sxs-lookup"><span data-stu-id="35540-117">When the first message is sent on the channel, the security context is established.</span></span> <span data-ttu-id="35540-118">之後，內容會以可設定的間隔主動更新。</span><span class="sxs-lookup"><span data-stu-id="35540-118">After that, the context is proactively renewed at a configurable interval.</span></span> <span data-ttu-id="35540-119">如果伺服器傳回的錯誤指出內容需要更新，則會在傳送下一個訊息時更新內容。</span><span class="sxs-lookup"><span data-stu-id="35540-119">If the server returns a fault indicating that the context requires renewal, the context is renewed when the next message is sent.</span></span> <span data-ttu-id="35540-120">如果通道處於開啟狀態，則關閉通道時，會取消訊息的內容。</span><span class="sxs-lookup"><span data-stu-id="35540-120">If the channel is in the open state, the context is canceled by a cancel message when the channel is closed.</span></span>

## <a name="server"></a><span data-ttu-id="35540-121">伺服器</span><span class="sxs-lookup"><span data-stu-id="35540-121">Server</span></span>

<span data-ttu-id="35540-122">在伺服器上，安全性內容的設定方式與用戶端上的設定方式相同。</span><span class="sxs-lookup"><span data-stu-id="35540-122">On the server, a security context is configured the same way as on the client.</span></span> <span data-ttu-id="35540-123">但是，它並不會系結至任何特定通道。</span><span class="sxs-lookup"><span data-stu-id="35540-123">However, it is not tied to any particular channel.</span></span> <span data-ttu-id="35540-124">相反地，針對具有 [**WS \_ 安全性 \_ 內容 \_ 訊息 \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) 系結集的接聽程式所建立的所有通道，都能夠接收訊息，其中包含在該接聽程式的通道上建立的任何安全性內容。</span><span class="sxs-lookup"><span data-stu-id="35540-124">Instead, all channels created for the listener that has the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) set are capable of receiving messages with any of the security contexts that were established on channels of that listener.</span></span>

<span data-ttu-id="35540-125">當訊息抵達支援安全性內容的通道時，該訊息所使用的內容可以藉由呼叫 [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) 函數與 [**WS \_ message \_ 屬性 \_ 安全性 \_ 內容**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)來取得。</span><span class="sxs-lookup"><span data-stu-id="35540-125">When a message arrives on a channel that supports security contexts, the context used by that message can by obtained by calling the [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) function with the [**WS\_MESSAGE\_PROPERTY\_SECURITY\_CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="35540-126">抓取的值可以搭配 [**WsRevokeSecurityCoNtext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) 和 [**WsGetSecurityCoNtextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty)使用。</span><span class="sxs-lookup"><span data-stu-id="35540-126">The retrieved value can be used with [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) and [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).</span></span>

## <a name="metadata"></a><span data-ttu-id="35540-127">中繼資料</span><span class="sxs-lookup"><span data-stu-id="35540-127">Metadata</span></span>

<span data-ttu-id="35540-128">[**WS \_ 安全性 \_ 內容訊息安全性系結 \_ \_ \_ \_ 條件約束**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)結構是用來從中繼資料中解壓縮安全性內容原則。</span><span class="sxs-lookup"><span data-stu-id="35540-128">The [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) structure is used to extract the security context policy from metadata.</span></span> <span data-ttu-id="35540-129">如需詳細資訊，請參閱 [中繼資料匯入](metadata-import.md)。</span><span class="sxs-lookup"><span data-stu-id="35540-129">For more information, see [Metadata Import](metadata-import.md).</span></span>

<span data-ttu-id="35540-130">下列 API 專案會搭配安全性內容使用。</span><span class="sxs-lookup"><span data-stu-id="35540-130">The following API elements are used with security contexts.</span></span>

| <span data-ttu-id="35540-131">列舉型別</span><span class="sxs-lookup"><span data-stu-id="35540-131">Enumeration</span></span>                                                                    | <span data-ttu-id="35540-132">描述</span><span class="sxs-lookup"><span data-stu-id="35540-132">Description</span></span>                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="35540-133">**WS \_ 安全性 \_ 上下文 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="35540-133">**WS\_SECURITY\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | <span data-ttu-id="35540-134">識別安全性內容物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="35540-134">Identifies a property of a security context object.</span></span> |



 



| <span data-ttu-id="35540-135">函式</span><span class="sxs-lookup"><span data-stu-id="35540-135">Function</span></span>                                                             | <span data-ttu-id="35540-136">描述</span><span class="sxs-lookup"><span data-stu-id="35540-136">Description</span></span>                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="35540-137">**WsGetSecurityCoNtextProperty**</span><span class="sxs-lookup"><span data-stu-id="35540-137">**WsGetSecurityContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | <span data-ttu-id="35540-138">取得指定之安全性內容的屬性。</span><span class="sxs-lookup"><span data-stu-id="35540-138">Gets a property of the specified security context.</span></span> |
| [<span data-ttu-id="35540-139">**WsRevokeSecurityCoNtext**</span><span class="sxs-lookup"><span data-stu-id="35540-139">**WsRevokeSecurityContext**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | <span data-ttu-id="35540-140">撤銷安全性內容。</span><span class="sxs-lookup"><span data-stu-id="35540-140">Revokes a security context.</span></span>                        |



 



| <span data-ttu-id="35540-141">Handle</span><span class="sxs-lookup"><span data-stu-id="35540-141">Handle</span></span>                                           | <span data-ttu-id="35540-142">Description</span><span class="sxs-lookup"><span data-stu-id="35540-142">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="35540-143">WS \_ 安全性 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="35540-143">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md) | <span data-ttu-id="35540-144">用來參考安全性內容物件的不透明類型。</span><span class="sxs-lookup"><span data-stu-id="35540-144">An opaque type used to reference a security context object.</span></span> |



 



| <span data-ttu-id="35540-145">結構</span><span class="sxs-lookup"><span data-stu-id="35540-145">Structure</span></span>                                                               | <span data-ttu-id="35540-146">Description</span><span class="sxs-lookup"><span data-stu-id="35540-146">Description</span></span>                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="35540-147">**WS \_ 安全性 \_ 上下文 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="35540-147">**WS\_SECURITY\_CONTEXT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | <span data-ttu-id="35540-148">定義 [WS \_ 安全性 \_ 內容](ws-security-context.md)的屬性。</span><span class="sxs-lookup"><span data-stu-id="35540-148">Defines a property of a [WS\_SECURITY\_CONTEXT](ws-security-context.md).</span></span> |



 

 

 




