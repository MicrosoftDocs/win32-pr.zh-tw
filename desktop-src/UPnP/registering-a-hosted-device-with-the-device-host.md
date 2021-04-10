---
title: 向裝置主機註冊託管裝置
description: 註冊託管裝置表示提供裝置描述及其裝置控制物件給裝置主機。
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a607af4f6ada359a9ee32e98e416d8271fd502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183427"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a><span data-ttu-id="b9a3d-103">向裝置主機註冊託管裝置</span><span class="sxs-lookup"><span data-stu-id="b9a3d-103">Registering a Hosted Device With the Device Host</span></span>

<span data-ttu-id="b9a3d-104">註冊託管裝置表示提供裝置描述及其裝置控制物件給裝置主機。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-104">Registering a hosted device means providing the device host with the device description and its device control object.</span></span> <span data-ttu-id="b9a3d-105">然後，裝置主機會使用 UPnP 探索通訊協定來建立完整的 UPnP 裝置描述、發佈它，並在網路上公佈裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-105">The device host then constructs a complete UPnP device description, publishes it, and announces the device on the network using the UPnP discovery protocol.</span></span> <span data-ttu-id="b9a3d-106">一旦發佈裝置之後，就可以使用它來控制點。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-106">Once a device is published, it is available to control points.</span></span>

<span data-ttu-id="b9a3d-107">裝置的註冊方式有兩種：</span><span class="sxs-lookup"><span data-stu-id="b9a3d-107">Devices are registered in two ways:</span></span>

-   <span data-ttu-id="b9a3d-108">應用程式會建立裝置控制物件的實例，並將其指標傳遞至裝置主機。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-108">An application creates an instance of the device control object and passes a pointer to it to the device host.</span></span>
-   <span data-ttu-id="b9a3d-109">應用程式會將已註冊裝置控制物件的 ProgID 傳遞給裝置主機。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-109">The application passes the ProgID for a registered device control object to the device host.</span></span> <span data-ttu-id="b9a3d-110">裝置主機在接收裝置的第一個要求時，會將它具現化。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-110">The device host instantiates it when the device host receives the first request for the device.</span></span>

<span data-ttu-id="b9a3d-111">無論使用哪種方法，裝置主機都會在註冊後立即發佈並公告裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-111">Regardless of which method is used, the device host publishes and announces the device as soon as it is registered.</span></span> <span data-ttu-id="b9a3d-112">這兩種方法之間的差異與載入裝置程式碼的方式不同。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-112">The difference between the two approaches has to do with when the device code is loaded.</span></span> <span data-ttu-id="b9a3d-113">當應用程式傳入裝置控制物件的指標時，裝置程式碼會在註冊時載入並執行。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-113">When the application passes in a pointer to the device control object, the device code is loaded and running at the time of registration.</span></span> <span data-ttu-id="b9a3d-114">當應用程式傳遞 ProgID 時，只會在叫用動作、查詢屬性或事件訂閱要求時載入裝置程式碼。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-114">When the application passes a ProgID, the device code is only loaded when an action is invoked, a property is queried, or an event subscription request arrives.</span></span> <span data-ttu-id="b9a3d-115">第二種方法會稍微提高效率。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-115">The second approach is slightly more efficient.</span></span> <span data-ttu-id="b9a3d-116">不過，它不適用於必須在任何控制項或事件訂用帳戶要求抵達之前執行的裝置，因為使用此方法時，只會在需要時才建立裝置控制物件。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-116">However, it is not suitable for devices that must be running before any control or event subscription requests arrive, because using this approach, device control objects are only created when they are needed.</span></span> <span data-ttu-id="b9a3d-117">第二種方法也可能會在收到裝置類型的第一個要求時產生效能問題。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-117">This second method can also create performance issues when it receives the first request for a device type.</span></span>

