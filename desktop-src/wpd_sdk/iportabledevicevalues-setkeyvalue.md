---
description: SetKeyValue 方法會將新的 REFPROPERTYKEY 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'IPortableDeviceValues：： SetKeyValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982994"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="ee854-103">IPortableDeviceValues：： SetKeyValue 方法</span><span class="sxs-lookup"><span data-stu-id="ee854-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="ee854-104">**SetKeyValue** 方法會將新的 **REFPROPERTYKEY** 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="ee854-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee854-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee854-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="ee854-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee854-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee854-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee854-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee854-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="ee854-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ee854-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee854-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee854-110">指定新值的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="ee854-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee854-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee854-111">Return value</span></span>

<span data-ttu-id="ee854-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ee854-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ee854-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ee854-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ee854-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee854-114">Return code</span></span>                                                                          | <span data-ttu-id="ee854-115">Description</span><span class="sxs-lookup"><span data-stu-id="ee854-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ee854-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee854-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ee854-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ee854-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee854-118">備註</span><span class="sxs-lookup"><span data-stu-id="ee854-118">Remarks</span></span>

<span data-ttu-id="ee854-119">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="ee854-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="ee854-120">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="ee854-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee854-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee854-121">Requirements</span></span>



| <span data-ttu-id="ee854-122">需求</span><span class="sxs-lookup"><span data-stu-id="ee854-122">Requirement</span></span> | <span data-ttu-id="ee854-123">值</span><span class="sxs-lookup"><span data-stu-id="ee854-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee854-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ee854-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ee854-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee854-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee854-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee854-126">Library</span></span><br/> | <dl> <span data-ttu-id="ee854-127"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee854-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee854-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee854-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee854-129">將資源新增至物件</span><span class="sxs-lookup"><span data-stu-id="ee854-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ee854-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="ee854-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ee854-131">**IPortableDeviceValues::GetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="ee854-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




