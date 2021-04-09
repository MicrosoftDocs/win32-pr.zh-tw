---
title: 使用標記
description: 使用標記
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK，標記
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- Advanced Systems Format (ASF) ，搜尋標記
- ASF (Advanced Systems Format) ，搜尋標記
- 標記，關於
- 標記，加入
- 標記，移除
- 標記，正在抓取
- 標記，搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681561"
---
# <a name="using-markers"></a><span data-ttu-id="dacff-113">使用標記</span><span class="sxs-lookup"><span data-stu-id="dacff-113">Using Markers</span></span>

<span data-ttu-id="dacff-114">*標記* 是 ASF 檔案內的命名點。</span><span class="sxs-lookup"><span data-stu-id="dacff-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="dacff-115">每個標記都是由名稱和相關聯的時間所組成，其測量方式為從檔案開頭算起的位移。</span><span class="sxs-lookup"><span data-stu-id="dacff-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="dacff-116">應用程式可以使用標記，將名稱指派給內容內的不同點，將這些名稱顯示給使用者，然後搜尋標記位置。</span><span class="sxs-lookup"><span data-stu-id="dacff-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="dacff-117">應用程式可以從現有的 ASF 檔案新增或移除標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="dacff-118">[**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)介面包含使用標記的方法。</span><span class="sxs-lookup"><span data-stu-id="dacff-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="dacff-119">中繼資料編輯器物件支援加入和移除標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="dacff-120">寫入器和讀取器物件可以取出標記，但無法新增或移除標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="dacff-121">新增標記</span><span class="sxs-lookup"><span data-stu-id="dacff-121">Adding Markers</span></span>

<span data-ttu-id="dacff-122">若要加入標記，請查詢 **IWMHeaderInfo** 介面的中繼資料編輯器。</span><span class="sxs-lookup"><span data-stu-id="dacff-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="dacff-123">然後呼叫 [**IWMHeaderInfo：： AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) 方法，將標記名稱指定為寬字元字串，並將時間指定為 100-毫微秒單位。</span><span class="sxs-lookup"><span data-stu-id="dacff-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="dacff-124">時間不得超過檔案持續時間。</span><span class="sxs-lookup"><span data-stu-id="dacff-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="dacff-125">兩個標記可以有相同的時間。</span><span class="sxs-lookup"><span data-stu-id="dacff-125">Two markers can have the same time.</span></span>

<span data-ttu-id="dacff-126">下列範例會將數個標記新增至檔案：</span><span class="sxs-lookup"><span data-stu-id="dacff-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="dacff-127">移除標記</span><span class="sxs-lookup"><span data-stu-id="dacff-127">Removing Markers</span></span>

<span data-ttu-id="dacff-128">若要移除標記，請呼叫 [**IWMHeaderInfo：： RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker)，並指定要移除之標記的索引。</span><span class="sxs-lookup"><span data-stu-id="dacff-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="dacff-129">標記會自動依遞增的時間順序排序，因此索引0一律是第一個標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="dacff-130">請注意，呼叫 **RemoveMarker** 會變更後面任何標記的索引編號。</span><span class="sxs-lookup"><span data-stu-id="dacff-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="dacff-131">下列程式碼，其中 *pInfo* 是 **IWMHeaderInfo** 介面的指標，會從檔案中移除所有標記：</span><span class="sxs-lookup"><span data-stu-id="dacff-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="dacff-132">正在抓取標記</span><span class="sxs-lookup"><span data-stu-id="dacff-132">Retrieving Markers</span></span>

<span data-ttu-id="dacff-133">若要取出標記的名稱和時間，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="dacff-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="dacff-134">呼叫 [**IWMHeaderInfo：： GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) 方法，以判斷檔案包含多少個標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="dacff-135">取得包含標記名稱所需的字串大小。</span><span class="sxs-lookup"><span data-stu-id="dacff-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="dacff-136">若要這樣做，請呼叫 [**IWMHeaderInfo：： GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) 方法。</span><span class="sxs-lookup"><span data-stu-id="dacff-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="dacff-137">指定要抓取之標記的索引，並在 *pwszMarkerName* 參數)  (字串緩衝區的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="dacff-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="dacff-138">方法會在 PcchMarkerNameLen 參數中傳回字串的長度，包括結尾的 ' \\ 0 ' 字元。 </span><span class="sxs-lookup"><span data-stu-id="dacff-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="dacff-139">配置寬字元字串以接收名稱。</span><span class="sxs-lookup"><span data-stu-id="dacff-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="dacff-140">再次呼叫 **GetMarker** ，但這次在 *pwszMarkerName* 參數中傳遞字串的位址。</span><span class="sxs-lookup"><span data-stu-id="dacff-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="dacff-141">方法會將標記名稱寫入字串中，並傳回 *pcnsMarkerTime* 參數中的標記時間。</span><span class="sxs-lookup"><span data-stu-id="dacff-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="dacff-142">下列程式碼會依序執行每個標記的迴圈，並抓取名稱和時間：</span><span class="sxs-lookup"><span data-stu-id="dacff-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="dacff-143">搜尋標記</span><span class="sxs-lookup"><span data-stu-id="dacff-143">Seeking to a Marker</span></span>

<span data-ttu-id="dacff-144">若要從標記位置開始播放，請呼叫 reader 物件的 [**IWMReaderAdvanced2：： StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) 方法，並指定標記的索引。</span><span class="sxs-lookup"><span data-stu-id="dacff-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="dacff-145">其餘的參數與 [**IWMReader：： Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) 方法的參數相同。</span><span class="sxs-lookup"><span data-stu-id="dacff-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="dacff-146">下列範例會查詢 [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) 介面的讀取器，並搜尋第一個標記。</span><span class="sxs-lookup"><span data-stu-id="dacff-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="dacff-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="dacff-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dacff-148">**IWMHeaderInfo 介面**</span><span class="sxs-lookup"><span data-stu-id="dacff-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="dacff-149">**IWMReaderAdvanced2::StartAtMarker**</span><span class="sxs-lookup"><span data-stu-id="dacff-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="dacff-150">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="dacff-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




