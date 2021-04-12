---
title: 使用雙緩衝區繪製
description: 雙緩衝區會讓一個影像和螢幕上的另一個影像之間的轉換變平滑。
ms.assetid: 10801cc7-d26c-4bfd-95c0-f352a1c7a1f5
keywords:
- Windows 上的 OpenGL、雙緩衝區
- double 緩衝區 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe52d427467b2a6e460ea56a9e72e580ea6f97d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311079"
---
# <a name="drawing-with-double-buffers"></a><span data-ttu-id="60056-105">使用雙緩衝區繪製</span><span class="sxs-lookup"><span data-stu-id="60056-105">Drawing with Double Buffers</span></span>

<span data-ttu-id="60056-106">雙緩衝區會讓一個影像和螢幕上的另一個影像之間的轉換變平滑。</span><span class="sxs-lookup"><span data-stu-id="60056-106">Double buffers smooth the transition between one image and another on the screen.</span></span> <span data-ttu-id="60056-107">交換緩衝區通常會出現在一連串的繪圖命令的結尾。</span><span class="sxs-lookup"><span data-stu-id="60056-107">Swapping buffers typically comes at the end of a sequence of drawing commands.</span></span> <span data-ttu-id="60056-108">根據預設，Microsoft 在 Windows 中執行 OpenGL 會繪製到螢幕上的緩衝區;繪製完成時，您可以呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) 函式，將螢幕緩衝複製到螢幕緩衝區。</span><span class="sxs-lookup"><span data-stu-id="60056-108">By default, the Microsoft implementation of OpenGL in Windows draws to the off-screen buffer; when drawing is complete, you call the [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) function to copy the off-screen buffer to the on-screen buffer.</span></span> <span data-ttu-id="60056-109">下列程式碼範例會準備繪製、呼叫繪圖函式，然後將完成的影像複製到畫面上（如果有雙重緩衝處理）。</span><span class="sxs-lookup"><span data-stu-id="60056-109">The following code sample prepares to draw, calls a drawing function, and then copies the completed image on to the screen if double buffering is available.</span></span>


```C++
void myRedraw(void) 
{ 
    // set up for drawing commands  
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective(45, 1.0, 0.1, 100.0); 
 
    // draw our objects  
    myDrawAllObjects(GL_FALSE); 
 
    // if we're double-buffering ...  
    if (bDoubleBuffering)  
 
        // ...draw the copied image to the screen  
        SwapBuffers(hdc); 
}
```



<span data-ttu-id="60056-110">下列程式碼範例會取得視窗裝置內容、呈現場景、將影像複製到畫面 (以顯示轉譯) ，然後釋放裝置內容。</span><span class="sxs-lookup"><span data-stu-id="60056-110">The following code sample obtains a window device context, renders a scene, copies the image to the screen (to show the rendering), and then releases the device context.</span></span>


```C++
hdc = GetDC(hwnd); 
mySceneRenderingFunction(); 
SwapBuffers(hdc); 
ReleaseDC(hWnd, hdc);
```



 

 




