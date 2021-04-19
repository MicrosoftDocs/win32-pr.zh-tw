---
description: 評估運算式，並在運算式為 FALSE 時顯示診斷訊息。 在零售組建中略過。
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: 'ASSERT 宏 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977723"
---
# <a name="assert-macro"></a><span data-ttu-id="afde7-104">ASSERT 巨集</span><span class="sxs-lookup"><span data-stu-id="afde7-104">ASSERT macro</span></span>

<span data-ttu-id="afde7-105">評估運算式，並在運算式為 **FALSE** 時顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="afde7-105">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span> <span data-ttu-id="afde7-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="afde7-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="afde7-107">語法</span><span class="sxs-lookup"><span data-stu-id="afde7-107">Syntax</span></span>


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a><span data-ttu-id="afde7-108">參數</span><span class="sxs-lookup"><span data-stu-id="afde7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afde7-109">*待續*</span><span class="sxs-lookup"><span data-stu-id="afde7-109">*cond*</span></span> 
</dt> <dd>

<span data-ttu-id="afde7-110">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="afde7-110">Expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afde7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="afde7-111">Return value</span></span>

<span data-ttu-id="afde7-112">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="afde7-112">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="afde7-113">備註</span><span class="sxs-lookup"><span data-stu-id="afde7-113">Remarks</span></span>

<span data-ttu-id="afde7-114">在「偵錯工具組建」中，如果運算式為 **FALSE**，此宏會顯示訊息方塊，其中包含運算式的文字、原始程式檔的名稱，以及行號。</span><span class="sxs-lookup"><span data-stu-id="afde7-114">In debug builds, if the expression is **FALSE**, this macro displays a message box with the text of the expression, the name of the source file, and the line number.</span></span> <span data-ttu-id="afde7-115">使用者可以忽略判斷提示、輸入偵錯工具，或結束應用程式。</span><span class="sxs-lookup"><span data-stu-id="afde7-115">The user can ignore the assertion, enter the debugger, or quit the application.</span></span>

## <a name="examples"></a><span data-ttu-id="afde7-116">範例</span><span class="sxs-lookup"><span data-stu-id="afde7-116">Examples</span></span>


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a><span data-ttu-id="afde7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="afde7-117">Requirements</span></span>



| <span data-ttu-id="afde7-118">需求</span><span class="sxs-lookup"><span data-stu-id="afde7-118">Requirement</span></span> | <span data-ttu-id="afde7-119">值</span><span class="sxs-lookup"><span data-stu-id="afde7-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afde7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="afde7-120">Header</span></span><br/> | <dl> <span data-ttu-id="afde7-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="afde7-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afde7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afde7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afde7-123">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="afde7-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




