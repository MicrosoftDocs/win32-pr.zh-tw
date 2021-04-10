---
title: 移植意見函數
description: 使用鳶尾花 GL，處理意見反應的方式會因執行鳶尾花 GL 的電腦而有所不同。
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- 鳶尾花 GL 移植，意見反應
- 從鳶尾花 GL 進行移植，意見反應
- 從鳶尾花 GL 移植至 OpenGL，意見反應
- 鳶尾花 GL 的 OpenGL 移植，意見反應
- 意見回應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183898"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="ff45a-108">移植意見函數</span><span class="sxs-lookup"><span data-stu-id="ff45a-108">Porting Feedback Functions</span></span>

<span data-ttu-id="ff45a-109">使用鳶尾花 GL，處理意見反應的方式會因執行鳶尾花 GL 的電腦而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ff45a-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="ff45a-110">OpenGL 可將意見反應函式標準化，讓您可以依賴各種硬體平臺之間的一致意見反應。</span><span class="sxs-lookup"><span data-stu-id="ff45a-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="ff45a-111">下表列出鳶尾花 GL 意見反應函式及其對等的 OpenGL 函數。</span><span class="sxs-lookup"><span data-stu-id="ff45a-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="ff45a-112">鳶尾花 GL 函數</span><span class="sxs-lookup"><span data-stu-id="ff45a-112">IRIS GL function</span></span> | <span data-ttu-id="ff45a-113">OpenGL 函數</span><span class="sxs-lookup"><span data-stu-id="ff45a-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="ff45a-114">意義</span><span class="sxs-lookup"><span data-stu-id="ff45a-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="ff45a-115">**回饋**</span><span class="sxs-lookup"><span data-stu-id="ff45a-115">**feedback**</span></span>     | <span data-ttu-id="ff45a-116">[**glRenderMode**](glrendermode.md) ( GL \_ 意見反應 ) </span><span class="sxs-lookup"><span data-stu-id="ff45a-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="ff45a-117">切換至意見反應模式。</span><span class="sxs-lookup"><span data-stu-id="ff45a-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="ff45a-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="ff45a-118">**endfeedback**</span></span>  | <span data-ttu-id="ff45a-119">[**glRenderMode**](glrendermode.md) ( GL 轉譯 \_ ) [ **glFeedbackBuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="ff45a-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="ff45a-120">切換至轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="ff45a-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="ff45a-121">**通過**</span><span class="sxs-lookup"><span data-stu-id="ff45a-121">**passthrough**</span></span>  | [<span data-ttu-id="ff45a-122">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="ff45a-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="ff45a-123">將權杖標記放在意見緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="ff45a-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





