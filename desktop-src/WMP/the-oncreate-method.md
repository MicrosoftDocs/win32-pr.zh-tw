---
title: '>oncreate 方法'
description: '>oncreate 方法'
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player 外掛程式，>oncreate 方法
- 外掛程式，>oncreate 方法
- 使用者介面外掛程式，>oncreate 方法
- UI 外掛程式，>oncreate 方法
- '>oncreate 方法'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839395"
---
# <a name="the-oncreate-method"></a>>oncreate 方法

第一次建立外掛程式視窗時，會呼叫 >oncreate 方法。

下列程式碼會用來執行此方法：


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



這個方法會建立 **搜尋** 按鈕，並將其與在檔案 \_ 開頭定義的 IDC 搜尋命令識別碼產生關聯：


```C++
#define IDC_SEARCH 2000

```



此命令識別碼會對應至先前所述之訊息對應區段中的 OnSearch 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




