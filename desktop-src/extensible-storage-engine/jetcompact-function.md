---
description: 深入瞭解： JetCompact 函數
title: JetCompact 函式
TOCTitle: JetCompact Function
ms:assetid: 6944bd61-893d-4269-869b-56590e22580a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269284(v=EXCHG.10)
ms:contentKeyID: 32765576
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCompactW
- JetCompactA
- JetCompact
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebac7fe4f09a6c4456b5370af03ea24f2334cff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988844"
---
# <a name="jetcompact-function"></a>JetCompact 函式


_**適用于：** Windows |Windows Server_

## <a name="jetcompact-function"></a>JetCompact 函式

**JetCompact** 函數會建立現有資料庫的複本。 複本會壓縮為使用狀態的最佳狀態。 複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。 如此一來，壓縮的資料可能會盡可能儲存為密集。 或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。

```cpp
    JET_ERR JET_API JetCompact(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseSrc,
      __in          JET_PCSTR szDatabaseDest,
      __in          JET_PFNSTATUS pfnStatus,
      __in_opt      JET_CONVERT* pconvert,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*szDatabaseSrc*

將壓縮的源資料庫。

*szDatabaseDest*

要用於壓縮資料庫的名稱。

*pfnStatus*

可透過資料庫 compact 作業定期呼叫以報告進度的回呼函數。

*pconvert*

用來指定替代 ESE DLL 的指標，這個 DLL 可用來讀取源資料庫，並提供 **JetCompact** 作業的選擇性參數，將資料庫從較早的版本格式轉換為較新的版本。 這項功能已在 Windows Server 2003 中停用。

*grbit*

指定零或多個下列選項的位群組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitCompactRepair</p></td>
<td><p>當源資料庫已知已損毀時使用。 它會啟用一組完整的新行為，以盡可能從源資料庫中回收最多的資料。 使用這個選項組的<strong>JetCompact</strong>可能會傳回 JET_errSuccess 但不會複製在源資料庫中建立的所有資料。 將略過源資料庫中損毀部分的資料。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCompactStats</p></td>
<td><p>讓 <strong>JetCompact</strong> 將源資料庫的統計資料傾印到名為 DFRGINFO.TXT 的檔案。 統計資料包括源資料庫中每個資料表的名稱、每個資料表中的資料列數目、每個資料表中所有資料列的總大小（以位元組為單位）、所有資料行<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>類型的總大小（以位元組為單位），而這些資料行的大小總計與記錄、叢集索引分葉頁面的數目，以及 long 值分葉頁面的數目相同 此外，摘要統計資料，包括源資料庫的大小、目的地資料庫、資料庫壓縮所需的時間，也會全部傾印暫存資料庫空間。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errFeatureNotAvailable</p></td>
<td><p>已提供非 Null 的 <em>pconvert</em> 指標，但所使用的 ESE 版本不支援轉換功能。 這項功能已在 Windows Server 2003 版的 ESE 中移除。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>呼叫會話是在交易內。 <strong>JetCompact</strong> 必須由任何交易以外的會話呼叫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，源資料庫會複製到目的地資料庫。 目的地資料庫處於最佳狀態，例如，所有資料表索引都位於連續的邏輯磁碟空間中。 每個索引頁面都會填補至最初在源資料庫中建立索引時所設定的數量。 除非指定了 repair 選項，否則所有資料和中繼資料設定都會以完整的精確度複製。 如果指定了 repair 選項，源資料庫中的某些資料可能不會被覆制。

失敗時，目的地資料庫可能存在，但不是源資料庫的完整複本。

#### <a name="remarks"></a>備註

壓縮資料庫也用來將資料庫從舊版格式升級為較新式的版本。 選擇性參數為 *pconvert*，其中包含的結構可以保存舊版 DLL 的描述，以用來讀取源資料庫格式。 這項功能已在 Windows Server 2003 中停用。 在 Windows Server 2003 的後續版本中，新版本的 ESE 一律可以讀取舊版的資料庫格式，因此不需要這項功能。

當建立資料表和索引時，指定精簡作業之後所需的資料密度。 密度必須介於20% 到100% 之間。 如果資料庫主要是讀取和未更新，則應用程式會將密度設定為100%，以減少查詢處理期間的 i/o 作業數目。 但是，如果資料經常更新，且作業會增加與記錄一起儲存的資料大小，或經常插入新的資料，則應用程式會選擇較低的密度，讓更新更頻繁地找到所需的可用資源。 壓縮資料庫的作業會根據應用程式所選擇的填滿，在理想的情況下設定資料庫。

資料庫壓縮是離線作業。 當資料庫正在使用中時，無法執行此作業。 如此一來，通常會在開發應用程式的組建程式中完成，此應用程式會將資料集當作本身的一部分來傳遞。

離線資料庫壓縮會觸及資料庫中的每個資料，而且可用來做為檢查資料庫一致性的方法。 如果資料庫有問題，則可以將它壓縮。 如果從壓縮中找不到錯誤，則會知道資料庫處於 ESE 的有效狀態。

#### <a name="requirements"></a>規格需求

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
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetCompactW</strong> (Unicode) 和 <strong>JetCompactA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetStopService](./jetstopservice-function.md)
