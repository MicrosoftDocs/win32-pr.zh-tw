---
description: 在辨識系統手勢時發生。
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: 'InkPicture.SystemGesture 事件 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980053"
---
# <a name="inkpicturesystemgesture-event"></a>InkPicture.SystemGesture 事件

在辨識系統手勢時發生。

## <a name="syntax"></a>語法


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **SystemGesture** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

 \[ 中的識別碼\]
</dt> <dd>

系統手勢的值。

</dd> <dt>

*X* \[ 于\]
</dt> <dd>

手勢位置的 x 座標。

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

手勢位置的 y 座標。

</dd> <dt>

*修飾* \[ 詞在\]
</dt> <dd>

保留的。

</dd> <dt>

*字元* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*CursorMode* \[在\]
</dt> <dd>

值，指出 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件為正常模式或橡皮擦模式。 1適用于標準模式，2適用于橡皮擦模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

系統手勢提供用來建立手勢之 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件的相關資訊。 它們也提供滑鼠事件組合的快捷方式，也是偵測滑鼠事件的方式，對效能的影響較小。

例如，您可以尋找點一下或 RightTap 系統手勢，而不是尋找 [**MouseUp 事件 \[ InkPicture 控制項 \]**](inkpicture-mouseup.md) / 的 [**MouseDown 事件 \[ InkPicture 控制 \]**](inkpicture-mousedown.md)事件配對。

另一個範例是，而不是接聽 [**\[ InkPicture 控制項 \]**](inkpicture-mousedown.md)mousemove 事件 / [**\[ InkPicture 控制項 \]**](inkpicture-mousemove.md)事件，以及取得許多 **MouseMove 事件 \[ InkPicture 控制 \]** 訊息，只要您對滑鼠的每個位置的 (x，y) 座標都不感興趣，您就可以觀賞拖曳或 RightDrag 系統手勢。 這可讓您只接收一個訊息，而不是多個 **MouseMove 事件 \[ InkPicture 控制 \]** 訊息。

如需特定系統手勢的清單，請參閱 [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) 列舉型別。 如需系統手勢的詳細資訊，請參閱在[TABLET PC 上](/previous-versions//dd314533(v=vs.85))[使用筆勢](using-gestures.md)和命令輸入。

此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICESystemGesture 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**InkSystemGesture 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[使用手勢](using-gestures.md)
</dt> </dl>

 

