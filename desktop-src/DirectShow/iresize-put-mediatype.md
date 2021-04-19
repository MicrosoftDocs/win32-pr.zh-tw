---
description: Put 媒體 \_ 型方法會在調整器篩選器上設定輸出媒體類型。
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize：:p ut_MediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978683"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="99e01-103">IResize：:p 的 ui \_ 媒體方法</span><span class="sxs-lookup"><span data-stu-id="99e01-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="99e01-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="99e01-104">\[Deprecated.</span></span> <span data-ttu-id="99e01-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="99e01-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="99e01-106">`put_MediaType`方法會在調整器篩選器上設定輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="99e01-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e01-107">語法</span><span class="sxs-lookup"><span data-stu-id="99e01-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="99e01-108">參數</span><span class="sxs-lookup"><span data-stu-id="99e01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e01-109">*pmt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99e01-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e01-110">包含媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="99e01-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e01-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="99e01-111">Return value</span></span>

<span data-ttu-id="99e01-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="99e01-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="99e01-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99e01-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e01-114">備註</span><span class="sxs-lookup"><span data-stu-id="99e01-114">Remarks</span></span>

<span data-ttu-id="99e01-115">DES 會先呼叫這個方法，然後再連接篩選器的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="99e01-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="99e01-116">使用媒體類型作為輸出釘選的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="99e01-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="99e01-117">在 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法中傳回此媒體類型，並在 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法中檢查 agsint 此類型。</span><span class="sxs-lookup"><span data-stu-id="99e01-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="99e01-118">在輸出連接之後，DES 永遠不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="99e01-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="99e01-119">目前，DES 一律會將輸出媒體類型設定為 **VIDEOINFOHEADER** 格式區塊的未壓縮 RGB 格式， (格式類型等於 format \_ VideoInfo) 。</span><span class="sxs-lookup"><span data-stu-id="99e01-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="99e01-120">子類型可能是 MEDIASUBTYPE \_ ARGB32，表示具有 Alpha 色板的32位 RGB。</span><span class="sxs-lookup"><span data-stu-id="99e01-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="99e01-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="99e01-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="99e01-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="99e01-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="99e01-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="99e01-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99e01-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="99e01-124">Requirements</span></span>



| <span data-ttu-id="99e01-125">需求</span><span class="sxs-lookup"><span data-stu-id="99e01-125">Requirement</span></span> | <span data-ttu-id="99e01-126">值</span><span class="sxs-lookup"><span data-stu-id="99e01-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e01-127">版本</span><span class="sxs-lookup"><span data-stu-id="99e01-127">Version</span></span><br/> | <span data-ttu-id="99e01-128">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="99e01-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="99e01-129">標頭</span><span class="sxs-lookup"><span data-stu-id="99e01-129">Header</span></span><br/>  | <dl> <span data-ttu-id="99e01-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="99e01-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="99e01-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="99e01-131">Library</span></span><br/> | <dl> <span data-ttu-id="99e01-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99e01-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e01-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99e01-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e01-134">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="99e01-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="99e01-135">**IResize 介面**</span><span class="sxs-lookup"><span data-stu-id="99e01-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




