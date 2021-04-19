---
description: SetPropertySetter 方法會設定物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。 在轉換和效果物件上呼叫這個方法。
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: 'IAMTimelineObj：： SetPropertySetter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983134"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a><span data-ttu-id="58b19-105">IAMTimelineObj：： SetPropertySetter 方法</span><span class="sxs-lookup"><span data-stu-id="58b19-105">IAMTimelineObj::SetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="58b19-106">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="58b19-106">\[Deprecated.</span></span> <span data-ttu-id="58b19-107">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="58b19-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58b19-108">`SetPropertySetter`方法會設定物件的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="58b19-108">The `SetPropertySetter` method sets the object's property setter.</span></span> <span data-ttu-id="58b19-109">當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。</span><span class="sxs-lookup"><span data-stu-id="58b19-109">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span> <span data-ttu-id="58b19-110">在轉換和效果物件上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="58b19-110">Call this method on transition and effect objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b19-111">語法</span><span class="sxs-lookup"><span data-stu-id="58b19-111">Syntax</span></span>


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="58b19-112">參數</span><span class="sxs-lookup"><span data-stu-id="58b19-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58b19-113">*newVal*</span><span class="sxs-lookup"><span data-stu-id="58b19-113">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="58b19-114">屬性 setter [**IPropertySetter**](ipropertysetter.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="58b19-114">Pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58b19-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="58b19-115">Return value</span></span>

<span data-ttu-id="58b19-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="58b19-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="58b19-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="58b19-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b19-118">備註</span><span class="sxs-lookup"><span data-stu-id="58b19-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58b19-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="58b19-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58b19-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="58b19-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58b19-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="58b19-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58b19-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="58b19-122">Requirements</span></span>



| <span data-ttu-id="58b19-123">需求</span><span class="sxs-lookup"><span data-stu-id="58b19-123">Requirement</span></span> | <span data-ttu-id="58b19-124">值</span><span class="sxs-lookup"><span data-stu-id="58b19-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58b19-125">標頭</span><span class="sxs-lookup"><span data-stu-id="58b19-125">Header</span></span><br/>  | <dl> <span data-ttu-id="58b19-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="58b19-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58b19-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="58b19-127">Library</span></span><br/> | <dl> <span data-ttu-id="58b19-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58b19-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58b19-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58b19-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b19-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="58b19-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="58b19-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="58b19-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




