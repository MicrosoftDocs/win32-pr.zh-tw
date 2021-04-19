---
description: SetMediaType 方法會為群組設定未壓縮的媒體類型。
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'IAMTimelineGroup：： SetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a7c5366525b51367a5348bc47b9acbe0fb799db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980171"
---
# <a name="iamtimelinegroupsetmediatype-method"></a><span data-ttu-id="ec501-103">IAMTimelineGroup：： SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="ec501-103">IAMTimelineGroup::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="ec501-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ec501-104">\[Deprecated.</span></span> <span data-ttu-id="ec501-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ec501-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec501-106">`SetMediaType`方法會為群組設定未壓縮的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ec501-106">The `SetMediaType` method sets the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec501-107">語法</span><span class="sxs-lookup"><span data-stu-id="ec501-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="ec501-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec501-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec501-109">*pmt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec501-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec501-110">描述格式的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ec501-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure describing the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec501-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec501-111">Return value</span></span>

<span data-ttu-id="ec501-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="ec501-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ec501-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ec501-113">Return code</span></span>                                                                                             | <span data-ttu-id="ec501-114">Description</span><span class="sxs-lookup"><span data-stu-id="ec501-114">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ec501-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ec501-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ec501-116">成功。</span><span class="sxs-lookup"><span data-stu-id="ec501-116">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="ec501-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ec501-117"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="ec501-118">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="ec501-118">**NULL** pointer argument.</span></span><br/>           |
| <dl> <span data-ttu-id="ec501-119"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="ec501-119"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="ec501-120">指定的媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="ec501-120">The specified media type is invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec501-121">備註</span><span class="sxs-lookup"><span data-stu-id="ec501-121">Remarks</span></span>

<span data-ttu-id="ec501-122">以下是支援的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="ec501-122">The following media types are supported:</span></span>

-   <span data-ttu-id="ec501-123">未壓縮的 RGB 影片</span><span class="sxs-lookup"><span data-stu-id="ec501-123">Uncompressed RGB video</span></span>
-   <span data-ttu-id="ec501-124">每圖元16位，555格式 (MEDIASUBTYPE \_ RGB555) </span><span class="sxs-lookup"><span data-stu-id="ec501-124">16 bits per pixel, 555 format (MEDIASUBTYPE\_RGB555)</span></span>
-   <span data-ttu-id="ec501-125">每個圖元24個位 (MEDIASUBTYPE \_ RGB24) </span><span class="sxs-lookup"><span data-stu-id="ec501-125">24 bits per pixel (MEDIASUBTYPE\_RGB24)</span></span>
-   <span data-ttu-id="ec501-126">每圖元32位，Alpha (MEDIASUBTYPE \_ ARGB32，而非 MEDIASUBTYPE \_ RGB32) </span><span class="sxs-lookup"><span data-stu-id="ec501-126">32 bits per pixel, with alpha (MEDIASUBTYPE\_ARGB32, not MEDIASUBTYPE\_RGB32)</span></span>
-   <span data-ttu-id="ec501-127">16位身歷聲 PCM 音訊 (MEDIASUBTYPE \_ PCM) </span><span class="sxs-lookup"><span data-stu-id="ec501-127">16-bit stereo PCM audio (MEDIASUBTYPE\_PCM)</span></span>

<span data-ttu-id="ec501-128">影片類型必須使用格式 \_ VideoInfo 格式區塊的格式類型和 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 。</span><span class="sxs-lookup"><span data-stu-id="ec501-128">Video types must use FORMAT\_VideoInfo for the format type and [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) for the format block.</span></span> <span data-ttu-id="ec501-129">不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式。</span><span class="sxs-lookup"><span data-stu-id="ec501-129">The [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format is not supported.</span></span> <span data-ttu-id="ec501-130">此外，不支援 (*biHeight* < 0) 的上而下的影片格式。</span><span class="sxs-lookup"><span data-stu-id="ec501-130">Also, top-down video formats (*biHeight* < 0) are not supported.</span></span>

<span data-ttu-id="ec501-131">若要指定群組的壓縮格式，請呼叫 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ec501-131">To specify a compression format for the group, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="ec501-132">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ec501-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec501-133">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ec501-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec501-134">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ec501-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec501-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec501-135">Requirements</span></span>



| <span data-ttu-id="ec501-136">需求</span><span class="sxs-lookup"><span data-stu-id="ec501-136">Requirement</span></span> | <span data-ttu-id="ec501-137">值</span><span class="sxs-lookup"><span data-stu-id="ec501-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec501-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ec501-138">Header</span></span><br/>  | <dl> <span data-ttu-id="ec501-139"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec501-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec501-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="ec501-140">Library</span></span><br/> | <dl> <span data-ttu-id="ec501-141"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec501-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec501-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec501-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec501-143">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="ec501-143">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="ec501-144">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ec501-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




