---
title: " (WMDM) 列舉裝置"
description: 列舉裝置
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media 裝置管理員，列舉裝置
- 裝置管理員，列舉裝置
- 程式設計指南，列舉裝置
- 服務提供者，列舉裝置
- 建立服務提供者，列舉裝置
- 列舉裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "103679235"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="1b74b-109"> (WMDM) 列舉裝置</span><span class="sxs-lookup"><span data-stu-id="1b74b-109">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="1b74b-110">當 Windows Media 裝置管理員應用程式啟動、隨插即用 (PnP) 裝置連線或中斷連線，或應用程式呼叫 [**IWMDeviceManager2：：重新初始化**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize)時，windows media 裝置管理員會維護已連線裝置的快取。</span><span class="sxs-lookup"><span data-stu-id="1b74b-110">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="1b74b-111">當應用程式呼叫 [**IWMDeviceManager：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) 或 [**IWMDeviceManager2：： EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)時，此快取會公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b74b-111">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="1b74b-112">每個裝置都會以 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 介面的形式公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b74b-112">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="1b74b-113">如果已註冊服務提供者來處理 PnP 裝置，Windows Media 裝置管理員將會察覺目前連線的裝置清單。</span><span class="sxs-lookup"><span data-stu-id="1b74b-113">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="1b74b-114">如果服務提供者已註冊來處理非 PnP 裝置，則服務提供者負責探索連接的裝置。</span><span class="sxs-lookup"><span data-stu-id="1b74b-114">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="1b74b-115">服務提供者只能針對 PnP 或非 PnP 裝置註冊，且不能同時註冊。</span><span class="sxs-lookup"><span data-stu-id="1b74b-115">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="1b74b-116">下列動作顯示 Windows Media 裝置管理員如何維護或更新其快取。</span><span class="sxs-lookup"><span data-stu-id="1b74b-116">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="1b74b-117">請注意，當非 PnP 裝置連接或中斷連線時，快取永遠不會更新。</span><span class="sxs-lookup"><span data-stu-id="1b74b-117">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="1b74b-118">Windows Media 裝置管理員應用程式啟動</span><span class="sxs-lookup"><span data-stu-id="1b74b-118">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="1b74b-119">Windows Media 裝置管理員從 PnP 子系統抓取附加的 PnP 裝置清單，並在為每個連線裝置註冊的 SP 上呼叫 [**IMDServiceProvider2：： CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) 。</span><span class="sxs-lookup"><span data-stu-id="1b74b-119">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="1b74b-120"> (它會藉由查詢負責此裝置之服務提供者類別識別碼的 WMDMSPCLSID 裝置參數，來探索正確的服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1b74b-120">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="1b74b-121">如需詳細資訊，請參閱 [裝置參數](device-parameters.md) 。 ) 所有傳回的裝置都會新增至 Windows Media 裝置管理員快取裝置。</span><span class="sxs-lookup"><span data-stu-id="1b74b-121">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="1b74b-122">Windows Media 裝置管理員會尋找所有註冊的非 PnP 服務提供者，並在每個服務提供者上呼叫 [**IMDServiceProvider：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) ，以取得每個服務提供者的清單裝置。</span><span class="sxs-lookup"><span data-stu-id="1b74b-122">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="1b74b-123">所有傳回的裝置都會新增至快取。</span><span class="sxs-lookup"><span data-stu-id="1b74b-123">All devices returned are added to the cache.</span></span>

<span data-ttu-id="1b74b-124">應用程式會呼叫 IWMDeviceManager/2：： EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="1b74b-124">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="1b74b-125">Windows Media 裝置管理員會傳回其快取的裝置清單。</span><span class="sxs-lookup"><span data-stu-id="1b74b-125">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="1b74b-126">PnP 裝置連接</span><span class="sxs-lookup"><span data-stu-id="1b74b-126">A PnP device connects</span></span>

-   <span data-ttu-id="1b74b-127">Windows Media 裝置管理員會尋找相關的服務提供者並呼叫 **IMDServiceProvider2：： CreateDevice**，並將裝置新增至其快取。</span><span class="sxs-lookup"><span data-stu-id="1b74b-127">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="1b74b-128">如果應用程式會執行 [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)，Windows Media 裝置管理員會呼叫 [**IWMDMNotification：： WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) 與抵達通知。</span><span class="sxs-lookup"><span data-stu-id="1b74b-128">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="1b74b-129">PnP 裝置中斷連線</span><span class="sxs-lookup"><span data-stu-id="1b74b-129">A PnP device disconnects</span></span>

-   <span data-ttu-id="1b74b-130">Windows Media 裝置管理員從其快取中移除專案。</span><span class="sxs-lookup"><span data-stu-id="1b74b-130">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="1b74b-131">如果應用程式執行 IWMDMNotification，Windows Media 裝置管理員會呼叫 IWMDMNotification：： WMDMMessage 與起飛通知。</span><span class="sxs-lookup"><span data-stu-id="1b74b-131">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="1b74b-132">應用程式會呼叫 IWMDeviceManager2：：重新初始化</span><span class="sxs-lookup"><span data-stu-id="1b74b-132">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="1b74b-133">重新整理所有已連線裝置的快取。</span><span class="sxs-lookup"><span data-stu-id="1b74b-133">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="1b74b-134">非 PnP 裝置連接或中斷連線</span><span class="sxs-lookup"><span data-stu-id="1b74b-134">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="1b74b-135">Windows Media 裝置管理員不會收到抵達或離開的通知，也不會採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="1b74b-135">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b74b-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b74b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b74b-137">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="1b74b-137">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




