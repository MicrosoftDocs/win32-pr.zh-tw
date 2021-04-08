---
title: 撰寫事件程式碼
description: 撰寫事件程式碼
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Windows Media Player 的面板，撰寫程式碼
- 外觀，撰寫程式碼
- 事件，撰寫程式碼
- 撰寫適用于面板的程式碼，關於
- Windows Media Player 的外觀、事件
- 外觀，事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022055"
---
# <a name="writing-event-code"></a>撰寫事件程式碼

事件的處理方式類似于屬性。 您必須為事件提供值，而值則是您想要在事件發生時執行的程式碼。 "On" 這個字會新增至事件名稱的前方;例如，click 事件將會變成 **onclick**。

事件值是以雙引號括住，並以後面接著冒號的單字 JScript 開頭。 接下來是您想要執行的程式碼，後面接著分號和結尾雙引號。 例如，若要在使用者按一下按鈕時停止播放，請在 **按鈕** 元素程式碼中輸入下列內容做為屬性：


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



如果您的程式碼需要用引號括住，請使用單引號。 使用引號時必須特別小心，如此才能適當地平衡。 以下是使用這兩種類型的範例：


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



您也可以在處理外來事件時變更面板的屬性。 例如，若要關閉名為 myView 的視圖，您可以輸入：


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**處理事件**](handling-events.md)
</dt> </dl>

 

 




