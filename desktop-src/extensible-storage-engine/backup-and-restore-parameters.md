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
ms.openlocfilehash: e57cc3f1078d46436d56a56c48c31a3fac4956c0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481404"
---
# <a name="backup-and-restore-parameters"></a>備份和還原參數


_**適用于：** Windows |Windows伺服器_

## <a name="backup-and-restore-parameters"></a>備份和還原參數

本主題包含用於備份和還原的參數。

*JET_paramAlternateDatabaseRecoveryPath*  
113  

在執行時間，會將每個資料庫的完整路徑保存在交易記錄中。 一般來說，這些資料庫必須保留在原始位置，才能讓交易重新執行正常運作。 這個參數可以用來強制損毀復原或還原作業，以便在指定的資料夾中，尋找交易記錄中所參考的資料庫。


| | | <p>預設值：3</p> | <p>""</p> | | <p>輸入：</p> | <p>資料夾路徑 (字串) </p> | | <p>有效範圍：</p> | <p>0–246個字元</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramCleanupMismatchedLogFiles*  
77  

此參數可控制當資料庫引擎設定為在磁片上的交易記錄檔，與設定的大小不同時， [JetInit](./jetinit-function.md) 的結果。 一般來說， [JetInit](./jetinit-function.md) 會成功復原資料庫，但會失敗，並 JET_errLogFileSizeMismatchDatabasesConsistent 指出記錄檔大小設定不正確。 但是，當這個參數設定為 true 時，資料庫引擎將會以無訊息模式刪除所有舊的記錄檔、使用設定的記錄檔大小來啟動一組新的交易記錄檔，然後再傳回 JET_errSuccess。

當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>是</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>全部</p> | 



*JET_paramDeleteOutOfRangeLogs*  
52  

當此參數為 true 時， [JetInit](./jetinit-function.md)就會刪除在磁片上找到的任何非目前記錄檔順序的交易記錄檔。 這可用來在還原作業之後，自動清除多餘的記錄檔。

**Windows XP：** Windows XP 引進。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>是</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>是</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramOSSnapshotTimeout*  
82  

此參數會設定在發生超時之前呼叫 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 之間允許的時間量。 如需詳細資訊，請參閱 [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) 和 [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) 。 Timeout 是以毫秒為單位。


| | | <p>預設值：3</p> | <p>20000 (Windows XP 和 Windows Server 2003) ;</p><p>70000 (Windows Server 2003 SP1) </p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-2147483647</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>是</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramZeroDatabaseDuringBackup*  
71  

當此參數為 true 時，資料庫中正在進行串流備份的每個頁面將會清除已刪除的資料。 請務必注意，要清除的資料庫頁面是在磁片上。 在清除程式之前，會備份完整的資料集。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>是</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
