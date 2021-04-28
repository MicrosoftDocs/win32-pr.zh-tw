---
description: IPortableDeviceValues：： Clear 方法-Clear 方法會刪除集合中的所有專案。
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'IPortableDeviceValues：： Clear 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109896"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="df11a-103">IPortableDeviceValues：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="df11a-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="df11a-104">**Clear** 方法會刪除集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="df11a-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="df11a-105">語法</span><span class="sxs-lookup"><span data-stu-id="df11a-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="df11a-106">參數</span><span class="sxs-lookup"><span data-stu-id="df11a-106">Parameters</span></span>

<span data-ttu-id="df11a-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="df11a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df11a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="df11a-108">Return value</span></span>

<span data-ttu-id="df11a-109">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="df11a-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="df11a-110">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="df11a-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="df11a-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="df11a-111">Return code</span></span>                                                                          | <span data-ttu-id="df11a-112">Description</span><span class="sxs-lookup"><span data-stu-id="df11a-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="df11a-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="df11a-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df11a-114">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="df11a-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df11a-115">備註</span><span class="sxs-lookup"><span data-stu-id="df11a-115">Remarks</span></span>

<span data-ttu-id="df11a-116">這個方法會釋出集合中所有動態設定項目的記憶體。</span><span class="sxs-lookup"><span data-stu-id="df11a-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="df11a-117">針對介面，它會呼叫 **Release**。</span><span class="sxs-lookup"><span data-stu-id="df11a-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df11a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="df11a-118">Requirements</span></span>



| <span data-ttu-id="df11a-119">需求</span><span class="sxs-lookup"><span data-stu-id="df11a-119">Requirement</span></span> | <span data-ttu-id="df11a-120">值</span><span class="sxs-lookup"><span data-stu-id="df11a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df11a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="df11a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="df11a-122"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="df11a-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="df11a-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="df11a-123">Library</span></span><br/> | <dl> <span data-ttu-id="df11a-124"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="df11a-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df11a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df11a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df11a-126">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="df11a-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




