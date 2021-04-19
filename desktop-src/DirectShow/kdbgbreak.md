---
description: 導致中斷點例外狀況，並使用 DbgLog 宏來記錄指定的字串。 在零售組建中略過。
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: 'KDbgBreak 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985974"
---
# <a name="kdbgbreak-macro"></a><span data-ttu-id="41b6f-104">KDbgBreak 宏</span><span class="sxs-lookup"><span data-stu-id="41b6f-104">KDbgBreak macro</span></span>

<span data-ttu-id="41b6f-105">導致中斷點例外狀況，並使用 [**DbgLog**](dbglog.md) 宏來記錄指定的字串。</span><span class="sxs-lookup"><span data-stu-id="41b6f-105">Causes a breakpoint exception, and logs the specified string using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="41b6f-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="41b6f-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b6f-107">語法</span><span class="sxs-lookup"><span data-stu-id="41b6f-107">Syntax</span></span>


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="41b6f-108">參數</span><span class="sxs-lookup"><span data-stu-id="41b6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b6f-109">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="41b6f-109">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="41b6f-110">文字字串。</span><span class="sxs-lookup"><span data-stu-id="41b6f-110">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b6f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="41b6f-111">Return value</span></span>

<span data-ttu-id="41b6f-112">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41b6f-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41b6f-113">備註</span><span class="sxs-lookup"><span data-stu-id="41b6f-113">Remarks</span></span>

<span data-ttu-id="41b6f-114">與 [**DbgBreak**](dbgbreak.md) 宏不同的是，此宏不會顯示提示使用者的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="41b6f-114">Unlike the [**DbgBreak**](dbgbreak.md) macro, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="41b6f-115">在 debug 組建中，它會自動產生中斷點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="41b6f-115">In debug builds, it automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b6f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b6f-116">Requirements</span></span>



| <span data-ttu-id="41b6f-117">需求</span><span class="sxs-lookup"><span data-stu-id="41b6f-117">Requirement</span></span> | <span data-ttu-id="41b6f-118">值</span><span class="sxs-lookup"><span data-stu-id="41b6f-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b6f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="41b6f-119">Header</span></span><br/> | <dl> <span data-ttu-id="41b6f-120"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="41b6f-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b6f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41b6f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b6f-122">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="41b6f-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




