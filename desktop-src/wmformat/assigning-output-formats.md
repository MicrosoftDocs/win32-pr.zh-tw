---
title: 指派輸出格式
description: 指派輸出格式
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK，指派輸出格式
- Advanced Systems Format (ASF) ，指派輸出格式
- ASF (Advanced 系統格式) ，指派輸出格式
- Advanced Systems Format (ASF) 、output 數位和格式
- ASF (Advanced Systems Format) 、output 數位和格式
- 輸出編號和格式，指派
- 編解碼器、輸出編號和格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "106968484"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="ca5a7-110">指派輸出格式</span><span class="sxs-lookup"><span data-stu-id="ca5a7-110">Assigning Output Formats</span></span>

<span data-ttu-id="ca5a7-111">某些編解碼器可將數位媒體資料解壓縮成數個未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="ca5a7-112">您可以使用非同步讀取器或同步讀取器，來尋找特定輸出的所有支援格式。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="ca5a7-113">若要檢查輸出的所有可用格式，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="ca5a7-114">非同步讀取器和同步讀取器的這些程式都相同。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="ca5a7-115">在介面名稱不同的情況下，同步讀取器方法會在非同步讀取器方法之後的括弧中列出。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="ca5a7-116">建立讀取器物件，並載入要讀取的檔案。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="ca5a7-117">如需詳細資訊，請參閱 [建立讀取器和開啟](to-create-a-reader-and-open-a-file.md) 檔案 (或 [建立同步讀取器，並開啟](to-create-a-synchronous-reader-and-open-a-file.md) 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="ca5a7-118">判斷您想要尋找其可用格式的輸出。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="ca5a7-119">如果您還不知道要使用哪一個輸出，可以使用中的程式識別 [輸出編號](to-identify-output-numbers.md)，以識別檔案中的輸出。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="ca5a7-120">藉由呼叫 [**IWMReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (或 [**IWMSyncReader：： GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)) ，來取得所需輸出的可用格式總數。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="ca5a7-121">逐一執行一次可用的格式，對每個格式執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="ca5a7-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="ca5a7-122">藉由呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (或 [**IWMSyncReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)) ，取得目前輸出格式的 [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="ca5a7-123">藉由對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩個呼叫，以取出輸出格式的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="ca5a7-124">進行第一次呼叫以取得結構的大小，然後為其配置記憶體，並在第二次呼叫時將指標傳遞至配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="ca5a7-125">在 **WM \_ 媒體 \_ 類型** 中尋找輸出格式的媒體子類型。子類型。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="ca5a7-126">針對影片，如果目前的子類型是您想要用於輸出的格式，請中斷迴圈。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="ca5a7-127">否則，請移至下一個反復專案。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="ca5a7-128">若是音訊，您必須根據您的需求來檢查 **WAVEFORMATEX** 結構中的值。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="ca5a7-129">**WM \_媒體 \_ 類型。 pbFormat** 指向音訊輸出的 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="ca5a7-130">當您找到所需的輸出時，請呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (或 [**IWMSyncReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)) 來設定它以搭配讀取器使用。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="ca5a7-131">您必須將指標傳遞至在迴圈的第一個步驟中取得的 **IWMOutputMediaProps** 介面。</span><span class="sxs-lookup"><span data-stu-id="ca5a7-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca5a7-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca5a7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca5a7-133">**IWMMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="ca5a7-134">**IWMOutputMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="ca5a7-135">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="ca5a7-136">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="ca5a7-137">**使用輸出**</span><span class="sxs-lookup"><span data-stu-id="ca5a7-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




