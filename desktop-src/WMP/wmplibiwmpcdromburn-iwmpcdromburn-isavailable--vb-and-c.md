---
title: IWMPCdromBurn isAvailable 方法
description: IsAvailable 方法提供 CD 光碟機和媒體的相關資訊。
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- isAvailable 方法 Windows Media Player
- isAvailable 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，isAvailable 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992978"
---
# <a name="iwmpcdromburnisavailable-method"></a><span data-ttu-id="38d02-106">IWMPCdromBurn：： isAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="38d02-106">IWMPCdromBurn::isAvailable method</span></span>

<span data-ttu-id="38d02-107">**IsAvailable** 方法提供 CD 光碟機和媒體的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="38d02-107">The **isAvailable** method provides information about the CD drive and media.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d02-108">語法</span><span class="sxs-lookup"><span data-stu-id="38d02-108">Syntax</span></span>


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a><span data-ttu-id="38d02-109">參數</span><span class="sxs-lookup"><span data-stu-id="38d02-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38d02-110">*bstrItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38d02-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38d02-111">**System.string** ，包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="38d02-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="38d02-112">值</span><span class="sxs-lookup"><span data-stu-id="38d02-112">Value</span></span> | <span data-ttu-id="38d02-113">描述</span><span class="sxs-lookup"><span data-stu-id="38d02-113">Description</span></span>                 |
|-------|-----------------------------|
| <span data-ttu-id="38d02-114">燒錄</span><span class="sxs-lookup"><span data-stu-id="38d02-114">Burn</span></span>  | <span data-ttu-id="38d02-115">磁片磁碟機是 CD 燒錄機。</span><span class="sxs-lookup"><span data-stu-id="38d02-115">The drive is a CD burner.</span></span>   |
| <span data-ttu-id="38d02-116">光碟</span><span class="sxs-lookup"><span data-stu-id="38d02-116">Disc</span></span>  | <span data-ttu-id="38d02-117">磁片磁碟機中有 CD。</span><span class="sxs-lookup"><span data-stu-id="38d02-117">There is a CD in the drive.</span></span> |
| <span data-ttu-id="38d02-118">清除</span><span class="sxs-lookup"><span data-stu-id="38d02-118">Erase</span></span> | <span data-ttu-id="38d02-119">您可以清除 CD。</span><span class="sxs-lookup"><span data-stu-id="38d02-119">The CD can be erased.</span></span>       |
| <span data-ttu-id="38d02-120">寫入</span><span class="sxs-lookup"><span data-stu-id="38d02-120">Write</span></span> | <span data-ttu-id="38d02-121">您可以將 CD 寫入至。</span><span class="sxs-lookup"><span data-stu-id="38d02-121">The CD can be written to.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38d02-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="38d02-122">Return value</span></span>

<span data-ttu-id="38d02-123">表示結果的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="38d02-123">A **System.Boolean** that indicates the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d02-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d02-124">Requirements</span></span>



| <span data-ttu-id="38d02-125">需求</span><span class="sxs-lookup"><span data-stu-id="38d02-125">Requirement</span></span> | <span data-ttu-id="38d02-126">值</span><span class="sxs-lookup"><span data-stu-id="38d02-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d02-127">版本</span><span class="sxs-lookup"><span data-stu-id="38d02-127">Version</span></span><br/>   | <span data-ttu-id="38d02-128">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="38d02-128">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="38d02-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="38d02-129">Namespace</span></span><br/> | <span data-ttu-id="38d02-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="38d02-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="38d02-131">組件</span><span class="sxs-lookup"><span data-stu-id="38d02-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="38d02-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="38d02-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d02-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38d02-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d02-134">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="38d02-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





