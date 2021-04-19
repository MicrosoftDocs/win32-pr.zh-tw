---
description: SetIPortableDeviceValuesCollectionValue 方法會將新的 IPortableDeviceValuesCollection 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'IPortableDeviceValues：： SetIPortableDeviceValuesCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3f0c545a4daceed75971b0e659f85d72eca6d98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990173"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="e3e6a-103">IPortableDeviceValues：： SetIPortableDeviceValuesCollectionValue 方法</span><span class="sxs-lookup"><span data-stu-id="e3e6a-103">IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="e3e6a-104">**SetIPortableDeviceValuesCollectionValue** 方法會將新的 **IPortableDeviceValuesCollection** 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-104">The **SetIPortableDeviceValuesCollectionValue** method adds a new **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e6a-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3e6a-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e3e6a-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3e6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3e6a-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3e6a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e6a-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e3e6a-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3e6a-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3e6a-110">**IPortableDeviceValuesCollection** 介面的指標，指定新的值。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-110">Pointer to an **IPortableDeviceValuesCollection** interface that specifies the new value.</span></span> <span data-ttu-id="e3e6a-111">SDK 會將參考複製到已提交的介面，並在其上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3e6a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3e6a-112">Return value</span></span>

<span data-ttu-id="e3e6a-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e3e6a-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e3e6a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e3e6a-115">Return code</span></span>                                                                          | <span data-ttu-id="e3e6a-116">Description</span><span class="sxs-lookup"><span data-stu-id="e3e6a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e3e6a-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e3e6a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e3e6a-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3e6a-119">備註</span><span class="sxs-lookup"><span data-stu-id="e3e6a-119">Remarks</span></span>

<span data-ttu-id="e3e6a-120">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="e3e6a-121">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="e3e6a-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e6a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3e6a-122">Requirements</span></span>



| <span data-ttu-id="e3e6a-123">需求</span><span class="sxs-lookup"><span data-stu-id="e3e6a-123">Requirement</span></span> | <span data-ttu-id="e3e6a-124">值</span><span class="sxs-lookup"><span data-stu-id="e3e6a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e6a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e3e6a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e3e6a-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3e6a-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3e6a-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3e6a-127">Library</span></span><br/> | <dl> <span data-ttu-id="e3e6a-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3e6a-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e6a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3e6a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e6a-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="e3e6a-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e3e6a-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="e3e6a-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




