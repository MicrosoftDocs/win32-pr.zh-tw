---
title: SystemMonitor DataSourceType 屬性
description: 抓取或設定效能計數器資料的來源。
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- DataSourceType 屬性 SysMon
- DataSourceType 屬性 SysMon、SystemMonitor 介面
- SystemMonitor 介面 SysMon、DataSourceType 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025311"
---
# <a name="systemmonitordatasourcetype-property"></a>SystemMonitor：:D ataSourceType 屬性

抓取或設定效能計數器資料的來源。

## <a name="syntax"></a>Syntax


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>屬性值

效能計數器資料的來源。 如需可能的值，請參閱 [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants)。

## <a name="exceptions"></a>例外狀況



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>例外狀況類型</th>
<th>條件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. ArgumentException</strong></td>
<td>您可能會因為下列其中一個原因而收到此例外狀況：
<ul>
<li>指定的資料來源值無效。</li>
<li>如果資料來源是記錄檔，則 SYSMON 找不到其中一個指定的檔案。 Err 值為0xC0000BD1。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

**在 Windows Vista 之前：** 如果這個屬性的值設定為 sysmonLogFiles，您就無法從 [**記錄檔集合**](systemmonitor-logfiles.md) 加入或移除記錄檔。 只有在建立或修改記錄檔集合之後，才將這個屬性的值設定為 sysmonLogFiles。

此外，如果這個屬性的值不能設定為 sysmonSqlLog，則無法修改 [**SqlDsnName**](systemmonitor-sqldsnname.md) 和 [**SqlLogSetName**](systemmonitor-sqllogsetname.md) 屬性。 在修改伺服器和資料庫名稱之後，請只將這個屬性的值設定為 sysmonSqlLog。

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

 

 





