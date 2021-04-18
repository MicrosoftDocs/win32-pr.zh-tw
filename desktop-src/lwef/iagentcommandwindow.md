---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969051"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

**IAgentCommandWindow** 定義了一個介面，可讓應用程式設定和查詢 [語音命令] 視窗的屬性。 [語音命令] 視窗是一種共用資源，主要是設計來讓使用者能夠查看啟用語音的命令。 如果已停用 [語音辨識]，[語音命令] 視窗仍會顯示，並以字元) 的語言 (文字「語音輸入已停用」。 如果未安裝符合字元語言設定的語音引擎，則視窗會顯示「無法使用語音輸入」。 如果輸入-主動用戶端尚未針對其命令定義語音參數，且已停用全域語音命令，則視窗會顯示「沒有聲音命令」。 您也可以查詢 [語音命令] 視窗的內容，不論語音輸入是否已停用或是否已安裝相容的語音引擎。

**依照 Vtable 順序的方法**



| IAgentCommandWindow 方法                             | Description                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | 設定 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性值。    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | 傳回 [語音命令] 視窗的 [**Visible**](visible-property.md) 屬性值。 |
| [**GetPosition**](iagentcommandwindow--getposition.md) | 傳回語音命令視窗的位置。                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | 傳回語音命令視窗的大小。                                                      |



 

 

 




