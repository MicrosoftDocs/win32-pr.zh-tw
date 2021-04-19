---
description: CRefTime 類別是用來管理參考時間的 helper 類別。
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: 'CRefTime 類別 (Reftime) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995734"
---
# <a name="creftime-class"></a><span data-ttu-id="cc431-103">CRefTime 類別</span><span class="sxs-lookup"><span data-stu-id="cc431-103">CRefTime class</span></span>

![creftime 類別階層](images/cutil05.png)

<span data-ttu-id="cc431-105">`CRefTime`類別是用來管理參考時間的 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="cc431-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="cc431-106">*參考時間* 是以 100-毫微秒單位表示的時間單位。</span><span class="sxs-lookup"><span data-stu-id="cc431-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="cc431-107">這個類別會共用與 [**參考 \_ 時間**](reference-time.md) 資料類型相同的資料版面配置，但會加入一些可提供比較、轉換和算術函數的方法和運算子。</span><span class="sxs-lookup"><span data-stu-id="cc431-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="cc431-108">如需參考時間的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="cc431-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="cc431-109">Public 成員變數</span><span class="sxs-lookup"><span data-stu-id="cc431-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="cc431-110">Description</span><span class="sxs-lookup"><span data-stu-id="cc431-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="cc431-111">**m \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="cc431-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="cc431-112">指定 **參考 \_ 時間** 值。</span><span class="sxs-lookup"><span data-stu-id="cc431-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="cc431-113">公用方法</span><span class="sxs-lookup"><span data-stu-id="cc431-113">Public Methods</span></span>                                                          | <span data-ttu-id="cc431-114">Description</span><span class="sxs-lookup"><span data-stu-id="cc431-114">Description</span></span>                                           |
| [<span data-ttu-id="cc431-115">**CRefTime**</span><span class="sxs-lookup"><span data-stu-id="cc431-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="cc431-116">函式方法。</span><span class="sxs-lookup"><span data-stu-id="cc431-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="cc431-117">**GetUnits**</span><span class="sxs-lookup"><span data-stu-id="cc431-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="cc431-118">以 100-毫微秒單位來抓取參考時間。</span><span class="sxs-lookup"><span data-stu-id="cc431-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="cc431-119">**Millisecs**</span><span class="sxs-lookup"><span data-stu-id="cc431-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="cc431-120">將參考時間轉換為毫秒。</span><span class="sxs-lookup"><span data-stu-id="cc431-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="cc431-121">運算子</span><span class="sxs-lookup"><span data-stu-id="cc431-121">Operators</span></span>                                                               | <span data-ttu-id="cc431-122">說明</span><span class="sxs-lookup"><span data-stu-id="cc431-122">Description</span></span>                                           |
| [<span data-ttu-id="cc431-123">**運算子參考 \_ 時間 ()**</span><span class="sxs-lookup"><span data-stu-id="cc431-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="cc431-124">將物件轉換為 **參考 \_ 時間** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="cc431-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="cc431-125">**運算子 =**</span><span class="sxs-lookup"><span data-stu-id="cc431-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="cc431-126">指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="cc431-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="cc431-127">**運算子 + =**</span><span class="sxs-lookup"><span data-stu-id="cc431-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="cc431-128">加入兩個參考時間。</span><span class="sxs-lookup"><span data-stu-id="cc431-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="cc431-129">**運算子 =**</span><span class="sxs-lookup"><span data-stu-id="cc431-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="cc431-130">從另一個參考時間減去一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="cc431-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="cc431-131">備註</span><span class="sxs-lookup"><span data-stu-id="cc431-131">Remarks</span></span>

<span data-ttu-id="cc431-132">使用此類別可能會有缺陷。</span><span class="sxs-lookup"><span data-stu-id="cc431-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="cc431-133">如果您套用 + = 運算子和 **CRefTime** 物件做為左運算元，並將 **LONG** 類型的變數套用為右運算元，則編譯器會將右運算元隱含地轉換為 **CRefTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="cc431-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="cc431-134">這項強制型轉會使用將毫秒轉換成參考時間單位的 **CRefTime** 函式 \_ ; 因此，右運算元乘以10000：</span><span class="sxs-lookup"><span data-stu-id="cc431-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="cc431-135">不過，使用 + 運算子時，也不會發生相同的事：</span><span class="sxs-lookup"><span data-stu-id="cc431-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="cc431-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc431-136">Requirements</span></span>



| <span data-ttu-id="cc431-137">需求</span><span class="sxs-lookup"><span data-stu-id="cc431-137">Requirement</span></span> | <span data-ttu-id="cc431-138">值</span><span class="sxs-lookup"><span data-stu-id="cc431-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc431-139">標頭</span><span class="sxs-lookup"><span data-stu-id="cc431-139">Header</span></span><br/>  | <dl> <span data-ttu-id="cc431-140"><dt>Reftime (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cc431-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc431-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc431-141">Library</span></span><br/> | <dl> <span data-ttu-id="cc431-142"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cc431-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




