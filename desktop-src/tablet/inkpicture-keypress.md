---
description: 發生于 InkPicture 控制項具有焦點時按下按鍵時。
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: 'InkPicture： KeyPress 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943540"
---
# <a name="inkpicturekeypress-event"></a>InkPicture 的按鍵事件

發生于 [InkPicture](inkpicture-control-reference.md) 控制項具有焦點時按下按鍵時。

## <a name="syntax"></a>語法


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeyAscii* \[in、out\]
</dt> <dd>

所按下之索引鍵的 ASCII 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEKeyPress 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

 

