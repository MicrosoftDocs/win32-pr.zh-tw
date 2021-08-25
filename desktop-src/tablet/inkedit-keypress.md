---
description: 當使用者在 InkEdit 控制項具有焦點時按下並放開按鍵時發生。
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: 'InkEdit： KeyPress 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713100edeae3ce6b950433afb73d13f40aefb291047e98984cbd6908dde3ce2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935097"
---
# <a name="inkeditkeypress-event"></a>InkEdit 的按鍵事件

當使用者在 [InkEdit](inkedit-control-reference.md) 控制項具有焦點時按下並放開按鍵時發生。

## <a name="syntax"></a>語法


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Char* 
</dt> <dd>

傳回標準數值 ANSI keycode 的整數。 *Char* 參數是以傳址方式傳遞;變更它會將不同的字元傳送給控制項。 將 *Char* 參數變更為0會取消事件。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkEditEvents** 介面中定義。 **\_ IInkEditEvents** 介面會以 DISPID IeeKeyPress 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

[**KeyDown 事件 \[ InkEdit 控制項\]**](inkedit-keydown.md)
</dt> <dt>

[**KeyUp 事件 \[ InkEdit 控制項\]**](inkedit-keyup.md)
</dt> </dl>

 

