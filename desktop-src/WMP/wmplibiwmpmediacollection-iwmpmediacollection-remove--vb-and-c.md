---
title: IWMPMediaCollection remove 方法
description: Remove 方法會從媒體集合中移除指定的專案。
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player、remove 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771ae8be7a8a4586c132cb29b3af4d5d9180398d7db7d05e66c6e84b5a013b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734998"
---
# <a name="iwmpmediacollectionremove-method"></a>IWMPMediaCollection：： remove 方法

`remove`方法會從媒體集合中移除指定的專案。

## <a name="syntax"></a>語法


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a>參數

<dl> <dt>

*pItem* \[在\]
</dt> <dd>

識別要移除之專案的 **WMPLib IWMPMedia** 介面。

</dd> <dt>

*varfDeleteFile* \[在\]
</dt> <dd>

指定方法是否應從程式庫移除指定專案的 **布林** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會從程式庫中刪除專案。 這個方法不會刪除使用者電腦中的檔案。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會在提示使用者之後，使用來永久刪除媒體集合中的第一個媒體專案 `remove` 。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
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

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection：新增 (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





