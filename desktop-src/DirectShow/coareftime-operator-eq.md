---
description: 這個運算子會測試兩個參考時間是否相等。
ms.assetid: a265f7c6-8334-4bb3-8cb7-c7918ebdf97a
title: 'COARefTime： operator = = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04b19f7b75be840a293920b36fe5ab63d30520d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993664"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="169c3-103">COARefTime. operator = = 方法</span><span class="sxs-lookup"><span data-stu-id="169c3-103">COARefTime.operator== method</span></span>

<span data-ttu-id="169c3-104">這個運算子會測試兩個參考時間是否相等。</span><span class="sxs-lookup"><span data-stu-id="169c3-104">This operator tests for equality between two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="169c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="169c3-105">Syntax</span></span>


```C++
BOOL operator==(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="169c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="169c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="169c3-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="169c3-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="169c3-108">要比較的 **COARefTime** 物件參考。</span><span class="sxs-lookup"><span data-stu-id="169c3-108">Reference to the **COARefTime** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="169c3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="169c3-109">Return value</span></span>

<span data-ttu-id="169c3-110">如果兩個物件相等，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="169c3-110">Returns **TRUE** if the two objects are equal.</span></span> <span data-ttu-id="169c3-111">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="169c3-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="169c3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="169c3-112">Requirements</span></span>



| <span data-ttu-id="169c3-113">需求</span><span class="sxs-lookup"><span data-stu-id="169c3-113">Requirement</span></span> | <span data-ttu-id="169c3-114">值</span><span class="sxs-lookup"><span data-stu-id="169c3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="169c3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="169c3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="169c3-116"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="169c3-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="169c3-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="169c3-117">Library</span></span><br/> | <dl> <span data-ttu-id="169c3-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="169c3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="169c3-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="169c3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="169c3-120">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="169c3-120">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




