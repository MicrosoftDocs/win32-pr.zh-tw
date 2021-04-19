---
description: Clear 方法會釋出並移除集合中的所有專案。 呼叫這個方法之後，會將集合視為空白。
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'IPortableDevicePropVariantCollection：： Clear 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000892"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="9df99-104">IPortableDevicePropVariantCollection：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="9df99-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="9df99-105">**Clear** 方法會釋出並移除集合中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="9df99-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="9df99-106">呼叫這個方法之後，會將集合視為空白。</span><span class="sxs-lookup"><span data-stu-id="9df99-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9df99-107">語法</span><span class="sxs-lookup"><span data-stu-id="9df99-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="9df99-108">參數</span><span class="sxs-lookup"><span data-stu-id="9df99-108">Parameters</span></span>

<span data-ttu-id="9df99-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9df99-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9df99-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="9df99-110">Return value</span></span>

<span data-ttu-id="9df99-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9df99-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9df99-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9df99-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9df99-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9df99-113">Return code</span></span>                                                                          | <span data-ttu-id="9df99-114">Description</span><span class="sxs-lookup"><span data-stu-id="9df99-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9df99-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9df99-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9df99-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9df99-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9df99-117">備註</span><span class="sxs-lookup"><span data-stu-id="9df99-117">Remarks</span></span>

<span data-ttu-id="9df99-118">在呼叫 **Clear** 之後，集合會被視為不具型別，表示它先前設定的 VARTYPE 不再限制 **加入** 作業。</span><span class="sxs-lookup"><span data-stu-id="9df99-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="9df99-119">呼叫 **Clear** 之後要 **加入** 的呼叫會被視為此集合的「第一個」**加入**。</span><span class="sxs-lookup"><span data-stu-id="9df99-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9df99-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="9df99-120">Requirements</span></span>



| <span data-ttu-id="9df99-121">需求</span><span class="sxs-lookup"><span data-stu-id="9df99-121">Requirement</span></span> | <span data-ttu-id="9df99-122">值</span><span class="sxs-lookup"><span data-stu-id="9df99-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9df99-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9df99-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9df99-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="9df99-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9df99-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="9df99-125">Library</span></span><br/> | <dl> <span data-ttu-id="9df99-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9df99-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9df99-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9df99-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9df99-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="9df99-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




