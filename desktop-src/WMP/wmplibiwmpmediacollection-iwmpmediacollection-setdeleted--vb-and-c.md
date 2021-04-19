---
title: IWMPMediaCollection setDeleted 方法
description: SetDeleted 方法會將指定的媒體專案移到 [刪除的專案] 資料夾。 |IWMPMediaCollection setDeleted 方法
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- setDeleted 方法 Windows Media Player
- setDeleted 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，setDeleted 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999399"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a>IWMPMediaCollection：： setDeleted 方法

`setDeleted`方法會將指定的媒體專案移到 [刪除的專案] 資料夾。

## <a name="syntax"></a>語法


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a>參數

<dl> <dt>

*pItem* \[在\]
</dt> <dd>

要移動之專案的 **WMPLib IWMPMedia** 介面。

</dd> <dt>

*varfIsDeleted* \[在\]
</dt> <dd>

指定是否應將專案移至 [已刪除的專案] 資料夾的 [system.string] （ **布林** 值）值。 此值必須一律為 **true**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法不會從使用者的電腦移除檔案，而是將它們移到 [刪除的專案] 資料夾。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 `setDeleted` 將特定媒體專案移至 [已刪除的專案] 資料夾。 **IsDeleted** 方法會先測試是否已刪除專案。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

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
</dt> </dl>

 

 





