---
title: 共用顯示清單
description: 當您建立轉譯內容時，它會有自己的顯示清單空間。
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- Windows 上的 OpenGL，共用顯示清單
- 共用顯示清單 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311073"
---
# <a name="sharing-display-lists"></a><span data-ttu-id="70723-105">共用顯示清單</span><span class="sxs-lookup"><span data-stu-id="70723-105">Sharing Display Lists</span></span>

<span data-ttu-id="70723-106">當您建立轉譯內容時，它會有自己的顯示清單空間。</span><span class="sxs-lookup"><span data-stu-id="70723-106">When you create a rendering context, it has its own display-list space.</span></span> <span data-ttu-id="70723-107">[**WglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)函式可讓轉譯內容共用另一個呈現內容的顯示清單空間。</span><span class="sxs-lookup"><span data-stu-id="70723-107">The [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) function enables a rendering context to share the display-list space of another rendering context.</span></span> <span data-ttu-id="70723-108">任意數目的轉譯內容都可以共用單一顯示清單空間。</span><span class="sxs-lookup"><span data-stu-id="70723-108">Any number of rendering contexts can share a single display-list space.</span></span>

 

 




