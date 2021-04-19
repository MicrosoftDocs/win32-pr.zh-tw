---
description: Get \_ StreamType 方法會針對目前資料流程的媒體類型，抓取 (GUID) 的全域唯一識別碼。
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'IMediaDet：： get_StreamType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984826"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="4db9b-103">IMediaDet：： get \_ StreamType 方法</span><span class="sxs-lookup"><span data-stu-id="4db9b-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="4db9b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4db9b-104">\[Deprecated.</span></span> <span data-ttu-id="4db9b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4db9b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4db9b-106">`get_StreamType`方法會針對目前資料流程的媒體類型，抓取 (GUID) 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="4db9b-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="4db9b-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4db9b-108">參數</span><span class="sxs-lookup"><span data-stu-id="4db9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db9b-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4db9b-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4db9b-110">接收媒體類型的主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="4db9b-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db9b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4db9b-111">Return value</span></span>

<span data-ttu-id="4db9b-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4db9b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4db9b-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4db9b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4db9b-114">備註</span><span class="sxs-lookup"><span data-stu-id="4db9b-114">Remarks</span></span>

<span data-ttu-id="4db9b-115">這個方法會抓取 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的 **majortype** 成員。</span><span class="sxs-lookup"><span data-stu-id="4db9b-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="4db9b-116">**AM \_ 媒體 \_ 類型** 結構描述資料流程的格式，而 **majortype** 成員是指出一般類別的 GUID，例如音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="4db9b-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="4db9b-117">若為影片串流，GUID 為媒體媒體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4db9b-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="4db9b-118">若是音訊，則是媒體媒體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4db9b-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="4db9b-119">若要取出整個 **AM \_ 媒體 \_ 類型** 結構，請呼叫 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4db9b-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="4db9b-120">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="4db9b-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="4db9b-121">如果媒體偵測器處於點陣圖抓取模式，這個方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="4db9b-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="4db9b-122">如需詳細資訊，請參閱 [**IMediaDet：： EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)。</span><span class="sxs-lookup"><span data-stu-id="4db9b-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="4db9b-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4db9b-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4db9b-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4db9b-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4db9b-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4db9b-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4db9b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4db9b-126">Requirements</span></span>



| <span data-ttu-id="4db9b-127">需求</span><span class="sxs-lookup"><span data-stu-id="4db9b-127">Requirement</span></span> | <span data-ttu-id="4db9b-128">值</span><span class="sxs-lookup"><span data-stu-id="4db9b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4db9b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4db9b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4db9b-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4db9b-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4db9b-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="4db9b-131">Library</span></span><br/> | <dl> <span data-ttu-id="4db9b-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db9b-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db9b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4db9b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db9b-134">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="4db9b-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="4db9b-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4db9b-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




