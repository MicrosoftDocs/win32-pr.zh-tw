---
description: 提醒宏會在編譯時期產生提醒。 此宏會產生字串，其中包含參數字串、原始程式檔的名稱，以及行號。
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: '提醒 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995760"
---
# <a name="remind"></a><span data-ttu-id="5125b-104">提醒</span><span class="sxs-lookup"><span data-stu-id="5125b-104">REMIND</span></span>

<span data-ttu-id="5125b-105">`REMIND`宏會在編譯時期產生提醒。</span><span class="sxs-lookup"><span data-stu-id="5125b-105">The `REMIND` macro generates a reminder at compile time.</span></span> <span data-ttu-id="5125b-106">此宏會產生字串，其中包含參數字串、原始程式檔的名稱，以及行號。</span><span class="sxs-lookup"><span data-stu-id="5125b-106">This macro generates a string that includes the parameter string, the name of the source file, and the line number.</span></span>

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a><span data-ttu-id="5125b-107">參數</span><span class="sxs-lookup"><span data-stu-id="5125b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5125b-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="5125b-108"><span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*</span></span>
</dt> <dd>

<span data-ttu-id="5125b-109">文字字串。</span><span class="sxs-lookup"><span data-stu-id="5125b-109">Text string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5125b-110">備註</span><span class="sxs-lookup"><span data-stu-id="5125b-110">Remarks</span></span>

<span data-ttu-id="5125b-111">此宏適用于產生編譯時期警告：</span><span class="sxs-lookup"><span data-stu-id="5125b-111">This macro is useful for generating compile-time warnings:</span></span>


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a><span data-ttu-id="5125b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5125b-112">Requirements</span></span>



| <span data-ttu-id="5125b-113">需求</span><span class="sxs-lookup"><span data-stu-id="5125b-113">Requirement</span></span> | <span data-ttu-id="5125b-114">值</span><span class="sxs-lookup"><span data-stu-id="5125b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5125b-115">標頭</span><span class="sxs-lookup"><span data-stu-id="5125b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5125b-116"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5125b-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5125b-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="5125b-117">Library</span></span><br/> | <dl> <span data-ttu-id="5125b-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5125b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5125b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5125b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5125b-120">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="5125b-120">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




