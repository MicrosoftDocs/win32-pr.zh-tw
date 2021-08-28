---
description: 深入瞭解： JetGetDatabaseInfo 函數
title: JetGetDatabaseInfo 函式
TOCTitle: JetGetDatabaseInfo Function
ms:assetid: bd3f92d0-7e98-4aa6-87c5-1c2760cbd1b5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294076(v=EXCHG.10)
ms:contentKeyID: 32765691
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 335ad13411dbfcc83dce559eb4b77adefcc8a5da
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477954"
---
# <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetdatabaseinfo-function"></a>JetGetDatabaseInfo 函式

**JetGetDatabaseInfo** 函式會抓取與資料庫相關的各種資訊類型。 當資料庫已附加或線上 (使用 **JetGetDatabaseInfo**) ，或資料庫或資料庫引擎離線 ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) 時，可以呼叫這個 API。

```cpp
    JET_ERR JET_API JetGetDatabaseInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*dbid*

要從中取得資訊的資料庫 [JET_DBID](./jet-dbid.md) 。

*pvResult*

將接收指定資訊之緩衝區的指標。 緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。

失敗時， *pvResult* 的內容是未定義的。

儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。

*cbMax*

在 *pvResult* 中傳遞的緩衝區大小（以位元組為單位）。

*InfoLevel*

*InfoLevel* 指定應該針對指定的資料庫抓取何種類型的資訊。 它會影響 *pvResult* 的解讀方式。 某些 *InfoLevel* 僅適用于離線 ([JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)) 或線上 (**JetGetDatabaseInfo**) 版本的 API。

如果提供的 *pvResult* 緩衝區太小，可能會根據 *InfoLevel* 傳回 JET_errInvalidBufferSize 或 JET_errBufferTooSmall。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_DbInfoCollate</p> | <p>尚未支援並會傳回預設值。 請勿使用。</p> | 
| <p>JET_DbInfoConnect</p> | <p>這些 <em>InfoLevels</em> 已被取代，目前不受支援。 請勿使用。</p> | 
| <p>JET_DbInfoCountry</p> | <p>尚未支援並會傳回預設值。 請勿使用。</p> | 
| <p>JET_DbInfoCp</p> | <p>尚未支援並會傳回預設值。 請勿使用。</p> | 
| <p>JET_DbInfoFilename</p> | <p><em>pvResult</em> 將會被視為字串緩衝區 (char * ) 。 建議使用 MAX_PATH 緩衝區，但不是必要的。 如果緩衝區不夠長，則會傳回 JET_errBufferTooSmall。 字串將會填入此 DBID 的資料庫路徑。</p> | 
| <p>JET_DbInfoFilesize</p> | <p><em>pvResult</em> 將會被視為 DWORD (4 個位元組) 。 傳回頁面中資料庫的大小。</p> | 
| <p>JET_DbInfoIsam</p> | <p>這些 <em>InfoLevels</em> 已被取代，目前不受支援。 請勿使用。</p> | 
| <p>JET_DbInfoLCID</p> | <p> (Windows XP 及更新版本) 此<em>InfoLevel</em>最初指定為： JET_DbInfoLangid (Windows 2000) </p><p><em>pvResult</em> 將會被解讀為 long。 這會傳回與此資料庫相關聯之 (LCID) 的地區設定識別碼。</p> | 
| <p>JET_DbInfoMisc</p> | <p><em>pvResult</em> 將會被視為 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>。 <a href="gg294147(v=exchg.10).md">JET_DBINFOMISC</a>結構將會填入與所指定資料庫有關的資訊。</p> | 
| <p>JET_DbInfoOptions</p> | <p><em>pvResult</em> 將會被視為 <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> 的 (DWORD) 。 這會傳回資料庫是否在獨佔模式中開啟。 如果資料庫處於獨佔模式 JET_bitDbExclusive 將會在提供的 <a href="gg294066(v=exchg.10).md">JET_GRBIT</a> 中設定，否則會設定零。 請注意，不會傳回<a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>和<a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>的其他資料庫<em>grbit</em>選項。</p> | 
| <p>JET_DbInfoPageSize</p> | <p>只有 Windows XP 及更新版本才提供。 <em>pvResult</em> 將會被視為不帶正負號的 long。 這會傳回資料庫的頁面大小（以位元組為單位）。</p> | 
| <p>JET_DbInfoSpaceAvailable</p> | <p><em>pvResult</em> 將會被解釋為 DWORD。 這會傳回資料庫在頁面中的可用空間。</p> | 
| <p>JET_DbInfoSpaceOwned</p> | <p><em>pvResult</em> 將會被解釋為 DWORD。 這會傳回資料庫在頁面中所擁有的空間。</p> | 
| <p>JET_DbInfoTransactions</p> | <p><em>pvResult</em> 將會被解讀為 long。 這會傳回一個大於最大層級的交易（可進行交易）。 如果以嵌套的方式 (呼叫 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> ，也就是在相同的會話中，如果沒有認可或復原) 的次數與此值相同，則會從 <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a>傳回最後一個呼叫 JET_errTransTooDeep。 請注意 Windows 2000、Windows XP 和 Windows Server 2003 的值為7。</p> | 
| <p>JET_DbInfoVersion</p> | <p><em>pvResult</em> 將會被解讀為 long。 這會傳回資料庫引擎的原生主要版本。 此值為 Windows 2000、Windows XP 和 Windows Server 2003 的0x620。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p><em>CbMax</em>中提供的緩衝區大小太小 (或不正確) 來保存所需的資訊。</p> | 
| <p>JET_errFeatureNotAvailable</p> | <p>JET_DbInfoIsam 要求的 <em>InfoLevel</em> 。 不支援此連結方式。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p><em>CbMax</em>中提供的緩衝區大小太小 (或不正確) 來保存所需的資訊。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當提供的<a href="gg269248(v=exchg.10).md">JET_DBID</a>不是附加) 資料庫的有效 (時， <strong>JetGetDatabaseInfo</strong>會傳回這個錯誤。 當該版本的函式不支援要求的<em>InfoLevel</em>時， <a href="gg269239(v=exchg.10).md">JetGetDatabaseFileInfo</a>和<strong>JetGetDatabaseInfo</strong>會傳回此錯誤。</p> | 



成功時，會在輸出緩衝區中傳回所要求的資料。

失敗時，輸出緩衝區會處於未定義狀態。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetDatabaseInfoW</strong> (Unicode) 和 <strong>JetGetDatabaseInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_DBINFOUPGRADE](./jet-dbinfoupgrade-structure.md)  
[JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md)
