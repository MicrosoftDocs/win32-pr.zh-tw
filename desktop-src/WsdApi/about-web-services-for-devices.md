---
description: 裝置上的 web 服務 API (WSDAPI) 是適用于 Web 服務的裝置設定檔 (DPWS) 適用于 Windows Vista 和 Windows Server 2008。
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: 關於裝置上的 Web 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca7f7dc97dabd3dde7af12f3cece992b4f0ef6d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "103853284"
---
# <a name="about-web-services-on-devices"></a><span data-ttu-id="f4a39-103">關於裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="f4a39-103">About Web Services on Devices</span></span>

<span data-ttu-id="f4a39-104">裝置上的 web 服務 API (WSDAPI) 是適用于 [Web 服務的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) 適用于 windows Vista 和 windows Server 2008。</span><span class="sxs-lookup"><span data-stu-id="f4a39-104">Web Service on Devices API (WSDAPI) is an implementation of the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) for Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f4a39-105">DPWS 會限制 Web 服務規格，讓用戶端可以輕鬆地探索裝置。</span><span class="sxs-lookup"><span data-stu-id="f4a39-105">The DPWS constrains Web Services specifications so clients can easily discover devices.</span></span> <span data-ttu-id="f4a39-106">探索到裝置之後，用戶端就可以取出該裝置上所裝載之服務的描述，並使用這些服務。</span><span class="sxs-lookup"><span data-stu-id="f4a39-106">Once a device is discovered, a client can retrieve a description of services hosted on that device and use those services.</span></span>

## <a name="devices-and-services"></a><span data-ttu-id="f4a39-107">裝置和服務</span><span class="sxs-lookup"><span data-stu-id="f4a39-107">Devices and Services</span></span>

<span data-ttu-id="f4a39-108">*裝置* 是連接到網路的元件，通常是硬體。</span><span class="sxs-lookup"><span data-stu-id="f4a39-108">*Devices* are components, usually hardware, which are attached to the network.</span></span> <span data-ttu-id="f4a39-109">範例包括印表機、網路攝影機和影片系統。</span><span class="sxs-lookup"><span data-stu-id="f4a39-109">Examples include printers, Web cameras, and video systems.</span></span>

<span data-ttu-id="f4a39-110">裝置可能包含零或多個 *服務*。</span><span class="sxs-lookup"><span data-stu-id="f4a39-110">Devices may include zero or more *services*.</span></span> <span data-ttu-id="f4a39-111">例如，影片裝置可能包含支援開啟和關閉電源、播放控制、媒體彈出和影片串流的服務。</span><span class="sxs-lookup"><span data-stu-id="f4a39-111">For example, a video device may include services that support power on and off, play control, media ejection, and video streaming.</span></span> <span data-ttu-id="f4a39-112">Play 控制項可能會支援播放、暫停、倒轉和向前快轉等動作。</span><span class="sxs-lookup"><span data-stu-id="f4a39-112">Play control may support actions such as play, pause, rewind, and fast forward.</span></span>

## <a name="discovering-and-manipulating-a-device"></a><span data-ttu-id="f4a39-113">探索和操作裝置</span><span class="sxs-lookup"><span data-stu-id="f4a39-113">Discovering and Manipulating a Device</span></span>

<span data-ttu-id="f4a39-114">WSDAPI 可讓用戶端透過網路探索及存取遠端裝置及其相關聯的服務，以擴充本機隨插即用模型。</span><span class="sxs-lookup"><span data-stu-id="f4a39-114">WSDAPI extends the local Plug and Play model by allowing a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="f4a39-115">它支援探索、單向和雙向控制訊息，以及事件。</span><span class="sxs-lookup"><span data-stu-id="f4a39-115">It supports discovery, one-way and two-way control messaging, and eventing.</span></span>

![此圖顯示 WSDAPI 如何讓用戶端探索及存取遠端裝置。](images/overview01.png)

