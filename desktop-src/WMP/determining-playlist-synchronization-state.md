---
title: 判斷播放清單同步處理狀態
description: 判斷播放清單同步處理狀態
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Windows Media Player，同步播放清單
- Windows Media Player 物件模型，同步播放清單
- 物件模型，同步處理播放清單
- Windows Media Player 行動裝置、同步播放清單
- Windows Media Player ActiveX 控制項，同步播放清單
- Windows Media Player 的行動 ActiveX 控制項、同步播放清單
- ActiveX 控制項，同步播放清單
- 播放清單，同步處理
- 中繼檔播放清單，同步處理
- Windows Media 中繼檔播放清單，同步處理
- 可攜式裝置，判斷同步播放清單的狀態
- 同步播放清單，同步處理狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106996362"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="4c399-115">判斷播放清單同步處理狀態</span><span class="sxs-lookup"><span data-stu-id="4c399-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="4c399-116">Windows Media Player 10 或更新版本會使用 **SyncState** 屬性來包含特定數位媒體檔案是否已複製到可攜式裝置的相關資訊，以及是否因為裝置沒有足夠的記憶體而導致複製失敗的情況。</span><span class="sxs-lookup"><span data-stu-id="4c399-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="4c399-117">下列程式碼範例會建立函式，此函式會從數位媒體檔案抓取此資訊。</span><span class="sxs-lookup"><span data-stu-id="4c399-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="4c399-118">函數會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="4c399-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="4c399-119">*pMedia*。</span><span class="sxs-lookup"><span data-stu-id="4c399-119">*pMedia*.</span></span> <span data-ttu-id="4c399-120">**IWMPMedia** 介面的指標，代表要檢查的數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="4c399-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="4c399-121">*lPsIndex*。</span><span class="sxs-lookup"><span data-stu-id="4c399-121">*lPsIndex*.</span></span> <span data-ttu-id="4c399-122">目前裝置的合作關係索引。</span><span class="sxs-lookup"><span data-stu-id="4c399-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="4c399-123">*pulOnDevice*。</span><span class="sxs-lookup"><span data-stu-id="4c399-123">*pulOnDevice*.</span></span> <span data-ttu-id="4c399-124">**長** 變數的指標，此變數會接收指出數位媒體檔案是否已複製到裝置的值。</span><span class="sxs-lookup"><span data-stu-id="4c399-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="4c399-125">*pulDidNotFit*。</span><span class="sxs-lookup"><span data-stu-id="4c399-125">*pulDidNotFit*.</span></span> <span data-ttu-id="4c399-126">**長** 變數的指標，此變數會接收值，指出複製作業是否因為裝置沒有足夠的記憶體而失敗。</span><span class="sxs-lookup"><span data-stu-id="4c399-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="4c399-127">**SyncState** 屬性中包含的資訊是以位方式編碼。</span><span class="sxs-lookup"><span data-stu-id="4c399-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="4c399-128">您可以在 [列舉媒體專案](enumerating-the-media-items.md)的範例程式碼中看到此函式的使用方式。</span><span class="sxs-lookup"><span data-stu-id="4c399-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4c399-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c399-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c399-130">**IWMPMedia 介面**</span><span class="sxs-lookup"><span data-stu-id="4c399-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="4c399-131">**IWMPMedia3::getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="4c399-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="4c399-132">**管理同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="4c399-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="4c399-133">**SyncState 屬性**</span><span class="sxs-lookup"><span data-stu-id="4c399-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




