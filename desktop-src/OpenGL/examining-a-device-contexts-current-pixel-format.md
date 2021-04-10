---
title: 檢查裝置內容目前的像素格式
description: 使用 GetPixelFormat 和 DescribePixelFormat 函數來檢查裝置內容的目前像素格式，如下列程式碼片段所示。
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- Windows 上的 OpenGL，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea36f0f25b2cf76a6fb2ffb3159a4f2763a95af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183265"
---
# <a name="examining-a-device-contexts-current-pixel-format"></a>檢查裝置內容目前的像素格式

使用 [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) 和 [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) 函數來檢查裝置內容的目前像素格式，如下列程式碼片段所示。


```C++
PIXELFORMATDESCRIPTOR  pfd;
HDC    hdc;
int    iPixelFormat;
 
// if the device context has a current pixel format ...  
if (iPixelFormat = GetPixelFormat(hdc)) { 
 
    // obtain a detailed description of that pixel format  
    DescribePixelFormat(hdc, iPixelFormat, 
                             sizeof(PIXELFORMATDESCRIPTOR), &pfd); 
    }
```



 

 




