---
title: 透過 IWMDMDevice 取得格式功能
description: 在僅支援 IWMDMDevice 的裝置上取得格式功能
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media 裝置管理員，裝置功能
- 裝置管理員，裝置功能
- 程式設計指南，裝置功能
- 桌面應用程式，裝置功能
- 建立 Windows Media 裝置管理員應用程式，裝置功能
- 將檔案寫入裝置、裝置功能
- IWMDMDevice 方法
- Windows Media 裝置管理員，IWMDMDevice 方法
- 裝置管理員，IWMDMDevice 方法
- 程式設計手冊，IWMDMDevice 方法
- 桌面應用程式，IWMDMDevice 方法
- 建立 Windows Media 裝置管理員應用程式，IWMDMDevice 方法
- 將檔案寫入裝置，IWMDMDevice 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313845"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a><span data-ttu-id="534f6-116">透過 IWMDMDevice 取得格式功能</span><span class="sxs-lookup"><span data-stu-id="534f6-116">Getting format capabilities through IWMDMDevice</span></span>

<span data-ttu-id="534f6-117">查詢裝置的播放功能的建議方法是 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。</span><span class="sxs-lookup"><span data-stu-id="534f6-117">The recommended method for querying a device for its playback capabilities is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="534f6-118">但是，如果裝置不支援此方法，則應用程式會改為呼叫 [**IWMDMDevice：： GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) ，將支援的音訊格式陣列以 [**\_ WAVEFORMATEX**](-waveformatex.md)結構和 MIME 格式，從裝置取出為字串。</span><span class="sxs-lookup"><span data-stu-id="534f6-118">However, if a device does not support this method, the application instead can call [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) to retrieve an array of supported audio formats as [**\_WAVEFORMATEX**](-waveformatex.md) structures and MIME formats as strings from the device.</span></span>

<span data-ttu-id="534f6-119">下列步驟顯示應用程式如何使用此方法來查詢裝置以取得支援的格式：</span><span class="sxs-lookup"><span data-stu-id="534f6-119">The following steps show how an application can use this method to query a device for supported formats:</span></span>

1.  <span data-ttu-id="534f6-120">呼叫 **GetFormatSupport** 可取出音訊和 mime 格式的陣列。</span><span class="sxs-lookup"><span data-stu-id="534f6-120">Call **GetFormatSupport** to retrieve arrays of both audio and mime formats.</span></span>
2.  <span data-ttu-id="534f6-121">對抓取的音訊格式執行迴圈，並檢查每個 [**\_ WAVEFORMATEX**](-waveformatex.md)結構，以嘗試尋找可接受的音訊格式</span><span class="sxs-lookup"><span data-stu-id="534f6-121">Loop through the retrieved audio formats and examine each [**\_WAVEFORMATEX**](-waveformatex.md) structure to try to find an acceptable audio format</span></span>
3.  <span data-ttu-id="534f6-122">如果需要) 尋找可接受的檔案類型，請在已取出的 MIME 格式字串之間執行迴圈 (。</span><span class="sxs-lookup"><span data-stu-id="534f6-122">Loop through the retrieved MIME format strings (if desired) to find an acceptable file type.</span></span> <span data-ttu-id="534f6-123">SDK 不會定義 MIME 格式的常數;您應使用業界標準值 (可在 iana.org 網站) 找到。</span><span class="sxs-lookup"><span data-stu-id="534f6-123">The SDK does not define constants for MIME formats; you should use industry standard values (which can be found at the iana.org Web site).</span></span> <span data-ttu-id="534f6-124">裝置應該會列出它所支援的特定 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="534f6-124">A device should list the specific MIME types that it supports.</span></span>

<span data-ttu-id="534f6-125">下列 c + + 程式碼示範如何使用 **GetFormatSupport** 從裝置上取出格式功能。</span><span class="sxs-lookup"><span data-stu-id="534f6-125">The following C++ code demonstrates retrieving format capabilities from a device, using **GetFormatSupport**.</span></span>


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="534f6-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="534f6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="534f6-127">**探索裝置格式功能**</span><span class="sxs-lookup"><span data-stu-id="534f6-127">**Discovering Device Format Capabilities**</span></span>](discovering-device-format-capabilities.md)
</dt> <dt>

[<span data-ttu-id="534f6-128">**在支援 IWMDMDevice3 的裝置上取得格式功能**</span><span class="sxs-lookup"><span data-stu-id="534f6-128">**Getting Format Capabilities on Devices That Support IWMDMDevice3**</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




