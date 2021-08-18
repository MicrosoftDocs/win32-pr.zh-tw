---
description: 發生于按下按鍵時，以及在 InkPicture 控制項有焦點時的向下位置。
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: InkPicture) 的 KeyDown 事件 (Msinkaut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9cf86a8efaacd1094330861bff63d38ae03ef056f4686a1286e06c8aca1ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451107"
---
# <a name="inkpicturekeydown-event"></a>InkPicture。 KeyDown 事件

發生于按下按鍵時，以及在 [InkPicture](inkpicture-control-reference.md) 控制項有焦點時的向下位置。

## <a name="syntax"></a>語法


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*KeyCode* \[in、out\]
</dt> <dd>

所按下之索引鍵的 ASCII 值。

</dd> <dt>

*Shift* \[in、out\]
</dt> <dd>

SHIFT 鍵的狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEKeyDown 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

 

