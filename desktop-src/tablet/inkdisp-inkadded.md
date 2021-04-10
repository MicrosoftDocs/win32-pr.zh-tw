---
description: 在將筆劃加入至 InkDisp 物件時發生。
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: 'InkDisp. InkAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d25266a8cd75f873c5a7c1c18fa20fcf5126faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026191"
---
# <a name="inkdispinkadded-event"></a>InkDisp. InkAdded 事件

在將筆劃加入至 [**InkDisp**](inkdisp-class.md) 物件時發生。

## <a name="syntax"></a>語法


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StrokeIds* \[在\]
</dt> <dd>

當此事件發生時，已新增之所有筆劃的筆觸識別碼資訊的整數陣列。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

如果您使用 [**InkOverlay**](inkoverlay-class.md) 物件或 [InkPicture](inkpicture-control-reference.md) 控制項 (其中 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) 等於 [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) 和 [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) 並透過筆劃傳遞橡皮擦，則會取得下列一連串的事件：

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

因為基礎程式碼會新增內部、不可見的筆觸來追蹤橡皮擦，所以會發生其他 **InkAdded** 和 [**InkDeleted**](inkdisp-inkdeleted.md) 事件。

此事件方法是在 \_ IInkEvents 介面中定義。 \_IInkEvents 介面會以 DISPID IEInkAdded 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

即使在選取或清除模式下，也不只是在插入筆墨時，也會引發 **InkAdded** 事件。 這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。 這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> <dt>

[**System.windows.controls.inkcanvas.editingmode 屬性 \[ InkOverlay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**EraserMode 屬性 \[ InkOverlay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**InkDeleted 事件**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> <dt>

[InkPicture 控制項參考](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

