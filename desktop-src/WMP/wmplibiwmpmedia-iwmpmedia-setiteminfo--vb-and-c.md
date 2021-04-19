---
title: IWMPMedia setItemInfo 方法
description: SetItemInfo 方法會設定媒體專案的指定屬性值。
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994310"
---
# <a name="iwmpmediasetiteminfo-method"></a>IWMPMedia：： setItemInfo 方法

**SetItemInfo** 方法會設定媒體專案的指定屬性值。

## <a name="syntax"></a>語法


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrItemName* \[在\]
</dt> <dd>

表示屬性名稱的 **system.string** 。

</dd> <dt>

*bstrVal* \[在\]
</dt> <dd>

表示新值的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**AttributeCount** 屬性會取得指定媒體專案可用的屬性數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷可搭配此方法使用的內建屬性名稱。

使用這個方法之前，請使用 **isReadOnlyItem** 方法來探索是否可以設定特定屬性。

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

注意

如果您在應用程式中內嵌 Windows Media Player 控制項，您所變更的檔案屬性將不會寫入數位媒體檔案，直到使用者執行 Windows Media Player 為止。

## <a name="examples"></a>範例

下列範例會使用 **setItemInfo** 來變更目前媒體專案的 [內容類型] 屬性值。 文字方塊可讓使用者輸入字串，然後用它來變更屬性資訊，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. isReadOnlyItem (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





