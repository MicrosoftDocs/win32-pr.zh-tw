---
description: SetUnsignedIntegerValue 方法會將新的 ULONG 值新增 (型別 VT \_ UI4) 或覆寫現有的值。
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'IPortableDeviceValues：： SetUnsignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981282"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="fd55b-103">IPortableDeviceValues：： SetUnsignedIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="fd55b-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="fd55b-104">**SetUnsignedIntegerValue** 方法會將新的 **ULONG** 值新增 (型別 VT \_ UI4) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="fd55b-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd55b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fd55b-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="fd55b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fd55b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd55b-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd55b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd55b-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="fd55b-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="fd55b-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd55b-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd55b-110">指定新值的 **ULONG** 。</span><span class="sxs-lookup"><span data-stu-id="fd55b-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd55b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd55b-111">Return value</span></span>

<span data-ttu-id="fd55b-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="fd55b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd55b-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="fd55b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd55b-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fd55b-114">Return code</span></span>                                                                          | <span data-ttu-id="fd55b-115">Description</span><span class="sxs-lookup"><span data-stu-id="fd55b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd55b-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fd55b-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd55b-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="fd55b-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd55b-118">備註</span><span class="sxs-lookup"><span data-stu-id="fd55b-118">Remarks</span></span>

<span data-ttu-id="fd55b-119">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="fd55b-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="fd55b-120">範例</span><span class="sxs-lookup"><span data-stu-id="fd55b-120">Examples</span></span>

<span data-ttu-id="fd55b-121">如需如何使用此方法的範例，請參閱 [**指定用戶端資訊**](specifying-client-information.md)。</span><span class="sxs-lookup"><span data-stu-id="fd55b-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd55b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd55b-122">Requirements</span></span>



| <span data-ttu-id="fd55b-123">需求</span><span class="sxs-lookup"><span data-stu-id="fd55b-123">Requirement</span></span> | <span data-ttu-id="fd55b-124">值</span><span class="sxs-lookup"><span data-stu-id="fd55b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd55b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="fd55b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fd55b-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd55b-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd55b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="fd55b-127">Library</span></span><br/> | <dl> <span data-ttu-id="fd55b-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd55b-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd55b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd55b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd55b-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="fd55b-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="fd55b-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="fd55b-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="fd55b-132">**指定用戶端資訊**</span><span class="sxs-lookup"><span data-stu-id="fd55b-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




