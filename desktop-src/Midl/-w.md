---
title: /W 參數
description: /W 參數指定 MIDL 編譯器的警告層級。 警告層級表示警告的嚴重性。
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W 參數 MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969083"
---
# <a name="w-switch"></a><span data-ttu-id="fc778-105">/W 參數</span><span class="sxs-lookup"><span data-stu-id="fc778-105">/W switch</span></span>

<span data-ttu-id="fc778-106">**/W** 參數指定 MIDL 編譯器的警告層級。</span><span class="sxs-lookup"><span data-stu-id="fc778-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="fc778-107">警告層級表示警告的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="fc778-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="fc778-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="fc778-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fc778-109">*level*</span><span class="sxs-lookup"><span data-stu-id="fc778-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="fc778-110">指定警告層級，此為0到4範圍內的整數。</span><span class="sxs-lookup"><span data-stu-id="fc778-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="fc778-111">**/W** 參數和表示警告層級值的數位之間沒有空格。</span><span class="sxs-lookup"><span data-stu-id="fc778-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc778-112">備註</span><span class="sxs-lookup"><span data-stu-id="fc778-112">Remarks</span></span>

<span data-ttu-id="fc778-113">警告層級的範圍為1到4，值為零表示不顯示警告資訊。</span><span class="sxs-lookup"><span data-stu-id="fc778-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="fc778-114">最高嚴重性的警告為層級1。</span><span class="sxs-lookup"><span data-stu-id="fc778-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="fc778-115">下表說明每個警告層級的警告。</span><span class="sxs-lookup"><span data-stu-id="fc778-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="fc778-116">警告層級</span><span class="sxs-lookup"><span data-stu-id="fc778-116">Warning level</span></span> | <span data-ttu-id="fc778-117">描述</span><span class="sxs-lookup"><span data-stu-id="fc778-117">Description</span></span>                                             | <span data-ttu-id="fc778-118">範例</span><span class="sxs-lookup"><span data-stu-id="fc778-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="fc778-119">W0</span><span class="sxs-lookup"><span data-stu-id="fc778-119">W0</span></span>            | <span data-ttu-id="fc778-120">沒有警告。</span><span class="sxs-lookup"><span data-stu-id="fc778-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="fc778-121">W1</span><span class="sxs-lookup"><span data-stu-id="fc778-121">W1</span></span>            | <span data-ttu-id="fc778-122">可能造成應用程式錯誤的嚴重警告。</span><span class="sxs-lookup"><span data-stu-id="fc778-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="fc778-123">未指定任何系結控制碼、未歸屬指標、衝突的參數。</span><span class="sxs-lookup"><span data-stu-id="fc778-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="fc778-124">W2</span><span class="sxs-lookup"><span data-stu-id="fc778-124">W2</span></span>            | <span data-ttu-id="fc778-125">可能會在使用者的操作環境中造成問題。</span><span class="sxs-lookup"><span data-stu-id="fc778-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="fc778-126">識別碼長度超過31個字元。</span><span class="sxs-lookup"><span data-stu-id="fc778-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="fc778-127">未指定預設聯集 arm。</span><span class="sxs-lookup"><span data-stu-id="fc778-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="fc778-128">W3</span><span class="sxs-lookup"><span data-stu-id="fc778-128">W3</span></span>            | <span data-ttu-id="fc778-129">保留的。</span><span class="sxs-lookup"><span data-stu-id="fc778-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="fc778-130">W4</span><span class="sxs-lookup"><span data-stu-id="fc778-130">W4</span></span>            | <span data-ttu-id="fc778-131">最低警告層級。</span><span class="sxs-lookup"><span data-stu-id="fc778-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="fc778-132">非 ANSI C 結構。</span><span class="sxs-lookup"><span data-stu-id="fc778-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="fc778-133">警告與錯誤不同。</span><span class="sxs-lookup"><span data-stu-id="fc778-133">Warnings are different from errors.</span></span> <span data-ttu-id="fc778-134">錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。</span><span class="sxs-lookup"><span data-stu-id="fc778-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="fc778-135">警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="fc778-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="fc778-136">**/W** 參數所設定的警告層級可以搭配 [**/wx**](-wx.md)參數使用，使 MIDL 編譯器停止處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="fc778-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="fc778-137">**/W** 參數的行為與 [**/warn**](-warn.md)參數相同。</span><span class="sxs-lookup"><span data-stu-id="fc778-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="fc778-138">範例</span><span class="sxs-lookup"><span data-stu-id="fc778-138">Examples</span></span>

<span data-ttu-id="fc778-139">**midl/W2 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="fc778-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="fc778-140">**midl/W4 bar .idl**</span><span class="sxs-lookup"><span data-stu-id="fc778-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fc778-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc778-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc778-142">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="fc778-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fc778-143">**/warn**</span><span class="sxs-lookup"><span data-stu-id="fc778-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




