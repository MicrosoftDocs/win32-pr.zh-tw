---
description: 深入瞭解： JetGetTableInfo 函數
title: JetGetTableInfo 函式
TOCTitle: JetGetTableInfo Function
ms:assetid: 0602186c-b5c3-44b5-87df-482680442afd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269177(v=EXCHG.10)
ms:contentKeyID: 32765480
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableInfoW
- JetGetTableInfo
- JetGetTableInfoA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c17e1c5aa23e8e2fe77aaa07f98fee1b2df0c12
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465795"
---
# <a name="jetgettableinfo-function"></a>JetGetTableInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgettableinfo-function"></a>JetGetTableInfo 函式

**JetGetTableInfo** 函數會抓取資料庫中資料表的各種相關資訊。

```cpp
    JET_ERR JET_API JetGetTableInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

適用資訊的資料表。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel*。 呼叫端必須負責適當地對齊緩衝區。

*cbMax*

在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。

*InfoLevel*

針對 *tableid* 所指定之資料表將抓取的資訊類型。 儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。

您可以為此參數設定下列選項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_TblInfo</p> | <p><em>pvResult</em> 會被視為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。 如果方法成功，則會以適當的資料填入 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。 如果失敗，則內容為未定義。</p> | 
| <p>JET_TblInfoDbid</p> | <p><em>pvResult</em> 會被視為兩個 <a href="gg269248(v=exchg.10).md">JET_DBID</a> 物件的陣列。 擁有資料表之資料庫的資料庫識別碼會儲存在這個陣列中兩次。</p> | 
| <p>JET_TblInfoDumpTable</p> | <p>JET_TblInfoDumpTable 已被取代。 API 會傳回 JET_errFeatureNotAvailable。</p> | 
| <p>JET_TblInfoName</p> | <p>JET_TblInfoName 會抓取資料表的名稱，並將其儲存在 <em>pvResult</em>中。 如果緩衝區太小，則行為是未定義的。</p> | 
| <p>JET_TblInfoMostMany</p> | <p>JET_TblInfoMostMany 會抓取資料表的名稱，並將其儲存在 <em>pvResult</em>中。 如果緩衝區太小，則行為是未定義的。</p> | 
| <p>JET_TblInfoOLC</p> | <p>JET_TblInfoOLC 已被取代。 API 會傳回 JET_errFeatureNotAvailable。</p> | 
| <p>JET_TblInfoRvt</p> | <p>JET_TblInfoRvt 已被取代。 API 會傳回 JET_errQueryNotSupported。</p> | 
| <p>JET_TblInfoResetOLC</p> | <p>JET_TblInfoResetOLC 已被取代。 API 會傳回 JET_errFeatureNotAvailable。</p> | 
| <p>JET_TblInfoSpaceAlloc</p> | <p><em>pvResult</em> 會被視為兩個 ulong 的陣列：</p><ul><li><p>第一個 <strong>ULONG</strong> 是資料表中的頁面數目。</p></li><li><p>第二個 <strong>ULONG</strong> 是資料表頁面的目標密度。</p></li></ul> | 
| <p>JET_TblInfoSpaceAvailable</p> | <p><em>pvResult</em> 會被解釋為 <strong>ULONG</strong>。 <strong>ULONG</strong>是資料表中可用的頁數、其索引和 long 值樹狀目錄的總和。</p> | 
| <p>JET_TblInfoSpaceOwned</p> | <p><em>pvResult</em> 會被解釋為 <strong>ULONG</strong>。 <strong>ULONG</strong>是資料表所擁有的頁面數目總和 (包括其索引，以及) 的完整值樹狀目錄和任何可用頁面。</p> | 
| <p>JET_TblInfoSpaceUsage</p> | <p>API 的行為取決於傳遞給 API 的緩衝區大小。 兩個 <em>cbMax</em> 值至少必須是 ( 2 * SIZEOF ( ULONG ) ) 。</p><ul><li><p>如果 <em>cbMax</em> 是 ( 2 * SIZEOF ( ULONG ) ) ，則會將 <em>pvResult</em> 解釋為兩個 ulong 的陣列：</p><ul><li><p>第一個 <strong>ULONG</strong> 是資料表的擁有範圍數目。</p></li><li><p>第二個 <strong>ULONG</strong> 是資料表的可用範圍數目。</p></li></ul></li><li><p><em>pvResult</em> 會被解釋為的陣列：</p><ul><li><p>第一個 <strong>ULONG</strong> 是資料表的擁有範圍數目。</p></li><li><p>第二個 <strong>ULONG</strong> 是資料表的可用範圍數目。</p></li></ul></li></ul> | 
| <p>JET_TblInfoTemplateTableName</p> | <p><em>pvResult</em> 會被視為字串緩衝區。 緩衝區至少必須是 JET_cbNameMost + 1，包括終止的 <strong>Null</strong>。 如果資料表是衍生的資料表，則會使用衍生資料表繼承其 DDL 的資料表名稱填入緩衝區。 如果資料表不是衍生的資料表，則緩衝區將會是空字串。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>緩衝區太小。</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>指定了已被取代的 <em>InfoLevel</em> 。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>緩衝區的大小不正確。</p> | 
| <p>JET_errInvalidOperation</p> | <p>傳入的資料表是臨時表，而且無法針對臨時表抓取要求的 <em>InfoLevel</em> 。</p> | 
| <p>JET_errObjectNotFound</p> | <p>傳入的資料表是臨時表，而且無法針對臨時表抓取要求的 <em>InfoLevel</em> 。</p> | 
| <p>JET_errQueryNotSupported</p> | <p>不支援 <em>InfoLevel</em> 。</p> | 
| <p>JET_errTableInUse</p> | <p>資料表正由另一個資料庫作業使用中。</p> | 
| <p>JET_errTableLocked</p> | <p>資料表已由另一個資料庫操作鎖定。</p> | 
| <p>JET_wrnTableInUseBySystem</p> | <p>系統正在使用資料表。 這個警告不是嚴重的。</p> | 



#### <a name="remarks"></a>備註

某些資訊片段對臨時表而言是不正確 (請參閱 [JetOpenTempTable](./jetopentemptable-function.md)) 。

資料表統計資料包括記錄的數目以及叢集索引中的頁面數目 (也就是包含記錄資料) 的索引。 索引統計資料是使用 [JetGetIndexInfo](./jetgetindexinfo-function.md) 或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)，依名稱個別存取。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetTableInfoW</strong> (Unicode) 和 <strong>JetGetTableInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)
