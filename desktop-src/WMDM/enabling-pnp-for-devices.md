---
title: 啟用裝置的 PnP
description: 啟用裝置的 PnP
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media 裝置管理員、PnP 裝置
- 裝置管理員，PnP 裝置
- 程式設計指南，PnP 裝置
- 服務提供者、PnP 裝置
- 建立服務提供者，PnP 裝置
- PnP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839775"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="98a3b-109">啟用裝置的 PnP</span><span class="sxs-lookup"><span data-stu-id="98a3b-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="98a3b-110">Windows Media 裝置管理員可監視通告便攜音訊播放機裝置介面之裝置的抵達和移除通知。</span><span class="sxs-lookup"><span data-stu-id="98a3b-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="98a3b-111">在這類裝置抵達時，Windows Media 裝置管理員會查詢名為 *WMDMSPCLSID* 的裝置參數，以取得負責此裝置之服務提供者的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="98a3b-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="98a3b-112">Windows Media 裝置管理員會在此服務提供者上呼叫 [**IMDServiceProvider2：： CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) 來建立裝置物件，該物件會以 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 物件的形式公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="98a3b-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="98a3b-113">服務提供者可以處理 PnP 裝置或非 PnP 裝置;它無法處理這兩種類型。</span><span class="sxs-lookup"><span data-stu-id="98a3b-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="98a3b-114">若要讓裝置使用上述機制 (並因此啟用 Windows Media 裝置管理員應用程式) 下裝置的抵達和移除通知，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="98a3b-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="98a3b-115">此裝置的設備磁碟機必須通告 Windows Media 裝置管理員便攜音訊播放機裝置介面。</span><span class="sxs-lookup"><span data-stu-id="98a3b-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="98a3b-116">此裝置介面的 GUID 定義如下：</span><span class="sxs-lookup"><span data-stu-id="98a3b-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="98a3b-117">如果裝置通告磁片區介面 (定義為 \_) winioctl 中的 VolumeClassGuid 或 GUID DEVINTERFACE 磁片區，則裝置不應通告此介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="98a3b-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="98a3b-118">如果裝置通告磁片區介面，則在 Windows Media 裝置管理員下，它已啟用 PnP。</span><span class="sxs-lookup"><span data-stu-id="98a3b-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="98a3b-119">-AND/OR-</span><span class="sxs-lookup"><span data-stu-id="98a3b-119">-AND/OR-</span></span>

    <span data-ttu-id="98a3b-120">您必須在子機碼 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Media 裝置管理員 \\ KnownDevices 中建立服務提供者的新登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="98a3b-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="98a3b-121">此金鑰應該有您服務提供者的名稱，而且必須具有下列兩個 Reg \_ SZ 值專案：</span><span class="sxs-lookup"><span data-stu-id="98a3b-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="98a3b-122">裝置必須具有名為 WMDMSPCLSID 的裝置參數。</span><span class="sxs-lookup"><span data-stu-id="98a3b-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="98a3b-123">此參數的值應該設定為字串形式的服務提供者 CLSID。</span><span class="sxs-lookup"><span data-stu-id="98a3b-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="98a3b-124">如需裝置參數的詳細資訊，請參閱 [裝置參數](device-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="98a3b-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="98a3b-125">參數值必須是 CLSID，而不是服務提供者的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="98a3b-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="98a3b-126">此裝置的服務提供者必須執行 IMDServiceProvider2 介面。</span><span class="sxs-lookup"><span data-stu-id="98a3b-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="98a3b-127">HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media 裝置管理員外掛程式 SP sp 名稱下的服務提供者金鑰 \\ \\ \\ 必須包含下列 DWORD 值</span><span class="sxs-lookup"><span data-stu-id="98a3b-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="98a3b-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="98a3b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a3b-129">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="98a3b-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




