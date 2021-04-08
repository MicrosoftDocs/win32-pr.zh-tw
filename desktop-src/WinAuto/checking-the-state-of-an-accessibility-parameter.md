---
title: 檢查協助工具參數的狀態
description: 下列程式碼片段會使用 GetSystemMetrics 函式來檢查 [聲音] 參數。 如果 GetSystemMetrics 傳回 TRUE，則應用程式應該以視覺化形式呈現所有重要資訊。
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023567"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a><span data-ttu-id="9ee0f-104">檢查協助工具參數的狀態</span><span class="sxs-lookup"><span data-stu-id="9ee0f-104">Checking the State of an Accessibility Parameter</span></span>

<span data-ttu-id="9ee0f-105">下列程式碼片段會使用 [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) 函式來檢查 [聲音] 參數。</span><span class="sxs-lookup"><span data-stu-id="9ee0f-105">The following code fragment uses the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to check the ShowSounds parameter.</span></span> <span data-ttu-id="9ee0f-106">如果 **GetSystemMetrics** 傳回 **TRUE**，則應用程式應該以視覺化形式呈現所有重要資訊。</span><span class="sxs-lookup"><span data-stu-id="9ee0f-106">If **GetSystemMetrics** returns **TRUE**, the application should present all important information in visual form.</span></span>


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 