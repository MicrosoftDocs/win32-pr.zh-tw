---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件顯示或隱藏本身時發生。
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: 'PenInputPanel. VisibleChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979840"
---
# <a name="peninputpanelvisiblechanged-event"></a>PenInputPanel. VisibleChanged 事件

已取代。 [**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。

在 [**PenInputPanel**](peninputpanel-class.md) 物件顯示或隱藏本身時發生。

## <a name="syntax"></a>語法


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewVisibility* \[在\]
</dt> <dd>

**變異 \_TRUE** 表示讓 [**PenInputPanel**](peninputpanel-class.md) 物件變成可見;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**VisibleChanged** 事件會套用至 Tablet PC 輸入面板的滑鼠停留目標。 不過，當滑鼠停留目標展開以顯示完整的 Tablet PC 輸入面板時，不會引發此功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 




