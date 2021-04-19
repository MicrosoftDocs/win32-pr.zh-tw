---
description: NOTE 宏會將字串傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: '注意 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990811"
---
# <a name="note"></a><span data-ttu-id="45e23-104">注意</span><span class="sxs-lookup"><span data-stu-id="45e23-104">NOTE</span></span>

<span data-ttu-id="45e23-105">`NOTE`宏會將字串傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="45e23-105">The `NOTE` macro sends a string to the debug output location.</span></span> <span data-ttu-id="45e23-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="45e23-106">Ignored in retail builds.</span></span>

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a><span data-ttu-id="45e23-107">參數</span><span class="sxs-lookup"><span data-stu-id="45e23-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e23-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="45e23-108"><span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*</span></span>
</dt> <dd>

<span data-ttu-id="45e23-109">Printf 樣式的格式字串。</span><span class="sxs-lookup"><span data-stu-id="45e23-109">A printf -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="45e23-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span><span class="sxs-lookup"><span data-stu-id="45e23-110"><span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*</span></span>
</dt> <dd>

<span data-ttu-id="45e23-111">格式字串的其他引數。</span><span class="sxs-lookup"><span data-stu-id="45e23-111">Additional arguments for the format string.</span></span> <span data-ttu-id="45e23-112">引數的數目必須符合宏名稱。</span><span class="sxs-lookup"><span data-stu-id="45e23-112">The number of arguments must match the macro name.</span></span> <span data-ttu-id="45e23-113">例如， **NOTE1** 會採用一個引數，而 **NOTE5** 會採用五個引數。</span><span class="sxs-lookup"><span data-stu-id="45e23-113">For example, **NOTE1** takes one argument, and **NOTE5** takes five arguments.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45e23-114">備註</span><span class="sxs-lookup"><span data-stu-id="45e23-114">Remarks</span></span>

<span data-ttu-id="45e23-115">這些宏是 [**DbgLog**](dbglog.md) 宏的變體。</span><span class="sxs-lookup"><span data-stu-id="45e23-115">These macros are variants of the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="45e23-116">它們會產生層級5記錄 \_ 追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="45e23-116">They generate level 5 LOG\_TRACE messages.</span></span>

## <a name="example"></a><span data-ttu-id="45e23-117">範例</span><span class="sxs-lookup"><span data-stu-id="45e23-117">Example</span></span>


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a><span data-ttu-id="45e23-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="45e23-118">Requirements</span></span>



| <span data-ttu-id="45e23-119">需求</span><span class="sxs-lookup"><span data-stu-id="45e23-119">Requirement</span></span> | <span data-ttu-id="45e23-120">值</span><span class="sxs-lookup"><span data-stu-id="45e23-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45e23-121">標頭</span><span class="sxs-lookup"><span data-stu-id="45e23-121">Header</span></span><br/>  | <dl> <span data-ttu-id="45e23-122"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="45e23-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="45e23-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="45e23-123">Library</span></span><br/> | <dl> <span data-ttu-id="45e23-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="45e23-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45e23-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45e23-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e23-126">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="45e23-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




