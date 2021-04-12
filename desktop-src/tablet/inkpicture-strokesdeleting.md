---
description: 發生于從 Ink 屬性中刪除 IInkStrokeDisp 物件之前。
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: 'InkPicture. StrokesDeleting 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027206"
---
# <a name="inkpicturestrokesdeleting-event"></a>InkPicture. StrokesDeleting 事件

發生于從 [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性中刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之前。

## <a name="syntax"></a>語法


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*筆觸* \[在\]
</dt> <dd>

引發 **StrokesDeleting** 事件時，會刪除 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEStrokesDeleting 識別碼的) \_ 。

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

 

