---
title: 使用 IWMPPlayerServices setTaskPane 轉錄
description: 使用 IWMPPlayerServices setTaskPane 轉錄
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media Player 的行動 ActiveX 控制項、CD 翻錄
- Windows Media Player 行動電話、CD 翻錄
- CD 翻錄、IWMPPlayerServices setTaskPane 介面
- 翻錄 Cd、IWMPPlayerServices setTaskPane 介面
- IWMPPlayerServices setTaskPane 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104462777"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="b9eee-113">使用 IWMPPlayerServices：： setTaskPane 進行翻錄</span><span class="sxs-lookup"><span data-stu-id="b9eee-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="b9eee-114">本節記載 Windows Media Player 9 系列和 Windows Media Player 10 個 ActiveX 控制項的功能。</span><span class="sxs-lookup"><span data-stu-id="b9eee-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="b9eee-115">建議您在較新的版本中使用 **IWMPCdromRip** 介面。</span><span class="sxs-lookup"><span data-stu-id="b9eee-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="b9eee-116">請參閱 [IWMPCdromRip 介面](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)。</span><span class="sxs-lookup"><span data-stu-id="b9eee-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="b9eee-117">您可以使用 Windows Media Player 9 系列或更新版本的控制項，將 CD 曲目複製到使用者的電腦。</span><span class="sxs-lookup"><span data-stu-id="b9eee-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="b9eee-118">此進程稱為「 *翻錄*」。</span><span class="sxs-lookup"><span data-stu-id="b9eee-118">This process is called *ripping*.</span></span> <span data-ttu-id="b9eee-119">若要這樣做，您必須在遠端模式中內嵌 Windows Media Player 控制項。</span><span class="sxs-lookup"><span data-stu-id="b9eee-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="b9eee-120">如需遠端模式的詳細資訊，請參閱遠端 [處理 Windows Media Player 控制項](remoting-the-windows-media-player-control.md)。</span><span class="sxs-lookup"><span data-stu-id="b9eee-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="b9eee-121">若要開始進行翻錄程式，請呼叫 [IWMPPlayerServices：： setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane)，並傳遞 CopyFromCD？自動]： *bstrTaskPane* 參數的 *識別碼* 值，其中 *id* 是要複製之來源 CD 光碟機的索引。</span><span class="sxs-lookup"><span data-stu-id="b9eee-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="b9eee-122">此索引對應于 **IWMPCdromCollection** 介面或 **CdromMediaChange** 事件中之 **Cdrom** 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="b9eee-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="b9eee-123">下列範例程式碼是一種函式，它會啟動從索引零所識別的 CD 光碟機翻錄 CD 的程式。</span><span class="sxs-lookup"><span data-stu-id="b9eee-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="b9eee-124">函數會使用下列成員變數：</span><span class="sxs-lookup"><span data-stu-id="b9eee-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="b9eee-125">下列程式碼顯示函數的主體：</span><span class="sxs-lookup"><span data-stu-id="b9eee-125">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



<span data-ttu-id="b9eee-126">向使用者顯示狀態</span><span class="sxs-lookup"><span data-stu-id="b9eee-126">Displaying Status to the User</span></span>

<span data-ttu-id="b9eee-127">從 CD 複製時，您可以取出包含複製作業之狀態資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="b9eee-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="b9eee-128">若要這樣做，您必須先透過呼叫 [IWMPCdrom：： get \_ 播放清單](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist)來取出內含媒體專案的播放清單，以代表 CD 曲目。</span><span class="sxs-lookup"><span data-stu-id="b9eee-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="b9eee-129">如同上述範例，下列範例程式碼適用于 CD 磁片磁碟機索引零。</span><span class="sxs-lookup"><span data-stu-id="b9eee-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="b9eee-130">它會將取出的播放清單儲存在下列成員變數中：</span><span class="sxs-lookup"><span data-stu-id="b9eee-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="b9eee-131">下列程式碼顯示函數的主體：</span><span class="sxs-lookup"><span data-stu-id="b9eee-131">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



<span data-ttu-id="b9eee-132">接著，處理 [IWMPEvents：： MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) 事件。</span><span class="sxs-lookup"><span data-stu-id="b9eee-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="b9eee-133">翻錄 CD 播放軌時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="b9eee-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="b9eee-134">傳遞至事件處理常式的 **IDispatch** 指標會指向 CD 軌的 **IWMPMedia** 介面。透過 **IDispatch** 呼叫 **QueryInterface** 以取出 **IWMPMedia** 的指標。</span><span class="sxs-lookup"><span data-stu-id="b9eee-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="b9eee-135">若要偵測正在翻錄的 CD 播放軌，請藉由呼叫 [IWMPMedia：： get \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical)，將事件的 **IWMPMedia** 指標與 CD 播放清單中的媒體專案進行比較。</span><span class="sxs-lookup"><span data-stu-id="b9eee-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="b9eee-136">呼叫 [IWMPMedia：： getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)，並傳遞字串 "Status" 作為專案名稱。</span><span class="sxs-lookup"><span data-stu-id="b9eee-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="b9eee-137">**狀態** 是從 CD 進行翻錄時，Windows Media Player 在媒體專案上設定的暫存屬性;它無法從程式庫中使用。</span><span class="sxs-lookup"><span data-stu-id="b9eee-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="b9eee-138">下列範例程式碼顯示 **MediaChange** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="b9eee-138">The following example code shows a **MediaChange** event handler.</span></span>


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a><span data-ttu-id="b9eee-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9eee-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9eee-140">**IWMPCdrom 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="b9eee-141">**IWMPCdromCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="b9eee-142">**IWMPEvents 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="b9eee-143">**IWMPMedia 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="b9eee-144">**IWMPPlayerServices 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="b9eee-145">**IWMPPlaylist 介面**</span><span class="sxs-lookup"><span data-stu-id="b9eee-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="b9eee-146">**播放機控制指南**</span><span class="sxs-lookup"><span data-stu-id="b9eee-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="b9eee-147">**使用 IWMPCdromRip 介面進行翻錄**</span><span class="sxs-lookup"><span data-stu-id="b9eee-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




