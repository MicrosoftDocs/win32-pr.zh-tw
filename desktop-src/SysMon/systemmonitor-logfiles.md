---
title: SystemMonitor 記錄檔屬性
description: 收集一或多個要作為系統監視器中顯示的計數器值來源的記錄檔。
ms.assetid: 6e9e7205-3516-404d-b67d-777e484900da
keywords:
- 記錄檔屬性 SysMon
- 記錄檔屬性 SysMon，SystemMonitor 物件
- SystemMonitor 物件 SysMon，記錄檔屬性
topic_type:
- apiref
api_name:
- SystemMonitor.LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8127433319290b44498b272834923784b714052
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967336"
---
# <a name="systemmonitorlogfiles-property"></a>SystemMonitor 記錄檔屬性

收集一或多個要作為系統監視器中顯示的計數器值來源的記錄檔。

## <a name="syntax"></a>Syntax


```VB
Property LogFiles As ILogFiles
```



## <a name="property-value"></a>屬性值

[**LogFileItem**](logfileitem.md)物件的集合，這些物件會指定當做圖形之資料來源使用的記錄檔。

## <a name="remarks"></a>備註

若要從記錄檔集合加入或移除記錄檔， [**SystemMonitor**](systemmonitor-datasourcetype.md) 的值不得設定為 sysmonLogFiles。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon .ocx</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)
</dt> <dt>

[**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md)
</dt> <dt>

[**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





