---
description: AlignUp 方法會將值四捨五入到指定的對齊界限。請注意，已在 Windows 7 中移除。 .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: 'CPullPin. AlignUp 方法 (Pullpin .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987137"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="22adc-104">CPullPin. AlignUp 方法</span><span class="sxs-lookup"><span data-stu-id="22adc-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="22adc-105">**AlignUp** 方法會將值四捨五入到指定的對齊界限。</span><span class="sxs-lookup"><span data-stu-id="22adc-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="22adc-106">已在 Windows 7 中移除。</span><span class="sxs-lookup"><span data-stu-id="22adc-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="22adc-107">語法</span><span class="sxs-lookup"><span data-stu-id="22adc-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="22adc-108">參數</span><span class="sxs-lookup"><span data-stu-id="22adc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22adc-109">*將*</span><span class="sxs-lookup"><span data-stu-id="22adc-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="22adc-110">指定要對齊的數位。</span><span class="sxs-lookup"><span data-stu-id="22adc-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="22adc-111">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="22adc-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="22adc-112">指定對齊界限。</span><span class="sxs-lookup"><span data-stu-id="22adc-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22adc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="22adc-113">Return value</span></span>

<span data-ttu-id="22adc-114">傳回對齊的結果。</span><span class="sxs-lookup"><span data-stu-id="22adc-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="22adc-115">備註</span><span class="sxs-lookup"><span data-stu-id="22adc-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="22adc-116">如果 *ll* + (*lAlign* -1) 溢位，這個方法可能會造成數值溢位。</span><span class="sxs-lookup"><span data-stu-id="22adc-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="22adc-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="22adc-117">Requirements</span></span>



| <span data-ttu-id="22adc-118">需求</span><span class="sxs-lookup"><span data-stu-id="22adc-118">Requirement</span></span> | <span data-ttu-id="22adc-119">值</span><span class="sxs-lookup"><span data-stu-id="22adc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22adc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="22adc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="22adc-121"><dt>Pullpin。h</dt></span><span class="sxs-lookup"><span data-stu-id="22adc-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="22adc-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="22adc-122">Library</span></span><br/> | <dl> <span data-ttu-id="22adc-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="22adc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22adc-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22adc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22adc-125">**CPullPin 類別**</span><span class="sxs-lookup"><span data-stu-id="22adc-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




