---
description: Windows Media MPEG-2 V3 解碼會解碼 MPEG-2 V3 影片串流。
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: 'Windows Media MPEG-2 V3 解碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106988097"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="f38c3-103">Windows Media MPEG-2 V3 解碼器</span><span class="sxs-lookup"><span data-stu-id="f38c3-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="f38c3-104">Windows Media MPEG-2 V3 解碼會解碼 MPEG-2 V3 影片串流。</span><span class="sxs-lookup"><span data-stu-id="f38c3-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="f38c3-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="f38c3-105">Class Identifier</span></span>

<span data-ttu-id="f38c3-106">Windows MPEG-2 V3 解碼器 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMpeg43DecMediaObject** 來表示。</span><span class="sxs-lookup"><span data-stu-id="f38c3-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="f38c3-107">您可以藉由呼叫 **CoCreateInstance** 來建立 mpeg-2 V3 解碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="f38c3-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="f38c3-108">格式</span><span class="sxs-lookup"><span data-stu-id="f38c3-108">Formats</span></span>

<span data-ttu-id="f38c3-109">Windows Media MPEG-2 V3 解碼支援下列輸入媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f38c3-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="f38c3-110">MEDIASUBTYPE \_ MP43</span><span class="sxs-lookup"><span data-stu-id="f38c3-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="f38c3-111">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="f38c3-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="f38c3-112">當 Windows Media MPEG-2 V3 解碼器作為 DirectX 媒體物件 (的) 時，支援下列輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="f38c3-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="f38c3-113">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="f38c3-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="f38c3-114">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="f38c3-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="f38c3-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="f38c3-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="f38c3-116">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="f38c3-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="f38c3-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="f38c3-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="f38c3-118">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="f38c3-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="f38c3-119">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="f38c3-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="f38c3-120">當 Windows Media MPEG-2 V3 解碼器作為媒體基礎轉換 (MFT) 時，支援下列輸出媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="f38c3-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="f38c3-121">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="f38c3-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="f38c3-122">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="f38c3-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="f38c3-123">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="f38c3-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="f38c3-124">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="f38c3-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="f38c3-125">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="f38c3-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="f38c3-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="f38c3-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="f38c3-127">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="f38c3-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="f38c3-128">備註</span><span class="sxs-lookup"><span data-stu-id="f38c3-128">Remarks</span></span>

<span data-ttu-id="f38c3-129">Windows Media MPEG-2 V3 解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="f38c3-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f38c3-130">物件具有相同的類別識別碼 (CLSID) ，不論它是以 SQL-DMO 或 MFT 的形式。</span><span class="sxs-lookup"><span data-stu-id="f38c3-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="f38c3-131">根據您取得的介面以及正在執行的 Windows 版本而定，MPEG 4 V3 解碼器會以一或 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="f38c3-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="f38c3-132">下表顯示的是 MPEG-2 V3 解碼器以 SQL-DMO 或 MFT 行為的條件。</span><span class="sxs-lookup"><span data-stu-id="f38c3-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="f38c3-133">作業系統</span><span class="sxs-lookup"><span data-stu-id="f38c3-133">Operating system</span></span>            | <span data-ttu-id="f38c3-134">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="f38c3-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f38c3-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f38c3-135">Windows XP</span></span>                  | <span data-ttu-id="f38c3-136">MPEG-2 V3 解碼器的行為一律會是 SQL-DMO。</span><span class="sxs-lookup"><span data-stu-id="f38c3-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="f38c3-137">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="f38c3-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="f38c3-138">根據預設，MPEG 4 V3 解碼器的行為就像是一。</span><span class="sxs-lookup"><span data-stu-id="f38c3-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="f38c3-139">如果您在 MPEG 4 V3 解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="f38c3-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="f38c3-140">針對 RGB 媒體子類型 (Guid) 的全域唯一識別碼，會根據解碼器是以 SQL-DMO 或 MFT 作為依據而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f38c3-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="f38c3-141">非 RGB 媒體子類型的 Guid 是相同的，不論是以 SQL-DMO 或 MFT 的形式來表示。</span><span class="sxs-lookup"><span data-stu-id="f38c3-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="f38c3-142">如需表示媒體子類型之 Guid 的詳細資訊，請參閱 [影片子類型 guid](video-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="f38c3-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f38c3-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="f38c3-143">Requirements</span></span>



| <span data-ttu-id="f38c3-144">需求</span><span class="sxs-lookup"><span data-stu-id="f38c3-144">Requirement</span></span> | <span data-ttu-id="f38c3-145">值</span><span class="sxs-lookup"><span data-stu-id="f38c3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38c3-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f38c3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f38c3-147">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f38c3-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f38c3-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f38c3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f38c3-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f38c3-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f38c3-150">標頭</span><span class="sxs-lookup"><span data-stu-id="f38c3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f38c3-151"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f38c3-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="f38c3-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f38c3-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f38c3-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f38c3-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38c3-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f38c3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38c3-155">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="f38c3-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
