---
description: 發生于滑鼠滾輪移動時，InkPicture 控制項有焦點時。
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: 'InkPicture. 滑鼠滾輪事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e139604b4fbfd3293203d82b44be15fa36c090e72f40cfedc8ce0641b75b27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938988"
---
# <a name="inkpicturemousewheel-event"></a>InkPicture. 滑鼠滾輪事件

發生于滑鼠滾輪移動時， [InkPicture](inkpicture-control-reference.md) 控制項有焦點時。

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

已按下的按鈕。

</dd> <dt>

*Shift* \[在\]
</dt> <dd>

SHIFT 鍵的狀態。

</dd> <dt>

*差異* \[在\]
</dt> <dd>

滑鼠滾輪的距離。

</dd> <dt>

*x* \[ 于\]
</dt> <dd>

[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 x 座標（以圖元為單位）。

</dd> <dt>

*y* \[ in\]
</dt> <dd>

[**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 y 座標（以圖元為單位）。

</dd> <dt>

*取消* \[in、out\]
</dt> <dd>

VARIANT \_ TRUE 表示取消父控制項的 **滑鼠滾輪** 事件，否則為 variant \_ FALSE。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 參數 *x* 和 *y* 是以圖元為單位，而不是與筆墨空間座標系統相關聯的 HIMETRIC 單位。 這是因為此事件會取代無法辨識的應用程式的相關滑鼠事件，而且該應用程式類型只會參考圖元。

 

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEMouseWheel 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

