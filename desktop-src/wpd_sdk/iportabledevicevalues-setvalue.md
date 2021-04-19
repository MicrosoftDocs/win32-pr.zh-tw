---
description: SetValue 方法會加入新的 PROPVARIANT 值，或覆寫現有值。
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues：： SetValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990593"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="55f73-103">IPortableDeviceValues：： SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="55f73-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="55f73-104">**SetValue** 方法會加入新的 **PROPVARIANT** 值，或覆寫現有值。</span><span class="sxs-lookup"><span data-stu-id="55f73-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f73-105">語法</span><span class="sxs-lookup"><span data-stu-id="55f73-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="55f73-106">參數</span><span class="sxs-lookup"><span data-stu-id="55f73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f73-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55f73-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f73-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="55f73-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="55f73-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55f73-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f73-110">指定新值的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="55f73-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="55f73-111">SDK 會複製值，讓呼叫端可以在呼叫這個方法之後呼叫 **PropVariantClear** ，藉以釋放本機變數。</span><span class="sxs-lookup"><span data-stu-id="55f73-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f73-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="55f73-112">Return value</span></span>

<span data-ttu-id="55f73-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="55f73-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="55f73-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="55f73-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="55f73-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="55f73-115">Return code</span></span>                                                                          | <span data-ttu-id="55f73-116">Description</span><span class="sxs-lookup"><span data-stu-id="55f73-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="55f73-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="55f73-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="55f73-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="55f73-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55f73-119">備註</span><span class="sxs-lookup"><span data-stu-id="55f73-119">Remarks</span></span>

<span data-ttu-id="55f73-120">當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援設定 **Null** 或零大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="55f73-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="55f73-121">例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。</span><span class="sxs-lookup"><span data-stu-id="55f73-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="55f73-122">這個方法可以用來從集合中取出任何型別的值。</span><span class="sxs-lookup"><span data-stu-id="55f73-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="55f73-123">但是，如果您事先知道值型別，請使用此介面的其中一個特製化 **Set ...** 方法，以避免直接使用 PROPVARIANT 值的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="55f73-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="55f73-124">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="55f73-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="55f73-125">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="55f73-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f73-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="55f73-126">Requirements</span></span>



| <span data-ttu-id="55f73-127">需求</span><span class="sxs-lookup"><span data-stu-id="55f73-127">Requirement</span></span> | <span data-ttu-id="55f73-128">值</span><span class="sxs-lookup"><span data-stu-id="55f73-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f73-129">標頭</span><span class="sxs-lookup"><span data-stu-id="55f73-129">Header</span></span><br/>  | <dl> <span data-ttu-id="55f73-130"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="55f73-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="55f73-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="55f73-131">Library</span></span><br/> | <dl> <span data-ttu-id="55f73-132"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="55f73-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f73-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55f73-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f73-134">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="55f73-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="55f73-135">**IPortableDeviceValues：： GetValue**</span><span class="sxs-lookup"><span data-stu-id="55f73-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="55f73-136">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="55f73-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




