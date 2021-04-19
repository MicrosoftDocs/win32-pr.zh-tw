---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件移動時發生。
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: 'PenInputPanel. PanelMoving 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980070"
---
# <a name="peninputpanelpanelmoving-event"></a>PenInputPanel. PanelMoving 事件

已取代。 [**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。

在 [**PenInputPanel**](peninputpanel-class.md) 物件移動時發生。

## <a name="syntax"></a>語法


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*左方* \[in、out\]
</dt> <dd>

[**PenInputPanel**](peninputpanel-class.md)物件左邊緣的新水準或 X 軸位置（以螢幕座標表示）。

</dd> <dt>

*頂端* \[in、out\]
</dt> <dd>

[**PenInputPanel**](peninputpanel-class.md)物件左邊緣的新垂直軸（或 y 軸）位置（以螢幕座標為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

**PanelMoving** 事件是設計用來變更 [畫筆輸入] 面板的位置，方法是變更 *左方* 和 *前幾* 個參數。

[**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)和 [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)方法會導致 [**PenInputPanel**](peninputpanel-class.md)物件呼叫其自動定位程式碼，以觸發 **PanelMoving** 事件。 因此，在 **PanelMoving** 處理常式中呼叫這些方法，可能會導致遞迴的無限迴圈。

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

 

 




