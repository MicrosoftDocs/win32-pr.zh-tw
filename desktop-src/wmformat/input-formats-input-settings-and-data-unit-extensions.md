---
title: 輸入格式、輸入設定和資料單位延伸
description: 輸入格式、輸入設定和資料單位延伸
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- Windows Media 格式 SDK、輸入格式和設定
- Windows Media Format SDK，資料單位延伸模組
- Windows Media Format SDK，承載延伸系統
- Advanced Systems Format (ASF) 、輸入格式和設定
- ASF (Advanced Systems Format) 、輸入格式和設定
- Advanced Systems Format (ASF) 、資料單位延伸模組
- ASF (Advanced Systems Format) 、資料單位延伸模組
- Advanced Systems Format (ASF) 、承載延伸系統
- ASF (Advanced Systems Format) ，承載延伸系統
- 資料單位延伸，關於
- 承載延伸系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932457"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="9cb09-114">輸入格式、輸入設定和資料單位延伸</span><span class="sxs-lookup"><span data-stu-id="9cb09-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="9cb09-115">寫入器物件支援輸入設定、輸入格式和資料單位延伸，這些都可讓您控制寫入器的功能。</span><span class="sxs-lookup"><span data-stu-id="9cb09-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="9cb09-116">用來控制特定功能的方法並不一定很明顯。</span><span class="sxs-lookup"><span data-stu-id="9cb09-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="9cb09-117">輸入格式是媒體格式，可描述您傳遞給寫入器以進行編碼之媒體的基本屬性。</span><span class="sxs-lookup"><span data-stu-id="9cb09-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="9cb09-118">例如，輸入影片的框架大小和色彩空間會由輸入格式描述。</span><span class="sxs-lookup"><span data-stu-id="9cb09-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="9cb09-119">輸入設定是輸入資料的特性，而不是基本概念，或是要對資料執行轉換的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9cb09-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="9cb09-120">交錯式影片設定和浮水印系統的相關資訊是輸入設定的範例。</span><span class="sxs-lookup"><span data-stu-id="9cb09-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="9cb09-121">資料單位延伸模組（也稱為承載延伸系統）是附加至檔案的資料區段中個別樣本的值。</span><span class="sxs-lookup"><span data-stu-id="9cb09-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="9cb09-122">SMPTE 時間代碼和非正方形圖元資訊是資料單位延伸模組的範例。</span><span class="sxs-lookup"><span data-stu-id="9cb09-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cb09-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cb09-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cb09-124">**設定資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="9cb09-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="9cb09-125">**資料單位延伸模組**</span><span class="sxs-lookup"><span data-stu-id="9cb09-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="9cb09-126">**檔案寫入功能**</span><span class="sxs-lookup"><span data-stu-id="9cb09-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="9cb09-127">**輸入格式列舉**</span><span class="sxs-lookup"><span data-stu-id="9cb09-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="9cb09-128">**輸入設定**</span><span class="sxs-lookup"><span data-stu-id="9cb09-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="9cb09-129">**使用輸入**</span><span class="sxs-lookup"><span data-stu-id="9cb09-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




