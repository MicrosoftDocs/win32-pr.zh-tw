---
title: 檢查裝置內容目前的像素格式
description: 使用 GetPixelFormat 和 DescribePixelFormat 函數來檢查裝置內容的目前像素格式，如下列程式碼片段所示。
ms.assetid: 1da8c8e0-9444-421a-9c2e-c196b5a9db36
keywords:
- Windows 上的 OpenGL，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b76dd8db71356b16a5a258669ffe2938d0982ab5e1417389840610c57a0fcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361368"
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



 

 




