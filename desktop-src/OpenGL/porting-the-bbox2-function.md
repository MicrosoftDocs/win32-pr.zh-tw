---
title: 移植 bbox2 函式
description: 鳶尾花 GL bbox2 函數沒有任何 OpenGL 對等專案。
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- 鳶尾花 GL 移植，bbox2 函式
- 從鳶尾花 GL、bbox2 函式移植
- 從鳶尾花 GL、bbox2 函式移植至 OpenGL
- 從鳶尾花 GL、bbox2 函式移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674532"
---
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="d17dc-107">移植 bbox2 函式</span><span class="sxs-lookup"><span data-stu-id="d17dc-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="d17dc-108">鳶尾花 GL **bbox2** 函數沒有任何 OpenGL 對等專案。</span><span class="sxs-lookup"><span data-stu-id="d17dc-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="d17dc-109">**若要移植包含 bbox2 函式的程式碼**</span><span class="sxs-lookup"><span data-stu-id="d17dc-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="d17dc-110">建立新的 (OpenGL) 顯示清單，其中包含對等鳶尾花 GL 顯示清單中的所有專案，但呼叫 **bbox2** 除外。</span><span class="sxs-lookup"><span data-stu-id="d17dc-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="d17dc-111">使用適當的 Windows 程式碼來繪製與鳶尾花 GL **bbox** 相同大小的矩形。</span><span class="sxs-lookup"><span data-stu-id="d17dc-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 




