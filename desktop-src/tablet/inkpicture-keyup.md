---
description: 當 InkPicture 控制項具有焦點時，放開按鍵時發生。
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: InkPicture (Msinkaut) 的 KeyUp 事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985238"
---
# <a name="inkpicturekeyup-event"></a>InkPicture KeyUp 事件

當 [InkPicture](inkpicture-control-reference.md) 控制項具有焦點時，放開按鍵時發生。

## <a name="syntax"></a>語法


```C++
void KeyUp(
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

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPEKeyUp 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

 

