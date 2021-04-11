---
title: 存取控制項方法、屬性和事件
description: 存取控制項方法、屬性和事件
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372121"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a>存取控制項方法、屬性和事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

使用 Microsoft Agent 的 control 搭配 Visual Basic 與使用 VBScript 的控制項非常類似，不同之處在于 Visual Basic 中的事件必須包含所傳遞參數的資料類型。 將 Microsoft Agent 控制項新增至表單時，會自動包含 Microsoft Agent 的事件及其適當的參數。 它也會在應用程式執行時，自動建立與代理程式伺服器的連接。

您也可以使用程式設計語言的 object's 建立語法，在執行時間建立控制項的實例。 例如，在 Visual Basic (5.0 或更新版本的) 中，如果您將 Microsoft Agent 2.0 控制項包含在專案的參考中，您可以使用 [**With 事件**](https://www.bing.com/search?q=**With+Events**)。[**新**](https://www.bing.com/search?q=**New**) 宣告。 如果您未包含參考，VB 會引發錯誤，指出 Microsoft Agent 無法啟動 (錯誤碼 80042502) 。

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

針對5.0 之前的 VB 版本，您可以使用不含 [**WithEvents**](https://www.bing.com/search?q=**WithEvents**)宣告或 vb [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx)函式的 vb [**New**](https://www.bing.com/search?q=**New**)關鍵字，但這些慣例不會公開 Agent 控制項的事件。 您也必須先使用 [**連接**](https://www.bing.com/search?q=**Connected**) 的屬性，才能參考任何代理程式方法或屬性。 如果未這麼做，VB 將會引發錯誤，指出 Microsoft Agent 無法啟動 (錯誤碼 80042502) 。

同樣地，對於其他程式設計語言，您可能必須使用 [**連接**](https://www.bing.com/search?q=**Connected**) 的屬性來建立與代理程式元件物件模型的連接， (COM) server，然後您的程式碼才能呼叫任何 agent 控制項的方法或屬性。 此外，針對某些程式設計語言，除非您使用它的型別來宣告 Agent 控制項，否則可能不會直接公開代理程式的方法和屬性。 例如，在 Microsoft Access 97 中，當您輸入時，您必須將物件宣告為類型代理程式，才能看到 [自動清單成員] 下拉式方塊中顯示的方法和屬性。

大部分支援 ActiveX 控制項的程式設計語言都遵循類似 Visual Basic 的慣例。 針對不支持對象集合的程式設計語言，您可以使用 [**字元**](https://www.bing.com/search?q=**Character**) 方法和 [**命令**](https://www.bing.com/search?q=**Command**) 方法來存取集合中專案的方法和屬性。

程式設計語言（例如 Visual Basic）可提供 Agent 控制項所公開之物件類型的存取權，讓您在物件宣告中使用這些語言。 例如，不會將物件宣告為泛型型別：

``` syntax
   Dim Genie as Object
```

您可以將物件宣告為特定類型：

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

這可能會改善您應用程式的整體效能。

針對某些物件類型，您可能會發現兩種類型都相同，但 "Ex" 尾碼除外。 兩者都存在，請使用 "Ex" 類型，因為這會提供代理程式的完整功能。 非「Ex」的對應專案只是為了與舊版相容。

 

 




