---
title: 新增 User-Controlled 播放
description: 新增 User-Controlled 播放
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999574"
---
# <a name="adding-user-controlled-playback"></a>新增 User-Controlled 播放

您可以藉由呼叫 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式，將使用者控制的播放新增至現有的應用程式，如下所示：


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)參數會識別父視窗的控制碼，以及與 MCIWnd 視窗相關聯的模組實例。 它們也會指定視窗樣式和檔案名 (或裝置名稱，) 要與 MCIWnd 視窗相關聯。

**MCIWndCreate** 會自動執行下列步驟，針對其他視窗類別，您可以自行在程式碼中執行：

1.  註冊 MCIWnd 視窗類別。
2.  建立 MCIWnd 視窗。
3.  載入指定的內容。
4.  在內容的開頭建立目前的播放位置。
5.  顯示裝置控制項。
6.  如有需要，顯示視窗的播放區域。

 

 




