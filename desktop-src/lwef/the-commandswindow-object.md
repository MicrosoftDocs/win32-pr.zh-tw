---
title: CommandsWindow 物件
description: CommandsWindow 物件
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336bdff598a75a9b0b07adabb11c271a45ca84940f528ebe082de17841592d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882462"
---
# <a name="the-commandswindow-object"></a>CommandsWindow 物件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

[**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object)物件可讓您存取 [語音命令] 視窗的屬性。 [語音命令] 視窗是一種共用資源，主要是設計來讓使用者能夠查看啟用語音的命令。 如果已停用 [語音辨識]，[語音命令] 視窗仍會顯示，並以字元) 的語言 (文字「語音輸入已停用」。 如果未安裝任何符合字元語言設定的語音引擎，則會顯示「無法使用語音輸入」。 如果輸入-主動用戶端尚未針對其命令定義語音參數，且已停用全域語音命令，則視窗會顯示「沒有聲音命令」。 您也可以查詢 [語音命令] 視窗的內容，不論語音輸入是否已停用或是否已安裝相容的語音引擎。

-   [CommandsWindow 屬性](commandswindow-properties.md)

 

 