---
description: 深入瞭解：事件記錄常數
title: 事件記錄常數
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986988"
---
# <a name="event-logging-constants"></a>事件記錄常數


_**適用于：** Windows |Windows Server_

## <a name="event-logging-constants"></a>事件記錄常數

下列常數指出 [JET_ParamEventLoggingLevel](./event-log-parameters.md) 系統參數之事件記錄檔訊息的詳細層級。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常數/值</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_EventLoggingDisable<br />
0</p></td>
<td><p>停用事件記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_EventLoggingLevelMax<br />
100</p></td>
<td><p>設定要用於事件記錄檔的最大層級（目前為100個字元）。</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[事件記錄檔參數](./event-log-parameters.md)
