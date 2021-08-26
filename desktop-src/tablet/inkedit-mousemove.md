---
description: 發生于滑鼠停留在 InkEdit 控制項上時，使用者移動滑鼠時。
ms.assetid: 6ccaf2eb-acec-4dfd-9ec7-c78aca043900
title: 'InkEdit： MouseMove 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 601bcaa4c5bc3379c207302c28e5eb17d44b2b184ce42452d5b78b6079d88ead
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939108"
---
# <a name="inkeditmousemove-event"></a>InkEdit MouseMove 事件

發生于滑鼠停留在 [InkEdit](inkedit-control-reference.md) 控制項上時，使用者移動滑鼠時。

## <a name="syntax"></a>語法


```C++
HRESULT MouseMove(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*按鈕* 
</dt> <dd>

[**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton)列舉的成員，指出要按下的滑鼠按鍵。



| 值                                                                                                                                                            | 意義                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <dt>**否 \_按鈕**</dt> </dl>             | 預設值。 不按任何滑鼠鍵。 <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <dt>**左方 \_按鈕**</dt> </dl>       | 按滑鼠左鍵。 <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <dt>**RIGHT \_按鈕**</dt> </dl>    | 按滑鼠右鍵。 <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <dt>**中間 \_按鈕**</dt> </dl> | 按滑鼠中間鍵。 <br/>  |



 

</dd> <dt>

*ShiftKey* 
</dt> <dd>

[**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)列舉的成員，指出事件時要按下的輔助按鍵。



| 值                                                                                                                                                                                     | 意義                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | 指定 SHIFT 鍵已做為修飾詞使用。 <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_控制項**</dt> </dl> | 指定使用 CTRL 鍵做為修飾詞。 <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_Alt**</dt> </dl>                 | 指定使用 ALT 鍵做為修飾詞。 <br/>   |



 

</dd> <dt>

*xMouse* 
</dt> <dd>

滑鼠指標的目前 x 座標（以圖元為單位）。

</dd> <dt>

*yMouse* 
</dt> <dd>

滑鼠指標的目前 y 座標（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

當指標停留在 [InkEdit](inkedit-control-reference.md) 控制項上時，如果按下滑鼠按鍵，該控制項就會捕捉滑鼠並接收所有的滑鼠事件，直到和包含最後一個 [**MouseUp**](inkedit-mouseup.md) 事件為止。 這表示滑鼠事件所傳回的 (x、y) 滑鼠指標座標不一定會在接收它們的物件內部區域中。

如果連續按下滑鼠按鍵，則在第一次按下時捕捉滑鼠的物件會收到所有的滑鼠事件，直到所有按鈕都放開為止。

當滑鼠指標在物件間移動時，會持續產生 **MouseMove** 事件。 除非有另一個物件已捕捉到滑鼠，否則只要滑鼠位置在其框線內， [InkEdit](inkedit-control-reference.md) 控制項就會辨識 **MouseMove** 事件。

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 DISPID IeeMouseMove 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>筆跡 (也需要筆跡 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**InkMouseButton 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**MouseDown 事件 \[ InkEdit 控制項\]**](inkedit-mousedown.md)
</dt> <dt>

[**MouseUp 事件 \[ InkEdit 控制項\]**](inkedit-mouseup.md)
</dt> </dl>

 

