---
description: 當一或多個筆劃加入至 InkStrokes 集合時發生。
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: 'InkStrokes. StrokesAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983743"
---
# <a name="inkstrokesstrokesadded-event"></a>InkStrokes. StrokesAdded 事件

當一或多個筆劃加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合時發生。

## <a name="syntax"></a>語法


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StrokeIds* \[在\]
</dt> <dd>

當此事件發生時，所加入之每個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的識別碼的整數陣列。

如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

此事件方法是在 \_ IInkEvents 介面中定義。 \_IInkEvents 介面會以 DISPID SEStrokesAdded 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**新增方法 \[ InkStrokes 集合\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)
</dt> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> </dl>

 

