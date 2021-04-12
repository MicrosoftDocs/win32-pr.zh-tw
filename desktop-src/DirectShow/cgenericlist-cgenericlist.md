---
description: 瞭解 CGenericList. CGenericList () Wxlist 的函式方法。 這個方法會使用 ' pName ' 和 ' iItems ' 參數。
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: 'CGenericList. CGenericList (Wxlist. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323456"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="3939c-104">CGenericList. CGenericList (Wxlist .h) -pName，iItems 參數</span><span class="sxs-lookup"><span data-stu-id="3939c-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="3939c-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="3939c-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3939c-106">語法</span><span class="sxs-lookup"><span data-stu-id="3939c-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="3939c-107">參數</span><span class="sxs-lookup"><span data-stu-id="3939c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3939c-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="3939c-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3939c-109">清單名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="3939c-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="3939c-110">*iItems*</span><span class="sxs-lookup"><span data-stu-id="3939c-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="3939c-111">節點快取的大小。</span><span class="sxs-lookup"><span data-stu-id="3939c-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="3939c-112">*塊*</span><span class="sxs-lookup"><span data-stu-id="3939c-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="3939c-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="3939c-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3939c-114">*bAlert*</span><span class="sxs-lookup"><span data-stu-id="3939c-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="3939c-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="3939c-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3939c-116">備註</span><span class="sxs-lookup"><span data-stu-id="3939c-116">Remarks</span></span>

<span data-ttu-id="3939c-117">為了提高效率， `CGenericList` 類別會維護清單節點的快取。</span><span class="sxs-lookup"><span data-stu-id="3939c-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="3939c-118">如果您知道清單將保留多少專案，請使用此版本的函式。</span><span class="sxs-lookup"><span data-stu-id="3939c-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="3939c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3939c-119">Requirements</span></span>

| <span data-ttu-id="3939c-120">需求</span><span class="sxs-lookup"><span data-stu-id="3939c-120">Requirement</span></span> | <span data-ttu-id="3939c-121">值</span><span class="sxs-lookup"><span data-stu-id="3939c-121">Value</span></span> |
|-|-|
| <span data-ttu-id="3939c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3939c-122">Header</span></span> | <span data-ttu-id="3939c-123">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="3939c-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="3939c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3939c-124">Library</span></span>| <span data-ttu-id="3939c-125"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="3939c-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3939c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3939c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3939c-127">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="3939c-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




