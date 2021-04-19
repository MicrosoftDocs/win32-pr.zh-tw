---
description: 評估 debug 和 retail 組建中的運算式。 在 [偵錯工具] 組建中，如果運算式為 FALSE，則會顯示診斷訊息。
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: 'EXECUTE_ASSERT 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 5db5e78d198cc9f66aa5de6fdb0160e325b82591
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993678"
---
# <a name="execute_assert-macro"></a><span data-ttu-id="4a68e-104">EXECUTE \_ ASSERT 宏</span><span class="sxs-lookup"><span data-stu-id="4a68e-104">EXECUTE\_ASSERT macro</span></span>

<span data-ttu-id="4a68e-105">評估 debug 和 retail 組建中的運算式。</span><span class="sxs-lookup"><span data-stu-id="4a68e-105">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="4a68e-106">在 [偵錯工具] 組建中，如果運算式為 **FALSE**，則會顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="4a68e-106">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a68e-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a68e-107">Syntax</span></span>


```C++
void EXECUTE_ASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="4a68e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a68e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a68e-109">*待續*</span><span class="sxs-lookup"><span data-stu-id="4a68e-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="4a68e-110">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="4a68e-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a68e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a68e-111">Return value</span></span>

<span data-ttu-id="4a68e-112">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4a68e-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a68e-113">備註</span><span class="sxs-lookup"><span data-stu-id="4a68e-113">Remarks</span></span>

<span data-ttu-id="4a68e-114">與 [**ASSERT**](assert.md) 宏不同的是，此宏會評估零售組建中的運算式。</span><span class="sxs-lookup"><span data-stu-id="4a68e-114">Unlike the [**ASSERT**](assert.md) macro, this macro evaluates the expression in retail builds.</span></span> <span data-ttu-id="4a68e-115">在偵錯工具組建中，如果運算式為 **FALSE**，則宏會顯示訊息方塊，其中包含運算式的文字、原始程式檔的名稱，以及行號。</span><span class="sxs-lookup"><span data-stu-id="4a68e-115">In debug builds, if the expression is **FALSE**, the macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="4a68e-116">使用者可以忽略判斷提示、輸入偵錯工具，或結束應用程式。</span><span class="sxs-lookup"><span data-stu-id="4a68e-116">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a68e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a68e-117">Requirements</span></span>



| <span data-ttu-id="4a68e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4a68e-118">Requirement</span></span> | <span data-ttu-id="4a68e-119">值</span><span class="sxs-lookup"><span data-stu-id="4a68e-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a68e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4a68e-120">Header</span></span><br/> | <dl> <span data-ttu-id="4a68e-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4a68e-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a68e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a68e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a68e-123">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="4a68e-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




