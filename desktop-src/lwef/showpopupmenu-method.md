---
title: ShowPopupMenu 方法
description: ShowPopupMenu 方法
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600988"
---
# <a name="showpopupmenu-method"></a>ShowPopupMenu 方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

顯示指定位置的字元快顯功能表。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) 。ShowPopupMenu_ * _x、y_



| 部分 | 描述                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | 必要。 整數值，表示用來顯示功能表的水準 (*x*) 螢幕座標。 這些座標必須以圖元為單位來指定。 |
| *y*  | 必要。 整數值，指出垂直 (*y*) 螢幕座標，以顯示功能表。 這些座標必須以圖元為單位來指定。   |



 

</dd> </dl>

## <a name="remarks"></a>備註

當使用者以滑鼠右鍵按一下字元時，代理程式會自動顯示該字元的快顯功能表。 如果您將 [**AutoPopupMenu**](autopopupmenu-property.md) 設定為 **False**，則可以使用這個方法來顯示功能表。

功能表會保持顯示，直到使用者選取命令或顯示其他功能表為止。 一次只能顯示一個快顯功能表;因此，對此方法的呼叫將會取消 (移除) 前一個功能表中。

只有當您的用戶端應用程式是字元的作用中用戶端時，才應該呼叫這個方法。否則會失敗。 若要判斷這個方法是否成功，您可以呼叫它作為函式，它會傳回布林值，指出方法是否成功。


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>另請參閱

[**AutoPopupMenu 屬性**](autopopupmenu-property.md)


 

 




