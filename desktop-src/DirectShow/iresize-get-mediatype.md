---
description: 取得媒體型別方法會傳回檔整 \_ 器篩選的目前輸出媒體類型。
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'IResize：： get_MediaType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000478"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="5190e-103">IResize：： get \_ 媒體方法</span><span class="sxs-lookup"><span data-stu-id="5190e-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="5190e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5190e-104">\[Deprecated.</span></span> <span data-ttu-id="5190e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5190e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5190e-106">方法會傳回檔整 `get_MediaType` 器篩選的目前輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5190e-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5190e-107">語法</span><span class="sxs-lookup"><span data-stu-id="5190e-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="5190e-108">參數</span><span class="sxs-lookup"><span data-stu-id="5190e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5190e-109">*pmt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5190e-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5190e-110">由呼叫端配置的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="5190e-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="5190e-111">方法會以媒體類型來填滿此結構。</span><span class="sxs-lookup"><span data-stu-id="5190e-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="5190e-112">呼叫端必須釋放格式區塊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="5190e-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5190e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5190e-113">Return value</span></span>

<span data-ttu-id="5190e-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5190e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5190e-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5190e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5190e-116">備註</span><span class="sxs-lookup"><span data-stu-id="5190e-116">Remarks</span></span>

<span data-ttu-id="5190e-117">如果輸出媒體類型尚未設定，則會傳回預設的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5190e-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="5190e-118">當呼叫 **put \_** 媒體類型或 **put \_ 大小** 方法時，篩選必須更新其輸出媒體類型; 所傳回的媒體類型 `get_MediaType` 必須反映這些變更。</span><span class="sxs-lookup"><span data-stu-id="5190e-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="5190e-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5190e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5190e-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5190e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5190e-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5190e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5190e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5190e-122">Requirements</span></span>



| <span data-ttu-id="5190e-123">需求</span><span class="sxs-lookup"><span data-stu-id="5190e-123">Requirement</span></span> | <span data-ttu-id="5190e-124">值</span><span class="sxs-lookup"><span data-stu-id="5190e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5190e-125">版本</span><span class="sxs-lookup"><span data-stu-id="5190e-125">Version</span></span><br/> | <span data-ttu-id="5190e-126">DirectX 9.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5190e-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="5190e-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5190e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5190e-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5190e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5190e-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="5190e-129">Library</span></span><br/> | <dl> <span data-ttu-id="5190e-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5190e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5190e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5190e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5190e-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5190e-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5190e-133">**IResize 介面**</span><span class="sxs-lookup"><span data-stu-id="5190e-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




