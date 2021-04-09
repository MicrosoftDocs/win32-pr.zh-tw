---
title: 寫入器物件
description: 寫入器物件
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK，寫入器物件
- Advanced Systems Format (ASF) 、writer 物件
- ASF (Advanced Systems Format) 、writer 物件
- 物件、寫入器物件
- 寫入器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681563"
---
# <a name="writer-object"></a><span data-ttu-id="1ce77-108">寫入器物件</span><span class="sxs-lookup"><span data-stu-id="1ce77-108">Writer Object</span></span>

<span data-ttu-id="1ce77-109">寫入器物件是用來寫入使用 advanced systems 格式的數位媒體檔案， (ASF) 檔案結構。</span><span class="sxs-lookup"><span data-stu-id="1ce77-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="1ce77-110">寫入數位媒體檔案的程式牽涉到寫入器內部的許多步驟，這些步驟會協調壓縮、packetization 和多工處理。</span><span class="sxs-lookup"><span data-stu-id="1ce77-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="1ce77-111">寫入器物件包含輸出至檔案或網路的介面、支援一個回呼介面，並且可以建立一或多個輸入媒體屬性物件。</span><span class="sxs-lookup"><span data-stu-id="1ce77-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="1ce77-112">寫入器物件是由函式 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)所建立，它會將指標設定為 **IWMWriter** 介面。</span><span class="sxs-lookup"><span data-stu-id="1ce77-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="1ce77-113">您可以藉由呼叫 **QueryInterface** 方法來取得寫入器物件的其他介面。</span><span class="sxs-lookup"><span data-stu-id="1ce77-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="1ce77-114">寫入器物件支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="1ce77-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="1ce77-115">介面</span><span class="sxs-lookup"><span data-stu-id="1ce77-115">Interface</span></span>                                          | <span data-ttu-id="1ce77-116">描述</span><span class="sxs-lookup"><span data-stu-id="1ce77-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce77-117">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="1ce77-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="1ce77-118">提供產生 [*DRM*](wmformat-glossary.md) 金鑰的方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="1ce77-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="1ce77-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="1ce77-120">設定寫入器物件寫入檔案，其中包含符合網路裝置通訊協定之 Windows Media DRM 10 的預先加密資料流。</span><span class="sxs-lookup"><span data-stu-id="1ce77-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="1ce77-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="1ce77-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="1ce77-122">管理標頭資訊的規格和抓取，例如中繼資料、 [*標記*](wmformat-glossary.md)等等。</span><span class="sxs-lookup"><span data-stu-id="1ce77-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="1ce77-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="1ce77-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="1ce77-124">管理列舉可用的編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="1ce77-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="1ce77-125">繼承 **IWMHeaderInfo** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="1ce77-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="1ce77-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="1ce77-127">管理列舉可用的編解碼器資訊。</span><span class="sxs-lookup"><span data-stu-id="1ce77-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="1ce77-128">繼承 **IWMHeaderInfo** 和 **IWMHeaderInfo2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="1ce77-129">**IWMWatermarkInfo**</span><span class="sxs-lookup"><span data-stu-id="1ce77-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="1ce77-130">提供有關系統上浮水印系統資訊的存取權。</span><span class="sxs-lookup"><span data-stu-id="1ce77-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="1ce77-131">**IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="1ce77-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="1ce77-132">啟動和停止寫入 ASF 檔案;它包含配置緩衝區、設定和取出輸入屬性、設定設定檔和輸出檔名稱，以及解除鎖定寫入器的方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="1ce77-133">**IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="1ce77-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="1ce77-134">新增、取得和移除指定的接收物件;抓取統計資料、接收數目以及寫入器所使用的時鐘時間;並執行其他 advanced 函數。</span><span class="sxs-lookup"><span data-stu-id="1ce77-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="1ce77-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="1ce77-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="1ce77-136">提供一些先進的功能，特別是處理 deinterlaced 影片。</span><span class="sxs-lookup"><span data-stu-id="1ce77-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="1ce77-137">繼承 **IWMWriterAdvanced** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="1ce77-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="1ce77-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="1ce77-139">提供額外的寫入器功能，包括取得詳細寫入器統計資料的能力。</span><span class="sxs-lookup"><span data-stu-id="1ce77-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="1ce77-140">繼承 **IWMWriterAdvanced** 和 **IWMWriterAdvanced2** 的所有方法。</span><span class="sxs-lookup"><span data-stu-id="1ce77-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="1ce77-141">**IWMWriterPostView**</span><span class="sxs-lookup"><span data-stu-id="1ce77-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="1ce77-142">管理與 postviewing 範例相關的一些先進寫入功能。</span><span class="sxs-lookup"><span data-stu-id="1ce77-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="1ce77-143">Postviewing 正在查看輸出（通常是從編碼器）來檢查編碼/解碼程式是否正常運作。</span><span class="sxs-lookup"><span data-stu-id="1ce77-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="1ce77-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="1ce77-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="1ce77-145">管理寫入器所做的前置處理傳遞。</span><span class="sxs-lookup"><span data-stu-id="1ce77-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="1ce77-146">前置處理階段用來改善編碼輸出的品質。</span><span class="sxs-lookup"><span data-stu-id="1ce77-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="1ce77-147">應用程式必須執行下列回呼介面，才能追蹤 postviewing 的進度。</span><span class="sxs-lookup"><span data-stu-id="1ce77-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="1ce77-148">介面</span><span class="sxs-lookup"><span data-stu-id="1ce77-148">Interface</span></span>                                                      | <span data-ttu-id="1ce77-149">描述</span><span class="sxs-lookup"><span data-stu-id="1ce77-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ce77-150">**IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="1ce77-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="1ce77-151">管理如何從寫入器物件接收未壓縮的樣本，以預覽編解碼器的執行情況。</span><span class="sxs-lookup"><span data-stu-id="1ce77-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1ce77-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ce77-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ce77-153">**物件**</span><span class="sxs-lookup"><span data-stu-id="1ce77-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="1ce77-154">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="1ce77-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




