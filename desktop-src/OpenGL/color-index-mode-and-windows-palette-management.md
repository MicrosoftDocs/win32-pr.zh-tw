---
title: Color-Index 模式和 Windows 調色板管理
description: 色彩索引模式會以特定邏輯調色板專案的索引，指定邏輯調色板中的色彩。
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- Windows 上的 OpenGL，調色板管理
- Windows 上的 OpenGL、色彩索引模式
- 色彩索引模式 OpenGL
- 調色板管理 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873308c4ac64d496e344b1c71d440d4dc8321418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021726"
---
# <a name="color-index-mode-and-windows-palette-management"></a><span data-ttu-id="deec1-107">Color-Index 模式和 Windows 調色板管理</span><span class="sxs-lookup"><span data-stu-id="deec1-107">Color-Index Mode and Windows Palette Management</span></span>

<span data-ttu-id="deec1-108">色彩索引模式會以特定邏輯調色板專案的索引，指定邏輯調色板中的色彩。</span><span class="sxs-lookup"><span data-stu-id="deec1-108">The color-index mode specifies colors in a logical palette with an index to a specific logical-palette entry.</span></span> <span data-ttu-id="deec1-109">大部分的 GDI 程式都使用色彩索引調色板，但 RGBA 模式的效果較適用于 OpenGL 的數個效果，例如陰影、光源、霧化和材質對應。</span><span class="sxs-lookup"><span data-stu-id="deec1-109">Most GDI programs use color-index palettes, but the RGBA mode works better for OpenGL for several effects, such as shading, lighting, fog, and texture mapping.</span></span> <span data-ttu-id="deec1-110">如果您的 OpenGL 應用程式具有 truest 色彩並不重要，您可以選擇使用色彩索引模式 (例如，使用「false 色彩」的地形對應強調提高許可權漸層) 。</span><span class="sxs-lookup"><span data-stu-id="deec1-110">If having the truest color isn't critical for your OpenGL application, you might choose to use the color-index mode (for example, for a topographic map that uses "false color" to emphasize the elevation gradient).</span></span>

## <a name="color-index-mode-palette-sample"></a><span data-ttu-id="deec1-111">Color-Index 模式調色板範例</span><span class="sxs-lookup"><span data-stu-id="deec1-111">Color-Index Mode Palette Sample</span></span>

<span data-ttu-id="deec1-112">下列程式碼會設定 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 結構，將 **iPixelType** 成員的旗標設定為 PFD \_ 類型 \_ COLORINDEX。</span><span class="sxs-lookup"><span data-stu-id="deec1-112">The following code sets up a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) structure that sets the flag of the **iPixelType** member to PFD\_TYPE\_COLORINDEX.</span></span> <span data-ttu-id="deec1-113">這會指定應用程式使用色彩索引調色板。</span><span class="sxs-lookup"><span data-stu-id="deec1-113">This specifies that the application use a color-index palette.</span></span>


```C++
BOOL bSetupPixelFormat(HDC hdc) 
{ 
    PIXELFORMATDESCRIPTOR pfd, *ppfd; 
    int pixelformat; 
 
    ppfd = &pfd; 
 
    ppfd->nSize = sizeof(PIXELFORMATDESCRIPTOR); 
    ppfd->nVersion = 1; 
    ppfd->dwFlags = PFD_DRAW_TO_WINDOW | PFD_SUPPORT_OPENGL |  
                        PFD_DOUBLEBUFFER; 
    ppfd->dwLayerMask = PFD_MAIN_PLANE; 
 
    /* Set to color-index mode and use the default color palette. */ 
    ppfd->iPixelType = PFD_TYPE_COLORINDEX;  
 
    ppfd->cColorBits = 8; 
    ppfd->cDepthBits = 16; 
    ppfd->cAccumBits = 0; 
    ppfd->cStencilBits = 0; 
 
    pixelformat = ChoosePixelFormat(hdc, ppfd); 
 
    if ( (pixelformat = ChoosePixelFormat(hdc, ppfd)) == 0 ) 
    { 
        MessageBox(NULL, "ChoosePixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    if (SetPixelFormat(hdc, pixelformat, ppfd) == FALSE) 
    { 
        MessageBox(NULL, "SetPixelFormat failed", "Error", MB_OK); 
        return FALSE; 
    } 
 
    return TRUE; 
}
```



 

 




