---
title: 訊息對應
description: 訊息對應
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Windows Media Player 外掛程式、訊息對應
- 外掛程式，訊息對應
- 使用者介面外掛程式、訊息對應
- UI 外掛程式、訊息對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021558"
---
# <a name="the-message-map"></a>訊息對應

外掛程式視窗會藉由呼叫對應至對應事件訊息的方法，來回應各種事件。 Wizard 會提供對應，以便在適當的時間呼叫 OnPaint 和 OnEraseBackground。 若要建立 [ **搜尋** ] 按鈕，並從它回應按一下，則會修改訊息對應區段，如下所示：


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行 CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




