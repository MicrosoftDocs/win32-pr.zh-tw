---
description: CGenericList 類別範本，它會執行特定類型的清單。 如需詳細資訊，請參閱 CBaseList。
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: 'CGenericList 類別 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994766"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="f58b5-104">CGenericList 類別</span><span class="sxs-lookup"><span data-stu-id="f58b5-104">CGenericList class</span></span>

![cgenericlist 類別階層](images/list01.png)

<span data-ttu-id="f58b5-106">執行 `CGenericList` 類型特定清單的類別樣板。</span><span class="sxs-lookup"><span data-stu-id="f58b5-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="f58b5-107">如需詳細資訊，請參閱 [**CBaseList**](cbaselist.md)。</span><span class="sxs-lookup"><span data-stu-id="f58b5-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="f58b5-108">若要使用這個範本，請使用樣板 `CGenericList` 引數（定義清單中的物件類型）宣告類型的變數。</span><span class="sxs-lookup"><span data-stu-id="f58b5-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="f58b5-109">例如，下列語句會宣告 [**CBaseFilter**](cbasefilter.md) 物件的清單：</span><span class="sxs-lookup"><span data-stu-id="f58b5-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="f58b5-110">為了方便起見，Wxlist 會定義下列清單類型：</span><span class="sxs-lookup"><span data-stu-id="f58b5-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="f58b5-111">公用方法</span><span class="sxs-lookup"><span data-stu-id="f58b5-111">Public Methods</span></span>                                          | <span data-ttu-id="f58b5-112">Description</span><span class="sxs-lookup"><span data-stu-id="f58b5-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="f58b5-113">**CGenericList**</span><span class="sxs-lookup"><span data-stu-id="f58b5-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="f58b5-114">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f58b5-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="f58b5-115">**~ CGenericList**</span><span class="sxs-lookup"><span data-stu-id="f58b5-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="f58b5-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f58b5-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="f58b5-117">**GetHeadPosition**</span><span class="sxs-lookup"><span data-stu-id="f58b5-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="f58b5-118">抓取清單中第一個專案的位置。</span><span class="sxs-lookup"><span data-stu-id="f58b5-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="f58b5-119">**GetTailPosition**</span><span class="sxs-lookup"><span data-stu-id="f58b5-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="f58b5-120">抓取清單最後一個專案的位置。</span><span class="sxs-lookup"><span data-stu-id="f58b5-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="f58b5-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="f58b5-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="f58b5-122">捕獲清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f58b5-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="f58b5-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="f58b5-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="f58b5-124">抓取指定位置的專案，並將位置往前移。</span><span class="sxs-lookup"><span data-stu-id="f58b5-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="f58b5-125">**Get**</span><span class="sxs-lookup"><span data-stu-id="f58b5-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="f58b5-126">在指定位置抓取專案。</span><span class="sxs-lookup"><span data-stu-id="f58b5-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="f58b5-127">**GetHead**</span><span class="sxs-lookup"><span data-stu-id="f58b5-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="f58b5-128">抓取清單開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="f58b5-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="f58b5-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="f58b5-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="f58b5-130">移除清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="f58b5-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="f58b5-131">**RemoveTail**</span><span class="sxs-lookup"><span data-stu-id="f58b5-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="f58b5-132">移除清單中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="f58b5-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="f58b5-133">**移除**</span><span class="sxs-lookup"><span data-stu-id="f58b5-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="f58b5-134">移除位於指定位置的專案。</span><span class="sxs-lookup"><span data-stu-id="f58b5-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="f58b5-135">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="f58b5-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="f58b5-136">將專案或清單插入指定的位置之前。</span><span class="sxs-lookup"><span data-stu-id="f58b5-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="f58b5-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="f58b5-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="f58b5-138">將專案或清單插入指定的位置之後。</span><span class="sxs-lookup"><span data-stu-id="f58b5-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="f58b5-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="f58b5-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="f58b5-140">將專案或清單加入至清單的前方。</span><span class="sxs-lookup"><span data-stu-id="f58b5-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="f58b5-141">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="f58b5-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="f58b5-142">將專案或清單附加至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="f58b5-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="f58b5-143">**Find**</span><span class="sxs-lookup"><span data-stu-id="f58b5-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="f58b5-144">抓取保留指定專案的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="f58b5-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="f58b5-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="f58b5-145">Requirements</span></span>



| <span data-ttu-id="f58b5-146">需求</span><span class="sxs-lookup"><span data-stu-id="f58b5-146">Requirement</span></span> | <span data-ttu-id="f58b5-147">值</span><span class="sxs-lookup"><span data-stu-id="f58b5-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f58b5-148">標頭</span><span class="sxs-lookup"><span data-stu-id="f58b5-148">Header</span></span><br/>  | <dl> <span data-ttu-id="f58b5-149"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f58b5-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f58b5-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="f58b5-150">Library</span></span><br/> | <dl> <span data-ttu-id="f58b5-151"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f58b5-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




