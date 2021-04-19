---
title: IWMPCdromBurn getItemInfo 方法
description: GetItemInfo 方法會抓取 CD 的指定屬性值。
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990678"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="69325-106">IWMPCdromBurn：： getItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="69325-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="69325-107">**GetItemInfo** 方法會抓取 CD 的指定屬性值。</span><span class="sxs-lookup"><span data-stu-id="69325-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="69325-108">語法</span><span class="sxs-lookup"><span data-stu-id="69325-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="69325-109">參數</span><span class="sxs-lookup"><span data-stu-id="69325-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69325-110">*bstrItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69325-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69325-111">**System.string** ，包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="69325-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="69325-112">值</span><span class="sxs-lookup"><span data-stu-id="69325-112">Value</span></span>         | <span data-ttu-id="69325-113">描述</span><span class="sxs-lookup"><span data-stu-id="69325-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69325-114">AvailableTime</span><span class="sxs-lookup"><span data-stu-id="69325-114">AvailableTime</span></span> | <span data-ttu-id="69325-115">抓取 CD 上的可用時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="69325-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="69325-116">Blank</span><span class="sxs-lookup"><span data-stu-id="69325-116">Blank</span></span>         | <span data-ttu-id="69325-117">抓取 system.string **(表示** 為字串，) 指出 CD 是否為空白。</span><span class="sxs-lookup"><span data-stu-id="69325-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="69325-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="69325-118">FreeSpace</span></span>     | <span data-ttu-id="69325-119">抓取 CD 上的可用空間（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="69325-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="69325-120">TotalSpace</span><span class="sxs-lookup"><span data-stu-id="69325-120">TotalSpace</span></span>    | <span data-ttu-id="69325-121">抓取 CD 上的總空間（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="69325-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69325-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="69325-122">Return value</span></span>

<span data-ttu-id="69325-123">**System.string** ，這是指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="69325-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="69325-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="69325-124">Requirements</span></span>



| <span data-ttu-id="69325-125">需求</span><span class="sxs-lookup"><span data-stu-id="69325-125">Requirement</span></span> | <span data-ttu-id="69325-126">值</span><span class="sxs-lookup"><span data-stu-id="69325-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69325-127">版本</span><span class="sxs-lookup"><span data-stu-id="69325-127">Version</span></span><br/>   | <span data-ttu-id="69325-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="69325-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="69325-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="69325-129">Namespace</span></span><br/> | <span data-ttu-id="69325-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69325-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69325-131">組件</span><span class="sxs-lookup"><span data-stu-id="69325-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69325-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="69325-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69325-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69325-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69325-134">**IWMPCdromBurn 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="69325-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





