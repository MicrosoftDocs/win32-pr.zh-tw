---
title: 連接屬性
description: 連接屬性
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af3a44e97236060733adc55ec6e44eddd0b1d8879250b2a28b54c0bca384cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726088"
---
# <a name="connected-property"></a>連接屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定目前的控制項是否連接至 Microsoft 代理程式伺服器。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式。 * * * 已連線* *  \[  = *布林值*\]



| 部分      | 描述                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| *boolean* | 指定控制項是否已連接的布林運算式。 **True** 控制項已連接。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

在許多情況下，指定控制項會自動建立與 Microsoft 代理程式伺服器之間的連接。 例如，在網頁的標籤中指定 Microsoft Agent 控制項的 CLSID 時， <OBJECT> 會自動開啟伺服器連接，而結束頁面則會關閉連接。 同樣地，對於可讓您將控制項放在表單上的 Visual Basic 或其他語言，執行程式會自動開啟連接，而結束程式則會關閉連接。 如果伺服器目前不在執行中，則會自動啟動。

但是，如果您想要在執行時間建立 Agent 控制項，您可能也需要使用 **連接** 的屬性來明確開啟伺服器的新連接。 例如，在 Visual Basic 您可以在執行時間使用 Set 語句搭配 **New** 關鍵字 (或 CreateObject 函數) 來建立 ActiveX 物件。 雖然這會建立物件，但它可能不會建立與伺服器的連接。 您可以在呼叫 Microsoft 代理程式的程式設計介面的任何程式碼之前使用 **連接** 的屬性，如下列範例所示：


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



使用這項技術來建立控制項，並不會公開 Agent 控制項的事件。 在 Visual Basic 5.0 (和更新版本的) 中，您可以在專案的參考中包含控制項，以存取控制項的事件，並在您的變數宣告中使用 **WithEvents** 關鍵字：


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



當您在執行時間使用 **WithEvents** 建立 Agent 控制項的實例時，會自動開啟與 Microsoft 代理程式伺服器之間的連接。 因此，您不需要包含 **連接** 的語句。

您可以將建立的所有參考釋出至代理程式物件（例如 IAgentCtlCharacterEx 和 IAgentCtlCommandEx），以關閉與伺服器的連接。 您也必須釋放 Agent 控制項本身的參考。 在 Visual Basic 中，您可以藉由將物件的變數設定為 **Nothing** 來釋出物件的參考。 如果您已載入字元，請在釋放字元物件之前先將它們卸載。


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> 您無法藉由釋放已加入元件的參考，關閉與伺服器的連接。 例如，您無法在使用標記來宣告控制項的網頁上， <OBJECT> 或是在您將控制項放在表單上的 Visual Basic 應用程式中，關閉與伺服器的連接。 釋放所有的代理程式參考時，將會降低代理程式的工作集，而在您流覽至下一個頁面或結束應用程式之前，連接都會保持不變。

 

 

 





