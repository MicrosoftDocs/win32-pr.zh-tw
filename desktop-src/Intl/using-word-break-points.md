---
description: 當應用程式處理整個單字時，插入號的有效位置會以 SCRIPT LOGATTR 結構的 fWordStop 成員值標示 \_ 。 藉由呼叫 ScriptBreak 來取出此值。
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: 使用斷詞點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195428"
---
# <a name="using-word-break-points"></a><span data-ttu-id="3c7b1-104">使用斷詞點</span><span class="sxs-lookup"><span data-stu-id="3c7b1-104">Using Word Break Points</span></span>

<span data-ttu-id="3c7b1-105">當應用程式處理整個單字時，插入號的有效位置會以 [**SCRIPT \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員值標示。</span><span class="sxs-lookup"><span data-stu-id="3c7b1-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="3c7b1-106">藉由呼叫 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)來取出此值。</span><span class="sxs-lookup"><span data-stu-id="3c7b1-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="3c7b1-107">單字之間的斷線有效位置會以 [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)所抓取的 **fSoftBreak** 值標示。</span><span class="sxs-lookup"><span data-stu-id="3c7b1-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c7b1-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c7b1-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c7b1-109">使用 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="3c7b1-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



