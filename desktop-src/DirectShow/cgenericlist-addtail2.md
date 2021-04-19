---
description: AddTail 方法會將清單附加至清單結尾。
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: CGenericList. AddTail 方法 (Wxlist .h) -pList 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "106984279"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="64c0e-103">CGenericList. AddTail 方法 (Wxlist .h) -pList 參數</span><span class="sxs-lookup"><span data-stu-id="64c0e-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="64c0e-104">方法會將 `AddTail` 清單附加至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="64c0e-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c0e-105">語法</span><span class="sxs-lookup"><span data-stu-id="64c0e-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="64c0e-106">參數</span><span class="sxs-lookup"><span data-stu-id="64c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c0e-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="64c0e-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="64c0e-108">要附加之清單的指標。</span><span class="sxs-lookup"><span data-stu-id="64c0e-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c0e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="64c0e-109">Return value</span></span>

<span data-ttu-id="64c0e-110">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="64c0e-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c0e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="64c0e-111">Requirements</span></span>

| <span data-ttu-id="64c0e-112">需求</span><span class="sxs-lookup"><span data-stu-id="64c0e-112">Requirement</span></span> | <span data-ttu-id="64c0e-113">值</span><span class="sxs-lookup"><span data-stu-id="64c0e-113">Value</span></span> |
|-|-|
| <span data-ttu-id="64c0e-114">標頭</span><span class="sxs-lookup"><span data-stu-id="64c0e-114">Header</span></span> | <span data-ttu-id="64c0e-115">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="64c0e-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="64c0e-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="64c0e-116">Library</span></span>| <span data-ttu-id="64c0e-117"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="64c0e-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="64c0e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64c0e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c0e-119">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="64c0e-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