<span data-ttu-id="f4a39-117">如果有任何) 使用唯一位址和一組標準化的 XML 訊息，DPWS 裝置就會宣佈其存在並公開服務 (。</span><span class="sxs-lookup"><span data-stu-id="f4a39-117">DPWS devices announce their presence and expose services (if any) using a unique address and a standardized set of XML messages.</span></span> <span data-ttu-id="f4a39-118">DPWS 用戶端可以使用探索程式來尋找裝置、列舉其服務，並連接到這些服務以執行特定動作。</span><span class="sxs-lookup"><span data-stu-id="f4a39-118">DPWS clients can use the discovery process to find the device, enumerate its services, and connect to those services to perform specific actions.</span></span>

<span data-ttu-id="f4a39-119">WSDAPI 用戶端會先查詢裝置以取得其服務的完整說明，包括服務類型 (例如印表機服務類型或掃描器服務類型) 。</span><span class="sxs-lookup"><span data-stu-id="f4a39-119">A WSDAPI client first queries the device for complete descriptions of its services, including the service types (such as a printer service type or a scanner service type).</span></span> <span data-ttu-id="f4a39-120">然後，用戶端會藉由呼叫服務類型所定義的命令來控制裝置 (例如，藉由在印表機服務類型為) 的裝置上呼叫 **CreatePrintJob** 。</span><span class="sxs-lookup"><span data-stu-id="f4a39-120">The client then controls the device by calling commands defined by a service type (for example, by calling **CreatePrintJob** on a device with a printer service type).</span></span> <span data-ttu-id="f4a39-121">此外，用戶端也可以藉由訂閱命令執行期間發生的事件，監視每個服務中的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="f4a39-121">Optionally, the client can also monitor state changes in each service by subscribing to events that occur during command execution.</span></span>

![顯示 WSDAPI 用戶端如何查詢和與裝置互動的圖表。](images/netdevice01.png)

<span data-ttu-id="f4a39-123">如需裝置訊息模式的詳細資訊，請參閱 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)。</span><span class="sxs-lookup"><span data-stu-id="f4a39-123">For more information about device messaging patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

## <a name="logical-and-physical-addressing"></a><span data-ttu-id="f4a39-124">邏輯與實體定址</span><span class="sxs-lookup"><span data-stu-id="f4a39-124">Logical and Physical Addressing</span></span>

<span data-ttu-id="f4a39-125">邏輯定址可用來唯一識別與實體位址無關的裝置。</span><span class="sxs-lookup"><span data-stu-id="f4a39-125">Logical addressing is used to uniquely identify devices independent of their physical addresses.</span></span> <span data-ttu-id="f4a39-126">WS-Discovery 提供了一種機制，可將邏輯位址解析成實體位址，讓用戶端對裝置的訊息得以進行。</span><span class="sxs-lookup"><span data-stu-id="f4a39-126">WS-Discovery provides a mechanism to resolve logical addresses into physical addresses, allowing client-to-device messaging to take place.</span></span> <span data-ttu-id="f4a39-127">例如，網路連接儲存體 (NAS) 與您一起攜帶。</span><span class="sxs-lookup"><span data-stu-id="f4a39-127">An example is network attached storage (NAS) that you carry with you.</span></span> <span data-ttu-id="f4a39-128">如果您有膝上型電腦和 NAS，則不論您是在子網之間移動 (IP 位址) 的實體位址為何，您的膝上型電腦都應該能夠辨識它是相同的裝置。</span><span class="sxs-lookup"><span data-stu-id="f4a39-128">If you have a laptop and a NAS, your laptop should be able to recognize that it is the same device, regardless of the physical address (IP address) that the NAS obtains as you move between subnets.</span></span> <span data-ttu-id="f4a39-129">完成此程式需要裝置具有與其取得的 IP 位址無關的身分識別;由於傳統的漫遊案例中無法使用 DNS 等傳統機制，因此 WS-Addressing 和 WS-Discovery 提供邏輯定址和解決方式作為臨機操作的替代方案。</span><span class="sxs-lookup"><span data-stu-id="f4a39-129">Accomplishing this requires the device have identity that is independent of the IP address it obtains; since traditional mechanisms like DNS are not available in a normal roaming scenario, WS-Addressing and WS-Discovery provide logical addressing and resolution as an ad-hoc alternative.</span></span>

