---
description: 深入瞭解： JET_ERRCAT 列舉
title: 'JET_ERRCAT 列舉的 (Windows8) '
TOCTitle: JET_ERRCAT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errcat(v=EXCHG.10)
ms:contentKeyID: 55104419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Max
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Obsolete
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Unknown
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Operation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Usage
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Disk
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.IO
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Error
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Resource
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Api
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Data
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Inconsistent
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Quota
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Corruption
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fragmentation
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Memory
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.Fatal
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRCAT.State
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f259edf0e087831cfb667caa5fa8dcf215638ab6d739812fa2e6208327a22f7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232798"
---
# <a name="jet_errcat-enumeration"></a>JET_ERRCAT 列舉

錯誤類別。 階層如下： JET_errcatError | |--JET_errcatOperation | |--JET_errcatFatal | |--JET_errcatIO//錯誤的 IO 問題，可能或可能不是暫時性問題。 | |--JET_errcatResource | |--JET_errcatMemory//記憶體不足 (所有變體) | |--JET_errcatQuota | |--JET_errcatDisk//磁碟空間 (所有變體) |--JET_errcatData | |--JET_errcatCorruption | |--JET_errcatInconsistent//通常是由使用者承載錯誤處理所造成 | |--JET_errcatFragmentation |--JET_errcatApi |--JET_errcatUsage |--JET_errcatState |--JET_errcatObsolete

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_ERRCAT
'Usage
Dim instance As JET_ERRCAT
```

``` csharp
public enum JET_ERRCAT
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Unknown</td>
<td>未知的類別。</td>
</tr>
<tr class="even">
<td></td>
<td>錯誤</td>
<td>泛型類別目錄。</td>
</tr>
<tr class="odd">
<td></td>
<td>作業</td>
<td>通常由於無法控制條件而可能發生的錯誤。 通常是暫時性的，但並非一律如此。 復原：可能會重試，或最後通知操作員。</td>
</tr>
<tr class="even">
<td></td>
<td>嚴重</td>
<td>只有當 ESE 遇到錯誤狀況時，才會發生這種排序錯誤，因此我們無法在安全的 (中繼續，通常是交易式) 方式，而不是損毀的資料，我們會擲回這個類別的錯誤。 Recovery：重新開機實例或進程。 如果問題持續發生，請通知操作員。</td>
</tr>
<tr class="odd">
<td></td>
<td>IO</td>
<td>O 錯誤來自 OS，而且不在 ESE 的控制之下，這類錯誤可能是暫時性的，可能不是暫時性的。 復原：重試。 如果未解決，請詢問操作員有關磁片的問題。</td>
</tr>
<tr class="even">
<td></td>
<td>資源</td>
<td>這是表示許多可能的資源不足狀況之一的類別。</td>
</tr>
<tr class="odd">
<td></td>
<td>記憶體</td>
<td>傳統記憶體不足的狀況。 復原：等候一段時間，然後再試一次、釋放記憶體或結束。</td>
</tr>
<tr class="even">
<td></td>
<td>配額</td>
<td>某些 &quot; 特殊 &quot; 資源會在特定大小的集區中，讓您更輕鬆地偵測這些資源的洩漏。 復原：可能需要一些次要的程式碼變更。 在這些情況下，您的應用程式應該要有僅限 debug 的動作（例如判斷提示），才能在開發期間偵測它們。 針對零售程式碼，我們建議您將此錯誤視為記憶體類別錯誤，然後重試、釋出記憶體或結束作業。</td>
</tr>
<tr class="odd">
<td></td>
<td>磁碟</td>
<td>磁片不足的情況。 復原：稍後可以在希望有更多可用空間的情況下重試，或要求操作員釋放一些磁碟空間。</td>
</tr>
<tr class="even">
<td></td>
<td>資料</td>
<td>資料相關的錯誤。</td>
</tr>
<tr class="odd">
<td></td>
<td>腐敗</td>
<td>我的硬碟 ate 我的工作空間。 傳統的損毀問題，經常永久沒有矯正措施。 復原：從備份還原，可能是 ese 公用程式修復作業 (只會 salvages 剩下/損及) 的資料。此外，在復原 (JetInit) 可能會藉由允許資料遺失來執行修復。</td>
</tr>
<tr class="even">
<td></td>
<td>不一致</td>
<td>這類似于損毀，因為資料庫和/或記錄檔處於不一致的狀態，且彼此 unreconcilable。 這通常是由應用程式/系統管理員承載錯誤處理所造成。 復原：從備份還原，可能是 ese 公用程式修復作業 (只會 salvages 剩下/損及) 的資料。 此外，在復原 (JetInit) 可能會藉由允許資料遺失來執行修復。</td>
</tr>
<tr class="odd">
<td></td>
<td>分割</td>
<td>這是一些持續性內部資源已用盡的錯誤類別。復原：針對資料庫錯誤，離線磁碟重組會修正問題，記錄檔會 _先_ 將所有附加的資料庫復原到正常關機，然後再刪除所有記錄檔和檢查點。</td>
</tr>
<tr class="even">
<td></td>
<td>API</td>
<td>使用方式和狀態的容器。</td>
</tr>
<tr class="odd">
<td></td>
<td>使用量</td>
<td>傳統使用方式錯誤，這表示用戶端程式代碼未傳遞正確的引數給 JET API。 此錯誤可能不會在重試後消失。 復原：一般而言，用戶端程式代碼應該判斷提示 () 此類別的錯誤不會傳回，因此在開發期間可能會發生問題。 在零售版中，應用程式可能會有極少的選項，但是將問題傳回給操作員。</td>
</tr>
<tr class="even">
<td></td>
<td>狀態</td>
<td>這是 API 可能傳回的不同信號的分類，可描述資料庫的狀態，傳統案例是 JET_errRecordNotFound 當找不到您要求的記錄時，可由 JetSeek () 傳回。 復原：與 API 很大的差異。</td>
</tr>
<tr class="odd">
<td></td>
<td>已淘汰</td>
<td>錯誤會被辨識為有效的錯誤，但此版本的 API 預期不會傳回此錯誤。</td>
</tr>
<tr class="even">
<td></td>
<td>最大值</td>
<td>列舉的最大值。 這不應該使用。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
