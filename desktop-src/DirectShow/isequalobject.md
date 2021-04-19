---
description: IsEqualObject 函式會檢查兩個介面是否位於相同的物件上。
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: 'IsEqualObject 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999160"
---
# <a name="isequalobject-function"></a><span data-ttu-id="db18d-103">IsEqualObject 函式</span><span class="sxs-lookup"><span data-stu-id="db18d-103">IsEqualObject function</span></span>

<span data-ttu-id="db18d-104">`IsEqualObject`函數會檢查兩個介面是否位於相同的物件上。</span><span class="sxs-lookup"><span data-stu-id="db18d-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="db18d-105">語法</span><span class="sxs-lookup"><span data-stu-id="db18d-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="db18d-106">參數</span><span class="sxs-lookup"><span data-stu-id="db18d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db18d-107">*pFirst*</span><span class="sxs-lookup"><span data-stu-id="db18d-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="db18d-108">指向某個介面的指標。</span><span class="sxs-lookup"><span data-stu-id="db18d-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="db18d-109">*pSecond*</span><span class="sxs-lookup"><span data-stu-id="db18d-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="db18d-110">指向其他介面的指標。</span><span class="sxs-lookup"><span data-stu-id="db18d-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db18d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="db18d-111">Return value</span></span>

<span data-ttu-id="db18d-112">如果介面同時位於相同的物件上，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="db18d-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="db18d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="db18d-113">Requirements</span></span>



| <span data-ttu-id="db18d-114">需求</span><span class="sxs-lookup"><span data-stu-id="db18d-114">Requirement</span></span> | <span data-ttu-id="db18d-115">值</span><span class="sxs-lookup"><span data-stu-id="db18d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db18d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="db18d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="db18d-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="db18d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="db18d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="db18d-118">Library</span></span><br/> | <dl> <span data-ttu-id="db18d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="db18d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db18d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db18d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db18d-121">其他 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="db18d-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




