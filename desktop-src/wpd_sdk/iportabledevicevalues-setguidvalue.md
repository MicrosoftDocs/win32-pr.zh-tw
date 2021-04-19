---
description: SetGuidValue 方法會將新的 GUID 值 (型別 VT 的 \_ CLSID) 或覆寫現有的。
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'IPortableDeviceValues：： SetGuidValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983055"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="0e6a4-103">IPortableDeviceValues：： SetGuidValue 方法</span><span class="sxs-lookup"><span data-stu-id="0e6a4-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="0e6a4-104">**SetGuidValue** 方法會將新的 **GUID** 值 (型別 VT 的 \_ CLSID) 或覆寫現有的。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e6a4-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="0e6a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e6a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6a4-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e6a4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6a4-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="0e6a4-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e6a4-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e6a4-110">包含新值的 **REFGUID** 。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6a4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e6a4-111">Return value</span></span>

<span data-ttu-id="0e6a4-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0e6a4-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0e6a4-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0e6a4-114">Return code</span></span>                                                                          | <span data-ttu-id="0e6a4-115">Description</span><span class="sxs-lookup"><span data-stu-id="0e6a4-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0e6a4-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0e6a4-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0e6a4-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e6a4-118">備註</span><span class="sxs-lookup"><span data-stu-id="0e6a4-118">Remarks</span></span>

<span data-ttu-id="0e6a4-119">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="0e6a4-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6a4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e6a4-120">Requirements</span></span>



| <span data-ttu-id="0e6a4-121">需求</span><span class="sxs-lookup"><span data-stu-id="0e6a4-121">Requirement</span></span> | <span data-ttu-id="0e6a4-122">值</span><span class="sxs-lookup"><span data-stu-id="0e6a4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6a4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0e6a4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0e6a4-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e6a4-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e6a4-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="0e6a4-125">Library</span></span><br/> | <dl> <span data-ttu-id="0e6a4-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e6a4-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6a4-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e6a4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6a4-128">將資源新增至物件</span><span class="sxs-lookup"><span data-stu-id="0e6a4-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="0e6a4-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="0e6a4-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0e6a4-130">**IPortableDeviceValues::GetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="0e6a4-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




