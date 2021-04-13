---
title: 使用播放玩家
description: 使用播放玩家
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Windows Media Player 的外觀、JScript 中的播放機屬性
- 在 JScript 中的外觀、播放機屬性
- 屬性、播放機
- player 屬性
- 適用于外觀的 JScript 檔案，player 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372638"
---
# <a name="working-with-the-player"></a>使用播放玩家

使用 Microsoft JScript 存取 Windows Media Player 的方法和屬性時，您必須使用名稱 "Player" 作為控制項的名稱。 例如，若要參考 Stop 方法，您必須輸入：


```C++
player.Controls.Stop()

```



**Player** global 屬性是透過外觀腳本存取 Windows Media Player 控制項的關鍵。 透過這個屬性，Windows Media Player 控制項的所有物件都會變成可透過其屬性和方法來進行執行時間修改的存取。 此外，還可以使用 **PLAYER** 元素，以便在設計階段指定事件處理常式和 **url** 屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 JScript**](using-jscript.md)
</dt> </dl>

 

 




