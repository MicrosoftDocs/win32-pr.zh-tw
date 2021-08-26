---
title: OnPaint 方法
description: OnPaint 方法
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Windows Media Player 外掛程式，OnPaint 方法
- 外掛程式，OnPaint 方法
- 使用者介面外掛程式，OnPaint 方法
- UI 外掛程式，OnPaint 方法
- OnPaint 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001948"
---
# <a name="the-onpaint-method"></a>OnPaint 方法

每當外掛程式視窗應該繪製本身時，就會呼叫 OnPaint 方法。 當外掛程式視窗收到 WM 油漆訊息時，就會發生這種情況 \_ ，這會對應至稍早所述之訊息對應中的 OnPaint 方法。 此 wizard 會提供這個方法的執行，以繪製背景黑色，並將外掛程式的名稱放在外掛程式視窗中。 搜尋 UI 外掛程式唯一需要的修改是移除顯示文字的程式碼。

下列程式碼會用來執行此方法：


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




