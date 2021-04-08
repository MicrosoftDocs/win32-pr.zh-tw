---
description: 瞭解 CGenericList. CGenericList () Wxlist 的函式方法。 這個方法會使用 ' pName ' 參數。
ms.assetid: 6311d84d-1723-4607-87f8-7cd2ad2582f3
title: CGenericList. CGenericList 函式 (Wxlist .h) -pName 參數
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
ms.openlocfilehash: 4a2aa2347e963839c18d904f2819d50de8d6d9c3
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "103854100"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-parameter"></a><span data-ttu-id="a2149-104">CGenericList. CGenericList 函式 (Wxlist .h) -pName 參數</span><span class="sxs-lookup"><span data-stu-id="a2149-104">CGenericList.CGenericList constructor (Wxlist.h) - pName parameter</span></span>

<span data-ttu-id="a2149-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a2149-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2149-106">語法</span><span class="sxs-lookup"><span data-stu-id="a2149-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="a2149-107">參數</span><span class="sxs-lookup"><span data-stu-id="a2149-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2149-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="a2149-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a2149-109">清單名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="a2149-109">Pointer to the name of the list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2149-110">備註</span><span class="sxs-lookup"><span data-stu-id="a2149-110">Remarks</span></span>

<span data-ttu-id="a2149-111">為了提高效率， `CGenericList` 類別會維護清單節點的快取。</span><span class="sxs-lookup"><span data-stu-id="a2149-111">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="a2149-112">此版本的函式會使用預設快取大小。</span><span class="sxs-lookup"><span data-stu-id="a2149-112">This version of the constructor uses a default cache size.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2149-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2149-113">Requirements</span></span>

| <span data-ttu-id="a2149-114">需求</span><span class="sxs-lookup"><span data-stu-id="a2149-114">Requirement</span></span> | <span data-ttu-id="a2149-115">值</span><span class="sxs-lookup"><span data-stu-id="a2149-115">Value</span></span> |
|-|-|
| <span data-ttu-id="a2149-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a2149-116">Header</span></span> | <span data-ttu-id="a2149-117">Wxlist (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="a2149-117">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="a2149-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2149-118">Library</span></span>| <span data-ttu-id="a2149-119"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="a2149-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a2149-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2149-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2149-121">**CGenericList 類別**</span><span class="sxs-lookup"><span data-stu-id="a2149-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




