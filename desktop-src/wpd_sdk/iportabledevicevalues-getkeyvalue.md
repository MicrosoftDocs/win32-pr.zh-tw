---
description: GetKeyValue 方法會抓取索引鍵所指定的 PROPERTYKEY 值。
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'IPortableDeviceValues：： GetKeyValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976043"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="e720f-103">IPortableDeviceValues：： GetKeyValue 方法</span><span class="sxs-lookup"><span data-stu-id="e720f-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="e720f-104">**GetKeyValue** 方法會抓取索引鍵所指定的 **PROPERTYKEY** 值。</span><span class="sxs-lookup"><span data-stu-id="e720f-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e720f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e720f-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e720f-106">參數</span><span class="sxs-lookup"><span data-stu-id="e720f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e720f-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e720f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e720f-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="e720f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e720f-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e720f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e720f-110">已抓取 **PROPERTYKEY** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="e720f-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e720f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e720f-111">Return value</span></span>

<span data-ttu-id="e720f-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="e720f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e720f-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="e720f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e720f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e720f-114">Return code</span></span>                                                                                                            | <span data-ttu-id="e720f-115">Description</span><span class="sxs-lookup"><span data-stu-id="e720f-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e720f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e720f-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e720f-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="e720f-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e720f-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e720f-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e720f-119">索引 *鍵* 所指定的屬性不是 **PROPERTYKEY** 類型。</span><span class="sxs-lookup"><span data-stu-id="e720f-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="e720f-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="e720f-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e720f-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="e720f-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="e720f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e720f-122">Requirements</span></span>



| <span data-ttu-id="e720f-123">需求</span><span class="sxs-lookup"><span data-stu-id="e720f-123">Requirement</span></span> | <span data-ttu-id="e720f-124">值</span><span class="sxs-lookup"><span data-stu-id="e720f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e720f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e720f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e720f-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="e720f-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e720f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e720f-127">Library</span></span><br/> | <dl> <span data-ttu-id="e720f-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e720f-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e720f-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e720f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e720f-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="e720f-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e720f-131">**IPortableDeviceValues::SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="e720f-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




