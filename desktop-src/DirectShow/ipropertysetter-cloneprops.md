---
description: CloneProps 方法會從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'IPropertySetter：： CloneProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998386"
---
# <a name="ipropertysettercloneprops-method"></a><span data-ttu-id="9d5ab-103">IPropertySetter：： CloneProps 方法</span><span class="sxs-lookup"><span data-stu-id="9d5ab-103">IPropertySetter::CloneProps method</span></span>

> [!Note]  
> <span data-ttu-id="9d5ab-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-104">\[Deprecated.</span></span> <span data-ttu-id="9d5ab-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9d5ab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9d5ab-106">`CloneProps`方法會從這個屬性 setter 複製一組屬性，並將其加入至新的屬性 setter。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-106">The `CloneProps` method clones a set of properties from this property setter and adds them to a new property setter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5ab-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d5ab-107">Syntax</span></span>


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a><span data-ttu-id="9d5ab-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d5ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5ab-109">*ppSetter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d5ab-109">*ppSetter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5ab-110">接收新屬性 setter 之 **IPropertySetter** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-110">Receives a pointer to the **IPropertySetter** interface of the new property setter.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ab-111">*rtStart* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d5ab-111">*rtStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5ab-112">要複製之值範圍的開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-112">Start time of the range of values to clone, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="9d5ab-113">*rtStop* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d5ab-113">*rtStop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d5ab-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5ab-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d5ab-115">Return value</span></span>

<span data-ttu-id="9d5ab-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d5ab-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5ab-118">備註</span><span class="sxs-lookup"><span data-stu-id="9d5ab-118">Remarks</span></span>

<span data-ttu-id="9d5ab-119">只會複製在指定開始時間之後的值。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-119">Only values that fall after the specified start time are cloned.</span></span> <span data-ttu-id="9d5ab-120">然後，會根據開始時間調整複製值的時間。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-120">The times on the cloned values are then adjusted relative to the start time.</span></span> <span data-ttu-id="9d5ab-121">例如，如果 *rtStart* 為 20000000 (2 秒) ，則時間 30000000 (3) 秒的值會以時間 10000000 (1 秒) 進行複製。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-121">For example, if *rtStart* is 20000000 (2 seconds), then a value at time 30000000 (3 seconds) is cloned with time 10000000 (1 second).</span></span> <span data-ttu-id="9d5ab-122">最後，每個複製的屬性都會有一個初始值，其初始值等於開始時間的原始屬性值 (正確地插入（如有必要）) 。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-122">Finally, each cloned property is given an initial value equal to the value of the original property at the start time (correctly interpolated if necessary).</span></span> <span data-ttu-id="9d5ab-123">實際上，屬性資料會在指定的開始時間進行分割。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-123">In effect, the property data is split at the specified start time.</span></span>

<span data-ttu-id="9d5ab-124">如果方法成功，則傳回的 [**IPropertySetter**](ipropertysetter.md) 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-124">If the method succeeds, the [**IPropertySetter**](ipropertysetter.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="9d5ab-125">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="9d5ab-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9d5ab-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9d5ab-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="9d5ab-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d5ab-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d5ab-129">Requirements</span></span>



| <span data-ttu-id="9d5ab-130">需求</span><span class="sxs-lookup"><span data-stu-id="9d5ab-130">Requirement</span></span> | <span data-ttu-id="9d5ab-131">值</span><span class="sxs-lookup"><span data-stu-id="9d5ab-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5ab-132">標頭</span><span class="sxs-lookup"><span data-stu-id="9d5ab-132">Header</span></span><br/>  | <dl> <span data-ttu-id="9d5ab-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ab-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9d5ab-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d5ab-134">Library</span></span><br/> | <dl> <span data-ttu-id="9d5ab-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d5ab-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5ab-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d5ab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5ab-137">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="9d5ab-137">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="9d5ab-138">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="9d5ab-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




