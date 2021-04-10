---
title: 已淘汰的桌面通訊協定提供者介面
description: 下列介面已被取代，不應該再使用。 針對新的專案，請改用遠端桌面通訊協定提供者介面介面。
ms.assetid: FD64A6B9-AE15-4311-BD69-4824CAF53544
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11a586084bc4938727e632ca196e97117f7b8a4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841544"
---
# <a name="deprecated-desktop-protocol-provider-interfaces"></a><span data-ttu-id="cce72-104">已淘汰的桌面通訊協定提供者介面</span><span class="sxs-lookup"><span data-stu-id="cce72-104">Deprecated Desktop Protocol Provider Interfaces</span></span>

<span data-ttu-id="cce72-105">下列介面已被取代，不應該再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-105">The following interfaces have been deprecated and should no longer be used.</span></span> <span data-ttu-id="cce72-106">針對新的專案，請改用 [遠端桌面通訊協定提供者介面](custom-remote-protocol-interfaces.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="cce72-106">For new projects, use the [Remote Desktop Protocol Provider Interfaces](custom-remote-protocol-interfaces.md) interfaces instead.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cce72-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="cce72-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cce72-108">**IWTSProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="cce72-108">**IWTSProtocolConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection)
</dt> <dd>

<span data-ttu-id="cce72-109">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-109">[**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) is no longer available.</span></span> <span data-ttu-id="cce72-110">相反地，請使用 [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)。</span><span class="sxs-lookup"><span data-stu-id="cce72-110">Instead, use [**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-111">**IWTSProtocolConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="cce72-111">**IWTSProtocolConnectionCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback)
</dt> <dd>

<span data-ttu-id="cce72-112">[**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-112">[**IWTSProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback) is no longer available.</span></span> <span data-ttu-id="cce72-113">相反地，請使用 [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)。</span><span class="sxs-lookup"><span data-stu-id="cce72-113">Instead, use [**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-114">**IWTSProtocolLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="cce72-114">**IWTSProtocolLicenseConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection)
</dt> <dd>

<span data-ttu-id="cce72-115">[**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-115">[**IWTSProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection) is no longer available.</span></span> <span data-ttu-id="cce72-116">相反地，請使用 [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)。</span><span class="sxs-lookup"><span data-stu-id="cce72-116">Instead, use [**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-117">**IWTSProtocolListener**</span><span class="sxs-lookup"><span data-stu-id="cce72-117">**IWTSProtocolListener**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener)
</dt> <dd>

<span data-ttu-id="cce72-118">[**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-118">[**IWTSProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener) is no longer available.</span></span> <span data-ttu-id="cce72-119">相反地，請使用 [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)。</span><span class="sxs-lookup"><span data-stu-id="cce72-119">Instead, use [**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-120">**IWTSProtocolListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="cce72-120">**IWTSProtocolListenerCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback)
</dt> <dd>

<span data-ttu-id="cce72-121">[**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-121">[**IWTSProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistenercallback) is no longer available.</span></span> <span data-ttu-id="cce72-122">相反地，請使用 [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)。</span><span class="sxs-lookup"><span data-stu-id="cce72-122">Instead, use [**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-123">**IWTSProtocolLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="cce72-123">**IWTSProtocolLogonErrorRedirector**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector)
</dt> <dd>

<span data-ttu-id="cce72-124">[**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-124">[**IWTSProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector) is no longer available.</span></span> <span data-ttu-id="cce72-125">相反地，請使用 [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)。</span><span class="sxs-lookup"><span data-stu-id="cce72-125">Instead, use [**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-126">**IWTSProtocolManager**</span><span class="sxs-lookup"><span data-stu-id="cce72-126">**IWTSProtocolManager**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager)
</dt> <dd>

<span data-ttu-id="cce72-127">[**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-127">[**IWTSProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager) is no longer available.</span></span> <span data-ttu-id="cce72-128">相反地，請使用 [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)。</span><span class="sxs-lookup"><span data-stu-id="cce72-128">Instead, use [**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-129">**IWTSProtocolShadowCallback**</span><span class="sxs-lookup"><span data-stu-id="cce72-129">**IWTSProtocolShadowCallback**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback)
</dt> <dd>

<span data-ttu-id="cce72-130">[**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-130">[**IWTSProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowcallback) is no longer available.</span></span> <span data-ttu-id="cce72-131">相反地，請使用 [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)。</span><span class="sxs-lookup"><span data-stu-id="cce72-131">Instead, use [**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback).</span></span>

</dd> <dt>

[<span data-ttu-id="cce72-132">**IWTSProtocolShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="cce72-132">**IWTSProtocolShadowConnection**</span></span>](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection)
</dt> <dd>

<span data-ttu-id="cce72-133">[**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) 已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="cce72-133">[**IWTSProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection) is no longer available.</span></span> <span data-ttu-id="cce72-134">相反地，請使用 [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)。</span><span class="sxs-lookup"><span data-stu-id="cce72-134">Instead, use [**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection).</span></span>

</dd> </dl>

 

 




