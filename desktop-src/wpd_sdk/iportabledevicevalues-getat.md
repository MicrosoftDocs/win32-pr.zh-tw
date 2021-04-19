---
description: GetAt 方法會使用提供的以零為基底的索引，從集合中抓取值。
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000839"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="090db-103">IPortableDeviceValues：： GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="090db-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="090db-104">**GetAt** 方法會使用提供的以零為基底的索引，從集合中抓取值。</span><span class="sxs-lookup"><span data-stu-id="090db-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="090db-105">語法</span><span class="sxs-lookup"><span data-stu-id="090db-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="090db-106">參數</span><span class="sxs-lookup"><span data-stu-id="090db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090db-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="090db-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090db-108">**DWORD** ，指定集合中以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="090db-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="090db-109">*pKey* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="090db-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="090db-110">選擇性的 **PROPERTYKEY** 指標，可抓取指定專案的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="090db-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="090db-111">*pValue* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="090db-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="090db-112">可抓取指定專案值的選擇性 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="090db-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="090db-113">呼叫端完成時，必須呼叫 **PropVariantClear** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="090db-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090db-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="090db-114">Return value</span></span>

<span data-ttu-id="090db-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="090db-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="090db-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="090db-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="090db-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="090db-117">Return code</span></span>                                                                                  | <span data-ttu-id="090db-118">Description</span><span class="sxs-lookup"><span data-stu-id="090db-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="090db-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="090db-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="090db-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="090db-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="090db-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="090db-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="090db-122">指定了不正確索引編號。</span><span class="sxs-lookup"><span data-stu-id="090db-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="090db-123">備註</span><span class="sxs-lookup"><span data-stu-id="090db-123">Remarks</span></span>

<span data-ttu-id="090db-124">如果屬性指出 [VT 不明] 類型的 \_ 值，則此屬性將會是其中一個 Windows 可攜式裝置 [**(IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)、 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)、 [**IPortableDeviceValues**](iportabledevicevalues.md) 或 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)) 。</span><span class="sxs-lookup"><span data-stu-id="090db-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="090db-125">Windows 可攜式裝置不能傳回其他介面。</span><span class="sxs-lookup"><span data-stu-id="090db-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="090db-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="090db-126">Requirements</span></span>



| <span data-ttu-id="090db-127">需求</span><span class="sxs-lookup"><span data-stu-id="090db-127">Requirement</span></span> | <span data-ttu-id="090db-128">值</span><span class="sxs-lookup"><span data-stu-id="090db-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090db-129">標頭</span><span class="sxs-lookup"><span data-stu-id="090db-129">Header</span></span><br/>  | <dl> <span data-ttu-id="090db-130"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="090db-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="090db-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="090db-131">Library</span></span><br/> | <dl> <span data-ttu-id="090db-132"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="090db-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090db-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="090db-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090db-134">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="090db-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="090db-135">**IPortableDeviceValues：： GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="090db-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




