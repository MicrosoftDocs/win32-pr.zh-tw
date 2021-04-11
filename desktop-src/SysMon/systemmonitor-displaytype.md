---
title: SystemMonitor 屬性
description: 抓取或設定用來繪製效能計數器資料圖形的圖表類型。
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- DisplayType 屬性 SysMon
- DisplayType 屬性 SysMon，SystemMonitor 類別
- SystemMonitor 類別 SysMon，DisplayType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103835"
---
# <a name="systemmonitordisplaytype-property"></a>SystemMonitor 屬性

抓取或設定用來繪製效能計數器資料圖形的圖表類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>屬性值

用來繪製效能計數器資料圖形的圖表類型。 如需可能的值，請參閱 [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)。

## <a name="exceptions"></a>例外狀況



| 例外狀況類型               | 條件                                         |
|------------------------------|---------------------------------------------------|
| **System. ArgumentException** | 指定的圖形或報表值無效。 |



 

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

 

 





