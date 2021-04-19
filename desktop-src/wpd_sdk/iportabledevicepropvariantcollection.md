---
description: IPortableDevicePropVariantCollection 介面會保存相同 VARTYPE 之索引 PROPVARIANT 值的集合。
ms.assetid: 41224958-a5a0-4e09-8733-d0ae036f68b9
title: 'IPortableDevicePropVariantCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 14ba07894c74567487704bb1f63e7242542af313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000752"
---
# <a name="iportabledevicepropvariantcollection-interface"></a><span data-ttu-id="2b439-103">IPortableDevicePropVariantCollection 介面</span><span class="sxs-lookup"><span data-stu-id="2b439-103">IPortableDevicePropVariantCollection interface</span></span>

<span data-ttu-id="2b439-104">**IPortableDevicePropVariantCollection** 介面會保存相同 VARTYPE 之索引 **PROPVARIANT** 值的集合。</span><span class="sxs-lookup"><span data-stu-id="2b439-104">The **IPortableDevicePropVariantCollection** interface holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="2b439-105">加入至集合的第一個專案的 VARTYPE 會決定集合的 VARTYPE。</span><span class="sxs-lookup"><span data-stu-id="2b439-105">The VARTYPE of the first item that is added to the collection determines the VARTYPE of the collection.</span></span> <span data-ttu-id="2b439-106">如果 **PROPVARIANT** 值無法變更為集合的目前 VARTYPE，嘗試加入不同 VARTYPE 的專案可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="2b439-106">An attempt to add an item of a different VARTYPE may fail if the **PROPVARIANT** value cannot be changed to the collection's current VARTYPE.</span></span> <span data-ttu-id="2b439-107">若要變更集合的 VARTYPE，請呼叫 **ChangeType**。</span><span class="sxs-lookup"><span data-stu-id="2b439-107">To change the VARTYPE of the collection, call **ChangeType**.</span></span>

<span data-ttu-id="2b439-108">您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDevicePropVariantCollection** 呼叫 **CoCreate** 。</span><span class="sxs-lookup"><span data-stu-id="2b439-108">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDevicePropVariantCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="2b439-109">成員</span><span class="sxs-lookup"><span data-stu-id="2b439-109">Members</span></span>

<span data-ttu-id="2b439-110">**IPortableDevicePropVariantCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="2b439-110">The **IPortableDevicePropVariantCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2b439-111">**IPortableDevicePropVariantCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="2b439-111">**IPortableDevicePropVariantCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="2b439-112">方法</span><span class="sxs-lookup"><span data-stu-id="2b439-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2b439-113">方法</span><span class="sxs-lookup"><span data-stu-id="2b439-113">Methods</span></span>

<span data-ttu-id="2b439-114">**IPortableDevicePropVariantCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="2b439-114">The **IPortableDevicePropVariantCollection** interface has these methods.</span></span>



| <span data-ttu-id="2b439-115">方法</span><span class="sxs-lookup"><span data-stu-id="2b439-115">Method</span></span>                                                                | <span data-ttu-id="2b439-116">描述</span><span class="sxs-lookup"><span data-stu-id="2b439-116">Description</span></span>                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b439-117">**添加**</span><span class="sxs-lookup"><span data-stu-id="2b439-117">**Add**</span></span>](iportabledevicepropvariantcollection-add.md)               | <span data-ttu-id="2b439-118">將項目新增至集合。</span><span class="sxs-lookup"><span data-stu-id="2b439-118">Adds an item to the collection.</span></span><br/>                                          |
| [<span data-ttu-id="2b439-119">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="2b439-119">**ChangeType**</span></span>](iportabledevicepropvariantcollection-changetype.md) | <span data-ttu-id="2b439-120">將集合中的所有專案轉換為指定的 VARTYPE。</span><span class="sxs-lookup"><span data-stu-id="2b439-120">Converts all items in the collection to the specified VARTYPE.</span></span><br/>           |
| [<span data-ttu-id="2b439-121">**清楚**</span><span class="sxs-lookup"><span data-stu-id="2b439-121">**Clear**</span></span>](iportabledevicepropvariantcollection-clear.md)           | <span data-ttu-id="2b439-122">釋放和移除集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="2b439-122">Frees, and then removes, all items from the collection.</span></span><br/>                  |
| [<span data-ttu-id="2b439-123">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="2b439-123">**GetAt**</span></span>](iportabledevicepropvariantcollection-getat.md)           | <span data-ttu-id="2b439-124">以零為基底的索引，從集合中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="2b439-124">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="2b439-125">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="2b439-125">**GetCount**</span></span>](iportabledevicepropvariantcollection-getcount.md)     | <span data-ttu-id="2b439-126">捕獲此集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="2b439-126">Retrieves the number of items in this collection.</span></span><br/>                        |
| [<span data-ttu-id="2b439-127">**GetType**</span><span class="sxs-lookup"><span data-stu-id="2b439-127">**GetType**</span></span>](iportabledevicepropvariantcollection-gettype.md)       | <span data-ttu-id="2b439-128">抓取集合中專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="2b439-128">Retrieves the data type of the items in the collection.</span></span><br/>                  |
| [<span data-ttu-id="2b439-129">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="2b439-129">**RemoveAt**</span></span>](iportabledevicepropvariantcollection-removeat.md)     | <span data-ttu-id="2b439-130">移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="2b439-130">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b439-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b439-131">Requirements</span></span>



| <span data-ttu-id="2b439-132">需求</span><span class="sxs-lookup"><span data-stu-id="2b439-132">Requirement</span></span> | <span data-ttu-id="2b439-133">值</span><span class="sxs-lookup"><span data-stu-id="2b439-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b439-134">標頭</span><span class="sxs-lookup"><span data-stu-id="2b439-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2b439-135"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b439-135"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b439-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b439-136">Library</span></span><br/> | <dl> <span data-ttu-id="2b439-137"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b439-137"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b439-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b439-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b439-139">**集合介面**</span><span class="sxs-lookup"><span data-stu-id="2b439-139">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