<span data-ttu-id="b9a3d-118">如果您想要確保在電腦啟動時，網路上的裝置主機會自動宣告裝置，請叫用 [**IUPnPRegistrar：： >registerdevice.js**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-118">If you want to ensure that a device is announced by the device host on the network automatically when the computer is started, invoke [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice).</span></span> <span data-ttu-id="b9a3d-119">**>registerdevice.js** 可確保只有在收到控制項或事件訂閱要求時，才會載入您的裝置程式碼。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-119">**RegisterDevice** ensures that your device code is only loaded when a control or event subscription request is received.</span></span>

<span data-ttu-id="b9a3d-120">如果您的裝置是暫時性或橋接，請叫用 [**IUPnPRegistrar：： RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)，當電腦重新開機時，不會自動重新通告裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-120">If your devices are transient or bridged, invoke [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), and the device is not automatically re-advertised when the computer is restarted.</span></span>

## <a name="discovery-announcement-lifetime"></a><span data-ttu-id="b9a3d-121">探索公告存留期</span><span class="sxs-lookup"><span data-stu-id="b9a3d-121">Discovery Announcement Lifetime</span></span>

<span data-ttu-id="b9a3d-122">裝置主機所註冊的每個裝置都會與存留期相關聯，該存留期是由裝置在註冊時所指定。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-122">Each device registered with the device host is associated with a lifetime, which is specified by the device upon registration.</span></span> <span data-ttu-id="b9a3d-123">裝置的存留期是裝置的探索宣告有效的時間。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-123">The lifetime of the device is the period of time for which the device's discovery announcements are valid.</span></span> <span data-ttu-id="b9a3d-124">存留期會以首次探索宣告中的標頭形式傳遞至控制點。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-124">The lifetime is passed to the control point as a header in the initial discovery announcement.</span></span> <span data-ttu-id="b9a3d-125">裝置主機會在到期時間之前自動更新公告。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-125">The device host automatically refreshes the announcement prior to the expiration time.</span></span> <span data-ttu-id="b9a3d-126">探索公告存留期的值應該是15分鐘或更多 (預設值為30分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-126">The values of the discovery announcement lifetime should be 15 minutes or more (the default is 30 minutes).</span></span>

## <a name="device-identifiers-created-at-registration"></a><span data-ttu-id="b9a3d-127">註冊時建立的裝置識別碼</span><span class="sxs-lookup"><span data-stu-id="b9a3d-127">Device Identifiers Created at Registration</span></span>

<span data-ttu-id="b9a3d-128">建立裝置描述範本時，裝置開發人員必須提供服務描述的資源路徑和相關聯的圖示。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-128">When creating a device description template, the device developer must provide the resource path to the service description and associated icons.</span></span> <span data-ttu-id="b9a3d-129">資源路徑是由裝置應用程式所決定。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-129">The resource path is determined by the device application.</span></span>

<span data-ttu-id="b9a3d-130">由於相同的裝置可以在同一部電腦上多次註冊，因此裝置描述範本中指定的 UDN 不足以唯一識別裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-130">Since the same device can be registered multiple times on the same computer, the UDN specified in the device description template is not sufficient to uniquely identify a device.</span></span> <span data-ttu-id="b9a3d-131">因此，裝置在註冊後，裝置主機會建立裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-131">Therefore, when a device is registered, the device host creates a device identifier.</span></span> <span data-ttu-id="b9a3d-132">此裝置識別碼與裝置描述範本中的 UDN 相關，可以用來唯一識別裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-132">This device identifier, in association with the UDN in the device description template, can be used to uniquely identify a device.</span></span>

<span data-ttu-id="b9a3d-133">當裝置暫時取消註冊，然後重新註冊時，也會使用此識別碼。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-133">This identifier is also used when the device is temporarily unregistered and then re-registered.</span></span> <span data-ttu-id="b9a3d-134">當裝置暫時取消註冊時，裝置主機不會刪除 UDN。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-134">When a device is unregistered temporarily, the device host does not delete the UDN.</span></span> <span data-ttu-id="b9a3d-135">未刪除 UDN 的原因包括：</span><span class="sxs-lookup"><span data-stu-id="b9a3d-135">Reasons for not deleting the UDN include:</span></span>

-   <span data-ttu-id="b9a3d-136">正在升級裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-136">The device is being upgraded.</span></span>
-   <span data-ttu-id="b9a3d-137">您正在變更裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-137">You are changing the properties of the device.</span></span>
-   <span data-ttu-id="b9a3d-138">服務暫時無法使用。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-138">A service is temporarily unavailable.</span></span>
-   <span data-ttu-id="b9a3d-139">您正在將新的服務新增至裝置。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-139">You are adding a new service to a device.</span></span>
-   <span data-ttu-id="b9a3d-140">您正在更新 DLL。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-140">You are updating the DLL.</span></span>
-   <span data-ttu-id="b9a3d-141">裝置處於待命模式。</span><span class="sxs-lookup"><span data-stu-id="b9a3d-141">The device is in stand-by mode.</span></span>

<span data-ttu-id="b9a3d-142">如需註冊的詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="b9a3d-142">Refer to the following sections for further information on registration:</span></span>

-   [<span data-ttu-id="b9a3d-143">如何向裝置主機註冊裝置</span><span class="sxs-lookup"><span data-stu-id="b9a3d-143">How to Register a Device with the Device Host</span></span>](how-to-register-a-device-with-the-device-host.md)
-   [<span data-ttu-id="b9a3d-144">取消註冊裝置</span><span class="sxs-lookup"><span data-stu-id="b9a3d-144">Unregistering a Device</span></span>](unregistering-a-device.md)
-   [<span data-ttu-id="b9a3d-145">**IUPnPRegistrar::UnregisterDevice**</span><span class="sxs-lookup"><span data-stu-id="b9a3d-145">**IUPnPRegistrar::UnregisterDevice**</span></span>](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [<span data-ttu-id="b9a3d-146">**IUPnPReregistrar**</span><span class="sxs-lookup"><span data-stu-id="b9a3d-146">**IUPnPReregistrar**</span></span>](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




