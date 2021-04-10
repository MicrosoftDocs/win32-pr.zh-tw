---
description: ASFParser 範例
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: ASFParser 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191088"
---
# <a name="asfparser-sample"></a><span data-ttu-id="02910-103">ASFParser 範例</span><span class="sxs-lookup"><span data-stu-id="02910-103">ASFParser Sample</span></span>

<span data-ttu-id="02910-104">說明如何使用媒體基礎中的低層級 ASF 元件，從 Advanced 系統格式剖析資料 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="02910-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="02910-105">此範例會示範下列工作：</span><span class="sxs-lookup"><span data-stu-id="02910-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="02910-106">列舉 ASF 檔案中的音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="02910-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="02910-107">選取音訊或影片串流進行剖析。</span><span class="sxs-lookup"><span data-stu-id="02910-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="02910-108">在所需的播放時間搜尋封包。</span><span class="sxs-lookup"><span data-stu-id="02910-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="02910-109">正在為選取的資料流程產生壓縮的範例。</span><span class="sxs-lookup"><span data-stu-id="02910-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="02910-110">解碼音訊和影片範例。</span><span class="sxs-lookup"><span data-stu-id="02910-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="02910-111">示範的 Api</span><span class="sxs-lookup"><span data-stu-id="02910-111">APIs Demonstrated</span></span>

<span data-ttu-id="02910-112">這個範例會示範下列 Microsoft 媒體基礎介面：</span><span class="sxs-lookup"><span data-stu-id="02910-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="02910-113">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="02910-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="02910-114">**IMFASFIndexer**</span><span class="sxs-lookup"><span data-stu-id="02910-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="02910-115">**IMFASFSplitter**</span><span class="sxs-lookup"><span data-stu-id="02910-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="02910-116">使用方式</span><span class="sxs-lookup"><span data-stu-id="02910-116">Usage</span></span>

1.  <span data-ttu-id="02910-117">若要開啟 ASF 檔案，請按一下 [ **開啟媒體** 檔案] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="02910-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="02910-118">選取 ASF 檔案，然後按一下 [ **開啟**]。</span><span class="sxs-lookup"><span data-stu-id="02910-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="02910-119">檔案的相關資訊會顯示在 **資訊** 窗格中。</span><span class="sxs-lookup"><span data-stu-id="02910-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="02910-120">在 [剖析器設定 **] 下，** 選取要剖析的資料流程。</span><span class="sxs-lookup"><span data-stu-id="02910-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="02910-121">若要反向產生樣本，請選取 [ **反向**]。</span><span class="sxs-lookup"><span data-stu-id="02910-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="02910-122">若要指定起始點，請將滑杆拖曳至所要的位置。</span><span class="sxs-lookup"><span data-stu-id="02910-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="02910-123">若要開始剖析，請按一下 [ **產生範例** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="02910-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="02910-124">範例的相關資訊會顯示在 **資訊** 窗格中。</span><span class="sxs-lookup"><span data-stu-id="02910-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="02910-125">若要測試音訊串流的範例，請按一下 [ **測試音訊** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="02910-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="02910-126">若要測試影片串流的範例，請按一下 [ **顯示點陣圖** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="02910-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="02910-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="02910-127">Requirements</span></span>



| <span data-ttu-id="02910-128">產品</span><span class="sxs-lookup"><span data-stu-id="02910-128">Product</span></span>                                                        | <span data-ttu-id="02910-129">版本</span><span class="sxs-lookup"><span data-stu-id="02910-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="02910-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="02910-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="02910-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02910-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="02910-132">下載範例</span><span class="sxs-lookup"><span data-stu-id="02910-132">Downloading the Sample</span></span>

<span data-ttu-id="02910-133">此範例可在 [Windows 傳統範例 github 存放庫](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)中取得。</span><span class="sxs-lookup"><span data-stu-id="02910-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02910-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="02910-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02910-135">媒體基礎 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="02910-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="02910-136">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="02910-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="02910-137">教學課程：讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="02910-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="02910-138">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="02910-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



