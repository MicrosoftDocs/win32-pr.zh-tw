---
description: AddHead 方法會將清單新增至清單前端。
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: CGenericList. AddHead 方法 (Wxlist .h) -pList 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106992137"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="eccff-103">CGenericList. AddHead 方法 (Wxlist .h) -pList 參數</span><span class="sxs-lookup"><span data-stu-id="eccff-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="eccff-104">`AddHead`方法會將清單新增至清單前端。</span><span class="sxs-lookup"><span data-stu-id="eccff-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="eccff-105">語法</span><span class="sxs-lookup"><span data-stu-id="eccff-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="eccff-106">參數</span><span class="sxs-lookup"><span data-stu-id="eccff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eccff-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="eccff-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="eccff-108">要加入之專案清單的指標。</span><span class="sxs-lookup"><span data-stu-id="eccff-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eccff-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eccff-109">Return value</span></span>

<span data-ttu-id="eccff-110">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="eccff-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eccff-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="eccff-111">Requirements</span></span>

| <span data-ttu-id="eccff-112">需求</span><span class="sxs-lookup"><span data-stu-id="eccff-112">Requirement</span></span> | <span data-ttu-id="eccff-113">值</span><span class="sxs-lookup"><span data-stu-id="eccff-113">Value</span></span> |
|-|-|
| <span data-ttu-id="eccff-114">標頭</span><span class="sxs-lookup"><span data-stu-id="eccff-114">Header</span></span> | <span data-ttu-id="eccff-115">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="eccff-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="eccff-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="eccff-116">Library</span></span>| <span data-ttu-id="eccff-117"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="eccff-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="eccff-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eccff-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eccff-119">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="eccff-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




