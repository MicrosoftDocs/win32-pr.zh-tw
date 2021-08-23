---
title: Activate 方法
description: Activate 方法
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753157"
---
# <a name="activate-method"></a>Activate 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**描述**](../wmformat/description.md)
</dt> <dd>

設定使用中的用戶端或字元。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。啟用_ *  \[ *狀態*\]



| 部分    | 描述                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | 選擇性。 您可以為此參數指定下列值：0不是作用中的用戶端。<br/> 1個作用中用戶端。 <br/> 2 (預設) 最頂端的字元。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

當有多個字元可見時，一次只能有一個字元接收語音輸入。 同樣地，當多個用戶端應用程式共用相同的字元時，只有其中一個用戶端會收到滑鼠輸入 (例如，Microsoft Agent control click 或拖曳 events) 。 用來接收滑鼠和語音輸入的字元集是最上層的字元，而接收輸入的用戶端是該字元的作用中用戶端。  (最頂端的字元視窗也會出現在字元視窗的迭置順序頂端。 ) 一般會明確地選取字元，以決定最頂端的字元。 不過，當字元顯示或隱藏 (字元變成或不再是最上層時，最上層啟用也會變更。 ) 

您也可以使用這個方法，在用戶端收到導向字元的輸入時明確管理，例如當您的應用程式本身變成作用中時。 例如，將 [ *狀態* ] 設定為 [2] 會讓字元最上層，而您的用戶端會收到使用者與該字元互動所產生的所有滑鼠和語音輸入事件。 因此，它也會讓您的用戶端成為字元的輸入主動用戶端。

不過，您也可以將自己設定為字元的作用中用戶端，而不讓字元最上層，方法是將 *狀態* 設定為1。 這可讓您的用戶端在字元變成最上層時，接收導向該字元的輸入。 同樣地，您可以將用戶端設定為不是使用中的用戶端 (不會在字元變成最上層時，藉由將 *狀態* 設為0來接收輸入) 。

避免直接在 [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) 方法之後呼叫此方法。 **顯示** 自動設定輸入-主動用戶端。 隱藏字元時，如果在 **Show** 方法完成之前處理，[**啟動**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71))呼叫可能會失敗。

如果您將此方法呼叫至函式，它會傳回布林值，指出方法是否成功。 當指定的字元隱藏時，嘗試以 *State* 參數設定為2時，嘗試呼叫這個方法將會失敗。 同樣地，如果您將 *狀態* 設定為0，而您的應用程式是唯一的用戶端，則此呼叫會失敗，因為字元一律必須有最上層的用戶端。


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> 除非沒有載入任何其他字元或您的應用程式已經輸入主動，否則以 *狀態* 設定為1來呼叫這個方法通常不會產生 [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) 事件。

 

## <a name="see-also"></a>另請參閱

[**ActivateInput 事件**](activateinput-event.md)， [ **DeactivateInput 事件**](deactivateinput-event.md)


 

