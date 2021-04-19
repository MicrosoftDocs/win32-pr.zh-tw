---
description: Add 方法會將屬性索引鍵新增至集合。
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'IPortableDeviceKeyCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987921"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="64822-103">IPortableDeviceKeyCollection：： Add 方法</span><span class="sxs-lookup"><span data-stu-id="64822-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="64822-104">**Add** 方法會將屬性索引鍵新增至集合。</span><span class="sxs-lookup"><span data-stu-id="64822-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="64822-105">語法</span><span class="sxs-lookup"><span data-stu-id="64822-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="64822-106">參數</span><span class="sxs-lookup"><span data-stu-id="64822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64822-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64822-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64822-108">要加入至集合的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="64822-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="64822-109">這個方法會將索引鍵複製到集合，因此您可以在呼叫這個方法之後釋放本機變數。</span><span class="sxs-lookup"><span data-stu-id="64822-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64822-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="64822-110">Return value</span></span>

<span data-ttu-id="64822-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="64822-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64822-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="64822-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64822-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="64822-113">Return code</span></span>                                                                                   | <span data-ttu-id="64822-114">Description</span><span class="sxs-lookup"><span data-stu-id="64822-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64822-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="64822-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="64822-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="64822-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="64822-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="64822-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="64822-118">沒有足夠的記憶體可用來將索引鍵新增至集合。</span><span class="sxs-lookup"><span data-stu-id="64822-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="64822-119">範例</span><span class="sxs-lookup"><span data-stu-id="64822-119">Examples</span></span>

<span data-ttu-id="64822-120">如需如何使用此方法的範例，請參閱抓取 [單一物件的屬性](retrieving-properties-for-a-single-object.md)。</span><span class="sxs-lookup"><span data-stu-id="64822-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="64822-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="64822-121">Requirements</span></span>



| <span data-ttu-id="64822-122">需求</span><span class="sxs-lookup"><span data-stu-id="64822-122">Requirement</span></span> | <span data-ttu-id="64822-123">值</span><span class="sxs-lookup"><span data-stu-id="64822-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64822-124">標頭</span><span class="sxs-lookup"><span data-stu-id="64822-124">Header</span></span><br/>  | <dl> <span data-ttu-id="64822-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="64822-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="64822-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="64822-126">Library</span></span><br/> | <dl> <span data-ttu-id="64822-127"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="64822-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64822-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64822-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64822-129">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="64822-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="64822-130">正在抓取內容物件屬性</span><span class="sxs-lookup"><span data-stu-id="64822-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="64822-131">取得單一物件的屬性</span><span class="sxs-lookup"><span data-stu-id="64822-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="64822-132">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="64822-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




