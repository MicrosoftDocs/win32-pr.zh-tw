---
title: 強制插入 Key-Frame
description: 強制插入 Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF) ，強制執行主要畫面格插入
- ASF (Advanced Systems Format) ，強制執行主要畫面格插入
- Advanced Systems Format (ASF) 、主要畫面格插入
- ASF (Advanced Systems Format) ，主要畫面格插入
- 主要畫面格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104462781"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="6f443-108">強制插入 Key-Frame</span><span class="sxs-lookup"><span data-stu-id="6f443-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="6f443-109">Windows Media 視訊9編解碼器支援強制的主要畫面格插入。</span><span class="sxs-lookup"><span data-stu-id="6f443-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="6f443-110">當您將範例傳遞給寫入器時，可以指定必須將它編碼為 [*主要畫面*](wmformat-glossary.md)格。</span><span class="sxs-lookup"><span data-stu-id="6f443-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="6f443-111">若要強制執行範例的主要畫面格插入，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="6f443-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="6f443-112">配置緩衝區來保存範例，並藉由呼叫 [**IWMWriter：： AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)，取得包含緩衝區之 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6f443-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="6f443-113">藉由呼叫 [**INSSBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)，取出在步驟1中建立之緩衝區的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="6f443-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="6f443-114">將範例資料複製到緩衝區位置，確定傳遞的範例符合配置的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6f443-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="6f443-115">視範例的來源而定，您可以使用各種功能來複製資料。</span><span class="sxs-lookup"><span data-stu-id="6f443-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="6f443-116">例如，如果您要從 AVI 檔案複製資料流程，則可以使用 AVI 函數 **AVIStreamRead**。</span><span class="sxs-lookup"><span data-stu-id="6f443-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="6f443-117">藉由呼叫 [**INSSBuffer：： SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)來更新緩衝區中使用的資料量，以反映樣本的實際大小。</span><span class="sxs-lookup"><span data-stu-id="6f443-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="6f443-118">藉由呼叫 **INSSBuffer：： QueryInterface** 來取得 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6f443-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="6f443-119">藉由呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 方法來設定 WM \_ SampleExtensionGUID OutputCleanPoint 屬性，將範例設定為強制主要畫面格 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6f443-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="6f443-120">這個屬性是布林值;將它設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="6f443-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="6f443-121">使用 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法，將緩衝區介面傳遞至寫入器，以及輸入編號和取樣時間。</span><span class="sxs-lookup"><span data-stu-id="6f443-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f443-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f443-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f443-123">**IWMWriter::WriteSample**</span><span class="sxs-lookup"><span data-stu-id="6f443-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="6f443-124">**撰寫範例**</span><span class="sxs-lookup"><span data-stu-id="6f443-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="6f443-125">**變數位速率 (VBR) 編碼**</span><span class="sxs-lookup"><span data-stu-id="6f443-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="6f443-126">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="6f443-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




