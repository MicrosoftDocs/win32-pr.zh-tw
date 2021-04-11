---
title: 檢查裝置支援的像素格式
description: DescribePixelFormat 函式會取得裝置內容的像素格式資料。
ms.assetid: 1ebeb051-2dc9-4753-a0f3-7d2737b5f7f2
keywords:
- Windows 上的 OpenGL，圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ee45212111354d79b7a23fd35490a08f0aead4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372514"
---
# <a name="examining-a-devices-supported-pixel-formats"></a>檢查裝置支援的像素格式

[**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)函式會取得裝置內容的像素格式資料。 它也會傳回整數，這是裝置內容的最大像素格式索引。 下列程式碼範例會示範如何使用該結果逐步執行，並檢查裝置所支援的像素格式：


```C++
// local variables  
int                      iMax ; 
PIXELFORMATDESCRIPTOR    pfd; 
int                      iPixelFormat ; 
 
// initialize a pixel format index variable  
iPixelFormat = 1; 
 
// keep obtaining and examining pixel format data...  
do { 
    // try to obtain some pixel format data  
    iMax = DescribePixelFormat(hdc, iPixelFormat, sizeof(pfd), &pfd); 
 
    // if there was some problem with that...   
    if (iMax == 0) 
     
        // return indicating failure  
        return(FALSE); 
     
    // we have successfully obtained pixel format data  
 
    // let's examine the pixel format data...  
    myPixelFormatExaminer (&pfd); 
    }  
 
// ...until we've looked at all the device context's pixel formats  
while (++iPixelFormat <= iMax);
```



 

 




