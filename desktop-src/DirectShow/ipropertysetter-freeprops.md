---
description: FreeProps 方法會釋放 IPropertySetter：： GetProps 方法所配置的資源。 呼叫 GetProps 之後呼叫這個方法，並將 GetProps 傳回的結構傳遞給它。
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'IPropertySetter：： FreeProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987015"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="b6cc8-104">IPropertySetter：： FreeProps 方法</span><span class="sxs-lookup"><span data-stu-id="b6cc8-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="b6cc8-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-105">\[Deprecated.</span></span> <span data-ttu-id="b6cc8-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b6cc8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b6cc8-107">`FreeProps`方法會釋放 [**IPropertySetter：： GetProps**](ipropertysetter-getprops.md)方法所配置的資源。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="b6cc8-108">呼叫 **GetProps** 之後呼叫這個方法，並將 **GetProps** 傳回的結構傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6cc8-109">語法</span><span class="sxs-lookup"><span data-stu-id="b6cc8-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="b6cc8-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6cc8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6cc8-111">*cParams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6cc8-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6cc8-112">*PaParam* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="b6cc8-113">*paParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6cc8-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6cc8-114">[**DEXTER \_ PARAM**](dexter-param.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="b6cc8-115">*paValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b6cc8-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6cc8-116">[**DEXTER \_ 值**](dexter-value.md)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6cc8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6cc8-117">Return value</span></span>

<span data-ttu-id="b6cc8-118">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6cc8-119">備註</span><span class="sxs-lookup"><span data-stu-id="b6cc8-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6cc8-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b6cc8-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b6cc8-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b6cc8-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b6cc8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6cc8-123">Requirements</span></span>



| <span data-ttu-id="b6cc8-124">需求</span><span class="sxs-lookup"><span data-stu-id="b6cc8-124">Requirement</span></span> | <span data-ttu-id="b6cc8-125">值</span><span class="sxs-lookup"><span data-stu-id="b6cc8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6cc8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="b6cc8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b6cc8-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b6cc8-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b6cc8-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="b6cc8-128">Library</span></span><br/> | <dl> <span data-ttu-id="b6cc8-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6cc8-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6cc8-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6cc8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6cc8-131">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="b6cc8-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="b6cc8-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="b6cc8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




