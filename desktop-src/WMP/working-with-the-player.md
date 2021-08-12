---
title: 使用播放玩家
description: 使用播放玩家
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player 的外觀、JScript 中的播放機屬性
- 外觀，JScript 中的播放機屬性
- 屬性、播放機
- player 屬性
- 面板的 JScript 檔案、播放機屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77098f161244488d5097d2d022f105628a43ba50a40218da01295d99f2de0cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566980"
---
# <a name="working-with-the-player"></a>使用播放玩家

使用 Microsoft JScript 存取 Windows Media Player 的方法和屬性時，您必須使用名稱 "Player" 作為控制項的名稱。 例如，若要參考 Stop 方法，您必須輸入：


```C++
player.Controls.Stop()

```



**player** global 屬性是透過外觀腳本存取 Windows Media Player 控制項的關鍵。 透過這個屬性，Windows Media Player 控制項的所有物件都會變成可透過其屬性和方法來進行執行時間修改的存取。 此外，還可以使用 **PLAYER** 元素，以便在設計階段指定事件處理常式和 **url** 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 JScript**](using-jscript.md)
</dt> </dl>

 

 




