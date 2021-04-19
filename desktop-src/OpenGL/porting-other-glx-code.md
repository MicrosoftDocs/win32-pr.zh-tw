---
title: 移植其他 GLX 程式碼
description: 移植其他 GLX 程式碼
ms.assetid: 3a67a206-d249-493c-a774-c3bbaa933611
keywords:
- 移植至 OpenGL、GLX 程式碼
- OpenGL 移植，GLX 程式碼
- X 視窗系統，移植 GLX 程式碼
- GLX 函式，移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c2f9430fbef8bef7c41a2d6c6f86bf6e9f3e7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968242"
---
# <a name="porting-other-glx-code"></a><span data-ttu-id="90a80-107">移植其他 GLX 程式碼</span><span class="sxs-lookup"><span data-stu-id="90a80-107">Porting Other GLX Code</span></span>

<span data-ttu-id="90a80-108">除了上述各節所述的 Xlib 和 GLX 函式之外，您的程式可能還包含 [翻譯 GLX 程式庫](translating-the-glx-library.md)中列出的其他 GLX 或 Xlib 函式。</span><span class="sxs-lookup"><span data-stu-id="90a80-108">In addition to the Xlib and GLX functions described in the preceding sections, your program probably contains some of the other GLX or Xlib functions listed in [Translating the GLX Library](translating-the-glx-library.md).</span></span> <span data-ttu-id="90a80-109">將您的 X 視窗系統程式碼重寫為 Windows，並替代適當的函式。</span><span class="sxs-lookup"><span data-stu-id="90a80-109">Rewrite your X Window System code to Windows, substituting the appropriate functions.</span></span>

 

 




