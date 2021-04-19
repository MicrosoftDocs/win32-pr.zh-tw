---
description: GetAt 方法會依據索引，從集合中抓取 PROPERTYKEY。
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'IPortableDeviceKeyCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978780"
---
# <a name="iportabledevicekeycollectiongetat-method"></a><span data-ttu-id="81a04-103">IPortableDeviceKeyCollection：： GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="81a04-103">IPortableDeviceKeyCollection::GetAt method</span></span>

<span data-ttu-id="81a04-104">**GetAt** 方法會依據索引，從集合中抓取 **PROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="81a04-104">The **GetAt** method retrieves a **PROPERTYKEY** from the collection by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a04-105">語法</span><span class="sxs-lookup"><span data-stu-id="81a04-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a><span data-ttu-id="81a04-106">參數</span><span class="sxs-lookup"><span data-stu-id="81a04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a04-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81a04-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81a04-108">**DWORD** ，其中包含要抓取之索引鍵的索引。</span><span class="sxs-lookup"><span data-stu-id="81a04-108">**DWORD** that contains the index of the key to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="81a04-109">*pKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81a04-109">*pKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81a04-110">**PROPERTYKEY** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="81a04-110">Pointer to a **PROPERTYKEY** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a04-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="81a04-111">Return value</span></span>

<span data-ttu-id="81a04-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="81a04-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="81a04-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="81a04-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="81a04-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="81a04-114">Return code</span></span>                                                                                  | <span data-ttu-id="81a04-115">Description</span><span class="sxs-lookup"><span data-stu-id="81a04-115">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="81a04-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="81a04-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="81a04-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="81a04-117">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="81a04-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81a04-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="81a04-119">傳入的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="81a04-119">The index passed in was out of range.</span></span><br/>     |
| <dl> <span data-ttu-id="81a04-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="81a04-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="81a04-121">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="81a04-121">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="81a04-122">範例</span><span class="sxs-lookup"><span data-stu-id="81a04-122">Examples</span></span>

<span data-ttu-id="81a04-123">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="81a04-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81a04-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="81a04-124">Requirements</span></span>



| <span data-ttu-id="81a04-125">需求</span><span class="sxs-lookup"><span data-stu-id="81a04-125">Requirement</span></span> | <span data-ttu-id="81a04-126">值</span><span class="sxs-lookup"><span data-stu-id="81a04-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81a04-127">標頭</span><span class="sxs-lookup"><span data-stu-id="81a04-127">Header</span></span><br/>  | <dl> <span data-ttu-id="81a04-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="81a04-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="81a04-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="81a04-129">Library</span></span><br/> | <dl> <span data-ttu-id="81a04-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a04-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a04-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81a04-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a04-132">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="81a04-132">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="81a04-133">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="81a04-133">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="81a04-134">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="81a04-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




