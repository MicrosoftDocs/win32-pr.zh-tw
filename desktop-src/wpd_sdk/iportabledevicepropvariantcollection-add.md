---
description: IPortableDevicePropVariantCollection：： Add 方法-Add 方法會將專案加入至集合。
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112456"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="3b7c9-103">IPortableDevicePropVariantCollection：： Add 方法</span><span class="sxs-lookup"><span data-stu-id="3b7c9-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="3b7c9-104">**Add** 方法會將專案加入至集合。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b7c9-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3b7c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b7c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7c9-107">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b7c9-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7c9-108">要加入至集合之新 **PROPVARIANT** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="3b7c9-109">這個方法會將 **PROPVARIANT** 複製到集合中，因此您應該在呼叫這個方法之後，呼叫 **PropVariantClear** 來釋放變數的本機複本。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7c9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b7c9-110">Return value</span></span>

<span data-ttu-id="3b7c9-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3b7c9-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3b7c9-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3b7c9-113">Return code</span></span>                                                                          | <span data-ttu-id="3b7c9-114">Description</span><span class="sxs-lookup"><span data-stu-id="3b7c9-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3b7c9-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3b7c9-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3b7c9-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b7c9-117">備註</span><span class="sxs-lookup"><span data-stu-id="3b7c9-117">Remarks</span></span>

<span data-ttu-id="3b7c9-118">當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援設定和取出 **Null** 或零大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="3b7c9-119">例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="3b7c9-120">如果呼叫端嘗試加入集合中包含之不同 VARTYPE 的專案，而且這個介面無法自動變更 PROPVARIANT 值，此方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="3b7c9-121">若要手動變更集合類型，請呼叫 [**IPortableDevicePropVariantCollection：： ChangeType**](iportabledevicepropvariantcollection-changetype.md)。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3b7c9-122">範例</span><span class="sxs-lookup"><span data-stu-id="3b7c9-122">Examples</span></span>

<span data-ttu-id="3b7c9-123">如需如何使用此方法的範例，請參閱[從持續性唯一識別碼抓取物件識別碼](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)。</span><span class="sxs-lookup"><span data-stu-id="3b7c9-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7c9-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b7c9-124">Requirements</span></span>



| <span data-ttu-id="3b7c9-125">需求</span><span class="sxs-lookup"><span data-stu-id="3b7c9-125">Requirement</span></span> | <span data-ttu-id="3b7c9-126">值</span><span class="sxs-lookup"><span data-stu-id="3b7c9-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7c9-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3b7c9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3b7c9-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7c9-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b7c9-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b7c9-129">Library</span></span><br/> | <dl> <span data-ttu-id="3b7c9-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b7c9-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7c9-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b7c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7c9-132">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="3b7c9-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="3b7c9-133">移動裝置上的內容</span><span class="sxs-lookup"><span data-stu-id="3b7c9-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="3b7c9-134">從持續性唯一識別碼中取出物件識別碼</span><span class="sxs-lookup"><span data-stu-id="3b7c9-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




