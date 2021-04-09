---
title: /warn 參數
description: /Warn 參數會指定 MIDL 編譯器的警告層級。
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn 參數 MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678332"
---
# <a name="warn-switch"></a><span data-ttu-id="52187-104">/warn 參數</span><span class="sxs-lookup"><span data-stu-id="52187-104">/warn switch</span></span>

<span data-ttu-id="52187-105">**/Warn** 參數會指定 MIDL 編譯器的警告層級。</span><span class="sxs-lookup"><span data-stu-id="52187-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="52187-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="52187-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="52187-107">*level*</span><span class="sxs-lookup"><span data-stu-id="52187-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="52187-108">指定警告層級，此為0到4範圍內的整數。</span><span class="sxs-lookup"><span data-stu-id="52187-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="52187-109">**/Warn** 參數和表示警告層級值的數位之間沒有空格。</span><span class="sxs-lookup"><span data-stu-id="52187-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52187-110">備註</span><span class="sxs-lookup"><span data-stu-id="52187-110">Remarks</span></span>

<span data-ttu-id="52187-111">警告層級表示警告的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="52187-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="52187-112">警告層級的範圍為1到4，值為零表示不顯示警告資訊。</span><span class="sxs-lookup"><span data-stu-id="52187-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="52187-113">最高嚴重性警告為層級1。</span><span class="sxs-lookup"><span data-stu-id="52187-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="52187-114">下表說明每個警告層級的警告。</span><span class="sxs-lookup"><span data-stu-id="52187-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="52187-115">警告層級</span><span class="sxs-lookup"><span data-stu-id="52187-115">Warning level</span></span> | <span data-ttu-id="52187-116">描述</span><span class="sxs-lookup"><span data-stu-id="52187-116">Description</span></span>                                             | <span data-ttu-id="52187-117">範例</span><span class="sxs-lookup"><span data-stu-id="52187-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="52187-118">0</span><span class="sxs-lookup"><span data-stu-id="52187-118">0</span></span>             | <span data-ttu-id="52187-119">沒有警告。</span><span class="sxs-lookup"><span data-stu-id="52187-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="52187-120">1</span><span class="sxs-lookup"><span data-stu-id="52187-120">1</span></span>             | <span data-ttu-id="52187-121">可能造成應用程式錯誤的嚴重警告。</span><span class="sxs-lookup"><span data-stu-id="52187-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="52187-122">未指定任何系結控制碼、未歸屬指標、衝突的參數。</span><span class="sxs-lookup"><span data-stu-id="52187-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="52187-123">2</span><span class="sxs-lookup"><span data-stu-id="52187-123">2</span></span>             | <span data-ttu-id="52187-124">可能會在使用者的操作環境中造成問題。</span><span class="sxs-lookup"><span data-stu-id="52187-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="52187-125">識別碼長度超過31個字元。</span><span class="sxs-lookup"><span data-stu-id="52187-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="52187-126">未指定預設聯集 arm。</span><span class="sxs-lookup"><span data-stu-id="52187-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="52187-127">3</span><span class="sxs-lookup"><span data-stu-id="52187-127">3</span></span>             | <span data-ttu-id="52187-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="52187-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="52187-129">4</span><span class="sxs-lookup"><span data-stu-id="52187-129">4</span></span>             | <span data-ttu-id="52187-130">最低警告層級。</span><span class="sxs-lookup"><span data-stu-id="52187-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="52187-131">非 ANSI C 結構。</span><span class="sxs-lookup"><span data-stu-id="52187-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="52187-132">警告與錯誤不同。</span><span class="sxs-lookup"><span data-stu-id="52187-132">Warnings are different from errors.</span></span> <span data-ttu-id="52187-133">錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。</span><span class="sxs-lookup"><span data-stu-id="52187-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="52187-134">警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="52187-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="52187-135">**/Warn** 參數所設定的警告層級可以與 [**WX**](-wx.md)參數搭配使用，以使 MIDL 編譯器停止處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="52187-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="52187-136">**/Warn** 參數的行為與 [**/w**](-w.md)參數相同。</span><span class="sxs-lookup"><span data-stu-id="52187-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="52187-137">範例</span><span class="sxs-lookup"><span data-stu-id="52187-137">Examples</span></span>

<span data-ttu-id="52187-138">**midl/warn2 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="52187-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="52187-139">**midl/warn4 bar .idl**</span><span class="sxs-lookup"><span data-stu-id="52187-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="52187-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52187-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52187-141">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="52187-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




