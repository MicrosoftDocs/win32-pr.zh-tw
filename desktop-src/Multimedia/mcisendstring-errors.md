---
title: mciSendString 錯誤
description: mciSendString 錯誤
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR 傳回值，mciSendString 錯誤
- 多媒體參考，mciSendString 錯誤
- 多媒體、mciSendString 錯誤的參考
- 媒體控制介面 (MCI) ，mciSendString 錯誤
- MCI (媒體控制介面) ，mciSendString 錯誤
- MCI、mciSendString 錯誤的參考
- MCI 參考，mciSendString 錯誤
- 媒體控制介面 (MCI) ，錯誤
- MCI (媒體控制介面) ，錯誤
- MCI 的參考，錯誤
- MCI 參考，錯誤
- mciSendString 錯誤
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842216"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="bc48b-116">mciSendString 錯誤</span><span class="sxs-lookup"><span data-stu-id="bc48b-116">mciSendString Errors</span></span>

<span data-ttu-id="bc48b-117">[**MciSendString**](/previous-versions//dd757161(v=vs.85))函式會傳回下列錯誤，但不會由 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))傳回：</span><span class="sxs-lookup"><span data-stu-id="bc48b-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="bc48b-118">值</span><span class="sxs-lookup"><span data-stu-id="bc48b-118">Value</span></span>                             | <span data-ttu-id="bc48b-119">意義</span><span class="sxs-lookup"><span data-stu-id="bc48b-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="bc48b-120">MCIERR \_ 錯誤 \_ 常數</span><span class="sxs-lookup"><span data-stu-id="bc48b-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="bc48b-121">為參數指定的值不明。</span><span class="sxs-lookup"><span data-stu-id="bc48b-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="bc48b-122">MCIERR \_ 錯誤的 \_ 整數</span><span class="sxs-lookup"><span data-stu-id="bc48b-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="bc48b-123">命令中的整數無效或遺失。</span><span class="sxs-lookup"><span data-stu-id="bc48b-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="bc48b-124">MCIERR \_ 重複的 \_ 旗標</span><span class="sxs-lookup"><span data-stu-id="bc48b-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="bc48b-125">指定了兩次旗標或值。</span><span class="sxs-lookup"><span data-stu-id="bc48b-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="bc48b-126">MCIERR \_ 遺失 \_ 命令 \_ 字串</span><span class="sxs-lookup"><span data-stu-id="bc48b-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="bc48b-127">未指定任何命令。</span><span class="sxs-lookup"><span data-stu-id="bc48b-127">No command was specified.</span></span>                         |
| <span data-ttu-id="bc48b-128">MCIERR \_ 遺失的 \_ 裝置 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="bc48b-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="bc48b-129">未指定任何裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="bc48b-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="bc48b-130">MCIERR \_ 遺漏 \_ 字串 \_ 引數</span><span class="sxs-lookup"><span data-stu-id="bc48b-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="bc48b-131">命令中遺漏字串值。</span><span class="sxs-lookup"><span data-stu-id="bc48b-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="bc48b-132">MCIERR \_ 新的 \_ 需要 \_ 別名</span><span class="sxs-lookup"><span data-stu-id="bc48b-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="bc48b-133">別名必須與「新的」裝置名稱一起使用。</span><span class="sxs-lookup"><span data-stu-id="bc48b-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="bc48b-134">MCIERR \_ 沒有 \_ 右 \_ 引號</span><span class="sxs-lookup"><span data-stu-id="bc48b-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="bc48b-135">遺漏右引號。</span><span class="sxs-lookup"><span data-stu-id="bc48b-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="bc48b-136">MCIERR \_ \_ 在 \_ 自動 \_ 開啟時通知</span><span class="sxs-lookup"><span data-stu-id="bc48b-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="bc48b-137">「通知」旗標在自動開啟時不合法。</span><span class="sxs-lookup"><span data-stu-id="bc48b-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="bc48b-138">MCIERR \_ 參數 \_ 溢位</span><span class="sxs-lookup"><span data-stu-id="bc48b-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="bc48b-139">輸出字串的長度不足。</span><span class="sxs-lookup"><span data-stu-id="bc48b-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="bc48b-140">MCIERR 剖析器 \_ \_ 內部</span><span class="sxs-lookup"><span data-stu-id="bc48b-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="bc48b-141">發生內部剖析器錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc48b-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="bc48b-142">MCIERR \_ 無法辨識的 \_ 關鍵字</span><span class="sxs-lookup"><span data-stu-id="bc48b-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="bc48b-143">指定了未知的命令參數。</span><span class="sxs-lookup"><span data-stu-id="bc48b-143">An unknown command parameter was specified.</span></span>       |



 

 

 