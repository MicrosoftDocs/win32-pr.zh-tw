---
title: 移植消除鋸齒功能
description: 移植消除鋸齒功能
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- 鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植，消除鋸齒
- 從鳶尾花 GL 移植至 OpenGL，消除鋸齒
- 從鳶尾花 GL 的 OpenGL 移植，消除鋸齒
- 消除鋸齒 (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372612"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="dbaf6-108">移植消除鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="dbaf6-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="dbaf6-109">在 OpenGL 中，子圖元模式一律為開啟，因此鳶尾花 GL 函式 **子圖元** (**TRUE**) 不是必要的，而且沒有 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="dbaf6-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="dbaf6-110">下列主題描述移植鳶尾花 GL 消除鋸齒程式碼的各個層面。</span><span class="sxs-lookup"><span data-stu-id="dbaf6-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="dbaf6-111">移植混合程式碼</span><span class="sxs-lookup"><span data-stu-id="dbaf6-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="dbaf6-112">移植 afunction 測試函式</span><span class="sxs-lookup"><span data-stu-id="dbaf6-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="dbaf6-113">使用消除鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="dbaf6-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




