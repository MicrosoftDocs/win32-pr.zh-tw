---
description: DbgTerminate 函式會清除 debug 程式庫。 在零售組建中略過。
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: 'DbgTerminate 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989757"
---
# <a name="dbgterminate-function"></a><span data-ttu-id="a2753-104">DbgTerminate 函式</span><span class="sxs-lookup"><span data-stu-id="a2753-104">DbgTerminate function</span></span>

<span data-ttu-id="a2753-105">**DbgTerminate** 函式會清除 debug 程式庫。</span><span class="sxs-lookup"><span data-stu-id="a2753-105">The **DbgTerminate** function cleans up the debug library.</span></span> <span data-ttu-id="a2753-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="a2753-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2753-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2753-107">Syntax</span></span>


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a><span data-ttu-id="a2753-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2753-108">Parameters</span></span>

<span data-ttu-id="a2753-109">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="a2753-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2753-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2753-110">Return value</span></span>

<span data-ttu-id="a2753-111">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2753-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2753-112">備註</span><span class="sxs-lookup"><span data-stu-id="a2753-112">Remarks</span></span>

<span data-ttu-id="a2753-113">如果您呼叫 [**DbgInitialise**](dbginitialise.md) 函數，請呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="a2753-113">Call this function if you call the [**DbgInitialise**](dbginitialise.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2753-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2753-114">Requirements</span></span>



| <span data-ttu-id="a2753-115">需求</span><span class="sxs-lookup"><span data-stu-id="a2753-115">Requirement</span></span> | <span data-ttu-id="a2753-116">值</span><span class="sxs-lookup"><span data-stu-id="a2753-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2753-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a2753-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2753-118"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a2753-118"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2753-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2753-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2753-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a2753-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2753-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2753-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2753-122">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="a2753-122">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




