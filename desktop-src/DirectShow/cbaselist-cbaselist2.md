---
description: CBaseList。 CBaseList 函式-函數方法。
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: 'CBaseList. CBaseList (Wxlist. h) '
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
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096325"
---
# <a name="cbaselistcbaselist-constructor"></a><span data-ttu-id="d5729-103">CBaseList. CBaseList 函數</span><span class="sxs-lookup"><span data-stu-id="d5729-103">CBaseList.CBaseList constructor</span></span>

<span data-ttu-id="d5729-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="d5729-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5729-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5729-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="d5729-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5729-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d5729-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d5729-108">清單名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="d5729-108">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5729-109">備註</span><span class="sxs-lookup"><span data-stu-id="d5729-109">Remarks</span></span>

<span data-ttu-id="d5729-110">為了提高效率， `CBaseList` 類別會維護清單節點的快取。</span><span class="sxs-lookup"><span data-stu-id="d5729-110">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="d5729-111">此版本的函式會使用預設快取大小。</span><span class="sxs-lookup"><span data-stu-id="d5729-111">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5729-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5729-112">Requirements</span></span>



| <span data-ttu-id="d5729-113">需求</span><span class="sxs-lookup"><span data-stu-id="d5729-113">Requirement</span></span> | <span data-ttu-id="d5729-114">值</span><span class="sxs-lookup"><span data-stu-id="d5729-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5729-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d5729-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d5729-116"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d5729-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d5729-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5729-117">Library</span></span><br/> | <dl> <span data-ttu-id="d5729-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d5729-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5729-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5729-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5729-120">**CBaseList 類別**</span><span class="sxs-lookup"><span data-stu-id="d5729-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




