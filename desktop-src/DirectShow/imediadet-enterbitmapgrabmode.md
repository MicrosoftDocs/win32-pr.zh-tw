---
description: EnterBitmapGrabMode 方法會將媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'IMediaDet：： EnterBitmapGrabMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b6c332451bc9ebb5f2ccf5068003c9a33617da21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983050"
---
# <a name="imediadetenterbitmapgrabmode-method"></a><span data-ttu-id="6d9b2-103">IMediaDet：： EnterBitmapGrabMode 方法</span><span class="sxs-lookup"><span data-stu-id="6d9b2-103">IMediaDet::EnterBitmapGrabMode method</span></span>

> [!Note]  
> <span data-ttu-id="6d9b2-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-104">\[Deprecated.</span></span> <span data-ttu-id="6d9b2-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6d9b2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d9b2-106">方法會將 `EnterBitmapGrabMode` 媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-106">The `EnterBitmapGrabMode` method switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9b2-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d9b2-107">Syntax</span></span>


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a><span data-ttu-id="6d9b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d9b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9b2-109">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="6d9b2-109">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6d9b2-110">圖表搜尋的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-110">Time, in seconds, to which the graph seeks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d9b2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d9b2-111">Return value</span></span>

<span data-ttu-id="6d9b2-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6d9b2-113">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="6d9b2-113">Possible values include the following:</span></span>



| <span data-ttu-id="6d9b2-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6d9b2-114">Return code</span></span>                                                                                             | <span data-ttu-id="6d9b2-115">Description</span><span class="sxs-lookup"><span data-stu-id="6d9b2-115">Description</span></span>                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6d9b2-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="6d9b2-117">成功。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-117">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6d9b2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="6d9b2-119">無效引數。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-119">Invalid argument.</span></span><br/>                             |
| <dl> <span data-ttu-id="6d9b2-120"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-120"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="6d9b2-121">來源檔案沒有影片串流。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-121">The source file does not have a video stream.</span></span><br/> |
| <dl> <span data-ttu-id="6d9b2-122"><dt>**VFW \_ 電子 \_ 時間已 \_ 過期**</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-122"><dt>**VFW\_E\_TIME\_EXPIRED**</dt></span></span> </dl>    | <span data-ttu-id="6d9b2-123">搜尋命令逾時。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-123">Seek command timed out.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="6d9b2-124">備註</span><span class="sxs-lookup"><span data-stu-id="6d9b2-124">Remarks</span></span>

<span data-ttu-id="6d9b2-125">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="6d9b2-125">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="6d9b2-126">這個方法會將 [**範例捕獲**](sample-grabber-filter.md) 篩選器插入至篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-126">This method inserts the [**Sample Grabber**](sample-grabber-filter.md) filter into the filter graph.</span></span> <span data-ttu-id="6d9b2-127">然後，您可以呼叫 [**IMediaDet：： GetSampleGrabber**](imediadet-getsamplegrabber.md) 來取得 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-127">You can then call [**IMediaDet::GetSampleGrabber**](imediadet-getsamplegrabber.md) to obtain a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span> <span data-ttu-id="6d9b2-128">一旦媒體偵測器進入點陣圖抓取模式， **IMediaDet** 中的各種資訊方法就無法運作。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-128">Once the media detector enters bitmap grab mode, the various informational methods in **IMediaDet** do not work.</span></span>

<span data-ttu-id="6d9b2-129">[**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md)或 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)方法也會將媒體偵測器放入點陣圖抓取模式。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-129">The [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md) methods also put the media detector into bitmap grab mode.</span></span>

> [!Note]  
> <span data-ttu-id="6d9b2-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d9b2-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d9b2-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6d9b2-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d9b2-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d9b2-133">Requirements</span></span>



| <span data-ttu-id="6d9b2-134">需求</span><span class="sxs-lookup"><span data-stu-id="6d9b2-134">Requirement</span></span> | <span data-ttu-id="6d9b2-135">值</span><span class="sxs-lookup"><span data-stu-id="6d9b2-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9b2-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6d9b2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="6d9b2-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d9b2-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d9b2-138">Library</span></span><br/> | <dl> <span data-ttu-id="6d9b2-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b2-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9b2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d9b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9b2-141">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="6d9b2-141">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="6d9b2-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6d9b2-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