<span data-ttu-id="f4a39-130">製造裝置時，會提供一個全域唯一識別碼，以 UUID URI 表示。</span><span class="sxs-lookup"><span data-stu-id="f4a39-130">When a device is manufactured, it is given a globally unique identifier, represented as a UUID URI.</span></span> <span data-ttu-id="f4a39-131">裝置的這個識別碼永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="f4a39-131">This identifier will never change for the device.</span></span> <span data-ttu-id="f4a39-132">裝置開啟電源時，一律會透過 WS-Discovery [Hello](hello-message.md) 訊息來宣告其邏輯位址，並接受將其轉換為實體位址的要求， (通常是透過 WS-Discovery [解析](resolve-message.md) 或 [探查](probe-message.md) 訊息的 HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="f4a39-132">When the device is powered on, it will always announce its logical address via a WS-Discovery [Hello](hello-message.md) message, and will accept requests to convert that to a physical address (typically HTTP) via WS-Discovery [Resolve](resolve-message.md) or [Probe](probe-message.md) messages.</span></span> <span data-ttu-id="f4a39-133">一旦取得有效的實體位址 (IP 位址) 取得之後，所有訊息都會在該位址上進行，而且只有在位址變更、裝置變更狀態和用戶端需要通知，或裝置離線時，才會使用 WS-Discovery。</span><span class="sxs-lookup"><span data-stu-id="f4a39-133">Once a valid physical address (IP address) is obtained, all messaging happens over that address, and WS-Discovery is used only if the address changes, the device changes state and the clients need to be notified, or the device goes offline.</span></span>

## <a name="building-applications"></a><span data-ttu-id="f4a39-134">建置應用程式</span><span class="sxs-lookup"><span data-stu-id="f4a39-134">Building Applications</span></span>

<span data-ttu-id="f4a39-135">WSDAPI 提供一般 DPWS SOAP 堆疊，供用戶端和服務應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="f4a39-135">WSDAPI provides a generic DPWS SOAP stack for use by client and service applications.</span></span> <span data-ttu-id="f4a39-136">[裝置上的 Web 服務程式碼](web-services-for-devices-code-generator.md)產生器 (WsdCodeGen.exe) 可用來將服務描述 (WSDL) 轉換成應用程式可直接呼叫的 proxy 和存根程式碼。</span><span class="sxs-lookup"><span data-stu-id="f4a39-136">The [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) can be used to convert a service description (WSDL) into proxy and stub code that applications can call directly.</span></span> <span data-ttu-id="f4a39-137">這個產生的程式碼會自動將函式呼叫和參數轉換成 SOAP 訊息和 XML 欄位，然後呼叫 WSDAPI 來發出對遠端裝置或用戶端的要求。</span><span class="sxs-lookup"><span data-stu-id="f4a39-137">This generated code automatically transforms function calls and parameters into SOAP messages and XML fields, and then calls into WSDAPI to issue to requests to the remote device or client.</span></span>

<span data-ttu-id="f4a39-138">建立 WSDAPI 應用程式來建立和啟動 PnP 傳回的函式實例時，可以使用函數探索。</span><span class="sxs-lookup"><span data-stu-id="f4a39-138">Function Discovery can be used when building WSDAPI applications to create and activate function instances returned by PnP.</span></span> <span data-ttu-id="f4a39-139">這些函式實例包含的資料，可以在只需要簡單探索時，透過 PnP Api 取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f4a39-139">These function instances contain data that can be used to obtain more information through the PnP APIs when more than just simple discovery is required.</span></span> <span data-ttu-id="f4a39-140">如需詳細資訊，請參閱函式 [探索](/previous-versions/windows/desktop/fundisc/fd-portal) 和 [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x)。</span><span class="sxs-lookup"><span data-stu-id="f4a39-140">For more information, see [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) and [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4a39-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4a39-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4a39-142">探索和中繼資料交換訊息模式</span><span class="sxs-lookup"><span data-stu-id="f4a39-142">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="f4a39-143">WSDAPI 規格合規性</span><span class="sxs-lookup"><span data-stu-id="f4a39-143">WSDAPI Specification Compliance</span></span>](wsdapi-specification-compliance.md)
</dt> <dt>

[<span data-ttu-id="f4a39-144">WSDAPI 介面的總覽</span><span class="sxs-lookup"><span data-stu-id="f4a39-144">Overview of the WSDAPI Interfaces</span></span>](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
