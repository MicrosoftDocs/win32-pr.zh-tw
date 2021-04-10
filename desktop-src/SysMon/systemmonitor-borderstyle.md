---
title: SystemMonitor 屬性
description: 抓取或設定控制項的框線樣式。
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- BorderStyle 屬性 SysMon
- BorderStyle 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，BorderStyle 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843472"
---
# <a name="systemmonitorborderstyle-property"></a>SystemMonitor 屬性

抓取或設定控制項的框線樣式。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>屬性值

控制項的框線樣式。

您可以將此屬性設定為下列其中一個值。



| 值                                                                                                                                                                                                                                                                                                                                                                                                   | 意義                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**FormBorderStyle. VbBSNone**</dt> <dt>0</dt> </dl>                     | 無框線。 這是預設值。<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt> </dl> | 固定、單一框線。<br/>                 |



 

## <a name="exceptions"></a>例外狀況



| 例外狀況類型               | 條件                                |
|------------------------------|------------------------------------------|
| **System. ArgumentException** | 指定的框線樣式無效。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





