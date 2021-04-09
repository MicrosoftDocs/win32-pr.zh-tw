---
title: 顯示模式使用者介面
description: 顯示模式使用者介面
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Windows Media Player 外掛程式，顯示對話方塊和訊息方塊
- 外掛程式，顯示對話方塊和訊息方塊
- 使用者介面外掛程式，顯示對話方塊和訊息方塊
- UI 外掛程式，顯示對話方塊和訊息方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675884"
---
# <a name="displaying-modal-user-interfaces"></a>顯示模式使用者介面

UI 外掛程式不應顯示模式對話方塊或訊息方塊，以回應來自 Windows Media Player 的方法呼叫。 例如，請勿從 **IWMPPluginUI：： Create** 的執行顯示訊息方塊。

如果您必須從播放程式所呼叫的 UI 外掛程式方法執行中顯示對話方塊或訊息方塊，則必須遵循下列步驟：

1.  使用 **RegisterWindowMessage** 註冊新的視窗訊息。
2.  使用 **PostMessage** 將您註冊的視窗訊息傳送至 UI 外掛程式視窗。
3.  從訊息處理常式顯示新視窗訊息的對話方塊或訊息方塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**UI 外掛程式總覽**](ui-plug-in-overview.md)
</dt> </dl>

 

 




