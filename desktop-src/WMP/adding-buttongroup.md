---
title: 新增 BUTTONGROUP
description: 新增 BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- 建立外觀，BUTTONGROUP 元素
- Windows Media Player 的 BUTTONGROUP 元素
- 外觀，BUTTONGROUP 元素
- 外觀定義檔，BUTTONGROUP 元素
- BUTTONGROUP 元素
- 元素，BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300419"
---
# <a name="adding-buttongroup"></a>新增 BUTTONGROUP

這個範例會使用 **BUTTONGROUP** 專案來進行面板定義檔中的程式碼撰寫。 **BUTTONGROUP** 會建立一個簡單的方法來處理滑鼠事件，而不需要計算畫面上的確切位置，而是使用色彩，而不是 x 和 y 座標。

首先，您必須將 **BUTTONGROUP** 標記新增至您建立的面板定義檔。 將它們放在 **主題** 標記屬性之後。


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



針對您接下來要新增的按鈕，在結尾 **BUTTONGROUP** 標籤上方留下幾行空白行。

下列屬性是用來定義 **BUTTONGROUP**：

**mappingImage**

這是您先前建立之地圖美工檔案的檔案名，也就是具有紅色和綠色圓形的檔案名。 任何 **BUTTONGROUP** 都需要這個屬性。

**hoverImage**

這是您先前建立之暫止的美工圖案檔案的檔案名，其中有兩個黃色按鈕，其會讀取「播放」和「關閉」。 這並不是必要的，但暫留影像有助於將意見反應提供給使用者。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立外觀定義檔**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




