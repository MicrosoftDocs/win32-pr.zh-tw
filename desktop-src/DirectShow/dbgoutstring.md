---
description: DbgOutString 函式會將字串傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: 'DbgOutString 函式 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998794"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="88b72-104">DbgOutString 函式</span><span class="sxs-lookup"><span data-stu-id="88b72-104">DbgOutString function</span></span>

<span data-ttu-id="88b72-105">**DbgOutString** 函式會將字串傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="88b72-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="88b72-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="88b72-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b72-107">語法</span><span class="sxs-lookup"><span data-stu-id="88b72-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="88b72-108">參數</span><span class="sxs-lookup"><span data-stu-id="88b72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b72-109">*psz*</span><span class="sxs-lookup"><span data-stu-id="88b72-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="88b72-110">要輸出的字串。</span><span class="sxs-lookup"><span data-stu-id="88b72-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b72-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="88b72-111">Return value</span></span>

<span data-ttu-id="88b72-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="88b72-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88b72-113">備註</span><span class="sxs-lookup"><span data-stu-id="88b72-113">Remarks</span></span>

<span data-ttu-id="88b72-114">在 debug 組建中，此函式一律會輸出字串，而不論目前的偵錯工具輸出層級為何。</span><span class="sxs-lookup"><span data-stu-id="88b72-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="88b72-115">若要更精確地控制輸出，請使用 [**DbgLog**](dbglog.md) 宏。</span><span class="sxs-lookup"><span data-stu-id="88b72-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="88b72-116">範例</span><span class="sxs-lookup"><span data-stu-id="88b72-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="88b72-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="88b72-117">Requirements</span></span>



| <span data-ttu-id="88b72-118">需求</span><span class="sxs-lookup"><span data-stu-id="88b72-118">Requirement</span></span> | <span data-ttu-id="88b72-119">值</span><span class="sxs-lookup"><span data-stu-id="88b72-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88b72-120">標頭</span><span class="sxs-lookup"><span data-stu-id="88b72-120">Header</span></span><br/>  | <dl> <span data-ttu-id="88b72-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="88b72-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88b72-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="88b72-122">Library</span></span><br/> | <dl> <span data-ttu-id="88b72-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="88b72-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88b72-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88b72-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b72-125">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="88b72-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




