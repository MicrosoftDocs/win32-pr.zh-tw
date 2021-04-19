---
description: CBaseList 方法會執行 abtract 清單。 衍生自 CBaseList 的 CGenericList 類別樣板提供型別檢查和比 CBaseList 類別更簡單的介面。
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: 'CBaseList 類別 (Wxlist) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983985"
---
# <a name="cbaselist-class"></a><span data-ttu-id="a8f4f-104">CBaseList 類別</span><span class="sxs-lookup"><span data-stu-id="a8f4f-104">CBaseList class</span></span>

![cbaselist 類別階層](images/list01.png)

<span data-ttu-id="a8f4f-106">**CBaseList** 方法會執行 abtract 清單。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="a8f4f-107">衍生自 **CBaseList** 的 [**CGenericList**](cgenericlist.md)類別樣板提供型別檢查和比 **CBaseList** 類別更簡單的介面。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="a8f4f-108">**CBaseList** 類別會在 MFC) 程式庫的 Microsoft Foundation (類別中的 **CObList** 類別之後進行模型化。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="a8f4f-109">清單中的位置會以位置結構表示。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="a8f4f-110">呼叫端不應該存取位置結構的內部成員;將它視為清單節點的指標。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="a8f4f-111">物件在清單中的位置會維持有效，直到刪除物件為止。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="a8f4f-112">此清單不需要其所包含物件的任何支援。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="a8f4f-113">它不會在物件上執行任何儲存管理或複製。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="a8f4f-114">物件可以位於多個清單中。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="a8f4f-115">此類別中大約有一半的方法會在單一物件上作用。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="a8f4f-116">這些方法在方法名稱中有尾碼-I。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="a8f4f-117">其他方法會對整個清單採取行動。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-117">The other methods act on entire lists.</span></span> <span data-ttu-id="a8f4f-118">例如， [**CBaseList：： AddAfter**](cbaselist-addafter.md) 方法會將清單附加至另一個清單。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="a8f4f-119">單一物件作業會傳回位置值，或在失敗時傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="a8f4f-120">如果成功，則清單作業會傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="a8f4f-121">受保護的成員變數</span><span class="sxs-lookup"><span data-stu-id="a8f4f-121">Protected Member Variables</span></span>                             | <span data-ttu-id="a8f4f-122">Description</span><span class="sxs-lookup"><span data-stu-id="a8f4f-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a8f4f-123">**m \_ 計數**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="a8f4f-124">清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="a8f4f-125">**m \_ pFirst**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="a8f4f-126">清單中第一個節點的指標。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="a8f4f-127">**m \_ pLast**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="a8f4f-128">清單中最後一個節點的指標。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="a8f4f-129">保護方法</span><span class="sxs-lookup"><span data-stu-id="a8f4f-129">Protected Methods</span></span>                                      | <span data-ttu-id="a8f4f-130">Description</span><span class="sxs-lookup"><span data-stu-id="a8f4f-130">Description</span></span>                                                               |
| [<span data-ttu-id="a8f4f-131">**GetNextI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="a8f4f-132">抓取指定位置的專案，並將位置往前移。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="a8f4f-133">**GetI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="a8f4f-134">在指定位置抓取專案。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="a8f4f-135">**FindI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="a8f4f-136">抓取保留指定專案的第一個位置。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="a8f4f-137">**RemoveHeadI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="a8f4f-138">移除清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="a8f4f-139">**RemoveTailI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="a8f4f-140">移除清單中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="a8f4f-141">**RemoveI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="a8f4f-142">移除位於指定位置的專案。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="a8f4f-143">**AddTailI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="a8f4f-144">將專案加入至清單結尾。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="a8f4f-145">**AddHeadI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="a8f4f-146">將專案加入至清單的前方。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="a8f4f-147">**AddAfterI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="a8f4f-148">將專案插入指定的位置之後。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="a8f4f-149">**AddBeforeI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="a8f4f-150">在指定的位置之前插入專案。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="a8f4f-151">公用方法</span><span class="sxs-lookup"><span data-stu-id="a8f4f-151">Public Methods</span></span>                                         | <span data-ttu-id="a8f4f-152">Description</span><span class="sxs-lookup"><span data-stu-id="a8f4f-152">Description</span></span>                                                               |
| [<span data-ttu-id="a8f4f-153">**CBaseList**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="a8f4f-154">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="a8f4f-155">**~ CBaseList**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="a8f4f-156">函式方法。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="a8f4f-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="a8f4f-158">從清單中移除所有節點。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="a8f4f-159">**GetHeadPositionI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="a8f4f-160">抓取清單中第一個專案的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="a8f4f-161">**GetTailPositionI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="a8f4f-162">抓取清單最後一個專案的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="a8f4f-163">**GetCountI**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="a8f4f-164">捕獲清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="a8f4f-165">**下一步**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="a8f4f-166">抓取清單中的下一個位置。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="a8f4f-167">**昨日**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="a8f4f-168">抓取清單中先前的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="a8f4f-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="a8f4f-170">將另一個清單插入此清單的前面。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="a8f4f-171">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="a8f4f-172">將另一個清單附加至這份清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="a8f4f-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="a8f4f-174">在指定的位置之後插入清單。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="a8f4f-175">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="a8f4f-176">在指定的位置之前插入清單。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="a8f4f-177">**MoveToTail**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="a8f4f-178">分割清單，並將標頭部分附加至另一個清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="a8f4f-179">**MoveToHead**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="a8f4f-180">分割清單，並將結尾部分插入另一個清單的開頭。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="a8f4f-181">**反向**</span><span class="sxs-lookup"><span data-stu-id="a8f4f-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="a8f4f-182">反轉清單的順序。</span><span class="sxs-lookup"><span data-stu-id="a8f4f-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="a8f4f-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f4f-183">Requirements</span></span>



| <span data-ttu-id="a8f4f-184">需求</span><span class="sxs-lookup"><span data-stu-id="a8f4f-184">Requirement</span></span> | <span data-ttu-id="a8f4f-185">值</span><span class="sxs-lookup"><span data-stu-id="a8f4f-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f4f-186">標頭</span><span class="sxs-lookup"><span data-stu-id="a8f4f-186">Header</span></span><br/>  | <dl> <span data-ttu-id="a8f4f-187"><dt>Wxlist (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a8f4f-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8f4f-188">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8f4f-188">Library</span></span><br/> | <dl> <span data-ttu-id="a8f4f-189"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a8f4f-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f4f-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8f4f-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f4f-191">DirectShow 基類</span><span class="sxs-lookup"><span data-stu-id="a8f4f-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




