---
description: 其他來源物件
ms.assetid: 67482227-9df6-4e89-b16f-160a0bae6609
title: 其他來源物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0c76c8f6cb104e87630f178a82d613675b96723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688203"
---
# <a name="other-source-objects"></a><span data-ttu-id="7f30d-103">其他來源物件</span><span class="sxs-lookup"><span data-stu-id="7f30d-103">Other Source Objects</span></span>

<span data-ttu-id="7f30d-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7f30d-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="7f30d-105">除了影片和音訊來源之外， (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md) 也支援下列來源物件。</span><span class="sxs-lookup"><span data-stu-id="7f30d-105">In addition to video and audio sources, [DirectShow Editing Services](directshow-editing-services.md) (DES) supports the following source objects.</span></span>

<span data-ttu-id="7f30d-106">**靜止影像**</span><span class="sxs-lookup"><span data-stu-id="7f30d-106">**Still Images**</span></span>

<span data-ttu-id="7f30d-107">DES 針對靜止映射支援下列檔案格式：</span><span class="sxs-lookup"><span data-stu-id="7f30d-107">DES supports the following file formats for still images:</span></span>

-   <span data-ttu-id="7f30d-108">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="7f30d-108">Bitmap (.bmp)</span></span>
-   <span data-ttu-id="7f30d-109">GIF (圖形交換格式) </span><span class="sxs-lookup"><span data-stu-id="7f30d-109">GIF (Graphics Interchange Format)</span></span>
-   <span data-ttu-id="7f30d-110">JPEG (聯合攝影專家群組) </span><span class="sxs-lookup"><span data-stu-id="7f30d-110">JPEG (Joint Photographic Experts Group)</span></span>
-   <span data-ttu-id="7f30d-111">Targa 或 Truevision 圖形介面卡 (. tga) ： Mode 2 (16 位、24、bit 或32位格式的未壓縮 RGB) 。</span><span class="sxs-lookup"><span data-stu-id="7f30d-111">Targa or Truevision Graphics Adapter (.tga): Mode 2 (uncompressed RGB) in 16-bit, 24,-bit, or 32-bit format.</span></span>

<span data-ttu-id="7f30d-112">這些檔案可以用來當做靜止影像或建立動畫。</span><span class="sxs-lookup"><span data-stu-id="7f30d-112">These files can be used as still images or to create animations.</span></span> <span data-ttu-id="7f30d-113">若是點陣圖、JPEG 和 Targa 檔案，如果您使用檔案作為靜止影像，請呼叫 [**IAMTimelineSrc：： SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) 方法將畫面播放速率設定為零。</span><span class="sxs-lookup"><span data-stu-id="7f30d-113">For bitmap, JPEG, and Targa files, if you are using the file as a still image, call the [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md) method to set the frame rate to zero.</span></span>

<span data-ttu-id="7f30d-114">**DIB 順序**</span><span class="sxs-lookup"><span data-stu-id="7f30d-114">**DIB Sequences**</span></span>

<span data-ttu-id="7f30d-115">由於有一系列的點陣圖、JPEG 或 Targa 檔案，轉譯引擎可以建立一個 DIB 順序。</span><span class="sxs-lookup"><span data-stu-id="7f30d-115">Given a series of bitmap, JPEG, or Targa files, the render engine can construct a DIB sequence.</span></span> <span data-ttu-id="7f30d-116">若要建立 DIB 順序，請以數位順序提供檔案，例如 Image001.bmp、Image002.bmp、Image003.bmp 等等。</span><span class="sxs-lookup"><span data-stu-id="7f30d-116">To create a DIB sequence, give the files numerically sequential names, such as Image001.bmp, Image002.bmp, Image003.bmp, and so on.</span></span> <span data-ttu-id="7f30d-117">使用序列中的第一個檔案作為來源。</span><span class="sxs-lookup"><span data-stu-id="7f30d-117">Use the first file in the sequence as the source.</span></span> <span data-ttu-id="7f30d-118">藉由呼叫 [**IAMTimelineSrc：： SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)來設定序列的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="7f30d-118">Set the frame rate for the sequence by calling [**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md).</span></span> <span data-ttu-id="7f30d-119">轉譯引擎會依指定的畫面播放速率迴圈處理序列中的影像。</span><span class="sxs-lookup"><span data-stu-id="7f30d-119">The render engine cycles through the images in the sequence at the specified frame rate.</span></span>

<span data-ttu-id="7f30d-120">如果序列太短而無法填滿持續時間，則在給定畫面播放速率的情況下，其餘的持續時間會是實心。</span><span class="sxs-lookup"><span data-stu-id="7f30d-120">If the sequence is too short to fill the duration, given the frame rate, the rest of the duration is solid black.</span></span> <span data-ttu-id="7f30d-121">轉譯期間未發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="7f30d-121">No error occurs during rendering.</span></span>

<span data-ttu-id="7f30d-122">**GIF 來源**</span><span class="sxs-lookup"><span data-stu-id="7f30d-122">**GIF Sources**</span></span>

