---
title: SystemMonitor SqlLogSetName 屬性
description: 抓取或設定記錄集的易記名稱。
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- SqlLogSetName 屬性 SysMon
- SqlLogSetName 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、SqlLogSetName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024551"
---
# <a name="systemmonitorsqllogsetname-property"></a>SystemMonitor：： SqlLogSetName 屬性

抓取或設定記錄集的易記名稱。

## <a name="syntax"></a>Syntax


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>屬性值

記錄集的易記名稱，對應至 SQL database 中包含二進位或文字資料的單一記錄檔。

## <a name="remarks"></a>備註

**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 的值設定為 sysmonSqlLog，您就無法修改此屬性。

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

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





