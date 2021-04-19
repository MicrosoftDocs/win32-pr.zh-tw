---
description: GetCount 方法會抓取此集合中的索引鍵數目。
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: 'IPortableDeviceKeyCollection：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e867a171039a97cc0f83198f72eecaeb57ad3c16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995048"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a><span data-ttu-id="52e78-103">IPortableDeviceKeyCollection：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="52e78-103">IPortableDeviceKeyCollection::GetCount method</span></span>

<span data-ttu-id="52e78-104">**GetCount** 方法會抓取此集合中的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="52e78-104">The **GetCount** method retrieves the number of keys in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e78-105">語法</span><span class="sxs-lookup"><span data-stu-id="52e78-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="52e78-106">參數</span><span class="sxs-lookup"><span data-stu-id="52e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52e78-107">*pcElems* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52e78-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52e78-108">**DWORD** 的指標，其中包含集合中的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="52e78-108">Pointer to a **DWORD** that contains the number of keys in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52e78-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="52e78-109">Return value</span></span>

<span data-ttu-id="52e78-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="52e78-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52e78-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="52e78-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52e78-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="52e78-112">Return code</span></span>                                                                               | <span data-ttu-id="52e78-113">Description</span><span class="sxs-lookup"><span data-stu-id="52e78-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="52e78-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="52e78-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="52e78-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="52e78-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="52e78-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="52e78-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="52e78-117">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="52e78-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="52e78-118">範例</span><span class="sxs-lookup"><span data-stu-id="52e78-118">Examples</span></span>

<span data-ttu-id="52e78-119">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="52e78-119">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52e78-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="52e78-120">Requirements</span></span>



| <span data-ttu-id="52e78-121">需求</span><span class="sxs-lookup"><span data-stu-id="52e78-121">Requirement</span></span> | <span data-ttu-id="52e78-122">值</span><span class="sxs-lookup"><span data-stu-id="52e78-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52e78-123">標頭</span><span class="sxs-lookup"><span data-stu-id="52e78-123">Header</span></span><br/>  | <dl> <span data-ttu-id="52e78-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="52e78-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="52e78-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="52e78-125">Library</span></span><br/> | <dl> <span data-ttu-id="52e78-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52e78-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e78-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52e78-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e78-128">**IPortableDeviceKeyCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="52e78-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="52e78-129">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="52e78-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="52e78-130">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="52e78-130">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




