---
description: COARefTime 類別會轉換秒和 100-毫微秒單位之間的參考時間。
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: 'COARefTime 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989254"
---
# <a name="coareftime-class"></a><span data-ttu-id="0b961-103">COARefTime 類別</span><span class="sxs-lookup"><span data-stu-id="0b961-103">COARefTime class</span></span>

![coareftime 類別階層](images/cutil05.png)

<span data-ttu-id="0b961-105">`COARefTime`類別會轉換秒和 100-毫微秒單位之間的參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="0b961-106">這個類別會在與 C/c + + 相容的自動化和參考時間相容的參考時間之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="0b961-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="0b961-107">自動化相容的介面會使用 **雙精度浮點數** 來代表時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b961-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="0b961-108">其他介面會使用64位的 **LONGLONG** 值，以 100-毫微秒單位表示時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="0b961-109">以下是針對這些值定義的類型：</span><span class="sxs-lookup"><span data-stu-id="0b961-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="0b961-110">篩選準則可以使用 `COARefTime` 類別在這兩種格式之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="0b961-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="0b961-111">這個類別衍生自 [**CRefTime**](creftime.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="0b961-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="0b961-112">公用方法</span><span class="sxs-lookup"><span data-stu-id="0b961-112">Public Methods</span></span>                                          | <span data-ttu-id="0b961-113">Description</span><span class="sxs-lookup"><span data-stu-id="0b961-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="0b961-114">**COARefTime**</span><span class="sxs-lookup"><span data-stu-id="0b961-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="0b961-115">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0b961-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="0b961-116">運算子</span><span class="sxs-lookup"><span data-stu-id="0b961-116">Operators</span></span>                                               | <span data-ttu-id="0b961-117">說明</span><span class="sxs-lookup"><span data-stu-id="0b961-117">Description</span></span>                                                           |
| [<span data-ttu-id="0b961-118">**double**</span><span class="sxs-lookup"><span data-stu-id="0b961-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="0b961-119">將參考時間轉換為 **雙精度** 值。</span><span class="sxs-lookup"><span data-stu-id="0b961-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="0b961-120">**參考 \_ 時間**</span><span class="sxs-lookup"><span data-stu-id="0b961-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="0b961-121">將物件轉換為 **參考 \_ 時間** 值。</span><span class="sxs-lookup"><span data-stu-id="0b961-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="0b961-122">**運算子 =**</span><span class="sxs-lookup"><span data-stu-id="0b961-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="0b961-123">指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="0b961-124">**operator = =**</span><span class="sxs-lookup"><span data-stu-id="0b961-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="0b961-125">測試兩個參考時間是否相等。</span><span class="sxs-lookup"><span data-stu-id="0b961-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="0b961-126">**operator！ =**</span><span class="sxs-lookup"><span data-stu-id="0b961-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="0b961-127">測試兩個參考時間是否不相等。</span><span class="sxs-lookup"><span data-stu-id="0b961-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="0b961-128">**運算子 <**</span><span class="sxs-lookup"><span data-stu-id="0b961-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="0b961-129">測試某個參考時間是否小於另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="0b961-130">**運算子 >**</span><span class="sxs-lookup"><span data-stu-id="0b961-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="0b961-131">測試某個參考時間是否大於另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="0b961-132">**運算子 <=**</span><span class="sxs-lookup"><span data-stu-id="0b961-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="0b961-133">測試某個參考時間是否小於或等於另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="0b961-134">**運算子 >=**</span><span class="sxs-lookup"><span data-stu-id="0b961-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="0b961-135">測試某個參考時間是否大於或等於另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="0b961-136">**運算子 +**</span><span class="sxs-lookup"><span data-stu-id="0b961-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="0b961-137">加入兩個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="0b961-138">\* \* 運算子 \* \*</span><span class="sxs-lookup"><span data-stu-id="0b961-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="0b961-139">從另一個參考時間減去一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="0b961-140">**運算子 + =**</span><span class="sxs-lookup"><span data-stu-id="0b961-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="0b961-141">加入兩個參考時間，並將結果指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="0b961-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="0b961-142">**運算子 =**</span><span class="sxs-lookup"><span data-stu-id="0b961-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="0b961-143">減去兩個參考時間，並將結果指派給這個物件。</span><span class="sxs-lookup"><span data-stu-id="0b961-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="0b961-144">**運算元 \***</span><span class="sxs-lookup"><span data-stu-id="0b961-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="0b961-145">以值乘以參考時間。</span><span class="sxs-lookup"><span data-stu-id="0b961-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="0b961-146">**運算子**</span><span class="sxs-lookup"><span data-stu-id="0b961-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="0b961-147">將參考時間除以某個值。</span><span class="sxs-lookup"><span data-stu-id="0b961-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0b961-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b961-148">Requirements</span></span>



| <span data-ttu-id="0b961-149">需求</span><span class="sxs-lookup"><span data-stu-id="0b961-149">Requirement</span></span> | <span data-ttu-id="0b961-150">值</span><span class="sxs-lookup"><span data-stu-id="0b961-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b961-151">標頭</span><span class="sxs-lookup"><span data-stu-id="0b961-151">Header</span></span><br/>  | <dl> <span data-ttu-id="0b961-152"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0b961-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b961-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b961-153">Library</span></span><br/> | <dl> <span data-ttu-id="0b961-154"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0b961-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




