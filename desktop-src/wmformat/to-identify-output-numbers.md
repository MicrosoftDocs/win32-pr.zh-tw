---
title: 識別輸出編號
description: 識別輸出編號
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK，識別輸出編號
- Advanced Systems Format (ASF) ，識別輸出編號
- ASF (Advanced 系統格式) ，識別輸出編號
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出編號和格式，識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106967464"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="4e8f0-109">識別輸出編號</span><span class="sxs-lookup"><span data-stu-id="4e8f0-109">To Identify Output Numbers</span></span>

<span data-ttu-id="4e8f0-110">若要識別已載入檔案的輸出編號，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="4e8f0-111">非同步讀取器和同步讀取器的這些程式都相同。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="4e8f0-112">在介面名稱不同的情況下，同步讀取器方法會在非同步讀取器方法之後的括弧中列出。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="4e8f0-113">建立讀取器物件，並載入要讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="4e8f0-114">如需詳細資訊，請參閱 [建立讀取器和開啟](to-create-a-reader-and-open-a-file.md) 檔案 (或 [建立同步讀取器，並開啟](to-create-a-synchronous-reader-and-open-a-file.md) 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="4e8f0-115">藉由呼叫 [**IWMReader：： GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (或 [**IWMSyncReader：： GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)) ，來取出檔案的輸出總數。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="4e8f0-116">逐一執行一次輸出，執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="4e8f0-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="4e8f0-117">使用 [**IWMReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (或 [**IWMSyncReader：： GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)) 的呼叫，以取得目前輸出的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="4e8f0-118">對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩次呼叫，以抓取輸出的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="4e8f0-119">進行第一次呼叫以取得結構的大小，然後為其配置記憶體，並在第二次呼叫時將指標傳遞至配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="4e8f0-120">或者，您可以呼叫 [**IWMMediaProps：： GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)以傳遞主要型別，而不需要為 **WM \_ 媒體 \_ 類型** 結構配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4e8f0-121">您可以略過錯誤主要類型的輸出。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="4e8f0-122">從 **WM \_ 媒體 \_ 類型** 結構取出主要媒體類型和媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4e8f0-123">這些值分別儲存在資料成員 **majortype** 和 **子類型** 中。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="4e8f0-124">檢查 **WM \_ 媒體 \_ 類型** 的值 formattype。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="4e8f0-125">這會指定以 **WM \_ 媒體 \_ 類型 pbFormat** 之緩衝區中包含的結構類型。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="4e8f0-126">如需有關格式類型的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="4e8f0-127">配置記憶體來保存上一個步驟中所識別之類型的結構。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="4e8f0-128">將結構複製到配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="4e8f0-129">針對音訊和影片，此結構提供有關如何呈現資料的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="4e8f0-130">同步讀取器也會提供方法，以取得輸出數位與資料流程號碼之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="4e8f0-131">如需詳細資訊，請參閱 [尋找資料流程號碼和輸出編號](to-find-stream-numbers-and-output-numbers.md)。</span><span class="sxs-lookup"><span data-stu-id="4e8f0-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e8f0-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e8f0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e8f0-133">**輸入、串流和輸出**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="4e8f0-134">**IWMMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="4e8f0-135">**IWMOutputMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="4e8f0-136">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="4e8f0-137">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="4e8f0-138">**使用輸出**</span><span class="sxs-lookup"><span data-stu-id="4e8f0-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




