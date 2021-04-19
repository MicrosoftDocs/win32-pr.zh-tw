---
description: 裝置上的 Web 服務 API (WSDAPI) 用來開發用戶端應用程式，以尋找和存取裝置，以及開發在 Windows Vista 和 Windows Server 2008 上執行的裝置主機和相關聯的服務。
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: WSDAPI 介面的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975028"
---
# <a name="overview-of-the-wsdapi-interfaces"></a><span data-ttu-id="023cd-103">WSDAPI 介面的總覽</span><span class="sxs-lookup"><span data-stu-id="023cd-103">Overview of the WSDAPI Interfaces</span></span>

<span data-ttu-id="023cd-104">裝置上的 Web 服務 API (WSDAPI) 用來開發用戶端應用程式，以尋找和存取裝置，以及開發在 Windows Vista 和 Windows Server 2008 上執行的裝置主機和相關聯的服務。</span><span class="sxs-lookup"><span data-stu-id="023cd-104">Web Services on Devices API (WSDAPI) is used to develop client applications that find and access devices, and to develop device hosts and associated services that run on Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="023cd-105">[函數探索](/previous-versions/windows/desktop/fundisc/fd-portal)API 和[WsdCodeGen](web-services-for-devices-code-generator.md)工具是可用於用戶端、裝置主機和服務開發的補充工具。</span><span class="sxs-lookup"><span data-stu-id="023cd-105">The [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API and the [WsdCodeGen](web-services-for-devices-code-generator.md) tool are supplemental tools that can be used for client, device host, and service development.</span></span> <span data-ttu-id="023cd-106">WSDAPI 介面可以直接用來公開 advanced 功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-106">The WSDAPI interfaces can be used directly to expose advanced functionality.</span></span>

## <a name="major-wsdapi-interfaces"></a><span data-ttu-id="023cd-107">主要 WSDAPI 介面</span><span class="sxs-lookup"><span data-stu-id="023cd-107">Major WSDAPI interfaces</span></span>

<span data-ttu-id="023cd-108">四個主要的 WSDAPI 介面為 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider)、 [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher)、 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)和 [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)。</span><span class="sxs-lookup"><span data-stu-id="023cd-108">The four major WSDAPI interfaces are [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy), and [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost).</span></span> <span data-ttu-id="023cd-109">如需所有 WSDAPI 介面的清單，請參閱 [ [裝置上的 Web 服務] 介面](web-services-for-devices-interfaces.md)。</span><span class="sxs-lookup"><span data-stu-id="023cd-109">For a list of all of the WSDAPI interfaces, see [Web Services on Devices Interfaces](web-services-for-devices-interfaces.md).</span></span>

## <a name="iwsdiscoveryprovider"></a><span data-ttu-id="023cd-110">IWSDiscoveryProvider</span><span class="sxs-lookup"><span data-stu-id="023cd-110">IWSDiscoveryProvider</span></span>

