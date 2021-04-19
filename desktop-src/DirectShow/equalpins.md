---
description: EqualPins 函式會檢查兩個圖釘是否位於相同的物件上。
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: 'EqualPins 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994185"
---
# <a name="equalpins-function"></a><span data-ttu-id="d4f13-103">EqualPins 函式</span><span class="sxs-lookup"><span data-stu-id="d4f13-103">EqualPins function</span></span>

<span data-ttu-id="d4f13-104">EqualPins 函式會檢查兩個圖釘是否位於相同的物件上。</span><span class="sxs-lookup"><span data-stu-id="d4f13-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f13-105">語法</span><span class="sxs-lookup"><span data-stu-id="d4f13-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="d4f13-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4f13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f13-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="d4f13-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f13-108">指向一個釘選的指標。</span><span class="sxs-lookup"><span data-stu-id="d4f13-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="d4f13-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="d4f13-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="d4f13-110">指向其他釘選的指標。</span><span class="sxs-lookup"><span data-stu-id="d4f13-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f13-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4f13-111">Return value</span></span>

<span data-ttu-id="d4f13-112">如果兩個圖釘都在相同的物件上，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d4f13-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f13-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4f13-113">Requirements</span></span>



| <span data-ttu-id="d4f13-114">需求</span><span class="sxs-lookup"><span data-stu-id="d4f13-114">Requirement</span></span> | <span data-ttu-id="d4f13-115">值</span><span class="sxs-lookup"><span data-stu-id="d4f13-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f13-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d4f13-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d4f13-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d4f13-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d4f13-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4f13-118">Library</span></span><br/> | <dl> <span data-ttu-id="d4f13-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d4f13-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f13-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4f13-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f13-121">其他 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="d4f13-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




