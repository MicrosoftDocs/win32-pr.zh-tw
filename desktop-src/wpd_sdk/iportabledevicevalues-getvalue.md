---
description: GetValue 方法會抓取索引鍵所指定的 PROPVARIANT 值。
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'IPortableDeviceValues：： GetValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993988"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="d18e9-103">IPortableDeviceValues：： GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="d18e9-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="d18e9-104">**GetValue** 方法會抓取索引鍵所指定的 **PROPVARIANT** 值。</span><span class="sxs-lookup"><span data-stu-id="d18e9-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="d18e9-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d18e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="d18e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18e9-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d18e9-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d18e9-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d18e9-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d18e9-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d18e9-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d18e9-110">已抓取 **PROPVARIANT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="d18e9-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="d18e9-111">呼叫端完成時，必須呼叫 **PropVariantClear** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="d18e9-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18e9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d18e9-112">Return value</span></span>

<span data-ttu-id="d18e9-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d18e9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d18e9-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d18e9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d18e9-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d18e9-115">Return code</span></span>                                                                                                            | <span data-ttu-id="d18e9-116">Description</span><span class="sxs-lookup"><span data-stu-id="d18e9-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="d18e9-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d18e9-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d18e9-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d18e9-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d18e9-119"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="d18e9-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d18e9-120">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="d18e9-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d18e9-121">備註</span><span class="sxs-lookup"><span data-stu-id="d18e9-121">Remarks</span></span>

<span data-ttu-id="d18e9-122">當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援取出 **Null** 或零大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d18e9-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="d18e9-123">例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。</span><span class="sxs-lookup"><span data-stu-id="d18e9-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="d18e9-124">這個方法可以用來從集合中取出任何型別的值。</span><span class="sxs-lookup"><span data-stu-id="d18e9-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="d18e9-125">但是，如果您事先知道值型別，請使用此介面的其中一個特製化抓取方法，以避免直接使用 PROPVARIANT 值的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="d18e9-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d18e9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d18e9-126">Requirements</span></span>



| <span data-ttu-id="d18e9-127">需求</span><span class="sxs-lookup"><span data-stu-id="d18e9-127">Requirement</span></span> | <span data-ttu-id="d18e9-128">值</span><span class="sxs-lookup"><span data-stu-id="d18e9-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18e9-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d18e9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d18e9-130"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="d18e9-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d18e9-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d18e9-131">Library</span></span><br/> | <dl> <span data-ttu-id="d18e9-132"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d18e9-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18e9-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d18e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18e9-134">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d18e9-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d18e9-135">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="d18e9-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="d18e9-136">**IPortableDeviceValues：： SetValue**</span><span class="sxs-lookup"><span data-stu-id="d18e9-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




