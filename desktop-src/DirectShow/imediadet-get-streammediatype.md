---
description: Get \_ StreamMediaType 方法會抓取目前資料流程的媒體類型。 所有的影片串流都會轉換成 VIDEOINFOHEADER 類型，而所有音訊串流都會轉換成 WAVEFORMATEX 類型。
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'IMediaDet：： get_StreamMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981657"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="cf584-104">IMediaDet：： get \_ StreamMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="cf584-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="cf584-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="cf584-105">\[Deprecated.</span></span> <span data-ttu-id="cf584-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="cf584-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cf584-107">方法會抓取 `get_StreamMediaType` 目前資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="cf584-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="cf584-108">所有的影片串流都會轉換成 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 類型，而所有音訊串流都會轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 類型。</span><span class="sxs-lookup"><span data-stu-id="cf584-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf584-109">語法</span><span class="sxs-lookup"><span data-stu-id="cf584-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cf584-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf584-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf584-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="cf584-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf584-112">以媒體類型填滿的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cf584-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf584-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf584-113">Return value</span></span>

<span data-ttu-id="cf584-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cf584-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf584-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cf584-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf584-116">備註</span><span class="sxs-lookup"><span data-stu-id="cf584-116">Remarks</span></span>

<span data-ttu-id="cf584-117">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="cf584-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="cf584-118">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="cf584-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="cf584-119">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="cf584-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="cf584-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="cf584-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cf584-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cf584-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cf584-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="cf584-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf584-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf584-123">Requirements</span></span>



| <span data-ttu-id="cf584-124">需求</span><span class="sxs-lookup"><span data-stu-id="cf584-124">Requirement</span></span> | <span data-ttu-id="cf584-125">值</span><span class="sxs-lookup"><span data-stu-id="cf584-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf584-126">標頭</span><span class="sxs-lookup"><span data-stu-id="cf584-126">Header</span></span><br/>  | <dl> <span data-ttu-id="cf584-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf584-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cf584-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf584-128">Library</span></span><br/> | <dl> <span data-ttu-id="cf584-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf584-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf584-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf584-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf584-131">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="cf584-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="cf584-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="cf584-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
