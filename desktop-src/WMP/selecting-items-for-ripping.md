---
title: 選取要進行翻錄的專案
description: 選取要進行翻錄的專案
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄，選取專案
- 將 Cd 翻錄，選取專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932347"
---
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="71395-112">選取要進行翻錄的專案</span><span class="sxs-lookup"><span data-stu-id="71395-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="71395-113">有時候使用者不會想要在 CD 上翻錄每個曲目。</span><span class="sxs-lookup"><span data-stu-id="71395-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="71395-114">Windows Media Player 提供介面來指定要針對翻錄選取的追蹤。</span><span class="sxs-lookup"><span data-stu-id="71395-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="71395-115">通常在 CD 翻錄應用程式中有一個使用者介面，可讓使用者在 CD 的曲目清單中選取核取方塊。</span><span class="sxs-lookup"><span data-stu-id="71395-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="71395-116">預設可能不會針對翻錄選取某些曲目。</span><span class="sxs-lookup"><span data-stu-id="71395-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="71395-117">如果 Windows Media Player 程式庫中已經有一個曲目，它就不會自動選取以進行翻錄。</span><span class="sxs-lookup"><span data-stu-id="71395-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="71395-118">本節中的第二個程式碼範例會示範如何略過預設值，並在已翻錄的情況下手動選取要進行翻錄的播放軌。</span><span class="sxs-lookup"><span data-stu-id="71395-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="71395-119">下列程式碼範例示範如何判斷是否已選取要進行翻錄的追蹤：</span><span class="sxs-lookup"><span data-stu-id="71395-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



<span data-ttu-id="71395-120">下列程式碼範例示範如何指定是否已選取要進行翻錄的追蹤。</span><span class="sxs-lookup"><span data-stu-id="71395-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="71395-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="71395-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71395-122">**將 CD 翻錄**</span><span class="sxs-lookup"><span data-stu-id="71395-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="71395-123">**擷取轉錄介面**</span><span class="sxs-lookup"><span data-stu-id="71395-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="71395-124">**啟動 Rip 進程**</span><span class="sxs-lookup"><span data-stu-id="71395-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="71395-125">**正在抓取 Rip 狀態**</span><span class="sxs-lookup"><span data-stu-id="71395-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 




