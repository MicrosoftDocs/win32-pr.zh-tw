---
description: GetSmartRecompressFormat 方法會抓取 smart recompression 目前的壓縮格式。
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'IAMTimelineGroup：： GetSmartRecompressFormat 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982634"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="2009b-103">IAMTimelineGroup：： GetSmartRecompressFormat 方法</span><span class="sxs-lookup"><span data-stu-id="2009b-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="2009b-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2009b-104">\[Deprecated.</span></span> <span data-ttu-id="2009b-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2009b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2009b-106">方法會抓取 `GetSmartRecompressFormat` smart recompression 目前的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="2009b-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="2009b-107">語法</span><span class="sxs-lookup"><span data-stu-id="2009b-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2009b-108">參數</span><span class="sxs-lookup"><span data-stu-id="2009b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2009b-109">*ppFormat*</span><span class="sxs-lookup"><span data-stu-id="2009b-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2009b-110">接收指向 [**SCompFmt0**](scompfmt0.md) 結構的指標，轉換為 long 的指標。</span><span class="sxs-lookup"><span data-stu-id="2009b-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="2009b-111">如果方法失敗，則會將值設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2009b-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2009b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2009b-112">Return value</span></span>

<span data-ttu-id="2009b-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2009b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2009b-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2009b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2009b-115">備註</span><span class="sxs-lookup"><span data-stu-id="2009b-115">Remarks</span></span>

<span data-ttu-id="2009b-116">如果應用程式未藉由呼叫 [**IAMTimelineGroup：： SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)) 來設定智慧型壓縮格式 (，這個方法所傳回的格式將會無效。</span><span class="sxs-lookup"><span data-stu-id="2009b-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="2009b-117">呼叫 [**IAMTimelineGroup：： IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) 方法，以判斷是否已設定壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="2009b-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="2009b-118">如果方法成功，則呼叫端必須釋放傳回的媒體類型，並刪除 [**SCompFmt0**](scompfmt0.md) 結構：</span><span class="sxs-lookup"><span data-stu-id="2009b-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="2009b-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2009b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2009b-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2009b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2009b-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2009b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2009b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2009b-122">Requirements</span></span>



| <span data-ttu-id="2009b-123">需求</span><span class="sxs-lookup"><span data-stu-id="2009b-123">Requirement</span></span> | <span data-ttu-id="2009b-124">值</span><span class="sxs-lookup"><span data-stu-id="2009b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2009b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2009b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2009b-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2009b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2009b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2009b-127">Library</span></span><br/> | <dl> <span data-ttu-id="2009b-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2009b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2009b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2009b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2009b-130">**IAMTimelineGroup 介面**</span><span class="sxs-lookup"><span data-stu-id="2009b-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="2009b-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2009b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




