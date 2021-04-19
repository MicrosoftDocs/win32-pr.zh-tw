---
description: AlignDown 方法會將值截斷為指定的對齊界限。
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: 'CPullPin. AlignDown 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992933"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="2290a-103">CPullPin. AlignDown 方法</span><span class="sxs-lookup"><span data-stu-id="2290a-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="2290a-104">方法會將 `AlignDown` 值截斷為指定的對齊界限。</span><span class="sxs-lookup"><span data-stu-id="2290a-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="2290a-105">語法</span><span class="sxs-lookup"><span data-stu-id="2290a-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="2290a-106">參數</span><span class="sxs-lookup"><span data-stu-id="2290a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2290a-107">*將*</span><span class="sxs-lookup"><span data-stu-id="2290a-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="2290a-108">指定要對齊的數位。</span><span class="sxs-lookup"><span data-stu-id="2290a-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="2290a-109">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="2290a-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="2290a-110">指定對齊界限。</span><span class="sxs-lookup"><span data-stu-id="2290a-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2290a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2290a-111">Return value</span></span>

<span data-ttu-id="2290a-112">傳回對齊的結果。</span><span class="sxs-lookup"><span data-stu-id="2290a-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="2290a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2290a-113">Requirements</span></span>



| <span data-ttu-id="2290a-114">需求</span><span class="sxs-lookup"><span data-stu-id="2290a-114">Requirement</span></span> | <span data-ttu-id="2290a-115">值</span><span class="sxs-lookup"><span data-stu-id="2290a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2290a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2290a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2290a-117"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="2290a-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="2290a-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2290a-118">Library</span></span><br/> | <dl> <span data-ttu-id="2290a-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2290a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2290a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2290a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2290a-121">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="2290a-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




