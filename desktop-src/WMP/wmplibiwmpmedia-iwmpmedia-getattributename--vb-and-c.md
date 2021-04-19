---
title: IWMPMedia getAttributeName 方法
description: GetAttributeName 方法會傳回對應至指定之索引的屬性名稱。
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- getAttributeName 方法 Windows Media Player
- getAttributeName 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getAttributeName 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997738"
---
# <a name="iwmpmediagetattributename-method"></a>IWMPMedia：： getAttributeName 方法

**GetAttributeName** 方法會傳回對應至指定之索引的屬性名稱。

## <a name="syntax"></a>語法


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

作為索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

表示屬性名稱的 **system.string** 。

## <a name="remarks"></a>備註

傳回的屬性名稱可以與 **getItemInfo** 搭配使用，以抓取特定命名屬性的值。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。

## <a name="examples"></a>範例

下列範例會使用 **getAttributeName** ，在多行文字方塊中填入目前媒體專案的每個屬性的索引和名稱。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
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

[**IWMPMedia. getItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





