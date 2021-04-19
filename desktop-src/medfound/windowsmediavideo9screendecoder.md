---
description: Windows Media 視訊9螢幕編碼程式會將 Windows Media 視訊9螢幕編碼器編碼的資料流程解碼。
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: 'Windows Media 視訊9螢幕 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998816"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="2dfba-103">Windows Media 視訊9螢幕解碼</span><span class="sxs-lookup"><span data-stu-id="2dfba-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="2dfba-104">Windows Media 視訊9螢幕編碼程式會將 [**Windows Media 視訊9螢幕編碼器**](windowsmediavideo9screenencoder.md)編碼的資料流程解碼。</span><span class="sxs-lookup"><span data-stu-id="2dfba-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="2dfba-105">類別識別碼</span><span class="sxs-lookup"><span data-stu-id="2dfba-105">Class Identifier</span></span>

<span data-ttu-id="2dfba-106">Windows Media 視訊9螢幕解碼 (CLSID) 的類別識別碼是以常數 **CLSID \_ CMSSCDecMediaObject** 表示。</span><span class="sxs-lookup"><span data-stu-id="2dfba-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="2dfba-107">您可以藉由呼叫 **CoCreateInstance** 來建立此解碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="2dfba-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="2dfba-108">輸入類型</span><span class="sxs-lookup"><span data-stu-id="2dfba-108">Input Types</span></span>

<span data-ttu-id="2dfba-109">適用于 Windows Media 視訊螢幕第9版編碼內容的四個字元的程式碼 (FOURCC) 為 "MSS2"。</span><span class="sxs-lookup"><span data-stu-id="2dfba-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="2dfba-110">第9版螢幕解碼支援下列輸入類型。</span><span class="sxs-lookup"><span data-stu-id="2dfba-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="2dfba-111">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="2dfba-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="2dfba-112">輸出型別</span><span class="sxs-lookup"><span data-stu-id="2dfba-112">Output Types</span></span>

<span data-ttu-id="2dfba-113">當第9版螢幕解碼用來作為 DirectX 媒體物件 (的) 時，會支援下列輸出類型。</span><span class="sxs-lookup"><span data-stu-id="2dfba-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="2dfba-114">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="2dfba-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="2dfba-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="2dfba-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="2dfba-116">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="2dfba-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="2dfba-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="2dfba-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="2dfba-118">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="2dfba-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="2dfba-119">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="2dfba-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="2dfba-120">當第9版的螢幕解碼作為媒體基礎轉換 (MFT) 時，支援下列輸出類型。</span><span class="sxs-lookup"><span data-stu-id="2dfba-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="2dfba-121">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="2dfba-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="2dfba-122">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="2dfba-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="2dfba-123">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="2dfba-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="2dfba-124">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="2dfba-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="2dfba-125">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="2dfba-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="2dfba-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="2dfba-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="2dfba-127">備註</span><span class="sxs-lookup"><span data-stu-id="2dfba-127">Remarks</span></span>

<span data-ttu-id="2dfba-128">螢幕解碼物件會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 介面，讓物件可以作為 DirectX 媒體物件 (的) ，並公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，讓物件可以作為媒體基礎的轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="2dfba-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="2dfba-129">螢幕解碼器的行為就如同您取得的介面以及正在執行的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="2dfba-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="2dfba-130">下表所顯示的條件下，螢幕解碼器的運作方式是以 SQL-DMO 或 MFT 表示。</span><span class="sxs-lookup"><span data-stu-id="2dfba-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="2dfba-131">作業系統</span><span class="sxs-lookup"><span data-stu-id="2dfba-131">Operating system</span></span>            | <span data-ttu-id="2dfba-132">解碼器行為</span><span class="sxs-lookup"><span data-stu-id="2dfba-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfba-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2dfba-133">Windows XP</span></span>                  | <span data-ttu-id="2dfba-134">Windows Media Screen 的解碼器一律會以 SQL-DMO 的方式運作。</span><span class="sxs-lookup"><span data-stu-id="2dfba-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="2dfba-135">Windows Vista 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="2dfba-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="2dfba-136">Windows Media Screen 解碼器預設會以一種方式運作。</span><span class="sxs-lookup"><span data-stu-id="2dfba-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="2dfba-137">如果您在螢幕解碼器上取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面，它會以 MFT 的形式運作。</span><span class="sxs-lookup"><span data-stu-id="2dfba-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="2dfba-138">您可以使用相同的 CLSID (CLSID \_ CMSSCDecMediaObject) 來建立第7版的螢幕解碼和第9版的螢幕解碼器。</span><span class="sxs-lookup"><span data-stu-id="2dfba-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="2dfba-139">Windows Media 視訊螢幕第7版編碼內容的 FOURCC 為 "MSS1"。</span><span class="sxs-lookup"><span data-stu-id="2dfba-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="2dfba-140">第7版螢幕解碼支援 MEDIASUBTYPE \_ MSS1 輸入類型。</span><span class="sxs-lookup"><span data-stu-id="2dfba-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dfba-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dfba-141">Requirements</span></span>



| <span data-ttu-id="2dfba-142">需求</span><span class="sxs-lookup"><span data-stu-id="2dfba-142">Requirement</span></span> | <span data-ttu-id="2dfba-143">值</span><span class="sxs-lookup"><span data-stu-id="2dfba-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfba-144">用戶端</span><span class="sxs-lookup"><span data-stu-id="2dfba-144">Client</span></span><br/> | <span data-ttu-id="2dfba-145">Windows XP、Windows Vista 或 Windows 7</span><span class="sxs-lookup"><span data-stu-id="2dfba-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="2dfba-146">標頭</span><span class="sxs-lookup"><span data-stu-id="2dfba-146">Header</span></span><br/> | <dl> <span data-ttu-id="2dfba-147"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="2dfba-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="2dfba-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2dfba-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="2dfba-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dfba-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dfba-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dfba-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dfba-151">編解碼器物件</span><span class="sxs-lookup"><span data-stu-id="2dfba-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="2dfba-152">編解碼器實行</span><span class="sxs-lookup"><span data-stu-id="2dfba-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="2dfba-153">使用 Windows Media 視訊9螢幕編解碼器</span><span class="sxs-lookup"><span data-stu-id="2dfba-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="2dfba-154">Windows Media 視訊9螢幕編碼器</span><span class="sxs-lookup"><span data-stu-id="2dfba-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
