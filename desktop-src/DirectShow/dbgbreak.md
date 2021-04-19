---
description: 使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。 使用者可以忽略訊息、輸入偵錯工具，或結束應用程式。 在零售組建中略過。
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: 'DbgBreak 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983204"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="c60b9-105">DbgBreak 宏</span><span class="sxs-lookup"><span data-stu-id="c60b9-105">DbgBreak macro</span></span>

<span data-ttu-id="c60b9-106">使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="c60b9-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="c60b9-107">使用者可以忽略訊息、輸入偵錯工具，或結束應用程式。</span><span class="sxs-lookup"><span data-stu-id="c60b9-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="c60b9-108">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="c60b9-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="c60b9-109">語法</span><span class="sxs-lookup"><span data-stu-id="c60b9-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="c60b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="c60b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c60b9-111">*strLiteral*</span><span class="sxs-lookup"><span data-stu-id="c60b9-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="c60b9-112">文字字串。</span><span class="sxs-lookup"><span data-stu-id="c60b9-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c60b9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c60b9-113">Return value</span></span>

<span data-ttu-id="c60b9-114">這個宏不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c60b9-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c60b9-115">範例</span><span class="sxs-lookup"><span data-stu-id="c60b9-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="c60b9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c60b9-116">Requirements</span></span>



| <span data-ttu-id="c60b9-117">需求</span><span class="sxs-lookup"><span data-stu-id="c60b9-117">Requirement</span></span> | <span data-ttu-id="c60b9-118">值</span><span class="sxs-lookup"><span data-stu-id="c60b9-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60b9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c60b9-119">Header</span></span><br/> | <dl> <span data-ttu-id="c60b9-120"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c60b9-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60b9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c60b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60b9-122">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="c60b9-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




