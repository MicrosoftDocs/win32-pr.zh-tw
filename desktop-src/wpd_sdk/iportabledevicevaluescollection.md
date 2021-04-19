---
description: IPortableDeviceValuesCollection 介面會保存以零為基底的索引 IPortableDeviceValues 介面集合。
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: 'IPortableDeviceValuesCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993957"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="673c8-103">IPortableDeviceValuesCollection 介面</span><span class="sxs-lookup"><span data-stu-id="673c8-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="673c8-104">**IPortableDeviceValuesCollection** 介面會保存以零為基底的索引 **IPortableDeviceValues** 介面集合。</span><span class="sxs-lookup"><span data-stu-id="673c8-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="673c8-105">您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDeviceValuesCollection** 呼叫 **CoCreate** 。</span><span class="sxs-lookup"><span data-stu-id="673c8-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="673c8-106">成員</span><span class="sxs-lookup"><span data-stu-id="673c8-106">Members</span></span>

<span data-ttu-id="673c8-107">**IPortableDeviceValuesCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="673c8-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="673c8-108">**IPortableDeviceValuesCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="673c8-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="673c8-109">方法</span><span class="sxs-lookup"><span data-stu-id="673c8-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="673c8-110">方法</span><span class="sxs-lookup"><span data-stu-id="673c8-110">Methods</span></span>

<span data-ttu-id="673c8-111">**IPortableDeviceValuesCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="673c8-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="673c8-112">方法</span><span class="sxs-lookup"><span data-stu-id="673c8-112">Method</span></span>                                                       | <span data-ttu-id="673c8-113">描述</span><span class="sxs-lookup"><span data-stu-id="673c8-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="673c8-114">**添加**</span><span class="sxs-lookup"><span data-stu-id="673c8-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="673c8-115">將項目加入集合</span><span class="sxs-lookup"><span data-stu-id="673c8-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="673c8-116">**清楚**</span><span class="sxs-lookup"><span data-stu-id="673c8-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="673c8-117">釋放集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="673c8-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="673c8-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="673c8-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="673c8-119">以零為基底的索引，從集合中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="673c8-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="673c8-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="673c8-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="673c8-121">抓取集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="673c8-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="673c8-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="673c8-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="673c8-123">移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="673c8-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="673c8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="673c8-124">Requirements</span></span>



| <span data-ttu-id="673c8-125">需求</span><span class="sxs-lookup"><span data-stu-id="673c8-125">Requirement</span></span> | <span data-ttu-id="673c8-126">值</span><span class="sxs-lookup"><span data-stu-id="673c8-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="673c8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="673c8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="673c8-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="673c8-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="673c8-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="673c8-129">Library</span></span><br/> | <dl> <span data-ttu-id="673c8-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="673c8-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673c8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="673c8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673c8-132">**集合介面**</span><span class="sxs-lookup"><span data-stu-id="673c8-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

