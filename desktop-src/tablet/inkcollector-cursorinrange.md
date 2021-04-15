---
description: 當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: 'InkCollector. CursorInRange 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c1d59927f9ed0a932fe28a2c5243f328a223c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511020"
---
# <a name="inkcollectorcursorinrange-event"></a>InkCollector. CursorInRange 事件

當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。

## <a name="syntax"></a>語法


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **CursorInRange** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*NewCursor* \[在\]
</dt> <dd>

**變異 \_TRUE** 表示這個筆墨收集器第一次與產生 **CursorInRange** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件有關。否則， **VARIANT \_ FALSE**。

</dd> <dt>

*ButtonsState* \[在\]
</dt> <dd>

產生 **CursorInRange** 事件的資料指標之按鈕的狀態。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法定義于 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 僅分派介面中， (具有 DISPID ICECursorInRange 識別碼的) 的分配介面 \_ 。

即使在 [選取] 或 [清除] 模式中，也不只是在 [筆墨] 模式中，也會引發 **CursorInRange** 事件。 這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。 這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。

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

[**CursorOutOfRange 事件**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




