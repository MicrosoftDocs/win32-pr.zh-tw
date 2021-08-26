---
description: 從 InkStrokes 集合中刪除一或多個筆劃時發生。
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: 'InkStrokes. StrokesRemoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a5c4f7d53f88c50efd77e537cfa311f08ab168abdb4a05392286fb6c0b6b4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934858"
---
# <a name="inkstrokesstrokesremoved-event"></a>InkStrokes. StrokesRemoved 事件

從 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合中刪除一或多個筆劃時發生。

## <a name="syntax"></a>語法


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StrokeIds* \[在\]
</dt> <dd>

當此事件發生時，每個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件所刪除之識別碼的整數陣列。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkEvents 介面中定義。 \_IInkEvents 介面會以 DISPID SEStrokesRemoved 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Remove Method \[ InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> </dl>

 

