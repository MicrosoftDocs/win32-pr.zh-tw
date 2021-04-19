---
description: 評估運算式，並在運算式為 FALSE 時引發中斷點例外狀況。 運算式的文字、原始程式檔的名稱，以及使用 DbgLog 宏記錄行號的行號。 在零售組建中略過。
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: 'KASSERT 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976268"
---
# <a name="kassert-macro"></a><span data-ttu-id="d374a-105">KASSERT 宏</span><span class="sxs-lookup"><span data-stu-id="d374a-105">KASSERT macro</span></span>

<span data-ttu-id="d374a-106">評估運算式，並在運算式為 **FALSE** 時引發中斷點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d374a-106">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span> <span data-ttu-id="d374a-107">運算式的文字、原始程式檔的名稱，以及使用 [**DbgLog**](dbglog.md) 宏記錄行號的行號。</span><span class="sxs-lookup"><span data-stu-id="d374a-107">The text of the expression, the name of the source file, and the line number are logged using the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="d374a-108">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="d374a-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d374a-109">語法</span><span class="sxs-lookup"><span data-stu-id="d374a-109">Syntax</span></span>


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a><span data-ttu-id="d374a-110">參數</span><span class="sxs-lookup"><span data-stu-id="d374a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d374a-111">*待續*</span><span class="sxs-lookup"><span data-stu-id="d374a-111">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="d374a-112">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="d374a-112">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d374a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d374a-113">Return value</span></span>

<span data-ttu-id="d374a-114">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d374a-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d374a-115">備註</span><span class="sxs-lookup"><span data-stu-id="d374a-115">Remarks</span></span>

<span data-ttu-id="d374a-116">與 [**assert**](assert.md) 和 [**EXECUTE \_ assert**](execute-assert.md) 宏不同的是，此宏不會顯示提示使用者的訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="d374a-116">Unlike the [**ASSERT**](assert.md) and [**EXECUTE\_ASSERT**](execute-assert.md) macros, this macro does not display a message box prompting the user.</span></span> <span data-ttu-id="d374a-117">在 debug 組建中，如果運算式為 **FALSE**，宏會自動造成中斷點例外狀況發生。</span><span class="sxs-lookup"><span data-stu-id="d374a-117">In debug builds, if the expression is **FALSE**, the macro automatically causes a breakpoint exception to occur.</span></span>

## <a name="requirements"></a><span data-ttu-id="d374a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d374a-118">Requirements</span></span>



| <span data-ttu-id="d374a-119">需求</span><span class="sxs-lookup"><span data-stu-id="d374a-119">Requirement</span></span> | <span data-ttu-id="d374a-120">值</span><span class="sxs-lookup"><span data-stu-id="d374a-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d374a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d374a-121">Header</span></span><br/> | <dl> <span data-ttu-id="d374a-122"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d374a-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d374a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d374a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d374a-124">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="d374a-124">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




