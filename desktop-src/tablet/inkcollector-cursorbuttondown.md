---
description: InkCollector. CursorButtonDown 事件-當 InkCollector 類別偵測到已關閉的資料指標按鈕時，就會發生此事件。
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: 'InkCollector. CursorButtonDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110326"
---
# <a name="inkcollectorcursorbuttondown-event"></a>InkCollector. CursorButtonDown 事件

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

產生 **CursorButtonDown** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*按鈕* \[在\]
</dt> <dd>

已按下的按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當使用者將畫筆降至數位板並開始追蹤筆劃時，畫筆提示上的按鈕會關閉。 當按下按鈕時，會關閉圓柱上的按鈕。

當您按下滑鼠右鍵時，您實際上會收到兩個 **CursorButtonDown** 事件-一個是按下滑鼠右鍵，另一個用於按下滑鼠左鍵。

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

[**InkCollector 類別**](inkcollector-class.md)
</dt> <dt>

[**CursorDown 事件**](inkcollector-cursordown.md)
</dt> <dt>

[**CursorButtonUp 事件**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




