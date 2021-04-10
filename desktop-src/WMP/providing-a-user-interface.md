---
title: 提供消費者介面
description: 提供消費者介面
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Windows Media Player 外掛程式、屬性頁
- 外掛程式，屬性頁
- 數位信號處理外掛程式，屬性頁
- DSP 外掛程式、屬性頁
- 數位信號處理外掛程式，使用者介面
- DSP 外掛程式，使用者介面
- 屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183913"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="0ab57-110">提供消費者介面</span><span class="sxs-lookup"><span data-stu-id="0ab57-110">Providing a User Interface</span></span>

<span data-ttu-id="0ab57-111">DSP 外掛程式可以提供屬性頁來建立使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0ab57-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="0ab57-112">若要這樣做，外掛程式必須包含可提供 **IPropertyPage** 介面執行的屬性頁物件。</span><span class="sxs-lookup"><span data-stu-id="0ab57-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="0ab57-113">DSP 外掛程式物件必須執行 **ISpecifyPropertyPages：： GetPages**，以允許 Windows Media Player 找出並識別外掛程式的正確屬性頁。</span><span class="sxs-lookup"><span data-stu-id="0ab57-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="0ab57-114">**顯示狀態圖形**</span><span class="sxs-lookup"><span data-stu-id="0ab57-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="0ab57-115">DSP 外掛程式可在 [Windows Media Player 狀態] 區域中顯示一小圖形或圖形系列，以通知使用者外掛程式為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="0ab57-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="0ab57-116">若要支援這項功能，外掛程式必須執行 **IPropertyBag** 介面。</span><span class="sxs-lookup"><span data-stu-id="0ab57-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="0ab57-117">Windows Media Player 會呼叫 **IPropertyBag：： Read**，提供要求的屬性名稱 "IconStreams" 的指標，該名稱會區分大小寫，而 **VARIANT** 結構的指標則會接收圖形的資料。</span><span class="sxs-lookup"><span data-stu-id="0ab57-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="0ab57-118">如果有多個圖形) ，外掛程式會建立 **istream** 物件 (或 **ISTREAM** 物件的 SAFEARRAY，然後將圖形資料（包括標頭資訊）載入至資料流程，然後使用 **VARIANT** 結構的 **punkVal** 成員傳回 **istream** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0ab57-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="0ab57-119">如果外掛程式只提供一個圖形，則會將 **VARIANT** 結構的 **vt** 成員指定為 vt \_ UNKNOWN。</span><span class="sxs-lookup"><span data-stu-id="0ab57-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="0ab57-120">如果外掛程式使用 SAFEARRAY 來提供多個圖形 **IStream** 物件，它會將 **VARIANT** 結構的 **vt** 成員指定為 vt \_ 陣列。</span><span class="sxs-lookup"><span data-stu-id="0ab57-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="0ab57-121">圖形可以用各種不同的檔案格式儲存，包括：</span><span class="sxs-lookup"><span data-stu-id="0ab57-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="0ab57-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="0ab57-122">**BMP**</span></span>

<span data-ttu-id="0ab57-123">Microsoft Windows 點陣圖影像未壓縮。</span><span class="sxs-lookup"><span data-stu-id="0ab57-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="0ab57-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="0ab57-124">**JPEG**</span></span>

<span data-ttu-id="0ab57-125">通常用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="0ab57-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="0ab57-126">JPEG 格式檔案的副檔名通常為 .jpg。</span><span class="sxs-lookup"><span data-stu-id="0ab57-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="0ab57-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="0ab57-127">**GIF**</span></span>

<span data-ttu-id="0ab57-128">通常用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="0ab57-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="0ab57-129">**PNG**</span><span class="sxs-lookup"><span data-stu-id="0ab57-129">**PNG**</span></span>

<span data-ttu-id="0ab57-130">通常用於網頁的壓縮影像格式。</span><span class="sxs-lookup"><span data-stu-id="0ab57-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="0ab57-131">DSP 外掛程式圖形的大小上限為38圖元寬和14圖元高。</span><span class="sxs-lookup"><span data-stu-id="0ab57-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="0ab57-132">包含狀態圖形的 **IStream** 位元組資料流程必須包含標頭資訊。</span><span class="sxs-lookup"><span data-stu-id="0ab57-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="0ab57-133">如果沒有標頭資訊，Windows Media Player 無法正確地識別圖形的類型，因此不會載入影像。</span><span class="sxs-lookup"><span data-stu-id="0ab57-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ab57-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ab57-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ab57-135">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="0ab57-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




