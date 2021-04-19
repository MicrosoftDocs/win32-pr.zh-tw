---
description: SetIPortableDeviceValuesValue 方法會將新的 IPortableDeviceValues 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'IPortableDeviceValues：： SetIPortableDeviceValuesValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990046"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a><span data-ttu-id="07335-103">IPortableDeviceValues：： SetIPortableDeviceValuesValue 方法</span><span class="sxs-lookup"><span data-stu-id="07335-103">IPortableDeviceValues::SetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="07335-104">**SetIPortableDeviceValuesValue** 方法會將新的 **IPortableDeviceValues** 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="07335-104">The **SetIPortableDeviceValuesValue** method adds a new **IPortableDeviceValues** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="07335-105">語法</span><span class="sxs-lookup"><span data-stu-id="07335-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="07335-106">參數</span><span class="sxs-lookup"><span data-stu-id="07335-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07335-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07335-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07335-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="07335-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="07335-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07335-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07335-110">**IPortableDeviceValues** 介面的指標，指定新的值。</span><span class="sxs-lookup"><span data-stu-id="07335-110">Pointer to an **IPortableDeviceValues** interface that specifies the new value.</span></span> <span data-ttu-id="07335-111">SDK 會將參考複製到已提交的介面，並在其上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="07335-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07335-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="07335-112">Return value</span></span>

<span data-ttu-id="07335-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="07335-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="07335-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="07335-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="07335-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="07335-115">Return code</span></span>                                                                          | <span data-ttu-id="07335-116">Description</span><span class="sxs-lookup"><span data-stu-id="07335-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="07335-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="07335-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="07335-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="07335-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07335-119">備註</span><span class="sxs-lookup"><span data-stu-id="07335-119">Remarks</span></span>

<span data-ttu-id="07335-120">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="07335-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="07335-121">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="07335-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="07335-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="07335-122">Requirements</span></span>



| <span data-ttu-id="07335-123">需求</span><span class="sxs-lookup"><span data-stu-id="07335-123">Requirement</span></span> | <span data-ttu-id="07335-124">值</span><span class="sxs-lookup"><span data-stu-id="07335-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07335-125">標頭</span><span class="sxs-lookup"><span data-stu-id="07335-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07335-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="07335-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="07335-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="07335-127">Library</span></span><br/> | <dl> <span data-ttu-id="07335-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07335-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07335-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07335-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07335-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="07335-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="07335-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="07335-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




