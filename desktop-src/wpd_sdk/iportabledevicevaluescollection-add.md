---
description: Add 方法會將專案加入至集合。
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'IPortableDeviceValuesCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993959"
---
# <a name="iportabledevicevaluescollectionadd-method"></a><span data-ttu-id="13a6c-103">IPortableDeviceValuesCollection：： Add 方法</span><span class="sxs-lookup"><span data-stu-id="13a6c-103">IPortableDeviceValuesCollection::Add method</span></span>

<span data-ttu-id="13a6c-104">**Add** 方法會將專案加入至集合。</span><span class="sxs-lookup"><span data-stu-id="13a6c-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="13a6c-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a><span data-ttu-id="13a6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="13a6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a6c-107">*pValues* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13a6c-107">*pValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a6c-108">要加入至集合之 **IPortableDeviceValues** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="13a6c-108">Pointer to an **IPortableDeviceValues** interface to add to the collection.</span></span> <span data-ttu-id="13a6c-109">介面不會實際複製，但會在其上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="13a6c-109">The interface is not actually copied, but **AddRef** is called on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a6c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a6c-110">Return value</span></span>

<span data-ttu-id="13a6c-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="13a6c-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="13a6c-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="13a6c-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="13a6c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="13a6c-113">Return code</span></span>                                                                                   | <span data-ttu-id="13a6c-114">Description</span><span class="sxs-lookup"><span data-stu-id="13a6c-114">Description</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13a6c-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="13a6c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="13a6c-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="13a6c-116">The method succeeded.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="13a6c-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13a6c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="13a6c-118">沒有足夠的記憶體可將值新增至集合。</span><span class="sxs-lookup"><span data-stu-id="13a6c-118">There is not enough memory available to add the value to the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13a6c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a6c-119">Requirements</span></span>



| <span data-ttu-id="13a6c-120">需求</span><span class="sxs-lookup"><span data-stu-id="13a6c-120">Requirement</span></span> | <span data-ttu-id="13a6c-121">值</span><span class="sxs-lookup"><span data-stu-id="13a6c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a6c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="13a6c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="13a6c-123"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="13a6c-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="13a6c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="13a6c-124">Library</span></span><br/> | <dl> <span data-ttu-id="13a6c-125"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13a6c-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a6c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13a6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a6c-127">**IPortableDeviceValuesCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="13a6c-127">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




