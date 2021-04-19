---
title: 載入方法
description: 載入方法
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966854"
---
# <a name="load-method"></a>載入方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

將字元載入至 [**字元**](/windows/desktop/lwef/the-characters-object) 集合。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。字元。 Load "*** CharacterID * * *"，* *  *提供者*



| 部分          | 描述                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | 必要。 您將用來參考要載入之字元資料的字串值。                                                                                                                                                  |
| *提供者*    | 必要。 必須是下列其中一項的 variant 資料類型： **Filespec** 指定字元之定義檔的本機檔案位置。 <br/> **URL** 字元定義檔的 HTTP 位址。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

您可以從代理程式子目錄中指定相對路徑來載入字元， (不含冒號或開頭斜線字元) 。 這會在當地語系化的 Windows msagent 目錄) 中，使用代理程式的字元目錄 (路徑 \\ 。 例如，指定下列內容會從代理程式的字元目錄載入瓶精靈。


```
   Agent.Character.Load "genie", "genie.acs"
```



您也可以在代理程式的 [字元] 目錄中指定自己的目錄。


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



您可以將目前設定為目前使用者預設字元的字元載入，方法是不要將路徑包含為 **load** 方法的第二個參數。


```
   Agent.Character.Load "character"
```



您無法從控制項的單一實例，將相同的字元 (具有相同 GUID 的字元) 一次以上。 同樣地，您無法同時從控制項的單一實例載入預設字元和其他字元，因為預設字元可能與其他字元相同。 如果您嘗試這麼做，伺服器會引發錯誤。 不過，您可以建立 Agent 控制項的另一個實例，並載入相同的字元。

Microsoft Agent Data Provider 支援載入儲存為單一結構化檔案 ( 的字元資料。ACS) 搭配字元資料和動畫資料，或以個別的字元資料 (。ACF) 和動畫 (。ACA) 檔。 使用單一結構化。ACS 檔案來載入儲存在本機磁片或網路上的字元，並使用傳統的檔案通訊協定來存取， (例如 UNC 路徑) 。 使用不同的。ACF 和。當您想要從使用 HTTP 通訊協定來存取它們的遠端網站個別載入動畫檔案時，ACA 檔案。

出於.使用 **Load** 方法的 ACS 檔案可存取字元的動畫。 出於.ACF 檔案，您也可以使用 [**Get**](get-method.md) 方法來載入動畫資料。 **載入** 方法不支援下載。來自 HTTP 網站的 ACS 檔案。

載入字元不會自動顯示字元。 先使用 [**Show**](show-method.md) 方法讓字元變成可見。

如果您使用 **load** 方法載入儲存在本機電腦上的字元檔，則呼叫會失敗;例如，由於找不到檔案，因此 Agent 會引發錯誤。 您可以使用程式設計語言的支援，提供錯誤處理常式來攔截和處理錯誤。


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



您也可以將 [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) 設定為 **False**、宣告物件，並將 **載入** 要求指派給它，以處理錯誤。 然後，遵循具有檢查 [**要求**](/windows/desktop/lwef/the-request-object)物件狀態的語句，來進行 **Load** 呼叫。


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



如果您載入的字元不是本機，例如，您也可以使用 HTTP 通訊協定，藉由將 [**要求**](/windows/desktop/lwef/the-request-object)物件指派給 **load** 方法來檢查 **載入** 失敗。 不過，因為這種載入字元的方法會以非同步方式處理，所以請檢查其在 [**RequestComplete**](requestcomplete-event.md) 事件中的狀態。 這項技術將無法使用 UNC 通訊協定載入字元，因為會以同步方式處理 **Load** 方法。

 

