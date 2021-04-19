---
description: IPortableDeviceKeyCollection 介面會保存 PROPERTYKEY 值的集合。 您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 CLSID PortableDeviceKeyCollection 呼叫 CoCreate \_ 。
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: 'IPortableDeviceKeyCollection 介面 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994771"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="b2400-104">IPortableDeviceKeyCollection 介面</span><span class="sxs-lookup"><span data-stu-id="b2400-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="b2400-105">**IPortableDeviceKeyCollection** 介面會保存 **PROPERTYKEY** 值的集合。</span><span class="sxs-lookup"><span data-stu-id="b2400-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="b2400-106">您可以從方法中取出這個介面，或者，如果需要新的物件，請使用 **CLSID \_ PortableDeviceKeyCollection** 呼叫 **CoCreate** 。</span><span class="sxs-lookup"><span data-stu-id="b2400-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="b2400-107">成員</span><span class="sxs-lookup"><span data-stu-id="b2400-107">Members</span></span>

<span data-ttu-id="b2400-108">**IPortableDeviceKeyCollection** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b2400-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b2400-109">**IPortableDeviceKeyCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b2400-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b2400-110">方法</span><span class="sxs-lookup"><span data-stu-id="b2400-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b2400-111">方法</span><span class="sxs-lookup"><span data-stu-id="b2400-111">Methods</span></span>

<span data-ttu-id="b2400-112">**IPortableDeviceKeyCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b2400-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="b2400-113">方法</span><span class="sxs-lookup"><span data-stu-id="b2400-113">Method</span></span>                                                    | <span data-ttu-id="b2400-114">描述</span><span class="sxs-lookup"><span data-stu-id="b2400-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2400-115">**添加**</span><span class="sxs-lookup"><span data-stu-id="b2400-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="b2400-116">將屬性索引鍵加入至集合。</span><span class="sxs-lookup"><span data-stu-id="b2400-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="b2400-117">**清楚**</span><span class="sxs-lookup"><span data-stu-id="b2400-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="b2400-118">刪除集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="b2400-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="b2400-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="b2400-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="b2400-120">依據索引，從集合抓取 **PROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="b2400-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="b2400-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="b2400-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="b2400-122">捕獲此集合中的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="b2400-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="b2400-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="b2400-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="b2400-124">移除儲存在指定索引所指定之位置的元素。</span><span class="sxs-lookup"><span data-stu-id="b2400-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b2400-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2400-125">Requirements</span></span>



| <span data-ttu-id="b2400-126">需求</span><span class="sxs-lookup"><span data-stu-id="b2400-126">Requirement</span></span> | <span data-ttu-id="b2400-127">值</span><span class="sxs-lookup"><span data-stu-id="b2400-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2400-128">標頭</span><span class="sxs-lookup"><span data-stu-id="b2400-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b2400-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2400-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2400-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2400-130">Library</span></span><br/> | <dl> <span data-ttu-id="b2400-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2400-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2400-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2400-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2400-133">**集合介面**</span><span class="sxs-lookup"><span data-stu-id="b2400-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

