---
description: DbgDumpObjectRegister 函式會顯示作用中物件的相關資訊。 在零售組建中略過。
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: 'DbgDumpObjectRegister 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989791"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="6cb99-104">DbgDumpObjectRegister 函式</span><span class="sxs-lookup"><span data-stu-id="6cb99-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="6cb99-105">此函式會 `DbgDumpObjectRegister` 顯示作用中物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6cb99-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="6cb99-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="6cb99-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb99-107">語法</span><span class="sxs-lookup"><span data-stu-id="6cb99-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="6cb99-108">參數</span><span class="sxs-lookup"><span data-stu-id="6cb99-108">Parameters</span></span>

<span data-ttu-id="6cb99-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="6cb99-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cb99-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cb99-110">Return value</span></span>

<span data-ttu-id="6cb99-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6cb99-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb99-112">備註</span><span class="sxs-lookup"><span data-stu-id="6cb99-112">Remarks</span></span>

<span data-ttu-id="6cb99-113">在 debug 組建中，debug 程式庫會維護使用中物件的清單。</span><span class="sxs-lookup"><span data-stu-id="6cb99-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="6cb99-114">此清單包含任何衍生自 [**CBaseObject**](cbaseobject.md)的物件、目前的模組所建立的物件，而且尚未終結。</span><span class="sxs-lookup"><span data-stu-id="6cb99-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="6cb99-115">**CBaseObject** 的函式和析構函數方法會更新清單。</span><span class="sxs-lookup"><span data-stu-id="6cb99-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="6cb99-116">此函數會產生數個記錄檔 \_ 記憶體訊息。</span><span class="sxs-lookup"><span data-stu-id="6cb99-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="6cb99-117">在記錄層級1，此函數只會顯示物件的總數。</span><span class="sxs-lookup"><span data-stu-id="6cb99-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="6cb99-118">在記錄層級2或更高層級，它會顯示物件的清單。</span><span class="sxs-lookup"><span data-stu-id="6cb99-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb99-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cb99-119">Requirements</span></span>



| <span data-ttu-id="6cb99-120">需求</span><span class="sxs-lookup"><span data-stu-id="6cb99-120">Requirement</span></span> | <span data-ttu-id="6cb99-121">值</span><span class="sxs-lookup"><span data-stu-id="6cb99-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb99-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6cb99-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6cb99-123"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6cb99-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cb99-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="6cb99-124">Library</span></span><br/> | <dl> <span data-ttu-id="6cb99-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6cb99-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb99-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cb99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb99-127">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="6cb99-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




