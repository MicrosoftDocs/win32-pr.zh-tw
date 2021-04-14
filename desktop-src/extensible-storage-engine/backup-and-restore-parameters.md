---
description: 深入瞭解：備份和還原參數
title: 備份和還原參數
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514072"
---
# <a name="backup-and-restore-parameters"></a>備份和還原參數


_**適用于：** Windows |Windows Server_

## <a name="backup-and-restore-parameters"></a>備份和還原參數

本主題包含用於備份和還原的參數。

*JET_paramAlternateDatabaseRecoveryPath*  
113  

在執行時間，會將每個資料庫的完整路徑保存在交易記錄中。 一般來說，這些資料庫必須保留在原始位置，才能讓交易重新執行正常運作。 這個參數可以用來強制損毀復原或還原作業，以便在指定的資料夾中，尋找交易記錄中所參考的資料庫。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>資料夾路徑 (字串) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0–246個字元</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramCleanupMismatchedLogFiles*  
77  

此參數可控制當資料庫引擎設定為在磁片上的交易記錄檔，與設定的大小不同時， [JetInit](./jetinit-function.md) 的結果。 一般來說， [JetInit](./jetinit-function.md) 會成功復原資料庫，但會失敗，並 JET_errLogFileSizeMismatchDatabasesConsistent 指出記錄檔大小設定不正確。 但是，當這個參數設定為 true 時，資料庫引擎將會以無訊息模式刪除所有舊的記錄檔、使用設定的記錄檔大小來啟動一組新的交易記錄檔，然後再傳回 JET_errSuccess。

當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


*JET_paramDeleteOutOfRangeLogs*  
52  

當此參數為 true 時， [JetInit](./jetinit-function.md)就會刪除在磁片上找到的任何非目前記錄檔順序的交易記錄檔。 這可用來在還原作業之後，自動清除多餘的記錄檔。

**WINDOWS XP：**  在 Windows XP 中引進。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramOSSnapshotTimeout*  
82  

此參數會設定在發生超時之前呼叫 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 之間允許的時間量。 如需詳細資訊，請參閱 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 。 Timeout 是以毫秒為單位。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>20000 (Windows XP 和 Windows Server 2003) ;</p>
<p>70000 (Windows Server 2003 SP1) </p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0-2147483647</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>全球</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramZeroDatabaseDuringBackup*  
71  

當此參數為 true 時，資料庫中正在進行串流備份的每個頁面將會清除已刪除的資料。 請務必注意，要清除的資料庫頁面是在磁片上。 在清除程式之前，會備份完整的資料集。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>否</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
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

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
