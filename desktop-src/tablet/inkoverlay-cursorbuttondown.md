---
description: 當 InkCollector 類別偵測到已關閉的資料指標按鈕時發生。
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: 'CursorButtonDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393949be4d7b0f172805aa0b81ce86eac3cf3b3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980667"
---
# <a name="inkoverlaycursorbuttondown-event"></a>CursorButtonDown 事件

當 [**InkCollector 類別**](inkcollector-class.md) 偵測到已關閉的資料指標按鈕時發生。

## <a name="syntax"></a>語法


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 [**CursorButtonDown**](inkcollector-cursorbuttondown.md)事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*按鈕* \[在\]
</dt> <dd>

已按下的按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當使用者將畫筆降至數位板並開始追蹤筆劃時，畫筆提示上的按鈕會關閉。 當按下按鈕時，會關閉圓柱上的按鈕。

當您按下滑鼠右鍵時，您實際上會收到兩個 [**CursorButtonDown**](inkcollector-cursorbuttondown.md) 事件-一個是按下滑鼠右鍵，另一個用於按下滑鼠左鍵。

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICECursorButtonDown 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> <dt>

[**CursorDown 事件**](inkcollector-cursordown.md)
</dt> <dt>

[**CursorButtonUp 事件**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




