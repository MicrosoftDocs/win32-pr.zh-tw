---
description: Put \_ 篩選方法會指定要使用之媒體偵測器的來源篩選。
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet：:p ut_Filter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992171"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="dcf78-103">IMediaDet：:p 的 ui \_ 篩選方法</span><span class="sxs-lookup"><span data-stu-id="dcf78-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="dcf78-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="dcf78-104">\[Deprecated.</span></span> <span data-ttu-id="dcf78-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="dcf78-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dcf78-106">`put_Filter`方法會指定要使用之媒體偵測器的來源篩選。</span><span class="sxs-lookup"><span data-stu-id="dcf78-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcf78-107">請勿將來源篩選新增至您自己的篩選圖形，或使用已在篩選圖形中的篩選。</span><span class="sxs-lookup"><span data-stu-id="dcf78-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="dcf78-108">媒體偵測器物件會自動建立內部篩選圖形，並將篩選準則放在另一個圖表中，可能會導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="dcf78-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dcf78-109">語法</span><span class="sxs-lookup"><span data-stu-id="dcf78-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="dcf78-110">參數</span><span class="sxs-lookup"><span data-stu-id="dcf78-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf78-111">*newVal* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcf78-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf78-112">來源篩選的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="dcf78-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf78-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcf78-113">Return value</span></span>

<span data-ttu-id="dcf78-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dcf78-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dcf78-115">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="dcf78-115">Possible values include the following:</span></span>



| <span data-ttu-id="dcf78-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dcf78-116">Return code</span></span>                                                                                   | <span data-ttu-id="dcf78-117">Description</span><span class="sxs-lookup"><span data-stu-id="dcf78-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="dcf78-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf78-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dcf78-119">成功。</span><span class="sxs-lookup"><span data-stu-id="dcf78-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="dcf78-120"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf78-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="dcf78-121">*newVal* 不會指向篩選。</span><span class="sxs-lookup"><span data-stu-id="dcf78-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="dcf78-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf78-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dcf78-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="dcf78-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="dcf78-124">備註</span><span class="sxs-lookup"><span data-stu-id="dcf78-124">Remarks</span></span>

<span data-ttu-id="dcf78-125">對於大部分的應用程式而言，使用原始程式檔的名稱呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md) 的檔案名稱方法會比較簡單。</span><span class="sxs-lookup"><span data-stu-id="dcf78-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="dcf78-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="dcf78-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcf78-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="dcf78-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dcf78-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="dcf78-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcf78-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcf78-129">Requirements</span></span>



| <span data-ttu-id="dcf78-130">需求</span><span class="sxs-lookup"><span data-stu-id="dcf78-130">Requirement</span></span> | <span data-ttu-id="dcf78-131">值</span><span class="sxs-lookup"><span data-stu-id="dcf78-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf78-132">標頭</span><span class="sxs-lookup"><span data-stu-id="dcf78-132">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf78-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf78-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dcf78-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcf78-134">Library</span></span><br/> | <dl> <span data-ttu-id="dcf78-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf78-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf78-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcf78-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf78-137">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="dcf78-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="dcf78-138">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="dcf78-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




