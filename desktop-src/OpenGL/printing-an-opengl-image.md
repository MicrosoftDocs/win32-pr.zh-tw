---
title: 列印 OpenGL 影像
description: 您可以列印在增強型中繼檔中轉譯的 OpenGL 影像。
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- Windows 上的 OpenGL，列印
- 列印 OpenGL 影像 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967285"
---
# <a name="printing-an-opengl-image"></a>列印 OpenGL 影像

您可以列印在增強型中繼檔中轉譯的 OpenGL 影像。 當您 (HDC 轉譯為印表機裝置時) 必須由中繼檔多工緩衝處理器支援。 OpenGL 使用記憶體來取得深度、色彩和其他緩衝區，以將圖形輸出儲存至印表機。 由於一般印表機解析度需要大量的記憶體來儲存圖形輸出，列印 OpenGL 映射可能需要的記憶體比系統中提供的還多。 為了克服這項限制，OpenGL 的目前執行會將 OpenGL 圖形列印在帶狀中。 不過，這會增加列印 OpenGL 影像所花費的時間。

列印 OpenGL 映射之前，您必須先呼叫 [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) 函式來完成印表機裝置內容 (DC) 的初始化工作。 在呼叫 **StartDoc** 之後，您可以建立轉譯內容， (HGLRC) 轉譯為印表機裝置。 如果您在呼叫 **StartDoc** 之前建立轉譯內容，則無法判斷中繼檔是否為多工緩衝處理。

下列程式碼範例顯示如何列印 OpenGL 映射：

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

如需使用中繼檔的詳細資訊，請參閱 [增強的中繼檔作業](/windows/desktop/gdi/enhanced-metafile-operations)。

 

 