<span data-ttu-id="023cd-111">[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 用來在用戶端上執行 WS-Discovery 的功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-111">[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) is used to implement WS-Discovery functionality on clients.</span></span>

<span data-ttu-id="023cd-112">[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) WS-Discovery [探查](probe-message.md) 和 [解決](resolve-message.md) 訊息，以及接收 [Hello](hello-message.md)、 [再見](bye-message.md)、 [ProbeMatches](probematches-message.md)和 [ResolveMatches](resolvematches-message.md) 訊息的問題。</span><span class="sxs-lookup"><span data-stu-id="023cd-112">[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) issues WS-Discovery [Probe](probe-message.md) and [Resolve](resolve-message.md) messages, and receives [Hello](hello-message.md), [Bye](bye-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md) messages.</span></span> <span data-ttu-id="023cd-113">建立用來描述及控制特定 DPWS 裝置的 [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)介面時，請使用透過 **IWSDiscoveryProvider** 介面抓取的資訊。</span><span class="sxs-lookup"><span data-stu-id="023cd-113">Use the information retrieved through the **IWSDiscoveryProvider** interface when creating an [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) interface used to describe and control a specific DPWS device.</span></span>

<span data-ttu-id="023cd-114">在建立裝置 proxy 之前，只要先解析特定的 DPWS 裝置位址，就不需要 [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="023cd-114">An [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interface is not necessary when simply resolving a particular DPWS device address before creating a device proxy.</span></span> <span data-ttu-id="023cd-115">必要時， [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)會自動解析裝置位址。</span><span class="sxs-lookup"><span data-stu-id="023cd-115">[**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) will automatically resolve the device address if required.</span></span>

<span data-ttu-id="023cd-116">[函數探索](/previous-versions/windows/desktop/fundisc/fd-portal)API 可用於一般裝置和服務探索，因為 API 可以探索 DPWS 裝置以及使用其他通訊協定的裝置。</span><span class="sxs-lookup"><span data-stu-id="023cd-116">The [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API can be used for generic device and service discovery, as the API can discover DPWS devices and also devices using other protocols.</span></span> <span data-ttu-id="023cd-117">撰寫一般探索應用程式時，請考慮使用函數探索。</span><span class="sxs-lookup"><span data-stu-id="023cd-117">Consider using Function Discovery when writing a generic discovery application.</span></span>

## <a name="iwsdiscoverypublisher"></a><span data-ttu-id="023cd-118">IWSDiscoveryPublisher</span><span class="sxs-lookup"><span data-stu-id="023cd-118">IWSDiscoveryPublisher</span></span>

<span data-ttu-id="023cd-119">[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) 可用來在目標服務（例如裝置）上執行 WS-Discovery 功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-119">[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) is used to implement WS-Discovery functionality on target services, such as devices.</span></span>

<span data-ttu-id="023cd-120">[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) 可讓應用程式使用 WS-Discovery 的 Hello 和再見訊息發佈其存在。</span><span class="sxs-lookup"><span data-stu-id="023cd-120">[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) allows an application to publish its presence using WS-Discovery Hello and Bye messages.</span></span> <span data-ttu-id="023cd-121">此介面可讓應用程式接收探查和解析要求，以及建立和傳送 ProbeMatches 和 ResolveMatches 回應。</span><span class="sxs-lookup"><span data-stu-id="023cd-121">This interface allows an application to receive Probe and Resolve requests, and construct and send ProbeMatches and ResolveMatches responses.</span></span>

<span data-ttu-id="023cd-122">只要發行 [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)物件存在，就不需要 [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher)介面。</span><span class="sxs-lookup"><span data-stu-id="023cd-122">An [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) interface is not necessary when simply publishing the existence of an [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) object.</span></span> <span data-ttu-id="023cd-123">**IWSDDeviceHost** 會管理自己的 WS-Discovery 存在。</span><span class="sxs-lookup"><span data-stu-id="023cd-123">**IWSDDeviceHost** manages its own WS-Discovery presence.</span></span>

## <a name="iwsddeviceproxy"></a><span data-ttu-id="023cd-124">IWSDDeviceProxy</span><span class="sxs-lookup"><span data-stu-id="023cd-124">IWSDDeviceProxy</span></span>

<span data-ttu-id="023cd-125">[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) 可用來執行用戶端的 ws 探索、透過 ws-metadataexchange 和控制功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-125">[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) is used to implement client-side WS-Discovery, WS-MetadataExchange, and control functionality.</span></span> <span data-ttu-id="023cd-126">這種功能包括選擇性的安全通道、WS-事件和附件功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-126">This functionality includes optional secure channel, WS-Eventing, and attachment capabilities.</span></span>

<span data-ttu-id="023cd-127">[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)介面具有下列三種用途。</span><span class="sxs-lookup"><span data-stu-id="023cd-127">The [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) interface has the following three uses.</span></span>

-   <span data-ttu-id="023cd-128">視需要解析邏輯裝置位址。</span><span class="sxs-lookup"><span data-stu-id="023cd-128">Resolves logical device addresses, if necessary.</span></span>
-   <span data-ttu-id="023cd-129">起始對裝置的中繼資料要求，以列舉服務的類型和位址。</span><span class="sxs-lookup"><span data-stu-id="023cd-129">Initiates metadata requests to devices to enumerate the types and addresses of services.</span></span>
-   <span data-ttu-id="023cd-130">提供 [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) 物件的來源，可用來將控制訊息發出至裝置上的特定服務。</span><span class="sxs-lookup"><span data-stu-id="023cd-130">Provides a source for [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) objects, which can be used to issue control messages to specific services on a device.</span></span>

<span data-ttu-id="023cd-131">[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)物件通常是在 [WsdCodeGen](web-services-for-devices-code-generator.md)所產生的程式碼內建立和使用。</span><span class="sxs-lookup"><span data-stu-id="023cd-131">The [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) object is typically created and used entirely inside code generated by [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span>

## <a name="iwsddevicehost"></a><span data-ttu-id="023cd-132">IWSDDeviceHost</span><span class="sxs-lookup"><span data-stu-id="023cd-132">IWSDDeviceHost</span></span>

<span data-ttu-id="023cd-133">[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) 可用來執行裝置端的 ws 探索、Ws-透過 ws-metadataexchange 和服務裝載功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-133">[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) is used to implement device-side WS-Discovery, WS-MetadataExchange, and service hosting functionality.</span></span> <span data-ttu-id="023cd-134">託管服務可能會回應控制訊息，並且可能支援安全通道、WS-事件和附件功能。</span><span class="sxs-lookup"><span data-stu-id="023cd-134">Hosted services may respond to control messages, and may support secure channel, WS-Eventing, and attachment capabilities.</span></span>

<span data-ttu-id="023cd-135">[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)介面具有下列用途。</span><span class="sxs-lookup"><span data-stu-id="023cd-135">The [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) interface has the following uses.</span></span>

-   <span data-ttu-id="023cd-136">裝載服務物件。</span><span class="sxs-lookup"><span data-stu-id="023cd-136">Hosts service objects.</span></span>
-   <span data-ttu-id="023cd-137">使用 WS 探索宣佈網路上有裝置主機存在。</span><span class="sxs-lookup"><span data-stu-id="023cd-137">Announces the presence of a device host on the network using WS-Discovery.</span></span>
-   <span data-ttu-id="023cd-138">回應 WS-MetadataExchange 要求，並描述託管服務的類型和位置。</span><span class="sxs-lookup"><span data-stu-id="023cd-138">Responds to WS-MetadataExchange requests and describes the types and locations of hosted services.</span></span>
-   <span data-ttu-id="023cd-139">將網路要求分派至服務物件。</span><span class="sxs-lookup"><span data-stu-id="023cd-139">Dispatches network requests into service objects.</span></span>

<span data-ttu-id="023cd-140">WS-MANAGEMENT、透過 ws-metadataexchange 和 WS-Eventing 訂用帳戶管理功能完全是在裝置主機物件內處理。</span><span class="sxs-lookup"><span data-stu-id="023cd-140">WS-Discovery, WS-MetadataExchange, and WS-Eventing subscription management functionality is handled entirely within the device host object.</span></span> <span data-ttu-id="023cd-141">必須符合下列需求，才能在裝置主機內託管服務。</span><span class="sxs-lookup"><span data-stu-id="023cd-141">Before a service can be hosted inside a device host, the following requirements must be met.</span></span>

-   <span data-ttu-id="023cd-142">主機必須藉由呼叫 [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost)來建立。</span><span class="sxs-lookup"><span data-stu-id="023cd-142">The host must be created by calling [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).</span></span>
-   <span data-ttu-id="023cd-143">與服務相關聯的中繼資料必須註冊。</span><span class="sxs-lookup"><span data-stu-id="023cd-143">The metadata associated with the service must be registered.</span></span>
-   <span data-ttu-id="023cd-144">服務本身必須註冊。</span><span class="sxs-lookup"><span data-stu-id="023cd-144">The service itself must be registered.</span></span>
-   <span data-ttu-id="023cd-145">裝置主機必須啟動。</span><span class="sxs-lookup"><span data-stu-id="023cd-145">The device host must be started.</span></span>

<span data-ttu-id="023cd-146">[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)物件通常是在 [WsdCodeGen](web-services-for-devices-code-generator.md)所產生的程式碼內建立和使用。</span><span class="sxs-lookup"><span data-stu-id="023cd-146">The [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) object is typically created and used inside code generated by [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span>

 

 
