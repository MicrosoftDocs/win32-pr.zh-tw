---
title: 使用同步讀取器讀取檔案
description: 使用同步讀取器讀取檔案
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK，讀取檔案
- Windows Media Format SDK，同步讀取器
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- 同步讀取器，IWMReaderCallback 介面
- IWMReaderCallback，同步讀取器
- 同步讀取器，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374402"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="9b8d6-112">使用同步讀取器讀取檔案</span><span class="sxs-lookup"><span data-stu-id="9b8d6-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="9b8d6-113">您可以使用同步讀取器，以使用同步呼叫來讀取 ASF 檔案，而不是讀取器物件中的非同步方法。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="9b8d6-114">使用同步呼叫可減少讀取檔案所需的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="9b8d6-115">非同步讀取器會使用多個執行緒來處理資料流程。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="9b8d6-116">針對具有多個資料流程的檔案，使用的執行緒數目可能會變得非常大。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="9b8d6-117">同步讀取器只會使用一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="9b8d6-118">同步讀取器的設計目的是為了滿足內容建立和檔案編輯應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="9b8d6-119">您可以針對其他應用程式使用同步讀取器，但其功能有限。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="9b8d6-120">同步讀取器可以使用 UNC 路徑名稱 (例如 " \\ \\ someshare \\ somedirectory \\ somefile.txt 之 .wmv" ) ，開啟本機檔案或網路上的檔案。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="9b8d6-121">您無法將檔案串流至同步讀取器，或從網際網路位置開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="9b8d6-122">同步讀取器也提供使用 **IStream** COM 介面作為來源的支援。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="9b8d6-123">同步讀取器提供比非同步讀取器更能從 ASF 檔案抓取樣本的更多功能。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="9b8d6-124">同步讀取器可以依串流號碼和輸出來傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="9b8d6-125">您可以壓縮或解壓縮串流號碼所傳遞的範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="9b8d6-126">同步讀取器也可以在播放期間于壓縮和未壓縮的傳遞之間切換;這項功能稱為「快速編輯」。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="9b8d6-127">這項功能可讓編輯應用程式讀取以 Windows Media 為基礎的內容，並將它直接傳遞至寫入器，直到到達所需的框架為止。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="9b8d6-128">屆時，應用程式可以告訴讀者開始傳遞未壓縮的內容，讓應用程式可以修改並傳遞給 recompression 的寫入器。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="9b8d6-129">當應用程式完成修改指定的框架時，它可以告訴讀者再次開始傳遞壓縮的框架。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="9b8d6-130">同步讀取器物件的最基本功能可以細分為下列步驟。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="9b8d6-131">在這些步驟中，「應用程式」指的是您使用 Windows Media Format SDK 撰寫的程式。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="9b8d6-132">應用程式會將要讀取的檔案名傳遞給同步讀取器。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="9b8d6-133">當同步讀取器開啟檔案時，它會將輸出編號指派給每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="9b8d6-134">如果檔案使用相互排除，讀取器會為所有互斥資料流程指派單一輸出。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="9b8d6-135">應用程式會從讀取器取得各種輸出的設定相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="9b8d6-136">收集的資訊將可讓應用程式正確地轉譯媒體範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="9b8d6-137">應用程式會一次從同步讀取器開始要求範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="9b8d6-138">同步讀取器會以緩衝區物件傳遞 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) 介面的每個範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="9b8d6-139">應用程式會在讀取器傳遞之後，負責呈現資料。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="9b8d6-140">Windows Media Format SDK 不提供任何轉譯常式。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="9b8d6-141">一般而言，應用程式會使用其他 Sdk 來轉譯資料，例如 Microsoft Direct X SDK 或 Microsoft Windows Platform SDK 的多媒體功能。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="9b8d6-142">這些步驟說明于 WMSyncReader 範例應用程式中。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="9b8d6-143">如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="9b8d6-144">同步讀取器也支援更先進的功能。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="9b8d6-145">同步讀取器可讓您執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="9b8d6-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="9b8d6-146">指定要依時間或依畫面格編號取出的樣本範圍。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="9b8d6-147">適用于互斥資料流程的控制資料流程選取範圍。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="9b8d6-148">使用標準 COM 介面、 **IStream** 來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="9b8d6-149">讀取檔案標頭中的設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="9b8d6-150">從檔案標頭讀取中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="9b8d6-151">在播放期間于資料流程和輸出範例之間切換。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="9b8d6-152">在播放期間于壓縮和未壓縮的串流範例之間切換。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="9b8d6-153">下列各節將詳細說明同步讀取器物件的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="9b8d6-154">建立同步讀取器並開啟檔案</span><span class="sxs-lookup"><span data-stu-id="9b8d6-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="9b8d6-155">尋找資料流程號碼和輸出編號</span><span class="sxs-lookup"><span data-stu-id="9b8d6-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="9b8d6-156">使用同步讀取器取出媒體範例</span><span class="sxs-lookup"><span data-stu-id="9b8d6-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="9b8d6-157">使用同步讀取器依時間進行搜尋</span><span class="sxs-lookup"><span data-stu-id="9b8d6-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9b8d6-158">使用同步讀取器依框架編號搜尋</span><span class="sxs-lookup"><span data-stu-id="9b8d6-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9b8d6-159">使用同步讀取器依 SMPTE 時間碼進行搜尋</span><span class="sxs-lookup"><span data-stu-id="9b8d6-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="9b8d6-160">使用同步讀取器取出資料流程範例</span><span class="sxs-lookup"><span data-stu-id="9b8d6-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="9b8d6-161">使用同步讀取器取出壓縮的範例</span><span class="sxs-lookup"><span data-stu-id="9b8d6-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="9b8d6-162">**範例程式碼**</span><span class="sxs-lookup"><span data-stu-id="9b8d6-162">**Example Code**</span></span>

<span data-ttu-id="9b8d6-163">下列範例程式碼示範如何使用同步讀取器從 ASF 檔案讀取範例。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="9b8d6-164">它會依框架編號指定要傳遞的範例範圍。</span><span class="sxs-lookup"><span data-stu-id="9b8d6-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="9b8d6-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b8d6-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b8d6-166">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="9b8d6-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="9b8d6-167">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="9b8d6-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="9b8d6-168">**同步讀取器物件**</span><span class="sxs-lookup"><span data-stu-id="9b8d6-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




