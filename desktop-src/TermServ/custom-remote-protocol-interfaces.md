---
title: 遠端桌面通訊協定提供者介面
description: 遠端桌面通訊協定提供者 API 所支援的介面。
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931802"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a><span data-ttu-id="3e843-103">遠端桌面通訊協定提供者介面</span><span class="sxs-lookup"><span data-stu-id="3e843-103">Remote Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="3e843-104">遠端桌面通訊協定提供者 API 支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="3e843-104">The following interfaces are supported by the Remote Desktop Protocol Provider API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e843-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="3e843-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3e843-106">**IWRdsProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="3e843-106">**IWRdsProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

<span data-ttu-id="3e843-107">公開遠端桌面服務服務所呼叫的方法，以設定用戶端連接。</span><span class="sxs-lookup"><span data-stu-id="3e843-107">Exposes methods called by the Remote Desktop Services service to configure a client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-108">**IWRdsProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="3e843-108">**IWRdsProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="3e843-109">公開方法，這些方法會提供用戶端連接狀態的相關資訊，以及針對用戶端執行動作的資訊。</span><span class="sxs-lookup"><span data-stu-id="3e843-109">Exposes methods that provide information about the status of a client connection and that perform actions for the client.</span></span> <span data-ttu-id="3e843-110">此介面是由遠端桌面服務服務所執行，並由通訊協定呼叫。</span><span class="sxs-lookup"><span data-stu-id="3e843-110">This interface is implemented by the Remote Desktop Services service and called by the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-111">**IWRdsProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="3e843-111">**IWRdsProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="3e843-112">公開遠端桌面服務服務用來在連接順序期間執行授權交握的方法。</span><span class="sxs-lookup"><span data-stu-id="3e843-112">Exposes methods used by the Remote Desktop Services service to perform the licensing handshake during a connection sequence.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-113">**IWRdsProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="3e843-113">**IWRdsProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

<span data-ttu-id="3e843-114">公開方法，要求通訊協定開始和停止接聽用戶端連接要求。</span><span class="sxs-lookup"><span data-stu-id="3e843-114">Exposes methods that request that the protocol start and stop listening for client connection requests.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-115">**IWRdsProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="3e843-115">**IWRdsProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="3e843-116">公開方法，以通知用戶端已連線的遠端桌面服務服務。</span><span class="sxs-lookup"><span data-stu-id="3e843-116">Exposes methods that notify the Remote Desktop Services service that a client has connected.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-117">**IWRdsProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="3e843-117">**IWRdsProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="3e843-118">公開遠端桌面服務服務所呼叫的方法，以更新登入狀態，並決定如何指示登入錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3e843-118">Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-119">**IWRdsProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="3e843-119">**IWRdsProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

<span data-ttu-id="3e843-120">公開遠端桌面服務服務用來與通訊協定提供者進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="3e843-120">Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-121">**IWRdsProtocolSettings**</span><span class="sxs-lookup"><span data-stu-id="3e843-121">**IWRdsProtocolSettings**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

<span data-ttu-id="3e843-122">公開用來取得和新增原則相關設定的方法。</span><span class="sxs-lookup"><span data-stu-id="3e843-122">Exposes methods for retrieving and adding policy-related settings.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-123">**IWRdsProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="3e843-123">**IWRdsProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="3e843-124">公開由通訊協定呼叫的方法，以通知遠端桌面服務服務啟動或停止陰影的目標端。</span><span class="sxs-lookup"><span data-stu-id="3e843-124">Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-125">**IWRdsProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="3e843-125">**IWRdsProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="3e843-126">公開通知通訊協定提供者有關會話遮蔽狀態的方法。</span><span class="sxs-lookup"><span data-stu-id="3e843-126">Exposes methods that notify the protocol provider about the status of session shadowing.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-127">**IWRdsRemoteFXGraphicsConnection**</span><span class="sxs-lookup"><span data-stu-id="3e843-127">**IWRdsRemoteFXGraphicsConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

<span data-ttu-id="3e843-128">公開與用戶端連接上的圖形操作相關的方法。</span><span class="sxs-lookup"><span data-stu-id="3e843-128">Exposes methods relating to the manipulation and understanding of graphics on the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="3e843-129">已淘汰的桌面通訊協定提供者介面</span><span class="sxs-lookup"><span data-stu-id="3e843-129">Deprecated Desktop Protocol Provider Interfaces</span></span>](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

<span data-ttu-id="3e843-130">下列介面已被取代，不應該再使用。</span><span class="sxs-lookup"><span data-stu-id="3e843-130">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="3e843-131">針對新的專案，請改用遠端桌面通訊協定提供者介面介面。</span><span class="sxs-lookup"><span data-stu-id="3e843-131">For new projects, use the Remote Desktop Protocol Provider Interfaces interfaces instead.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="3e843-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e843-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e843-133">遠端桌面通訊協定提供者參考</span><span class="sxs-lookup"><span data-stu-id="3e843-133">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="3e843-134">遠端桌面通訊協定提供者列舉</span><span class="sxs-lookup"><span data-stu-id="3e843-134">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="3e843-135">遠端桌面通訊協定提供者結構</span><span class="sxs-lookup"><span data-stu-id="3e843-135">Remote Desktop Protocol Provider Structures</span></span>](custom-remote-protocol-structures.md)
</dt> <dt>

[<span data-ttu-id="3e843-136">遠端桌面通訊協定提供者聯集</span><span class="sxs-lookup"><span data-stu-id="3e843-136">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




