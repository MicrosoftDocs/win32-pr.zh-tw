---
description: 這個運算子會測試兩個參考時間是否不相等。
ms.assetid: c081fff2-d85e-409a-8902-4b2aa2c1fc78
title: 'COARefTime. operator！ = method (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e93934d7b31715422f2cc091e606b681a57e7f61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985781"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="6172a-103">COARefTime. operator！ = 方法</span><span class="sxs-lookup"><span data-stu-id="6172a-103">COARefTime.operator!= method</span></span>

<span data-ttu-id="6172a-104">這個運算子會測試兩個參考時間是否不相等。</span><span class="sxs-lookup"><span data-stu-id="6172a-104">This operator tests for inequality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="6172a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6172a-105">Syntax</span></span>


```C++
BOOL operator!=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="6172a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6172a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6172a-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="6172a-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="6172a-108">要比較的 **COARefTime** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="6172a-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6172a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6172a-109">Return value</span></span>

<span data-ttu-id="6172a-110">如果兩個物件不相等，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="6172a-110">Returns **TRUE** if the two objects are not equal.</span></span> <span data-ttu-id="6172a-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6172a-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6172a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6172a-112">Requirements</span></span>



| <span data-ttu-id="6172a-113">需求</span><span class="sxs-lookup"><span data-stu-id="6172a-113">Requirement</span></span> | <span data-ttu-id="6172a-114">值</span><span class="sxs-lookup"><span data-stu-id="6172a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6172a-115">標頭</span><span class="sxs-lookup"><span data-stu-id="6172a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6172a-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6172a-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6172a-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="6172a-117">Library</span></span><br/> | <dl> <span data-ttu-id="6172a-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6172a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6172a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6172a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6172a-120">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="6172a-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




