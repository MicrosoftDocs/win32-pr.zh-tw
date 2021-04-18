---
title: 外來事件
description: 外來事件
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Windows Media Player 的外觀、外來事件
- 外觀，外來事件
- 事件，外部
- 撰寫適用于外觀的程式碼，外來事件
- 外來事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965815"
---
# <a name="external-events"></a>外來事件

當使用者按一下按鈕或按下按鍵時，您可以使用事件處理常式來回應其輸入。 事件處理常式是每次觸發事件時執行的程式碼區段。

面板元素支援下列事件：

-   **載入**
-   **close**
-   **調整**
-   **計時 器**
-   **點擊**
-   **dblclick**
-   **error**
-   **mousedown**
-   **mouseup**
-   **mousemove**
-   **上方**
-   **mouseout**
-   **keypress**
-   **keydown**
-   **keyup**

如需特定事件的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md) 。

一般的外部事件處理常式會將事件命名，並定義將執行的程式碼。 例如，如果您想要建立程式碼來啟動 Windows Media Player 當使用者按一下按鈕時，您會將下列程式程式碼放在按鈕程式碼中。


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



這會播放名為 laure 的檔案。 請注意，您會將 "on" 這個字新增至特定事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**處理事件**](handling-events.md)
</dt> </dl>

 

 




