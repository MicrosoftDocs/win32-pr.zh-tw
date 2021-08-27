---
description: 深入瞭解： JetGetTableColumnInfo 函數
title: JetGetTableColumnInfo 函式
TOCTitle: JetGetTableColumnInfo Function
ms:assetid: b1c1df22-ad33-4320-9f08-baf2a3e7bd7d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294061(v=EXCHG.10)
ms:contentKeyID: 32765676
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTableColumnInfoW
- JetGetTableColumnInfoA
- JetGetTableColumnInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925ade657a4184d5b1cac447aa43619f375bc0b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468955"
---
# <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgettablecolumninfo-function"></a>JetGetTableColumnInfo 函式

**JetGetTableColumnInfo** 函數會抓取資料表資料行的相關資訊。

```cpp
JET_ERR JET_API JetGetTableColumnInfo(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName,
  __out         void* pvResult,
  __in          unsigned long cbMax,
  __in          unsigned long InfoLevel
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

包含要提取資訊之資料行的資料表。

*szColumnName*

要提取資訊的資料行名稱。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel*。 呼叫端必須設定為適當地對齊緩衝區。

*cbMax*

在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。

*InfoLevel*

針對 *szColumnName* 所指定的資料行，將抓取的資訊類型。 儲存在 *pvResult* 中的資料格式取決於 *InfoLevel*。 如需臨時表的架構，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。

  - JET_ColInfoListSortColumnid 會依 *columnid* 排序臨時表。

  - JET_ColInfoListCompact 將壓縮輸出。 如需 compact 輸出的詳細資訊，請參閱 [JET_COLUMNLIST](./jet-columnlist-structure.md)。

您可以為此參數設定下列選項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_ColInfo</p> | <p><em>pvResult</em> 會被視為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，而 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構的欄位會適當地填入。 JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。</p> | 
| <p>JET_ColInfoBase</p> | <p><em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a> 結構。 這類似于 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> 結構。 如果此函式成功，則會以適當的值填入結構。 如果此函式失敗，結構會包含未定義的資料。</p> | 
| <p>JET_ColInfoByColid</p> | <p><em>pvResult</em> 會被解釋為 <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>，但此 <em>InfoLevel</em> 表示所要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。 JET_ColInfo 和 JET_ColInfoByColid 都會取得相同的資訊。</p> | 
| <p>JET_ColInfoList</p> | <p><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。 如果此函式成功，則會以適當的值填入結構。 臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>的<em>tableid</em>成員識別。 資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。 如果此函式失敗，結構會包含未定義的資料。</p> | 
| <p>JET_ColInfoListCompact</p> | <p><em>pvResult</em> 會被視為 <a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a> 結構。 如果此函式成功，則會以適當的值填入結構。 臨時表會開啟，並由<a href="gg269228(v=exchg.10).md">JET_COLUMNLIST</a>的<em>tableid</em>成員識別。 資料表必須以 <a href="gg294087(v=exchg.10).md">JetCloseTable</a>關閉。 如果此函式失敗，結構會包含未定義的資料。</p> | 
| <p>JET_ColInfoListSortColumnid</p> | <p>相同于 JET_ColInfoList，但產生的資料表會依 <em>columnid</em>排序，而不是資料行名稱。</p> | 
| <p>JET_ColInfoSysTabCursor</p> | <p>JET_ColInfoSysTabCursor 已被取代，而且使用它將會傳回 JET_errFeatureNotAvailable。</p> | 
| <p>JET_ColInfoBaseByColId</p> | <p>如同 JET_ColInfoBase， <em>pvResult</em> 會被視為 <a href="gg269194(v=exchg.10).md">JET_COLUMNBASE</a>，但此 <em>InfoLevel</em> 表示要求的資料行 (<em>szColumName</em>) 不是字串資料行名稱，而是指向 <a href="gg294104(v=exchg.10).md">JET_COLUMNID</a>的指標。</p><p><strong>Windows Vista：</strong>這可在 Windows Vista 和更新版本中使用。</p> | 
| <p>JET_ColInfoGrbitNonDerivedColumnsOnly</p> | <p>只有當資料表衍生自範本) 時，才會傳回非衍生的資料行 (。</p><p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p><p><strong>Windows Vista：</strong>此值會在 Windows Vista 中引進。</p> | 
| <p>JET_ColInfoGrbitMinimalInfo</p> | <p>只傳回資料行名稱和每個資料行的 columnid。</p><p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p><p><strong>Windows Vista：</strong>此值會在 Windows Vista 中引進。</p> | 
| <p>JET_ColInfoGrbitSortByColumnid</p> | <p>依 columnid 排序傳回的資料行清單 (預設為依資料行名稱排序清單) 。</p><p>當基底<em>InfoLevel</em> JET_ColInfoList 時，此值可以邏輯或進入<em>InfoLevel</em>。</p><p><strong>Windows Vista：</strong>此值會在 Windows Vista 中引進。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errColumnNotFound</p> | <p>在資料表中找不到名為 <em>szColumnName</em> 的資料行。</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>指定了不正確的 <em>InfoLevel</em> 。</p> | 
| <p>JET_errInvalidName</p> | <p>下列情況可能會傳回此錯誤：</p><ul><li><p>指定了 <em>szTableName</em> 的錯誤名稱。</p></li><li><p>指定了 <em>szColumnName</em> 的錯誤名稱。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>下列情況可能會傳回此錯誤：</p><ul><li><p>指定了不正確的 <em>InfoLevel</em> 。</p></li><li><p>傳入的是 Null <em>szTableName</em> 。</p></li><li><p>緩衝區太小。</p></li></ul> | 



#### <a name="remarks"></a>備註

**JetGetTableColumnInfo** 和 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 都能取出資料行的相關資訊。 它們之間的差異在於如何識別資料表：

  - **JetGetTableColumnInfo** 會依 *tableid* 識別資料表。

  - [JetGetColumnInfo](./jetgetcolumninfo-function.md) 會依 *dbid* 和 *szTableName* 組合來識別資料表。

使用 JET_ColInfoList、JET_ColInfoListSortColumnid 或 JET_ColInfoListCompact 來抓取資料時，將會開啟臨時表。 臨時表包含資料，而 [JET_COLUMNLIST](./jet-columnlist-structure.md) 結構包含足夠的資訊來跨越臨時表。 臨時表必須以 [JetCloseTable](./jetclosetable-function.md)關閉。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetTableColumnInfoW</strong> (Unicode) 和 <strong>JetGetTableColumnInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎錯誤](./extensible-storage-engine-errors.md)  
[錯誤處理參數](./error-handling-parameters.md)  
[JET_COLUMNBASE](./jet-columnbase-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_COLUMNLIST](./jet-columnlist-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo]()
