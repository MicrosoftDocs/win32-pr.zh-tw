---
description: 發生于滑鼠指標位於 InkCollector 或 InkOverlay 物件上方，並放開滑鼠按鍵時。
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: 'InkOverlay 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16fd3dc5006f43e09e093cb2c474a8578f56c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194423"
---
# <a name="inkoverlaymouseup-event"></a>InkOverlay 事件

發生于滑鼠指標位於 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件上方，並放開滑鼠按鍵時。

## <a name="syntax"></a>語法


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*按鈕* \[在\]
</dt> <dd>

已釋放的滑鼠按鍵。

</dd> <dt>

*Shift* \[在\]
</dt> <dd>

SHIFT 鍵的狀態。

</dd> <dt>

*pX* \[在\]
</dt> <dd>

滑鼠點擊的 x 座標（以圖元為單位）。

</dd> <dt>

*.py* \[在\]
</dt> <dd>

滑鼠點擊的 y 座標（以圖元為單位）。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

是否應該取消父控制項的事件。 預設值為 **FALSE**，指定不應取消事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要改善即時筆墨效能，請在 [**MouseDown**](inkcollector-mousedown.md) 和 [**MouseUp**](inkcollector-mouseup.md) 事件處理常式中隱藏或顯示滑鼠游標。

> [!Note]  
> [ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。 這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。

 

> [!Note]  
> 某些控制項依賴 [**MouseDown**](inkcollector-mousedown.md)、 [**MouseMove**](inkcollector-mousemove.md)和 [**MouseUp**](inkcollector-mouseup.md) 事件之間的特定關聯性。 取消其中某些事件可能會產生非預期的結果。

 

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseUp 識別碼的) \_ 。

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

[**InkMouseButton 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




