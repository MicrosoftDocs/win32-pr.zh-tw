---
description: InkCollector. CursorDown 事件-發生于游標提示連線到數位化的平板電腦介面時。
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: 'InkCollector. CursorDown 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110296"
---
# <a name="inkcollectorcursordown-event"></a>InkCollector. CursorDown 事件

當游標提示接觸到數位化的 tablet 介面時發生。

## <a name="syntax"></a>語法


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>參數

<dl> <dt>

資料 *指標* \[在\]
</dt> <dd>

產生 **CursorDown** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。

</dd> <dt>

*筆觸* \[在\]
</dt> <dd>

[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件造成引發 **CursorDown** 事件時所啟動的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 IInkPictureEvents 中定義 \_ 。 \_IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 介面會以 DISPID ICECursorDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

請小心使用此事件，因為在事件處理常式中執行太多程式碼時，可能會對筆墨效能造成負面影響。 若要改善即時筆墨效能，請在 [**MouseDown**](inkcollector-mousedown.md) 和 [**MouseUp**](inkcollector-mouseup.md) 事件處理常式中隱藏或顯示滑鼠游標。

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

[**CursorButtonDown 事件**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**CursorButtonUp 事件**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

