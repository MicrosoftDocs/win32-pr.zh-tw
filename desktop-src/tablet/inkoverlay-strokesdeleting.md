---
description: 發生于從筆墨屬性刪除筆劃之前。
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: 'StrokesDeleting 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85e01eabc46e8e9cc4ca844ae8f5efa8b58e83fdee2724792a3856445b7dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712668"
---
# <a name="inkoverlaystrokesdeleting-event"></a>StrokesDeleting 事件

發生于從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃之前。

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

此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEStrokesDeleting 識別碼的) \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**InkOverlay 類別**](inkoverlay-class.md)
</dt> <dt>

[**Ink 屬性 \[ InkCollector/InkOverLay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)
</dt> </dl>

 

