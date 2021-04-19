---
description: CImageDisplay 類別是 GDI 影片轉譯器的 helper 類別，可管理顯示格式。
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: 'CImageDisplay 類別 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991199"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="6113e-103">CImageDisplay 類別</span><span class="sxs-lookup"><span data-stu-id="6113e-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="6113e-105">`CImageDisplay`類別是 GDI 影片轉譯器的 helper 類別，可管理顯示格式。</span><span class="sxs-lookup"><span data-stu-id="6113e-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="6113e-106">物件會儲存描述目前顯示模式的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構，此模式是在物件的「函式」方法中初始化。</span><span class="sxs-lookup"><span data-stu-id="6113e-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="6113e-107">物件的 **CheckMediaType** 方法會檢查建議的媒體類型是否可以使用 GDI 有效率地呈現。</span><span class="sxs-lookup"><span data-stu-id="6113e-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="6113e-108">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="6113e-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="6113e-109">Description</span><span class="sxs-lookup"><span data-stu-id="6113e-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="6113e-110">**m \_ 顯示**</span><span class="sxs-lookup"><span data-stu-id="6113e-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="6113e-111">描述目前顯示格式的 **VIDEOINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="6113e-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="6113e-112">保護方法</span><span class="sxs-lookup"><span data-stu-id="6113e-112">Protected Methods</span></span>                                                | <span data-ttu-id="6113e-113">Description</span><span class="sxs-lookup"><span data-stu-id="6113e-113">Description</span></span>                                                                            |
| [<span data-ttu-id="6113e-114">**CheckBitFields**</span><span class="sxs-lookup"><span data-stu-id="6113e-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="6113e-115">驗證 **VIDEOINFO** 結構中的色遮罩。</span><span class="sxs-lookup"><span data-stu-id="6113e-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="6113e-116">**CountPrefixBits**</span><span class="sxs-lookup"><span data-stu-id="6113e-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="6113e-117">計算指定位欄位開頭的零位位數。</span><span class="sxs-lookup"><span data-stu-id="6113e-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="6113e-118">**CountSetBits**</span><span class="sxs-lookup"><span data-stu-id="6113e-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="6113e-119">傳回在指定位欄位中設定為1的位數目。</span><span class="sxs-lookup"><span data-stu-id="6113e-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="6113e-120">公用方法</span><span class="sxs-lookup"><span data-stu-id="6113e-120">Public Methods</span></span>                                                   | <span data-ttu-id="6113e-121">Description</span><span class="sxs-lookup"><span data-stu-id="6113e-121">Description</span></span>                                                                            |
| [<span data-ttu-id="6113e-122">**CheckHeaderValidity**</span><span class="sxs-lookup"><span data-stu-id="6113e-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="6113e-123">驗證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="6113e-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="6113e-124">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="6113e-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="6113e-125">判斷建議的媒體類型是否與顯示格式相容。</span><span class="sxs-lookup"><span data-stu-id="6113e-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="6113e-126">**CheckPaletteHeader**</span><span class="sxs-lookup"><span data-stu-id="6113e-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="6113e-127">驗證 **VIDEOINFO** 結構中的調色板專案。</span><span class="sxs-lookup"><span data-stu-id="6113e-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="6113e-128">**CheckVideoType**</span><span class="sxs-lookup"><span data-stu-id="6113e-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="6113e-129">檢查指定的 **VIDEOINFO** 格式是否與顯示格式相容。</span><span class="sxs-lookup"><span data-stu-id="6113e-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="6113e-130">**CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="6113e-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="6113e-131">函式方法。</span><span class="sxs-lookup"><span data-stu-id="6113e-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="6113e-132">**GetBitMasks**</span><span class="sxs-lookup"><span data-stu-id="6113e-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="6113e-133">抓取指定 **VIDEOINFO** 格式的色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="6113e-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="6113e-134">**GetColourMask**</span><span class="sxs-lookup"><span data-stu-id="6113e-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="6113e-135">抓取目前顯示格式的色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="6113e-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="6113e-136">**GetDisplayDepth**</span><span class="sxs-lookup"><span data-stu-id="6113e-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="6113e-137">抓取目前顯示模式的位深度。</span><span class="sxs-lookup"><span data-stu-id="6113e-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="6113e-138">**GetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="6113e-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="6113e-139">抓取描述目前顯示模式的影片格式。</span><span class="sxs-lookup"><span data-stu-id="6113e-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="6113e-140">**IsPalettised**</span><span class="sxs-lookup"><span data-stu-id="6113e-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="6113e-141">Retermines，指出目前的顯示格式是否為調色盤。</span><span class="sxs-lookup"><span data-stu-id="6113e-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="6113e-142">**RefreshDisplayType**</span><span class="sxs-lookup"><span data-stu-id="6113e-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="6113e-143">更新物件的影片格式以符合指定的顯示</span><span class="sxs-lookup"><span data-stu-id="6113e-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="6113e-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="6113e-144">Requirements</span></span>



| <span data-ttu-id="6113e-145">需求</span><span class="sxs-lookup"><span data-stu-id="6113e-145">Requirement</span></span> | <span data-ttu-id="6113e-146">值</span><span class="sxs-lookup"><span data-stu-id="6113e-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6113e-147">標頭</span><span class="sxs-lookup"><span data-stu-id="6113e-147">Header</span></span><br/>  | <dl> <span data-ttu-id="6113e-148"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6113e-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6113e-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="6113e-149">Library</span></span><br/> | <dl> <span data-ttu-id="6113e-150"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6113e-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




