---
description: ClearProps 方法會清除屬性 setter 中的所有屬性資料。 應用程式可以在呼叫這個函數之後設定新的屬性資料。
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'IPropertySetter：： ClearProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995635"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="c0b32-104">IPropertySetter：： ClearProps 方法</span><span class="sxs-lookup"><span data-stu-id="c0b32-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="c0b32-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c0b32-105">\[Deprecated.</span></span> <span data-ttu-id="c0b32-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c0b32-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c0b32-107">`ClearProps`方法會清除屬性 setter 中的所有屬性資料。</span><span class="sxs-lookup"><span data-stu-id="c0b32-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="c0b32-108">應用程式可以在呼叫這個函數之後設定新的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="c0b32-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="c0b32-109">清除屬性資料並不會將物件的屬性還原為其原始值。</span><span class="sxs-lookup"><span data-stu-id="c0b32-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="c0b32-110">它只會防止 DirectShow 套用任何進一步的變更。</span><span class="sxs-lookup"><span data-stu-id="c0b32-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="c0b32-111">當專案呈現時，會在執行時間套用屬性值。</span><span class="sxs-lookup"><span data-stu-id="c0b32-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b32-112">語法</span><span class="sxs-lookup"><span data-stu-id="c0b32-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="c0b32-113">參數</span><span class="sxs-lookup"><span data-stu-id="c0b32-113">Parameters</span></span>

<span data-ttu-id="c0b32-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0b32-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0b32-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0b32-115">Return value</span></span>

<span data-ttu-id="c0b32-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c0b32-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0b32-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c0b32-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b32-118">備註</span><span class="sxs-lookup"><span data-stu-id="c0b32-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0b32-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c0b32-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c0b32-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c0b32-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c0b32-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c0b32-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0b32-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0b32-122">Requirements</span></span>



| <span data-ttu-id="c0b32-123">需求</span><span class="sxs-lookup"><span data-stu-id="c0b32-123">Requirement</span></span> | <span data-ttu-id="c0b32-124">值</span><span class="sxs-lookup"><span data-stu-id="c0b32-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b32-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c0b32-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0b32-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b32-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c0b32-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="c0b32-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0b32-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0b32-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0b32-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0b32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b32-130">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="c0b32-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c0b32-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="c0b32-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




