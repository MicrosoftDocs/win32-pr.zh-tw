---
title: 緩衝區函數
description: 若要將螢幕緩衝區的內容複寫到螢幕緩衝區，請呼叫 SwapBuffers。
ms.assetid: 605eba4e-ee38-4e62-adf8-1b7894030cb0
keywords:
- WGL 函式，緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b03a12cd07b76d1329f51cc982508c707e011701b072a42b099df05327842d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618591"
---
# <a name="buffer-functions"></a>緩衝區函數

若要將螢幕緩衝區的內容複寫到螢幕緩衝區，請呼叫 [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)。 **SwapBuffers** 函式會接受裝置內容的控制碼。 指定之裝置內容的目前像素格式必須包含背景緩衝區。 根據預設，背景緩衝區會在螢幕上，而前端緩衝區會在螢幕上。

> [!Note]  
> **SwapBuffers** 函式不會實際交換這兩個緩衝區的內容，而是會將一個緩衝區的內容複寫到另一個緩衝區。 在呼叫 **SwapBuffers** 之後，不會定義非螢幕緩衝區的內容。 因此，兩個連續呼叫 **SwapBuffers** 的結果為未定義。

 

下圖顯示呼叫 **SwapBuffers** 時，如何複製緩衝區的內容。

![此圖顯示連續呼叫 SwapBuffers 函式的未定義結果。](images/opengl00.png)

許多 OpenGL 核心函數也會管理緩衝區。 [**GlDrawBuffer**](gldrawbuffer.md)函式是與雙重緩衝最相關的函數;它會指定 OpenGL 繪製的畫面格緩衝區或緩衝區。

下列函數也會影響緩衝區：

-   [**glReadBuffer**](glreadbuffer.md)
-   [**glReadPixels**](glreadpixels.md)
-   [**glCopyPixels**](glcopypixels.md)
-   [**glAccum**](glaccum.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glIndexMask**](glindexmask.md)
-   [**glStencilMask**](glstencilmask.md)
-   [**glClearAccum**](glclearaccum.md)
-   [**glClearColor**](glclearcolor.md)
-   [**glClearDepth**](glcleardepth.md)
-   [**glClearIndex**](glclearindex.md)
-   [**glClearStencil**](glclearstencil.md)

 

 




