---
description: 當應用程式手勢被辨識時發生。
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: 'InkEdit 的軌跡事件 (筆跡) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193338"
---
# <a name="inkeditgesture-event"></a>InkEdit 手勢事件

當應用程式手勢被辨識時發生。

## <a name="syntax"></a>語法


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

用來建立此手勢的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) 物件。

</dd> <dt>

*筆觸* \[在\]
</dt> <dd>

[InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合，其中包含組成此手勢的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。

</dd> <dt>

*手勢* \[在\]
</dt> <dd>

[**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的陣列，以信賴度為限。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

是否應該取消組成此軌跡的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合，以免清除筆墨並引發 [**筆劃**](inkedit-stroke.md) 事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 DISPID IeeGesture 的識別碼來實作為 IDispatch 介面 \_ 。

只有在最後一次呼叫辨識方法或上次引發 [**辨識**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)超時時，才會引發 **手勢** 事件，因為 [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture)物件的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)是第一個 **IInkStrokeDisp** 物件。

如果已取消 **手勢** 事件，則會針對引發 **手勢** 事件的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合引發 [**筆劃**](inkedit-stroke.md)事件。

若要進行此事件， [InkEdit](inkedit-control-reference.md) 控制項必須訂閱一組應用程式手勢。 若要在一組手勢中設定 InkEdit 控制項的興趣，請呼叫 [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) 方法。

如需應用程式手勢的清單，請參閱 [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) 列舉型別。

[InkEdit](inkedit-control-reference.md)控制項無法辨識多個筆劃手勢。

[InkEdit](inkedit-control-reference.md)控制項會訂閱下列手勢。



| 手勢                              | 動作               |
|--------------------------------------|----------------------|
| 向左、向下、向左<br/> | Enter<br/>     |
| Right<br/>                     | Space<br/>     |
| Left<br/>                      | 退格鍵<br/> |
| 右上角、右上角<br/>   | 索引標籤<br/>       |



 

若要改變手勢的預設動作：

1.  加入 **筆勢** 和 [**筆觸**](inkedit-stroke.md) 事件的事件處理常式。
2.  **在軌跡事件處理** 程式中，取消筆勢的 **手勢** 事件，然後執行筆勢的替代動作。
3.  在 [[**筆劃**](inkedit-stroke.md)事件處理常式] 中，取消引發已取消的 **手勢** 事件之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 **筆觸** 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>筆跡 (也需要筆跡 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkApplicationGesture 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus 方法 \[ InkEdit 控制項\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**RecoTimeout 屬性**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**筆觸事件 \[ InkEdit 控制項\]**](inkedit-stroke.md)
</dt> <dt>

[使用手勢](using-gestures.md)
</dt> </dl>

 

