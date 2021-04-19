---
description: 深入瞭解： JET_ERRCAT
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981607"
---
# <a name="jet_errcat"></a>JET_ERRCAT


_**適用于：** Windows |Windows Server_

## <a name="jet_errcat"></a>JET_ERRCAT

**JET_ERRCAT** 的常數群組描述較高層級的分類或錯誤類別。 這個常數群組可讓應用程式定義錯誤分類的預設處理方式，而不是個別處理每個錯誤案例。 它也可確保應用程式不需要處理現有分類中包含的新錯誤條件。

注意：本檔是以可延伸儲存引擎的初步發行版本為基礎。 此資訊可能隨時變更。

**JET_ERRCAT** 的常數會排列在特定的條件和 subconditions 階層中，如下所示：

|---錯誤 |---作業 (al) | |---嚴重 | |---IO | |---資源 | |---記憶體 | |---配額 | |---磁片 | |---資料 | |---損毀 | |---不一致 | |---的片段 | |---Api |---使用量 |---狀態

下表列出 **JET_ERRCAT** 常數，並提供適用的描述和修復資訊。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常數/值</p></th>
<th><p>Description</p></th>
<th><p>復原</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errcatUnknown 0</p></td>
<td><p>不正確錯誤類別。</p></td>
<td><p>N/A。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatError 1</p></td>
<td><p>最上層類別 (此類別) 不會有任何錯誤。</p></td>
<td><p>請參閱特定的錯誤常數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatOperation 2</p></td>
<td><p>代表可能因為無法控制條件而發生的錯誤，而且通常是暫時性的。 如果有指定，請參閱子類別。</p></td>
<td><p>請重試一次，如果錯誤持續發生，請通知操作員。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatFatal 3</p></td>
<td><p>表示發生嚴重錯誤，當發生時，會產生一個風險，指出 ESE 無法在安全的 (（通常是交易式) 方式）中繼續，而且資料可能會損毀。</p></td>
<td><p>重新開機實例或進程。 如果問題持續發生，請通知操作員。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatIO 4</p></td>
<td><p>代表來自作業系統的 IO 錯誤，而不是 ESE 的控制權。 這種類型的錯誤可能是暫時性的。</p></td>
<td><p>請重試一次，如果錯誤持續發生，請要求操作員檢查磁片。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatResource 5</p></td>
<td><p>表示與缺乏資源條件相關的錯誤類別。</p></td>
<td><p>請參閱子類別。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatMemory 6</p></td>
<td><p>代表記憶體不足所造成的錯誤。</p></td>
<td><p>請在一段時間後重試，釋出記憶體或結束。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatQuota 7</p></td>
<td><p>某些 &quot; 特殊 &quot; 資源會在特定大小的集區中，讓您更輕鬆地偵測這些資源的洩漏。</p></td>
<td><p>應用程式應該判斷提示 <strong> () </strong> 在開發期間偵測這些問題。 不過，在零售程式碼中，應用程式應該將此視為記憶體錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatDisk 8</p></td>
<td><p>代表因磁碟空間不足而造成的錯誤。</p></td>
<td><p>請稍後再試一次，以判斷是否有更多可用的磁碟空間，或要求操作員釋放一些磁碟空間。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatData 9</p></td>
<td><p>表示與資料相關之錯誤的最上層類別。</p></td>
<td><p>請參閱子類別。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatCorruption 10</p></td>
<td><p>代表損毀問題，這通常不會有矯正措施的永久問題。</p></td>
<td><p>使用 ESE 公用程式修復作業從備份還原 (此作業只會還原) 的資料。 此外，當使用 recovery (JetInit) 方法時，您可以藉由允許資料遺失來執行復原 (如需詳細資訊，請參閱 <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatInconsistent 11</p></td>
<td><p>表示資料庫和/或記錄檔處於不一致且無法進行協調的狀態錯誤。 此錯誤可能是由應用程式/系統管理員承載錯誤處理所造成。</p></td>
<td><p>使用 ESE 公用程式修復作業從備份還原，這 (只會還原保持) 的資料。 此外，在復原 <strong> (JetInit) </strong> 作業的情況下，您可以藉由允許資料遺失來執行復原 (如需詳細資訊，請參閱 <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatFragmentation 12</p></td>
<td><p>代表某些持續性內部資源已用盡的錯誤類別。</p></td>
<td><p>針對資料庫錯誤，離線磁碟重組將會修正此問題。 針對記錄檔，先將所有附加的資料庫復原至正常關機，然後刪除所有記錄檔和檢查點。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatApi 13</p></td>
<td><p>請參閱子類別。</p></td>
<td><p>請參閱子類別。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatUsage 14</p></td>
<td><p>表示使用錯誤。 用戶端程式代碼未將正確的引數傳遞至 <strong>JET</strong> API。 此錯誤會在重試期間持續。</p></td>
<td><p>用戶端程式代碼應該使用 <strong>Assert () </strong> 方法來確保不會傳回這個錯誤類別，因此可能會在開發期間攔截問題。 在零售版中，應用程式應該通知操作員有關錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatState 15</p></td>
<td><p>表示 API 可傳回的訊息類別，以描述資料庫的狀態。 例如，當找不到要求的記錄時， <a href="gg294103(v=exchg.10).md">JetSeek () </a> 方法可能會傳回 <strong>JET_errRecordNotFound</strong> 。</p></td>
<td><p>根據 API 而有所不同。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errcatObsolete 16</p></td>
<td><p>表示來自舊版引擎的錯誤。 目前的引擎不應傳回這些錯誤。</p></td>
<td><p>不明。</p></td>
</tr>
<tr class="even">
<td><p>JET_errcatMax 17</p></td>
<td><p>常數，表示列舉的結尾。</p></td>
<td><p>N/A。</p></td>
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
<td><p>需要 Windows 8。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows 8 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>

