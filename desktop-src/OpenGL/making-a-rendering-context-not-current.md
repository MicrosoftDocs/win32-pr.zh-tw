---
title: 使轉譯內容不是最新的
description: 若要從執行緒卸離轉譯內容，請使它不是最新的。 您可以藉由呼叫 wglMakeCurrent 函式，並將參數設定為 Null 來完成這項作業。 以下是這項簡單工作的範例。
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300635"
---
# <a name="making-a-rendering-context-not-current"></a><span data-ttu-id="c2c9c-107">使轉譯內容不是最新的</span><span class="sxs-lookup"><span data-stu-id="c2c9c-107">Making a Rendering Context Not Current</span></span>

<span data-ttu-id="c2c9c-108">若要從執行緒卸離轉譯內容，請使它不是最新的。</span><span class="sxs-lookup"><span data-stu-id="c2c9c-108">To detach a rendering context from a thread, make it not current.</span></span> <span data-ttu-id="c2c9c-109">您可以藉由呼叫 [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) 函式，並將參數設定為 **Null** 來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="c2c9c-109">You can do this by calling the [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) function with the parameters set to **NULL**.</span></span> <span data-ttu-id="c2c9c-110">以下是這項簡單工作的範例。</span><span class="sxs-lookup"><span data-stu-id="c2c9c-110">The following is a sample of this simple task.</span></span>

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




