---
title: Color-Index 模式和 Windows 的管理元件管理
description: 色彩索引模式會以特定邏輯調色板專案的索引，指定邏輯調色板中的色彩。
ms.assetid: 8cf07c3e-8a8b-4f28-a363-34d3c0d33890
keywords:
- Windows 上的 OpenGL，管理元件管理
- Windows 上的 OpenGL、色彩索引模式
- 色彩索引模式 OpenGL
- 調色板管理 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e4d7c9db02a80bdffdef93655e88cc5b2ca8197a58c5ffdb488c2b782f10d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889258"
---
# <a name="color-index-mode-and-windows-palette-management"></a>Color-Index 模式和 Windows 的管理元件管理

色彩索引模式會以特定邏輯調色板專案的索引，指定邏輯調色板中的色彩。 大部分的 GDI 程式都使用色彩索引調色板，但 RGBA 模式的效果較適用于 OpenGL 的數個效果，例如陰影、光源、霧化和材質對應。 如果您的 OpenGL 應用程式具有 truest 色彩並不重要，您可以選擇使用色彩索引模式 (例如，使用「false 色彩」的地形對應強調提高許可權漸層) 。

## <a name="color-index-mode-palette-sample"></a>Color-Index 模式調色板範例

下列程式碼會設定 [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) 結構，將 **iPixelType** 成員的旗標設定為 PFD \_ 類型 \_ COLORINDEX。 這會指定應用程式使用色彩索引調色板。


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



 

 




