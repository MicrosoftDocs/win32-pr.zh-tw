---
title: 取得和設定影片格式
description: 取得和設定影片格式
ms.assetid: 0e6baf24-7a79-45ab-9fc7-69334419956d
keywords:
- capGetVideoFormat 宏
- capGetVideoFormatSize 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6890c3a1d653d43d24c5baa0790cc0d26040685b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842259"
---
# <a name="obtaining-and-setting-the-video-format"></a>取得和設定影片格式

[**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的長度可變，可容納標準和壓縮的資料格式。 因為此結構的長度不定，所以應用程式必須一律查詢結構的大小，並在抓取目前的影片格式之前配置記憶體。 下列範例會使用 [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) 宏來取出緩衝區大小，然後呼叫 [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) 宏以抓取目前的影片格式。


```C++
LPBITMAPINFO lpbi;
DWORD dwSize;

dwSize = capGetVideoFormatSize(hWndC);
lpbi = GlobalAllocPtr (GHND, dwSize);
capGetVideoFormat(hWndC, lpbi, dwSize); 

// Access the video format and then free the allocated memory.
 
```



應用程式可以使用 [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) 宏 (或 [**WM \_ CAP \_ SET \_ VIDEOFORMAT**](wm-cap-set-videoformat.md) message) 將 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 標頭結構傳送至 [capture] 視窗。 由於影片格式是裝置特定的，您的應用程式應該檢查傳回值，以判斷是否接受格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 