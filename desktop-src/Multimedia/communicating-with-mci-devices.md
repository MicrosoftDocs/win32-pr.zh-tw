---
title: 與 MCI 裝置通訊
description: 與 MCI 裝置通訊
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString 宏
- mciSendString 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969511"
---
# <a name="communicating-with-mci-devices"></a>與 MCI 裝置通訊

每個 MCI 裝置的驅動程式都會維護其目前設定和功能的清單，讓它可以在查詢資訊時發出精確的回應。

當您想要與 MCI 裝置通訊時，可以使用 MCIWnd 宏和函式。 許多最常見的 MCI 命令和查詢都會定義為宏。 但是，如果您要執行的工作無法作為函式或宏使用，您可以使用 [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) 宏或使用 MCI 命令的訊息表單或字串格式，將 mci 命令直接傳送到設備磁碟機。 使用 **MCIWndSendString** 宏相當於使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函數，如下所示：


```C++
mciSendString(sz, Null, 0, Null) 
```



[**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)的參數只會包含視窗控制碼和命令的字串形式。 若要取出字串命令所傳回的資訊，請使用 [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) 宏。

如需 MCI 的詳細資訊，請參閱 [mci](mci.md)。

> [!Note]  
> 當您使用 **MCIWndSendString** 時，必須從 MCI 命令排除裝置別名。 MCIWnd 程式庫會在將命令傳送至 MCI 裝置時，新增此別名。

 

 

 