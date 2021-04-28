---
description: InkCollector. 滑鼠滾輪事件-發生于滑鼠滾輪移動時，當 InkCollector 或 InkOverlay 物件具有焦點時，就會發生此事件。
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: 'InkCollector. 滑鼠滾輪事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110136"
---
# <a name="inkcollectormousewheel-event"></a>InkCollector. 滑鼠滾輪事件

發生于 [**InkCollector**](inkcollector-class.md) 或 [**InkOverlay**](inkoverlay-class.md) 物件具有焦點時，滑鼠滾輪移動時。

## <a name="syntax"></a>語法


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*按鈕* \[在\]
</dt> <dd>

已按下的滑鼠按鍵。

</dd> <dt>

*Shift* \[在\]
</dt> <dd>

SHIFT 鍵的狀態。

</dd> <dt>

*差異* \[在\]
</dt> <dd>

滑鼠滾輪旋轉的刻度數目的帶正負號計數。 一個刻度是一個滑鼠滾輪的刻痕。

</dd> <dt>

*x* \[ 于\]
</dt> <dd>

滑鼠點擊的 x 座標（以圖元為單位）。

</dd> <dt>

*y* \[ in\]
</dt> <dd>

滑鼠點擊的 y 座標（以圖元為單位）。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

**變異 \_TRUE** 表示取消父控制項的事件;否則， **VARIANT \_ FALSE**。 預設值為 **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> [ *PX* ] 和 [ *.py* ] 屬性是以圖元為單位，而不是與筆墨空間相關聯的 HIMETRIC 單位。 這是因為此事件會取代不知道應用程式的相關滑鼠事件，而這種類型的應用程式只瞭解圖元。

 

此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID IPEMouseWheel 識別碼的) \_ 。

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

[**InkMouseButton 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




