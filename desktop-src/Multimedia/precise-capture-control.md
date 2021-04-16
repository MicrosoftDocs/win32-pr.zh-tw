---
title: 精確的 Capture 控制項
description: 精確的 Capture 控制項
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- AVICap 回呼函式，精確的 capture 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507189"
---
# <a name="precise-capture-control"></a><span data-ttu-id="69adf-104">精確的 Capture 控制項</span><span class="sxs-lookup"><span data-stu-id="69adf-104">Precise Capture Control</span></span>

<span data-ttu-id="69adf-105">捕捉視窗可以提供 capture 控制項回呼函式，並精確地控制串流處理的開始和結束時間。</span><span class="sxs-lookup"><span data-stu-id="69adf-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="69adf-106">從 capture 驅動程式傳送到回呼程式的第一個訊息會將 *nState* 參數設定為 \_ 在配置所有緩衝區後 CONTROLCALLBACK 預先設定，並完成所有其他的捕獲準備工作。</span><span class="sxs-lookup"><span data-stu-id="69adf-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="69adf-107">此訊息可讓應用程式預先擁有影片來源的能力。</span><span class="sxs-lookup"><span data-stu-id="69adf-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="69adf-108"> (回呼函式會將 *nState* 指定為其第二個參數。 ) 回呼函式，則會在確切的時刻記錄開始時傳回。</span><span class="sxs-lookup"><span data-stu-id="69adf-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="69adf-109">回呼函式中 **TRUE** 的傳回值會繼續捕捉。</span><span class="sxs-lookup"><span data-stu-id="69adf-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="69adf-110">**FALSE** 中止捕捉的傳回值。</span><span class="sxs-lookup"><span data-stu-id="69adf-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="69adf-111">一旦開始 capture，會經常呼叫回呼函式，並將 *nState* 設定為 CONTROLCALLBACK capture， \_ 以允許應用程式藉由傳回 **FALSE** 來結束捕捉。</span><span class="sxs-lookup"><span data-stu-id="69adf-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




