---
description: SetMediaType 方法會在範例抓取的輸入釘選上指定連接的媒體類型。
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber：： SetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990812"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="91f90-103">ISampleGrabber：： SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="91f90-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="91f90-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="91f90-104">\[Deprecated.</span></span> <span data-ttu-id="91f90-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="91f90-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="91f90-106">方法會在範例抓取的 `SetMediaType` 輸入釘選上指定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="91f90-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f90-107">語法</span><span class="sxs-lookup"><span data-stu-id="91f90-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="91f90-108">參數</span><span class="sxs-lookup"><span data-stu-id="91f90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f90-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="91f90-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="91f90-110">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標會指定所需的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="91f90-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="91f90-111">不需要設定所有結構成員;如需詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="91f90-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f90-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="91f90-112">Return value</span></span>

<span data-ttu-id="91f90-113">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="91f90-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f90-114">備註</span><span class="sxs-lookup"><span data-stu-id="91f90-114">Remarks</span></span>

<span data-ttu-id="91f90-115">根據預設，範例抓取程式沒有慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="91f90-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="91f90-116">若要確保範例抓取程式會連接到正確的篩選，請在建立篩選圖形之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="91f90-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="91f90-117">這個方法會限制篩選器將接受的媒體類型範圍。</span><span class="sxs-lookup"><span data-stu-id="91f90-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="91f90-118">當篩選器連線時，它會嘗試符合 *pType* 中提供的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="91f90-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="91f90-119">若要這樣做，它會比較主要類型、子類型和格式類型 Guid （依該順序）。</span><span class="sxs-lookup"><span data-stu-id="91f90-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="91f90-120">針對上述每個 Guid，如果 *pType* 的值為 GUID \_ Null，範例會接受媒體類型，而不需要進行任何進一步的檢查。</span><span class="sxs-lookup"><span data-stu-id="91f90-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="91f90-121">如果 *pType* 有任何其他值，範例會將它與連線類型中的 GUID 做比較。</span><span class="sxs-lookup"><span data-stu-id="91f90-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="91f90-122">除非兩個 Guid 完全相符，否則範例捕獲會拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="91f90-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="91f90-123">針對影片媒體類型，範例捕獲會忽略格式區塊。</span><span class="sxs-lookup"><span data-stu-id="91f90-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="91f90-124">因此，它會接受任何影片大小和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="91f90-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="91f90-125">當您呼叫時 `SetMediaType` ，請將格式區塊 (**pbFormat**) 設定為 **Null** ，並將 (**cbFormat**) 大小設定為零。</span><span class="sxs-lookup"><span data-stu-id="91f90-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="91f90-126">針對音訊媒體類型，範例抓取程式將會檢查 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，而且會要求其他篩選準則與該格式連接，除非 *pType* 中的格式區塊為 **Null**，或者格式標記為 WAVE \_ 格式 PCM， \_ 而其他結構成員為零。</span><span class="sxs-lookup"><span data-stu-id="91f90-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="91f90-127">範例 1：</span><span class="sxs-lookup"><span data-stu-id="91f90-127">Example 1:</span></span>

-   <span data-ttu-id="91f90-128">主要類型：媒體類型 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="91f90-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="91f90-129">子類型： GUID \_ Null</span><span class="sxs-lookup"><span data-stu-id="91f90-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="91f90-130">格式類型： GUID \_ Null</span><span class="sxs-lookup"><span data-stu-id="91f90-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="91f90-131">範例抓取會接受主要類型等於媒體類型的任何影片類型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="91f90-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="91f90-132">它不會檢查子類型。</span><span class="sxs-lookup"><span data-stu-id="91f90-132">It will not check the subtype.</span></span>

<span data-ttu-id="91f90-133">範例 2：</span><span class="sxs-lookup"><span data-stu-id="91f90-133">Example 2:</span></span>

-   <span data-ttu-id="91f90-134">主要類型：媒體類型 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="91f90-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="91f90-135">子類型： MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="91f90-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="91f90-136">格式類型： GUID \_ Null</span><span class="sxs-lookup"><span data-stu-id="91f90-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="91f90-137">現在，範例抓取會檢查子類型，並只接受 RGB 24 video。</span><span class="sxs-lookup"><span data-stu-id="91f90-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="91f90-138">**限制：** 無論您設定何種類型，範例捕獲篩選器都會拒絕任何具有由上而下方向的影片類型 (負面 *biHeight*) ，或格式類型為 \_ VideoInfo2。</span><span class="sxs-lookup"><span data-stu-id="91f90-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="91f90-139">在此情況下，雖然 `SetMediaType` 方法成功，但篩選準則將不會連接。</span><span class="sxs-lookup"><span data-stu-id="91f90-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="91f90-140">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="91f90-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="91f90-141">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="91f90-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="91f90-142">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="91f90-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91f90-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="91f90-143">Requirements</span></span>



| <span data-ttu-id="91f90-144">需求</span><span class="sxs-lookup"><span data-stu-id="91f90-144">Requirement</span></span> | <span data-ttu-id="91f90-145">值</span><span class="sxs-lookup"><span data-stu-id="91f90-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91f90-146">標頭</span><span class="sxs-lookup"><span data-stu-id="91f90-146">Header</span></span><br/>  | <dl> <span data-ttu-id="91f90-147"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="91f90-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="91f90-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="91f90-148">Library</span></span><br/> | <dl> <span data-ttu-id="91f90-149"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="91f90-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f90-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91f90-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f90-151">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="91f90-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="91f90-152">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="91f90-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
