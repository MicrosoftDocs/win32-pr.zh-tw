---
description: 深入瞭解：可擴充儲存引擎系統參數
title: 可擴充儲存引擎系統參數
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
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
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512653"
---
# <a name="extensible-storage-engine-system-parameters"></a>可擴充儲存引擎系統參數


_**適用于：** Windows |Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>可擴充儲存引擎系統參數

下列常數會當做 [JetGetSystemParameter](./jetgetsystemparameter-function.md)和 [JetSetSystemParameter](./jetsetsystemparameter-function.md)函數之 *paramid* 參數的值使用。

  - [備份和還原參數](./backup-and-restore-parameters.md)

  - [回呼參數](./callback-parameters.md)

  - [資料庫參數](./database-parameters.md)

  - [資料庫快取參數](./database-cache-parameters.md)

  - [錯誤處理參數](./error-handling-parameters.md)

  - [事件記錄檔參數](./event-log-parameters.md)

  - [I/o 參數](./i-o-parameters.md)

  - [索引參數](./index-parameters.md)

  - [資訊參數](./informational-parameters.md)

  - [中繼參數](./meta-parameters.md)

  - [資源參數](./resource-parameters.md)

  - [暫存資料庫參數](./temporary-database-parameters.md)

  - [交易記錄檔參數](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>系統參數描述格式

系統會使用下列格式來描述每個系統參數：

JET_paramX

JET_paramX 系統參數的描述。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>參數的預設值。</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>參數的資料類型。</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>參數的合法值。</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>參數是全域或每個實例？</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>如果有任何實例存在，是否可以設定參數？</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>是否可以在初始化時設定參數？</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>參數是否會影響磁片上的檔案？</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>參數是否會影響引擎可靠性？</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>參數是否會影響引擎效能？</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>參數是否會影響引擎資源？</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>支援參數的 Windows 版本。</p></td>
</tr>
</tbody>
</table>
