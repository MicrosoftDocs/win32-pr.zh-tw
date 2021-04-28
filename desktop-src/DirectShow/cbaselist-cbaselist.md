---
description: CBaseList. CBaseList (TCHAR \* ，INT) 的函式，則為函數方法。
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: 'CBaseList. CBaseList (TCHAR *，INT)  (Wxlist. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099636"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="b2f6b-103">CBaseList. CBaseList (TCHAR \* ，INT) 函數</span><span class="sxs-lookup"><span data-stu-id="b2f6b-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="b2f6b-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="b2f6b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f6b-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2f6b-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="b2f6b-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2f6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f6b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="b2f6b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f6b-108">清單名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="b2f6b-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="b2f6b-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="b2f6b-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="b2f6b-110">節點快取的大小。</span><span class="sxs-lookup"><span data-stu-id="b2f6b-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2f6b-111">備註</span><span class="sxs-lookup"><span data-stu-id="b2f6b-111">Remarks</span></span>

<span data-ttu-id="b2f6b-112">為了提高效率， `CBaseList` 類別會維護清單節點的快取。</span><span class="sxs-lookup"><span data-stu-id="b2f6b-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="b2f6b-113">如果您知道清單將保留多少專案，請使用此版本的函式。</span><span class="sxs-lookup"><span data-stu-id="b2f6b-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f6b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2f6b-114">Requirements</span></span>



| <span data-ttu-id="b2f6b-115">需求</span><span class="sxs-lookup"><span data-stu-id="b2f6b-115">Requirement</span></span> | <span data-ttu-id="b2f6b-116">值</span><span class="sxs-lookup"><span data-stu-id="b2f6b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f6b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b2f6b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2f6b-118"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b2f6b-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b2f6b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2f6b-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2f6b-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b2f6b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f6b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2f6b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f6b-122">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="b2f6b-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




