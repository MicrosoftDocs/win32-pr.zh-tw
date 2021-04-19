---
description: GetPropertySetter 方法會抓取物件的屬性 setter。 當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj：： GetPropertySetter 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990949"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="20798-104">IAMTimelineObj：： GetPropertySetter 方法</span><span class="sxs-lookup"><span data-stu-id="20798-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="20798-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="20798-105">\[Deprecated.</span></span> <span data-ttu-id="20798-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="20798-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="20798-107">方法會抓取 `GetPropertySetter` 物件的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="20798-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="20798-108">當物件呈現時，屬性 setter 中包含的屬性資訊會套用至物件。</span><span class="sxs-lookup"><span data-stu-id="20798-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="20798-109">語法</span><span class="sxs-lookup"><span data-stu-id="20798-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="20798-110">參數</span><span class="sxs-lookup"><span data-stu-id="20798-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20798-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="20798-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="20798-112">接收屬性 setter [**IPropertySetter**](ipropertysetter.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="20798-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="20798-113">如果物件沒有屬性 setter，此值會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="20798-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20798-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="20798-114">Return value</span></span>

<span data-ttu-id="20798-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="20798-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20798-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="20798-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20798-117">備註</span><span class="sxs-lookup"><span data-stu-id="20798-117">Remarks</span></span>

<span data-ttu-id="20798-118">如果 *pVal* 中傳回的值不是 **Null**，則 **IPropertySetter** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="20798-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="20798-119">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="20798-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="20798-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="20798-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="20798-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="20798-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="20798-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="20798-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20798-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="20798-123">Requirements</span></span>



| <span data-ttu-id="20798-124">需求</span><span class="sxs-lookup"><span data-stu-id="20798-124">Requirement</span></span> | <span data-ttu-id="20798-125">值</span><span class="sxs-lookup"><span data-stu-id="20798-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20798-126">標頭</span><span class="sxs-lookup"><span data-stu-id="20798-126">Header</span></span><br/>  | <dl> <span data-ttu-id="20798-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="20798-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="20798-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="20798-128">Library</span></span><br/> | <dl> <span data-ttu-id="20798-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="20798-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20798-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20798-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20798-131">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="20798-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="20798-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="20798-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




