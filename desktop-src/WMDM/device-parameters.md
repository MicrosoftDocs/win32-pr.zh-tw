---
title: 裝置參數
description: 裝置參數
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media 裝置管理員、裝置參數
- 裝置管理員，裝置參數
- 程式設計指南，裝置參數
- 服務提供者，裝置參數
- 建立服務提供者，裝置參數
- 裝置參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300607"
---
# <a name="device-parameters"></a><span data-ttu-id="eef62-109">裝置參數</span><span class="sxs-lookup"><span data-stu-id="eef62-109">Device Parameters</span></span>

<span data-ttu-id="eef62-110">Windows Media 裝置管理員使用裝置參數來控制裝置的行為。</span><span class="sxs-lookup"><span data-stu-id="eef62-110">Windows Media Device Manager uses device parameters to control the behavior of a device.</span></span> <span data-ttu-id="eef62-111">這些參數會依照裝置的安裝檔案中指定的方式新增至登錄， (INF 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="eef62-111">These parameters are added to the registry as specified in the device's installation file (INF file).</span></span> <span data-ttu-id="eef62-112">下表列出 Windows Media 裝置管理員查詢的裝置參數。</span><span class="sxs-lookup"><span data-stu-id="eef62-112">The following table lists the device parameters that Windows Media Device Manager queries.</span></span>



| <span data-ttu-id="eef62-113">裝置參數名稱</span><span class="sxs-lookup"><span data-stu-id="eef62-113">Device parameter name</span></span> | <span data-ttu-id="eef62-114">登錄資料類型</span><span class="sxs-lookup"><span data-stu-id="eef62-114">Registry data type</span></span> | <span data-ttu-id="eef62-115">Description</span><span class="sxs-lookup"><span data-stu-id="eef62-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef62-116">*WMDMSPCLSID*</span><span class="sxs-lookup"><span data-stu-id="eef62-116">*WMDMSPCLSID*</span></span>         | <span data-ttu-id="eef62-117">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="eef62-117">**REG\_SZ**</span></span>        | <span data-ttu-id="eef62-118">值，指定控制此裝置的服務提供者 CLSID。</span><span class="sxs-lookup"><span data-stu-id="eef62-118">Value that specifies the CLSID of the service provider controlling this device.</span></span> <span data-ttu-id="eef62-119">此參數是 PnP 支援的必要參數。</span><span class="sxs-lookup"><span data-stu-id="eef62-119">This parameter is mandatory for PnP support.</span></span><br/> <span data-ttu-id="eef62-120">參數值必須是 CLSID，而不是服務提供者的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="eef62-120">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span> <span data-ttu-id="eef62-121">此參數是在 Windows Media 裝置管理員下支援隨插即用 (PnP) 的必要參數。</span><span class="sxs-lookup"><span data-stu-id="eef62-121">This parameter is mandatory to support Plug and Play (PnP) under Windows Media Device Manager.</span></span> <span data-ttu-id="eef62-122">如需詳細資訊，請參閱 [為裝置啟用 PnP](enabling-pnp-for-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="eef62-122">For more information, see [Enabling PnP for Devices](enabling-pnp-for-devices.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="eef62-123">*OptimalTransferSize*</span><span class="sxs-lookup"><span data-stu-id="eef62-123">*OptimalTransferSize*</span></span> | <span data-ttu-id="eef62-124">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eef62-124">**REG\_DWORD**</span></span>     | <span data-ttu-id="eef62-125">選擇性值，指定 Windows Media 裝置管理員在讀取和寫入作業期間使用的慣用傳輸大小。</span><span class="sxs-lookup"><span data-stu-id="eef62-125">Optional value that specifies the preferred transfer size that Windows Media Device Manager uses during read and write operations.</span></span> <span data-ttu-id="eef62-126">如果未提供，則會使用預設的傳輸大小。</span><span class="sxs-lookup"><span data-stu-id="eef62-126">If it is not supplied, a default transfer size is used.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="eef62-127">*UseMetadataViews*</span><span class="sxs-lookup"><span data-stu-id="eef62-127">*UseMetadataViews*</span></span>    | <span data-ttu-id="eef62-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eef62-128">**REG\_DWORD**</span></span>     | <span data-ttu-id="eef62-129">選擇性參數，指定 Windows Media 裝置管理員在將裝置內容呈現給應用程式時，是否以中繼資料來組織內容。</span><span class="sxs-lookup"><span data-stu-id="eef62-129">Optional parameter that specifies whether Windows Media Device Manager organizes the content by metadata while presenting device content to applications.</span></span> <span data-ttu-id="eef62-130">若未指定，預設值是 0。</span><span class="sxs-lookup"><span data-stu-id="eef62-130">If not specified, the default value is 0.</span></span><br/> <span data-ttu-id="eef62-131">當應用程式列舉便攜音訊播放程式之存儲的內容時，Windows Media 裝置管理員可以呈現以中繼資料組織的內容。</span><span class="sxs-lookup"><span data-stu-id="eef62-131">When applications enumerate the content on the storages of a portable audio player, Windows Media Device Manager can present the content organized by metadata.</span></span> <span data-ttu-id="eef62-132">這特別適用于具有大型儲存體容量的裝置。</span><span class="sxs-lookup"><span data-stu-id="eef62-132">This is especially useful for devices with large storage capacity.</span></span><br/> <span data-ttu-id="eef62-133">應用程式和裝置能夠控制此行為。</span><span class="sxs-lookup"><span data-stu-id="eef62-133">Applications and devices have the ability to control this behavior.</span></span> <span data-ttu-id="eef62-134">裝置會透過裝置參數 *UseMetadataViews* 來指出其喜好設定。</span><span class="sxs-lookup"><span data-stu-id="eef62-134">Devices indicate their preference through the device parameter *UseMetadataViews*.</span></span><br/> <span data-ttu-id="eef62-135">以下是支援的兩個整數值：</span><span class="sxs-lookup"><span data-stu-id="eef62-135">The following two integer values are supported:</span></span><br/> <span data-ttu-id="eef62-136">要求在裝置的檔案系統上，將內容呈現給應用程式的方式完全相同。</span><span class="sxs-lookup"><span data-stu-id="eef62-136">Requests that content be presented to the applications exactly as organized on the file system of the device.</span></span><br/> <span data-ttu-id="eef62-137">要求將內容呈現給以中繼資料組織的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eef62-137">Requests that the content be presented to the applications organized by metadata.</span></span><br/> |
| <span data-ttu-id="eef62-138">*ShowInShell*</span><span class="sxs-lookup"><span data-stu-id="eef62-138">*ShowInShell*</span></span>         | <span data-ttu-id="eef62-139">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eef62-139">**REG\_DWORD**</span></span>     | <span data-ttu-id="eef62-140">選擇性參數，指定裝置是否應該出現在 Windows 檔案總管中。</span><span class="sxs-lookup"><span data-stu-id="eef62-140">Optional parameter that specifies whether the device should appear in Windows Explorer.</span></span> <span data-ttu-id="eef62-141">值1表示裝置應該會出現在 Windows 檔案總管中。</span><span class="sxs-lookup"><span data-stu-id="eef62-141">The value 1 indicates that the device should appear in Windows Explorer.</span></span> <span data-ttu-id="eef62-142">如需詳細資訊，請參閱 [便攜音訊播放機的需求會出現在 Windows 檔案總管中](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)。</span><span class="sxs-lookup"><span data-stu-id="eef62-142">For more information, see [Requirements for Portable Audio Players to Appear in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="eef62-143">*UseExtendedWmdm*</span><span class="sxs-lookup"><span data-stu-id="eef62-143">*UseExtendedWmdm*</span></span>     | <span data-ttu-id="eef62-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eef62-144">**REG\_DWORD**</span></span>     | <span data-ttu-id="eef62-145">選擇性參數，會警示 Windows Media 裝置管理員服務提供者支援 **IMDSPDevice3**、 **IMDSPObject2** 和 **IMDSPStorage4**。</span><span class="sxs-lookup"><span data-stu-id="eef62-145">Optional parameter that alerts Windows Media Device Manager that the service provider supports **IMDSPDevice3**, **IMDSPObject2**, and **IMDSPStorage4**.</span></span> <span data-ttu-id="eef62-146">如果沒有此旗標，Windows Media 裝置管理員將永遠不會呼叫這些介面。</span><span class="sxs-lookup"><span data-stu-id="eef62-146">Without this flag, Windows Media Device Manager will never call these interfaces.</span></span> <span data-ttu-id="eef62-147">值1表示支援這些介面。</span><span class="sxs-lookup"><span data-stu-id="eef62-147">The value 1 indicates that these interfaces are supported.</span></span><br/> <span data-ttu-id="eef62-148">與 Windows Media Player 同步處理的服務提供者需要此旗標。</span><span class="sxs-lookup"><span data-stu-id="eef62-148">This flag is required for service providers that synchronize with Windows Media Player.</span></span> <span data-ttu-id="eef62-149"> (參閱 [啟用與 Windows Media Player) 的同步處理](enabling-synchronization-with-windows-media-player.md) 。</span><span class="sxs-lookup"><span data-stu-id="eef62-149">(See [Enabling Synchronization with Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="eef62-150">**編碼 INF 檔案**</span><span class="sxs-lookup"><span data-stu-id="eef62-150">**Coding the INF file**</span></span>

<span data-ttu-id="eef62-151">下列來自裝置 INF 檔案的範例程式碼示範如何在裝置安裝期間設定某些裝置參數。</span><span class="sxs-lookup"><span data-stu-id="eef62-151">The following example code from a device's INF file demonstrates setting some device parameters during device installation.</span></span>


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a><span data-ttu-id="eef62-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="eef62-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eef62-153">**建立服務提供者**</span><span class="sxs-lookup"><span data-stu-id="eef62-153">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="eef62-154">**IMDServiceProvider2 介面**</span><span class="sxs-lookup"><span data-stu-id="eef62-154">**IMDServiceProvider2 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[<span data-ttu-id="eef62-155">**IMDServiceProvider2::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="eef62-155">**IMDServiceProvider2::CreateDevice**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[<span data-ttu-id="eef62-156">**IWMDMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="eef62-156">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





