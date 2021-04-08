---
title: 使用非同步讀取器依框架編號搜尋
description: 使用非同步讀取器依框架編號搜尋
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF) ，依框架編號搜尋
- ASF (Advanced Systems Format) ，依框架編號搜尋
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，依框架編號搜尋
- 影片串流，依畫面格編號搜尋
- 影片串流，非同步讀取器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023025"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="d2c21-110">使用非同步讀取器依框架編號搜尋</span><span class="sxs-lookup"><span data-stu-id="d2c21-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="d2c21-111">您可以使用非同步讀取器物件，在 ASF 檔案中搜尋影片資料流程的框架數。</span><span class="sxs-lookup"><span data-stu-id="d2c21-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="d2c21-112">若要使用以框架為基礎的搜尋，讀取器中載入的檔案必須依框架編制索引。</span><span class="sxs-lookup"><span data-stu-id="d2c21-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="d2c21-113">每個個別的影片串流都可以建立索引。</span><span class="sxs-lookup"><span data-stu-id="d2c21-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="d2c21-114">若要判斷資料流程是否已依框架編制索引，您可以 \_ 呼叫 [**IWMHeaderInfo：： GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)來檢查檔案標頭中的 g wszWMNumberOfFrames 屬性。</span><span class="sxs-lookup"><span data-stu-id="d2c21-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="d2c21-115">若要使用非同步讀取器依框架號碼在 ASF 檔案中搜尋資料，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="d2c21-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="d2c21-116">藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d2c21-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="d2c21-117">藉由呼叫 [**IWMReaderAdvanced3：： StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)來設定開始畫面格編號和持續時間。</span><span class="sxs-lookup"><span data-stu-id="d2c21-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="d2c21-118">您必須指定框架索引影片資料流程的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="d2c21-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="d2c21-119">讀取器會將輸出的其餘部分與指定之資料流程的指定框架的呈現時間進行同步處理，並開始傳遞輸出範例。</span><span class="sxs-lookup"><span data-stu-id="d2c21-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="d2c21-120">如同您在 **IWMReaderCallback：： OnSample** 方法的實中一般地處理範例。</span><span class="sxs-lookup"><span data-stu-id="d2c21-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2c21-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d2c21-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2c21-122">**使用非同步讀取器讀取檔案**</span><span class="sxs-lookup"><span data-stu-id="d2c21-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="d2c21-123">**在播放時讀取中繼資料**</span><span class="sxs-lookup"><span data-stu-id="d2c21-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="d2c21-124">**使用索引**</span><span class="sxs-lookup"><span data-stu-id="d2c21-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




