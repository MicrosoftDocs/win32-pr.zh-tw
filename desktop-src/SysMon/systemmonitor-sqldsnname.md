---
title: SystemMonitor SqlDsnName 屬性
description: 抓取或設定 (DSN) 的 ODBC 資料來源名稱。
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- SqlDsnName 屬性 SysMon
- SqlDsnName 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、SqlDsnName 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383826"
---
# <a name="systemmonitorsqldsnname-property"></a>SystemMonitor：： SqlDsnName 屬性

抓取或設定 (DSN) 的 ODBC 資料來源名稱。

## <a name="syntax"></a>Syntax


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>屬性值

指向包含正確 Perfmon 資料表之資料庫的 ODBC 資料來源名稱。 格式為 SQL： DSN。

## <a name="remarks"></a>備註

您必須使用 Perfmon MMC 嵌入式管理單元來產生 SQL 記錄檔。 計數器記錄檔位於 **效能記錄檔及警示** 下。 若要指定 SQL 記錄檔，請以滑鼠右鍵按一下您所建立的記錄檔，然後從功能表中選取 [ **屬性** ]。 在 [**記錄** 檔] 屬性頁上，從 [**記錄檔案類型**] 下拉式清單方塊中選取 **SQL Database** 。

**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) 的值設定為 [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants)，您就無法修改此屬性。 您必須先指定名稱，然後將 **SystemMonitor DataSourceType** 設定為 **DataSourceTypeConstants.sysmonSqlLog**。

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

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





