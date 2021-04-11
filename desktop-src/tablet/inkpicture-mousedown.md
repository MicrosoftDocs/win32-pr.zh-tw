---
description: 發生于滑鼠指標位於 InkPicture 控制項上方且按下滑鼠按鍵時。
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: InkPicture)  (Msinkaut 的事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193724"
---
# <a name="inkpicturemousedown-event"></a>InkPicture 的 MouseDown 事件

發生于滑鼠指標位於 [InkPicture](inkpicture-control-reference.md) 控制項上方且按下滑鼠按鍵時。

## <a name="syntax"></a>語法


```C++
void MouseDown(
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

已按下的按鈕。

</dd> <dt>

*Shift* \[在\]
</dt> <dd>

SHIFT 鍵的狀態。

</dd> <dt>

*pX* \[在\]
</dt> <dd>

[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 x 座標（以圖元為單位）。

</dd> <dt>

*.py* \[在\]
</dt> <dd>

[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 y 座標（以圖元為單位）。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

**變異 \_TRUE** 表示取消父控制項的這個事件;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 參數 pX 與 .Py 是以圖元為單位，而不是與筆墨空間座標系統相關聯的 HIMETRIC 單位。 這是因為此事件會取代無法辨識的應用程式的相關滑鼠事件，而且該應用程式類型只會參考圖元。

 

> [!Caution]  
> 某些控制項依賴 **MouseDown**、 [**MouseMove**](inkpicture-mousemove.md)和 [**MouseUp**](inkpicture-mouseup.md) 事件之間的特定關聯性。 取消其中某些事件可能會產生非預期的結果。

 

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEMouseDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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
</dt> </dl>

 

