---
title: 使用反轉電影處理
description: 使用反轉電影處理
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK，反向電視
- Windows Media Format SDK，電影
- Advanced Systems Format (ASF) ，反向電視
- ASF (Advanced Systems Format) ，反向電視
- Advanced Systems Format (ASF) ，電影
- ASF (Advanced Systems Format) ，電影
- 反向電影
- 電影
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106968272"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="940c7-111">使用反轉電影處理</span><span class="sxs-lookup"><span data-stu-id="940c7-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="940c7-112">電視影片是將每秒24個畫面格的電影轉換成影片60，每秒 (半框架) 的影片。</span><span class="sxs-lookup"><span data-stu-id="940c7-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="940c7-113">此程式會將每個影片框架中的影像放在多個影片欄位中。</span><span class="sxs-lookup"><span data-stu-id="940c7-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="940c7-114">當您使用電影來數位編碼從電影建立的影片時，壓縮程式可能會造成運動成品和其他降低品質。</span><span class="sxs-lookup"><span data-stu-id="940c7-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="940c7-115">為了避免影響數位輸出的品質，Windows Media 視訊9編解碼器支援反向電視電影。</span><span class="sxs-lookup"><span data-stu-id="940c7-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="940c7-116">使用反向電視影片時，編解碼器會在編碼內容之前，從輸入影片重建原始的24個影片畫面格。</span><span class="sxs-lookup"><span data-stu-id="940c7-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="940c7-117">若要使用反向電視電影，您必須：</span><span class="sxs-lookup"><span data-stu-id="940c7-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="940c7-118">使用設定檔，並將影片串流設定為每秒24個畫面格。</span><span class="sxs-lookup"><span data-stu-id="940c7-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="940c7-119">知道輸入影片的欄位設定。</span><span class="sxs-lookup"><span data-stu-id="940c7-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="940c7-120">若要使用反向電視來輸入寫入器的輸入，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="940c7-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="940c7-121">照常設定寫入器。</span><span class="sxs-lookup"><span data-stu-id="940c7-121">Set up the writer as usual.</span></span> <span data-ttu-id="940c7-122">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="940c7-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="940c7-123">開始撰寫範例之前，請呼叫 **IWMWriter：： QueryInterface** 來取得 [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="940c7-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="940c7-124">針對所需的輸入編號呼叫 [**IWMWriterAdvanced2：： SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) ，以識別要重建的資料流程。</span><span class="sxs-lookup"><span data-stu-id="940c7-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="940c7-125">將 g \_ wszDeinterlaceMode 當作設定，並以 WM \_ DM \_ 的方式，將 \_ INVERSETELECINE 作為值進行傳遞。</span><span class="sxs-lookup"><span data-stu-id="940c7-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="940c7-126">再次呼叫 **SetInputSetting** ，以設定 g \_ wszInitialPatternForInverseTelecine。</span><span class="sxs-lookup"><span data-stu-id="940c7-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="940c7-127">照常寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="940c7-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="940c7-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="940c7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="940c7-129">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="940c7-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="940c7-130">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="940c7-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="940c7-131">**IWMWriterAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="940c7-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




