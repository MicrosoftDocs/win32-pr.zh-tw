---
description: 發生于 InkPicture 控制項的 SizeMode 屬性變更之後。
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: 'InkPicture. SizeModeChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320439"
---
# <a name="inkpicturesizemodechanged-event"></a>InkPicture. SizeModeChanged 事件

發生于 [InkPicture](inkpicture-control-reference.md)控制項的 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性變更之後。

## <a name="syntax"></a>語法


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Newmode.obj* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項的新狀態（以 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性的新值為基礎）。

</dd> <dt>

*OldMode* \[在\]
</dt> <dd>

[InkPicture](inkpicture-control-reference.md)控制項的舊狀態（以 [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)屬性的舊值為基礎）。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkPictureEvents** 介面中定義。 **\_ IInkPictureEvents** 介面會以 DISPID IPESizeModeChanged 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

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

 

