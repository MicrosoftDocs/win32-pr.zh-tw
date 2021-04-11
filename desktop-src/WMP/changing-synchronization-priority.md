---
title: 變更同步處理優先權
description: 變更同步處理優先權
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- 可攜式裝置，變更同步播放清單優先順序
- 同步播放清單，優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327f211282e2e3b35c21dce721a17f99dcb6583d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681436"
---
# <a name="changing-synchronization-priority"></a><span data-ttu-id="c95ab-115">變更同步處理優先權</span><span class="sxs-lookup"><span data-stu-id="c95ab-115">Changing Synchronization Priority</span></span>

<span data-ttu-id="c95ab-116">下列範例程式碼會針對 IDC PLVIEW 所識別的 ListView 控制項中的每個專案，指定優先順序值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c95ab-116">The following example code specifies a priority value for each item in the ListView control identified by IDC\_PLVIEW.</span></span> <span data-ttu-id="c95ab-117">標記有核取記號的專案，會根據其在清單中的順序來指派優先順序值。</span><span class="sxs-lookup"><span data-stu-id="c95ab-117">Items that are marked with a check mark are assigned a priority value based on their order in the list.</span></span> <span data-ttu-id="c95ab-118">未核取的專案會被指派優先順序值為零。</span><span class="sxs-lookup"><span data-stu-id="c95ab-118">Items that are not checked are assigned a priority value of zero.</span></span>


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a><span data-ttu-id="c95ab-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="c95ab-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c95ab-120">**IWMPMedia 介面**</span><span class="sxs-lookup"><span data-stu-id="c95ab-120">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="c95ab-121">**IWMPPlaylist 介面**</span><span class="sxs-lookup"><span data-stu-id="c95ab-121">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="c95ab-122">**管理同步播放清單**</span><span class="sxs-lookup"><span data-stu-id="c95ab-122">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




