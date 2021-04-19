---
description: WriteBitmapBits 方法會在指定的媒體時間取出影片畫面，並將其寫入檔案。 影片框架一律採用24位 RGB 格式。
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet：： WriteBitmapBits 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989593"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="45c65-104">IMediaDet：： WriteBitmapBits 方法</span><span class="sxs-lookup"><span data-stu-id="45c65-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="45c65-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="45c65-105">\[Deprecated.</span></span> <span data-ttu-id="45c65-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="45c65-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="45c65-107">`WriteBitmapBits`方法會在指定的媒體時間取出影片畫面，並將其寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="45c65-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="45c65-108">影片框架一律採用24位 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="45c65-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c65-109">語法</span><span class="sxs-lookup"><span data-stu-id="45c65-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="45c65-110">參數</span><span class="sxs-lookup"><span data-stu-id="45c65-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c65-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="45c65-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="45c65-112">取出影片畫面的時間。</span><span class="sxs-lookup"><span data-stu-id="45c65-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="45c65-113">*寬度*</span><span class="sxs-lookup"><span data-stu-id="45c65-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="45c65-114">影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="45c65-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="45c65-115">*高度*</span><span class="sxs-lookup"><span data-stu-id="45c65-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="45c65-116">影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="45c65-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="45c65-117">*檔案名稱*</span><span class="sxs-lookup"><span data-stu-id="45c65-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="45c65-118">要在其中儲存點陣圖之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="45c65-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="45c65-119">如果檔案已存在，這個方法會覆寫該檔案。</span><span class="sxs-lookup"><span data-stu-id="45c65-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c65-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="45c65-120">Return value</span></span>

<span data-ttu-id="45c65-121">傳回 \_ ，確定成功。</span><span class="sxs-lookup"><span data-stu-id="45c65-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="45c65-122">否則，會傳回 **HRESULT** 值，指出錯誤的原因。</span><span class="sxs-lookup"><span data-stu-id="45c65-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="45c65-123">可能的錯誤代碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="45c65-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="45c65-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="45c65-124">Return code</span></span>                                                                                             | <span data-ttu-id="45c65-125">Description</span><span class="sxs-lookup"><span data-stu-id="45c65-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45c65-126"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="45c65-127">無法將 [**範例捕獲**](sample-grabber-filter.md) 篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="45c65-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="45c65-128"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="45c65-129">失敗。</span><span class="sxs-lookup"><span data-stu-id="45c65-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="45c65-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="45c65-131">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="45c65-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="45c65-132"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="45c65-133">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="45c65-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="45c65-134"><dt>**STG. \_ E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="45c65-135">無法覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="45c65-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="45c65-136"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="45c65-137">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="45c65-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="45c65-138">備註</span><span class="sxs-lookup"><span data-stu-id="45c65-138">Remarks</span></span>

<span data-ttu-id="45c65-139">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="45c65-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="45c65-140">這個方法會將媒體偵測器放入點陣圖抓取模式。</span><span class="sxs-lookup"><span data-stu-id="45c65-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="45c65-141">一旦呼叫這個方法，除非您建立新的媒體偵測器實例，否則 **IMediaDet** 中的各種資料流程資訊方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="45c65-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="45c65-142">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="45c65-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="45c65-143">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="45c65-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="45c65-144">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="45c65-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45c65-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="45c65-145">Requirements</span></span>



| <span data-ttu-id="45c65-146">需求</span><span class="sxs-lookup"><span data-stu-id="45c65-146">Requirement</span></span> | <span data-ttu-id="45c65-147">值</span><span class="sxs-lookup"><span data-stu-id="45c65-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45c65-148">標頭</span><span class="sxs-lookup"><span data-stu-id="45c65-148">Header</span></span><br/>  | <dl> <span data-ttu-id="45c65-149"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="45c65-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="45c65-150">Library</span></span><br/> | <dl> <span data-ttu-id="45c65-151"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45c65-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c65-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45c65-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c65-153">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="45c65-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="45c65-154">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="45c65-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




