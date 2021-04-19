---
description: Windows Media MPEG4 V1/V2 解碼器會解碼 MPEG4 V1/V2 影片串流。
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: 'Windows Media MPEG4 V1/V2 解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106975592"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="0c813-103">Windows Media MPEG4 V1/V2 解碼器</span><span class="sxs-lookup"><span data-stu-id="0c813-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="0c813-104">Windows Media MPEG4 V1/V2 解碼器會解碼 MPEG4 V1/V2 影片串流。</span><span class="sxs-lookup"><span data-stu-id="0c813-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="0c813-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="0c813-105">Class Identifier</span></span>

<span data-ttu-id="0c813-106">Windows Media MPEG4 V1/V2 解碼器的類別識別碼 (CLSID) 是由常數 **CLSID \_ CMpeg4DecMediaObject** 所表示。</span><span class="sxs-lookup"><span data-stu-id="0c813-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="0c813-107">您可以藉由呼叫 **CoCreateInstance** 來建立 MPEG4 V1/V2 解碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="0c813-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="0c813-108">格式</span><span class="sxs-lookup"><span data-stu-id="0c813-108">Formats</span></span>

<span data-ttu-id="0c813-109">Windows Media MPEG4 V1/V2 解碼器支援下列輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0c813-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="0c813-110">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="0c813-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="0c813-111">MEDIASUBTYPE \_ mpg4</span><span class="sxs-lookup"><span data-stu-id="0c813-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="0c813-112">MEDIASUBTYPE \_ MP42</span><span class="sxs-lookup"><span data-stu-id="0c813-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="0c813-113">MEDIASUBTYPE \_ mp42</span><span class="sxs-lookup"><span data-stu-id="0c813-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="0c813-114">當 Windows Media MPEG4 V1/V2 解碼器作為 DirectX 媒體物件時，可支援下列輸出媒體子類型 (]) 。</span><span class="sxs-lookup"><span data-stu-id="0c813-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="0c813-115">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="0c813-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="0c813-116">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="0c813-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="0c813-117">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="0c813-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="0c813-118">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="0c813-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="0c813-119">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="0c813-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="0c813-120">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="0c813-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="0c813-121">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="0c813-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="0c813-122">當 Windows Media MPEG4 V1/V2 解碼器作為媒體基礎轉換 (MFT) 時，支援下列輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="0c813-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="0c813-123">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="0c813-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="0c813-124">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="0c813-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="0c813-125">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="0c813-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="0c813-126">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="0c813-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="0c813-127">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="0c813-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="0c813-128">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="0c813-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="0c813-129">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="0c813-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="0c813-130">備註</span><span class="sxs-lookup"><span data-stu-id="0c813-130">Remarks</span></span>

<span data-ttu-id="0c813-131">Windows Media MPEG4 V1/V2 解碼器物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，以便將物件當做媒體基礎轉換 (MFT) 使用。</span><span class="sxs-lookup"><span data-stu-id="0c813-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="0c813-132">物件具有相同的類別識別碼 (CLSID) ，不論它是以 SQL-DMO 或 MFT 的形式。</span><span class="sxs-lookup"><span data-stu-id="0c813-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="0c813-133">MPEG4 V1/V2 解碼器的行為，會視您取得的介面和正在執行的 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="0c813-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="0c813-134">下表顯示 MPEG4 V1/V2 解碼器以的方式運作的條件。</span><span class="sxs-lookup"><span data-stu-id="0c813-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="0c813-135">作業系統</span><span class="sxs-lookup"><span data-stu-id="0c813-135">Operating system</span></span>            | <span data-ttu-id="0c813-136">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="0c813-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c813-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c813-137">Windows XP</span></span>                  | <span data-ttu-id="0c813-138">MPEG4 V1/V2 解碼器一律會以 SQL-DMO 的方式運作。</span><span class="sxs-lookup"><span data-stu-id="0c813-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="0c813-139">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c813-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="0c813-140">根據預設，MPEG4 V1/V2 解碼器的行為就像是一。</span><span class="sxs-lookup"><span data-stu-id="0c813-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="0c813-141">如果您在 MPEG4 V1/V2 解碼器上取得 [影片子類型 guid](video-subtype-guids.md) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="0c813-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="0c813-142">針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據解碼器是以 SQL-DMO 或 MFT 作為依據而有所不同。</span><span class="sxs-lookup"><span data-stu-id="0c813-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="0c813-143">非 RGB 媒體子類型的 Guid 是相同的，不論是以 SQL-DMO 或 MFT 的形式來表示。</span><span class="sxs-lookup"><span data-stu-id="0c813-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="0c813-144">如需表示影片子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="0c813-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c813-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c813-145">Requirements</span></span>



| <span data-ttu-id="0c813-146">需求</span><span class="sxs-lookup"><span data-stu-id="0c813-146">Requirement</span></span> | <span data-ttu-id="0c813-147">值</span><span class="sxs-lookup"><span data-stu-id="0c813-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c813-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c813-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0c813-149">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c813-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0c813-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c813-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0c813-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c813-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c813-152">標頭</span><span class="sxs-lookup"><span data-stu-id="0c813-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c813-153"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c813-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="0c813-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0c813-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c813-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c813-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c813-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c813-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c813-157">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="0c813-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
