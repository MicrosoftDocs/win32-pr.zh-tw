---
description: 運算子會指派新的參考時間，並使用 ' rt [ref] ' 參數。
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. operator = method (Ctlutil .h) -rt [ref] 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106976533"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="ac3d1-103">COARefTime. operator = method (Ctlutil .h) -rt [ref] 參數</span><span class="sxs-lookup"><span data-stu-id="ac3d1-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="ac3d1-104">這個運算子會指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="ac3d1-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3d1-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac3d1-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ac3d1-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac3d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3d1-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="ac3d1-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3d1-108">參考 [**\_ 時間**](reference-time.md) 值的參考，此值會以 100-毫微秒單位來指定新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="ac3d1-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3d1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac3d1-109">Return value</span></span>

<span data-ttu-id="ac3d1-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ac3d1-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3d1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac3d1-111">Requirements</span></span>

| <span data-ttu-id="ac3d1-112">需求</span><span class="sxs-lookup"><span data-stu-id="ac3d1-112">Requirement</span></span>                    | <span data-ttu-id="ac3d1-113">值</span><span class="sxs-lookup"><span data-stu-id="ac3d1-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3d1-114">標頭</span><span class="sxs-lookup"><span data-stu-id="ac3d1-114">Header</span></span>  | <span data-ttu-id="ac3d1-115">Ctlutil (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="ac3d1-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="ac3d1-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac3d1-116">Library</span></span> | <span data-ttu-id="ac3d1-117"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="ac3d1-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ac3d1-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac3d1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3d1-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="ac3d1-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




