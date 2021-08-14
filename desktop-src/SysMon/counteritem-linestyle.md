---
title: CounterItem. LineStyle 屬性
description: 抓取或設定用來繪製計數器值的線條樣式。
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- LineStyle 屬性 SysMon
- LineStyle 屬性 SysMon、CounterItem 類別
- CounterItem 類別 SysMon，LineStyle 屬性
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60ce0c96f9e3eb25639cad9251d8cf3969d022001962e14ec9c3ef4d157ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883703"
---
# <a name="counteritemlinestyle-property"></a>CounterItem. LineStyle 屬性

抓取或設定用來繪製計數器值的線條樣式。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>屬性值

用來繪製計數器值的線條樣式。 這些值會對應至下表中顯示的系統常數。



| 值                                                                                                                                                                                                                                                                                                                                                                               | 意義                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**Drawing2D. DashStyle. 立體**</dt> <dt>0</dt> </dl>                     | 實線。 這是預設值。<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**Drawing2D. DashStyle. 破折號**</dt> <dt>1</dt> </dl>                         | 具有長段和窄空格的虛線。<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**Drawing2D. DashStyle 點**</dt> <dt>2</dt> </dl>                             | 具有統一區段和空格的虛線。<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**Drawing2D. DashStyle. 點**</dt> <dt>3</dt> </dl>             | 具有交替簡短和長段的虛線。<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**Drawing2D. DashStyle. DashDotDot**</dt> <dt>4</dt> </dl> | 具有交替連字號和雙點的虛線。<br/>  |



 

## <a name="exceptions"></a>例外狀況



| 例外狀況類型               | 條件                              |
|------------------------------|----------------------------------------|
| **System. ArgumentException** | 指定的線條樣式無效。 |



 

## <a name="remarks"></a>備註

若要指定 DashStyle 以外的值， [**CounterItem 寬度**](counteritem-width.md) 必須設定為1。 如果寬度大於1，SYSMON 會忽略指定的線條樣式並使用 DashStyle。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





