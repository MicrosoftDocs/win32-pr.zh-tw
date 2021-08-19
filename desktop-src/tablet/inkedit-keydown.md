---
description: 當使用者按下按鍵時，InkEdit 控制項有焦點時發生。
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: InkEdit) 的 KeyDown 事件 (筆跡
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ab1c1b54f9f60d4bd0868f6e093505e21255991502653712a540728394664c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967136"
---
# <a name="inkeditkeydown-event"></a>InkEdit。 KeyDown 事件

當使用者按下按鍵時， [InkEdit](inkedit-control-reference.md) 控制項有焦點時發生。

## <a name="syntax"></a>語法


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pKey* 
</dt> <dd>

使用者按下按鍵的虛擬金鑰碼。

</dd> <dt>

*ShiftKey* 
</dt> <dd>

[**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)列舉的成員，表示事件時要按下的輔助按鍵。



| 值                                                                                                                                                                                     | 意義                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <dt>**IKM \_ Shift**</dt> </dl>             | 指定 SHIFT 鍵已做為修飾詞使用。 <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <dt>**IKM \_控制項**</dt> </dl> | 指定使用 CTRL 鍵做為修飾詞。 <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <dt>**IKM \_Alt**</dt> </dl>                 | 指定使用 ALT 鍵做為修飾詞。 <br/>   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 DISPID IeeKeyDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

[**InkShiftKeyModifierFlags 列舉**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**KeyPress 事件 \[ InkEdit 控制項\]**](inkedit-keypress.md)
</dt> <dt>

[**KeyUp 事件 \[ InkEdit 控制項\]**](inkedit-keyup.md)
</dt> </dl>

 

