---
title: 安全性描述
description: 安全性描述是以 WS \_ 安全性 \_ 描述結構表示，而當您呼叫 WsCreateChannel 函式來建立安全通道或 WsCreateListener 函式以建立接聽程式時，會提供安全性描述的實例。
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- 適用于 Windows 的安全性描述 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104116017"
---
# <a name="security-description"></a><span data-ttu-id="733bc-106">安全性描述</span><span class="sxs-lookup"><span data-stu-id="733bc-106">Security Description</span></span>

<span data-ttu-id="733bc-107">安全性描述是以 [**WS \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構表示，而當您呼叫 [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) 函式來建立安全通道或 [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) 函式以建立接聽程式時，會提供安全性描述的實例。</span><span class="sxs-lookup"><span data-stu-id="733bc-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="733bc-108">安全性描述的結構</span><span class="sxs-lookup"><span data-stu-id="733bc-108">Structure of a Security Description</span></span>

<span data-ttu-id="733bc-109">通道安全性的基本模型是使用一或多個安全性權杖來保護通道。</span><span class="sxs-lookup"><span data-stu-id="733bc-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="733bc-110">建立此模型時， [**ws \_ 安全性 \_ 描述**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) 結構包含安全性系結的清單（由 [**ws \_ 安全性 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) 系結結構所代表），而每個安全性系結會說明如何取得和使用通道上的一個安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="733bc-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="733bc-111">通道上所使用的安全性類型是由安全性描述中所包含的安全性系結子類型選取專案所決定。</span><span class="sxs-lookup"><span data-stu-id="733bc-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="733bc-112">安全性系結特定的選用安全性設定會指定為安全性系結結構中的安全性系結 [設定](security-binding-settings.md);不過，與安全性系結無關的全通道設定，會直接在安全性描述本身的 [**屬性**] 欄位中指定為 [安全性通道設定](security-channel-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="733bc-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![顯示安全性描述結構的圖表。](images/securitydescription.png)

<span data-ttu-id="733bc-114">下列 API 元素會搭配安全性描述使用。</span><span class="sxs-lookup"><span data-stu-id="733bc-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="733bc-115">結構</span><span class="sxs-lookup"><span data-stu-id="733bc-115">Structure</span></span>                                                    | <span data-ttu-id="733bc-116">Description</span><span class="sxs-lookup"><span data-stu-id="733bc-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="733bc-117">**WS \_ 安全性 \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="733bc-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="733bc-118">最上層結構，用來指定用戶端上的通道 (的安全性需求) 或伺服器端)  (的接聽程式。</span><span class="sxs-lookup"><span data-stu-id="733bc-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 




