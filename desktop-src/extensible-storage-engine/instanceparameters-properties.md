---
description: 深入瞭解： InstanceParameters 屬性
title: InstanceParameters 屬性
TOCTitle: InstanceParameters properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.InstanceParameters
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters_properties(v=EXCHG.10)
ms:contentKeyID: 55103291
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1db9933e6e0a14b770e4250fc7e1faf564d3266ee258bfa71671093dceee763a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721158"
---
# <a name="instanceparameters-properties"></a>InstanceParameters 屬性

包含受保護的成員  
包含繼承的成員  

[InstanceParameters](./instanceparameters-class.md)類型會公開下列成員。

## <a name="properties"></a>屬性

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350971(v=exchg.10).md">AlternateDatabaseRecoveryDirectory</a></td>
<td>取得或設定資料夾的相對或絕對檔案系統路徑，其中損毀復原或還原作業可以在指定資料夾的交易記錄中找到參考的資料庫。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350972(v=exchg.10).md">BaseName</a></td>
<td>取得或設定用於資料庫引擎所使用之許多檔案的三個字母前置詞。 例如，檢查點檔案稱為「EDB」。因為 EDB 是預設的基底名稱，所以預設為使用 .CHK。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350951(v=exchg.10).md">CachedClosedTables</a></td>
<td>取得或設定值，這個值會在應用程式關閉實例所代表的資料表之後，提供實例快取的 B + 樹狀資源數目。 此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。 對於具有極大量資料表之架構的應用程式而言，這非常有用。 Windows Vista 和更新的支援。 在 Windows XP 和 Windows Server 2003 上略過。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350974(v=exchg.10).md">CachePriority</a></td>
<td>取得或設定相對快取優先權 (預設 = 100) 的每個實例屬性。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350953(v=exchg.10).md">CheckpointDepthMax</a></td>
<td>取得或設定在損毀之後，需要重新執行多少個交易記錄檔的閾值（以位元組為單位）。 如果使用 CircularLog 來啟用迴圈記錄，此參數也會控制要保留在磁片上的大約交易記錄檔量。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350977(v=exchg.10).md">CircularLog</a></td>
<td>取得或設定值，指出是否開啟迴圈記錄。 當迴圈記錄關閉時，所產生的所有交易記錄檔都會保留在磁片上，直到不再需要該檔案，因為已執行資料庫的完整備份。 當迴圈記錄開啟時，只有小於目前檢查點的交易記錄檔會保留在磁片上。 這種模式的好處是，備份不需要淘汰舊的交易記錄檔。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350955(v=exchg.10).md">CleanupMismatchedLogFiles</a></td>
<td>取得或設定值，這個值表示當資料庫引擎設定為開始使用磁片上的交易記錄檔時，如果磁片上的交易記錄檔的大小與所設定的不同，JetInit 是否會失敗。 一般來說， <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE) </a> 會成功復原資料庫，但會失敗並出現 <a href="hh564840(v=exchg.10).md">LogFileSizeMismatchDatabasesConsistent</a> ，指出記錄檔的大小設定不正確。 但是，當這個參數設定為 true 時，database engine 就會以無訊息模式刪除所有舊的記錄檔，並使用所設定的記錄檔大小來啟動一組新的交易記錄檔。 當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350978(v=exchg.10).md">CreatePathIfNotExist</a></td>
<td>取得或設定值，這個值表示 ESENT 是否會以無訊息方式建立檔案系統路徑中遺失的資料夾。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350957(v=exchg.10).md">DbExtensionSize</a></td>
<td>取得或設定每次需要成長以容納更多資料時，資料庫檔案中加入的頁面數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350980(v=exchg.10).md">DbScanIntervalMaxSec</a></td>
<td>取得或設定允許資料庫掃描完成的最大間隔（以秒為單位）。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350959(v=exchg.10).md">DbScanIntervalMinSec</a></td>
<td>取得或設定重複資料庫掃描的最小間隔（以秒為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350982(v=exchg.10).md">DbScanThrottle</a></td>
<td>取得或設定資料庫掃描的節流（以毫秒為單位）。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350961(v=exchg.10).md">EnableDbScanInRecovery</a></td>
<td>取得或設定值，指出是否應在復原期間執行資料庫維護。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350984(v=exchg.10).md">EnableDBScanSerialization</a></td>
<td>取得或設定值，指出是否為共用相同磁片的資料庫啟用資料庫維護序列化。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350986(v=exchg.10).md">EnableIndexChecking</a></td>
<td>取得或設定值，指出 <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) </a> 是否將檢查在作業系統中使用舊版 NLS 程式庫所建立的索引。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350963(v=exchg.10).md">EnableOnlineDefrag</a></td>
<td>取得或設定值，這個值表示是否已啟用線上磁碟重組。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350988(v=exchg.10).md">EventSource</a></td>
<td>取得或設定應用程式特定的字串，這個字串將加入 database engine 所發出的任何事件記錄檔訊息中。 這可讓事件記錄檔訊息與來源應用程式輕鬆相互關聯。 預設會使用主應用程式的可執行檔名稱。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350966(v=exchg.10).md">EventSourceKey</a></td>
<td>取得或設定資料庫引擎為其事件記錄檔訊息所使用的事件記錄檔名稱。 依預設，所有事件記錄檔訊息都會移至應用程式事件記錄檔。 如果已設定另一個事件記錄檔的登錄機碼名稱，則會改為將事件記錄檔訊息移至該處。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350968(v=exchg.10).md">LogBuffers</a></td>
<td>取得或設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。 此參數的單位是保存交易記錄檔之磁片區的磁區大小。 磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。 此參數會對效能造成影響。 當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。 交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。 在此情況下，已知的預設值太小。 請勿將此參數設定為大於交易記錄檔大小一半的緩衝區數 (以位元組為單位) 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350991(v=exchg.10).md">LogFileDirectory</a></td>
<td>取得或設定將包含實例之交易記錄之資料夾的相對或絕對檔案系統路徑。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350969(v=exchg.10).md">LogFileSize</a></td>
<td>取得或設定交易記錄檔的大小。 此參數應以1024個位元組的單位來設定 (例如，2048的設定會提供2MB 的記錄檔) 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350993(v=exchg.10).md">MaxCursors</a></td>
<td>取得或設定保留給這個實例的資料指標資源數目。 資料指標資源會直接對應至 JET_TABLEID。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350970(v=exchg.10).md">MaxOpenTables</a></td>
<td>取得或設定保留給此實例的 B + 樹系資源數目。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350994(v=exchg.10).md">MaxSessions</a></td>
<td>取得或設定保留給此實例的會話資源數目。 會話資源直接對應至 JET_SESID。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350997(v=exchg.10).md">MaxTemporaryTables</a></td>
<td>取得或設定實例所使用之臨時表資源的數目。 此設定會影響可同時使用的臨時表數目。 如果這個系統參數設定為零，則不會建立暫存資料庫，而且任何需要使用暫存資料庫的活動都將會失敗。 這項設定有助於避免建立暫存資料庫所需的 i/o （如果已知不會使用）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350973(v=exchg.10).md">MaxTransactionSize</a></td>
<td>取得或設定在 <a href="hh564840(v=exchg.10).md">VersionStoreOutOfMemory</a> (預設值 = 100) 之前，可供最舊交易使用的版本存放區百分比。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350975(v=exchg.10).md">MaxVerPages</a></td>
<td>取得或設定保留給此實例的版本存放區頁面數目上限。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351001(v=exchg.10).md">NoInformationEvent</a></td>
<td>取得或設定值，這個值表示是否會隱藏資料庫引擎通常會產生的資訊事件記錄檔訊息。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350976(v=exchg.10).md">OneDatabasePerSession</a></td>
<td>取得或設定值，這個值表示一次是否允許指定的會話使用 JetOpenDatabase 來開啟單一資料庫。 這項限制會排除暫存資料庫。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351002(v=exchg.10).md">PageTempDBMin</a></td>
<td>取得或設定暫存資料庫的初始大小。 大小是在資料庫頁面中。 大小為零表示應該使用一般資料庫的預設大小。 小型應用程式通常需要將暫存資料庫設定為盡可能小。 將此參數設定為 <a href="dn351211(v=exchg.10).md">PageTempDBSmallest</a> ，可以達到最小的暫存資料庫。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350979(v=exchg.10).md">PreferredVerPages</a></td>
<td>取得或設定保留給此實例之版本存放區頁面的慣用數目。 如果版本存放區的大小超過此臨界值，則只會針對選擇性的背景工作（例如回收資料庫中已刪除的空間）使用任何資訊，而不會犧牲保存交易資訊的空間。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351004(v=exchg.10).md">PrereadIOMax</a></td>
<td>取得或設定針對指定用途分派的 i/o 作業數目上限。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350981(v=exchg.10).md">復原</a></td>
<td>取得或設定值，指出是否開啟損毀復原。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351007(v=exchg.10).md">SystemDirectory</a></td>
<td>取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的檢查點檔案。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350983(v=exchg.10).md">TempDirectory</a></td>
<td>取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的暫存資料庫。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351008(v=exchg.10).md">VersionStoreTaskQueueMax</a></td>
<td>取得或設定可在任何時間佇列至資料庫引擎執行緒集區的背景清除工作專案數目。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn350985(v=exchg.10).md">WaypointLatency</a></td>
<td>取得或設定 esent 將延遲資料庫排清之記錄檔的數目。 如果失敗導致記錄檔遺失，這可以用來提高資料庫復原能力。 Windows 7 和更新的支援。 在 Windows XP、Windows Server 2003、Windows Vista 和 Windows Server 2008 上略過。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[InstanceParameters 類別](./instanceparameters-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