<span data-ttu-id="7f30d-123">DES 支援使用 GIF89a 規格的 GIF 來源，包括動畫和透明 Gif。</span><span class="sxs-lookup"><span data-stu-id="7f30d-123">DES supports GIF sources, including animated and transparent GIFs, using the GIF89a specification.</span></span> <span data-ttu-id="7f30d-124">使用動畫 GIF 時，與其他檔案類型不同的是，您不需要設定畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="7f30d-124">With an animated GIF, unlike the other file types, you do not need to set the frame rate.</span></span> <span data-ttu-id="7f30d-125">GIF 檔案指定動畫中每個影像之間的延遲。</span><span class="sxs-lookup"><span data-stu-id="7f30d-125">The GIF file specifies the delay between each image in the animation.</span></span>

<span data-ttu-id="7f30d-126">為了支援透明 Gif，DES 會將影像中的透明區域轉換為 RGB 三重 RGB (0，0，0) 。</span><span class="sxs-lookup"><span data-stu-id="7f30d-126">To support transparent GIFs, DES converts transparent regions in the image to the RGB triplet RGB(0,0,0).</span></span> <span data-ttu-id="7f30d-127">然後，您可以在 RGB (0、0、0) 上使用 [金鑰轉換](key-transition.md) 為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7f30d-127">You can then use the [Key Transition](key-transition.md) to key on RGB(0,0,0).</span></span>

<span data-ttu-id="7f30d-128">DES 也會將落在 RGB (0 –7、0–7、0– 7) 範圍內的任何黑色區域轉換為 RGB (8、8、8) 值（除了透明度索引，如果它落在該範圍內）。</span><span class="sxs-lookup"><span data-stu-id="7f30d-128">DES also converts any black regions that fall within the range RGB(0–7,0–7,0–7) to the value RGB(8,8,8)—except for the transparency index, if it falls in that range.</span></span> <span data-ttu-id="7f30d-129">這項轉換無法偵測到眼睛。</span><span class="sxs-lookup"><span data-stu-id="7f30d-129">This conversion is not detectable to the eye.</span></span>

<span data-ttu-id="7f30d-130">**影片色彩來源**</span><span class="sxs-lookup"><span data-stu-id="7f30d-130">**Video Color Source**</span></span>

<span data-ttu-id="7f30d-131">[影片色彩來源](video-color-source.md)物件會建立純色的連續影片影像。</span><span class="sxs-lookup"><span data-stu-id="7f30d-131">The [Video Color Source](video-color-source.md) object creates a continuous video image of a solid color.</span></span> <span data-ttu-id="7f30d-132">此物件的一個用途是讓它成為轉換中的一層。</span><span class="sxs-lookup"><span data-stu-id="7f30d-132">One use for this object is to make it a layer in a transition.</span></span> <span data-ttu-id="7f30d-133">例如，在影片淡入或淡出的影片中使用它。</span><span class="sxs-lookup"><span data-stu-id="7f30d-133">For example, use it in a video fade-in or fade-out.</span></span>

<span data-ttu-id="7f30d-134">**自訂來源篩選**</span><span class="sxs-lookup"><span data-stu-id="7f30d-134">**Custom Source Filters**</span></span>

<span data-ttu-id="7f30d-135">如果篩選準則符合下列條件，DES 可將 DirectShow 來源篩選器作為時間軸來源：</span><span class="sxs-lookup"><span data-stu-id="7f30d-135">DES can use a DirectShow source filter as a timeline source, if the filter meets the following conditions:</span></span>

-   <span data-ttu-id="7f30d-136">它支援搜尋</span><span class="sxs-lookup"><span data-stu-id="7f30d-136">It supports seeking</span></span>
-   <span data-ttu-id="7f30d-137">它會產生 DES 所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="7f30d-137">It produces a format that DES supports.</span></span> <span data-ttu-id="7f30d-138">只要使用者的系統具有能夠解碼的 DirectShow 篩選器，就可以壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="7f30d-138">The format can be compressed as long as the user's system has a DirectShow filter capable of decoding it.</span></span>

<span data-ttu-id="7f30d-139">若要使用自訂來源，請指定篩選的 CLSID 作為來源物件的子物件 GUID。</span><span class="sxs-lookup"><span data-stu-id="7f30d-139">To use a custom source, specify the CLSID of the filter as the subobject GUID of the source object.</span></span> <span data-ttu-id="7f30d-140">如需詳細資訊， [請參閱子](subobjects.md)內容。</span><span class="sxs-lookup"><span data-stu-id="7f30d-140">For more information, see [Subobjects](subobjects.md).</span></span> <span data-ttu-id="7f30d-141">若要支援自訂屬性，請將它們實作為 **IDispatch** "put" 屬性。</span><span class="sxs-lookup"><span data-stu-id="7f30d-141">To support custom properties, implement them as **IDispatch** "put" properties.</span></span> <span data-ttu-id="7f30d-142">來源物件僅支援靜態屬性;不支援動態屬性。</span><span class="sxs-lookup"><span data-stu-id="7f30d-142">Only static properties are supported on source objects; dynamic properties are not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f30d-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f30d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f30d-144">使用來源</span><span class="sxs-lookup"><span data-stu-id="7f30d-144">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



