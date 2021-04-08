---
title: 使用者的延伸錯誤資訊
description: 如果有可用的延伸錯誤資訊，參與建立延伸錯誤資訊的元件就必須能夠輕鬆地找出問題。
ms.assetid: 10c54f53-f449-4e7d-ba84-7b000beaee22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f52e45e3f181c5aaa0db196f9ce791581cc38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840187"
---
# <a name="extended-error-information-for-the-user"></a><span data-ttu-id="bcabe-103">使用者的延伸錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="bcabe-103">Extended Error Information for the User</span></span>

<span data-ttu-id="bcabe-104">如果有可用的延伸錯誤資訊，參與建立延伸錯誤資訊的元件就必須能夠輕鬆地找出問題。</span><span class="sxs-lookup"><span data-stu-id="bcabe-104">If extended error information is available, the components participating in the creation of the extended error information must make it easy to find the problem.</span></span> <span data-ttu-id="bcabe-105">第一個步驟是檢查最後一個延伸的錯誤記錄，並判斷問題的來源。</span><span class="sxs-lookup"><span data-stu-id="bcabe-105">The first step is to review the last extended error record, and determine on which computer and which process the problem originated.</span></span> <span data-ttu-id="bcabe-106">這通常是 RPC S 錯誤的原因 \_ \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="bcabe-106">This is often the cause of the RPC\_S\_\* error.</span></span> <span data-ttu-id="bcabe-107">尋找偵測位置，並判斷此偵測位置的參數是什麼意思。</span><span class="sxs-lookup"><span data-stu-id="bcabe-107">Find the detection location, and determine what the parameters for this detection location mean.</span></span> <span data-ttu-id="bcabe-108">它們通常表示函式呼叫失敗或特定檢查。</span><span class="sxs-lookup"><span data-stu-id="bcabe-108">Usually they indicate a failure of a function call or particular check.</span></span> <span data-ttu-id="bcabe-109">從該處，判斷函數或檢查失敗的原因，並採取更正動作。</span><span class="sxs-lookup"><span data-stu-id="bcabe-109">From there, determine why the function or check fails, and take corrective action.</span></span>

<span data-ttu-id="bcabe-110">最後一筆記錄之前的記錄會指出錯誤抵達的路徑，而且通常會做為例行性檢查，而不是疑難排解程式中的且有助於。</span><span class="sxs-lookup"><span data-stu-id="bcabe-110">The records before the last record indicate the path by which the error arrived, and generally serve as a sanity check rather than an aide in the troubleshooting process.</span></span>

 

 




