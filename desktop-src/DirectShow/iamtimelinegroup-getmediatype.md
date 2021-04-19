---
description: GetMediaType 方法會抓取群組的未壓縮媒體類型。
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'IAMTimelineGroup：： GetMediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983245"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="325e2-103">IAMTimelineGroup：： GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="325e2-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="325e2-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="325e2-104">\[Deprecated.</span></span> <span data-ttu-id="325e2-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="325e2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="325e2-106">方法會抓取 `GetMediaType` 群組的未壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="325e2-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="325e2-107">語法</span><span class="sxs-lookup"><span data-stu-id="325e2-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="325e2-108">參數</span><span class="sxs-lookup"><span data-stu-id="325e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325e2-109">*pmt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="325e2-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="325e2-110">以媒體類型填滿的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="325e2-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325e2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="325e2-111">Return value</span></span>

<span data-ttu-id="325e2-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="325e2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="325e2-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="325e2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="325e2-114">備註</span><span class="sxs-lookup"><span data-stu-id="325e2-114">Remarks</span></span>

<span data-ttu-id="325e2-115">呼叫端必須釋放傳回的媒體類型的格式區塊，指定于所傳回的 AM \_ 媒體類型結構的 pbFormat 成員中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="325e2-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="325e2-116">您可以從基類庫使用 helper 函式 [**FreeMediaType**](freemediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="325e2-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="325e2-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="325e2-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="325e2-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="325e2-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="325e2-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="325e2-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="325e2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="325e2-120">Requirements</span></span>



| <span data-ttu-id="325e2-121">需求</span><span class="sxs-lookup"><span data-stu-id="325e2-121">Requirement</span></span> | <span data-ttu-id="325e2-122">值</span><span class="sxs-lookup"><span data-stu-id="325e2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="325e2-123">標頭</span><span class="sxs-lookup"><span data-stu-id="325e2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="325e2-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="325e2-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="325e2-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="325e2-125">Library</span></span><br/> | <dl> <span data-ttu-id="325e2-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="325e2-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="325e2-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="325e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="325e2-128">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="325e2-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="325e2-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="325e2-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




