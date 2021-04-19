---
description: 取得 \_ 畫面播放速率方法會抓取目前資料流程的畫面播放速率。 資料流程必須是影片資料流程。
ms.assetid: f128d118-1147-4a0a-946e-bd1716606cef
title: 'IMediaDet：： get_FrameRate 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_FrameRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9ffabd57d85437911c323ee458d3758ee725d45a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996011"
---
# <a name="imediadetget_framerate-method"></a><span data-ttu-id="c1a75-104">IMediaDet：：取得 \_ 畫面播放速率方法</span><span class="sxs-lookup"><span data-stu-id="c1a75-104">IMediaDet::get\_FrameRate method</span></span>

> [!Note]  
> <span data-ttu-id="c1a75-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c1a75-105">\[Deprecated.</span></span> <span data-ttu-id="c1a75-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c1a75-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1a75-107">方法會抓取 `get_FrameRate` 目前資料流程的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c1a75-107">The `get_FrameRate` method retrieves the frame rate of the current stream.</span></span> <span data-ttu-id="c1a75-108">資料流程必須是影片資料流程。</span><span class="sxs-lookup"><span data-stu-id="c1a75-108">The stream must be a video stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1a75-109">語法</span><span class="sxs-lookup"><span data-stu-id="c1a75-109">Syntax</span></span>


```C++
HRESULT get_FrameRate(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="c1a75-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1a75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1a75-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="c1a75-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c1a75-112">接收畫面播放速率（以每秒畫面格數為單位）。</span><span class="sxs-lookup"><span data-stu-id="c1a75-112">Receives the frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1a75-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1a75-113">Return value</span></span>

<span data-ttu-id="c1a75-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c1a75-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c1a75-115">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="c1a75-115">Possible values include the following:</span></span>



| <span data-ttu-id="c1a75-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c1a75-116">Return code</span></span>                                                                                             | <span data-ttu-id="c1a75-117">Description</span><span class="sxs-lookup"><span data-stu-id="c1a75-117">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="c1a75-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="c1a75-119">影片格式標頭未指定畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c1a75-119">Video format header does not specify a frame rate.</span></span><br/> |
| <dl> <span data-ttu-id="c1a75-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c1a75-121">成功。</span><span class="sxs-lookup"><span data-stu-id="c1a75-121">Success.</span></span><br/>                                           |
| <dl> <span data-ttu-id="c1a75-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="c1a75-123">無效引數。</span><span class="sxs-lookup"><span data-stu-id="c1a75-123">Invalid argument.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c1a75-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="c1a75-125">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="c1a75-125">**NULL** pointer argument.</span></span><br/>                         |
| <dl> <span data-ttu-id="c1a75-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="c1a75-127">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="c1a75-127">Invalid media type.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="c1a75-128">備註</span><span class="sxs-lookup"><span data-stu-id="c1a75-128">Remarks</span></span>

<span data-ttu-id="c1a75-129">這個方法無法從 ASF 檔案取得畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c1a75-129">This method cannot retrieve the frame rate from an ASF file.</span></span>

<span data-ttu-id="c1a75-130">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="c1a75-130">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="c1a75-131">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="c1a75-131">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="c1a75-132">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="c1a75-132">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="c1a75-133">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c1a75-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1a75-134">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c1a75-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1a75-135">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c1a75-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1a75-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1a75-136">Requirements</span></span>



| <span data-ttu-id="c1a75-137">需求</span><span class="sxs-lookup"><span data-stu-id="c1a75-137">Requirement</span></span> | <span data-ttu-id="c1a75-138">值</span><span class="sxs-lookup"><span data-stu-id="c1a75-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1a75-139">標頭</span><span class="sxs-lookup"><span data-stu-id="c1a75-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c1a75-140"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1a75-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1a75-141">Library</span></span><br/> | <dl> <span data-ttu-id="c1a75-142"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1a75-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1a75-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1a75-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1a75-144">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="c1a75-144">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="c1a75-145">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="c1a75-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




