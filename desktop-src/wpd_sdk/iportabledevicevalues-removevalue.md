---
description: RemoveValue 方法會從集合中移除專案。
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'IPortableDeviceValues：： RemoveValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982552"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="2dcd7-103">IPortableDeviceValues：： RemoveValue 方法</span><span class="sxs-lookup"><span data-stu-id="2dcd7-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="2dcd7-104">**RemoveValue** 方法會從集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="2dcd7-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dcd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="2dcd7-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="2dcd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="2dcd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dcd7-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2dcd7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dcd7-108">指定要移除之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="2dcd7-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dcd7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2dcd7-109">Return value</span></span>

<span data-ttu-id="2dcd7-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="2dcd7-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2dcd7-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="2dcd7-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2dcd7-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2dcd7-112">Return code</span></span>                                                                          | <span data-ttu-id="2dcd7-113">Description</span><span class="sxs-lookup"><span data-stu-id="2dcd7-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2dcd7-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2dcd7-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2dcd7-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="2dcd7-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2dcd7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dcd7-116">Requirements</span></span>



| <span data-ttu-id="2dcd7-117">需求</span><span class="sxs-lookup"><span data-stu-id="2dcd7-117">Requirement</span></span> | <span data-ttu-id="2dcd7-118">值</span><span class="sxs-lookup"><span data-stu-id="2dcd7-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dcd7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2dcd7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2dcd7-120"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="2dcd7-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dcd7-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="2dcd7-121">Library</span></span><br/> | <dl> <span data-ttu-id="2dcd7-122"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dcd7-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dcd7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dcd7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dcd7-124">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="2dcd7-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2dcd7-125">**IPortableDeviceValues：： GetValue**</span><span class="sxs-lookup"><span data-stu-id="2dcd7-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="2dcd7-126">**IPortableDeviceValues：： SetValue**</span><span class="sxs-lookup"><span data-stu-id="2dcd7-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




