---
description: 深入瞭解： JetGetObjectInfo 函數
title: JetGetObjectInfo 函式
TOCTitle: JetGetObjectInfo Function
ms:assetid: 3e069c61-6dab-4b79-8bf2-7844d017598f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269232(v=EXCHG.10)
ms:contentKeyID: 32765534
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetObjectInfo
- JetGetObjectInfoA
- JetGetObjectInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 824c19fbb1fb1e479b805eb45bf8ff56458110d0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469785"
---
# <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetobjectinfo-function"></a>JetGetObjectInfo 函式

**JetGetObjectInfo** 函式會捕獲資料庫物件的相關資訊。 目前只支援資料表。 [JetGetTableInfo](./jetgettableinfo-function.md) 可以用來提取比 **JetGetObjectInfo** 更多的資訊。

```cpp
    JET_ERR JET_API JetGetObjectInfo(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_OBJTYP objtyp,
      __in_opt      const tchar* szContainerName,
      __in_opt      const tchar* szObjectName,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*sesid*

要使用的資料庫會話內容。

*dbid*

從中抓取資訊的資料庫。

*objtyp*

物件，包含要取出的資訊。 目前只支援 JET_objtypNil 和 JET_objtypTable，兩者的行為相同。 只會取出資料表。

*szContainerName*

此參數會保留供日後使用，並傳遞 **Null**。 要取得其資訊之物件的類型名稱。

*szObjectName*

物件的名稱，其中包含要取出的資訊。 當 *InfoLevel* 使用 JET_ObjInfoList 或 JET_ObjInfoListNoStats 選項來取出所有物件的清單時，此值應該是 **Null** 或空字串。

目前只支援資料表名稱。

*pvResult*

接收指定資訊之緩衝區的指標。

緩衝區的大小（以位元組為單位）會以 *cbMax* 傳遞。 失敗時， *pvResult* 的內容是未定義的。

儲存在 *pvResult* 中的資訊取決於 *InfoLevel*。

*cbMax*

傳入 *pvResult* 的緩衝區大小（以位元組為單位）。

*InfoLevel*

指定要為指定物件取出的資訊類型。 它會影響 *pvResult* 的解讀方式。

您可以針對此參數設定下列選項。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_ObjInfo</p> | <p><em>pvResult</em> 會被視為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a> 結構。</p><p><a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>結構會填入<em>szObjectName</em>中所命名物件的相關資訊。</p><p>如果呼叫者不想知道物件的記錄和頁面數目，請考慮使用 JET_ObjInfoNoStats 資訊層級，因為不包含統計資料，所以可能更快。</p> | 
| <p>JET_ObjInfoList</p> | <p><em>pvResult</em> 會被視為 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構。 會抓取所有物件的相關資訊。 系統將會建立臨時表，並在 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構中描述遍歷臨時表所需的資訊。 如需詳細資訊，請參閱 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>。 如果呼叫者不想知道物件的記錄和頁面數目，請考慮使用 JET_ObjInfoListNoStats，這樣可能會更快。</p> | 
| <p>JET_ObjInfoListACM</p> | <p>已淘汰，目前不支援。</p> | 
| <p>JET_ObjInfoListNoStats</p> | <p><em>pvResult</em> 會被視為 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構。 會抓取所有物件的相關資訊。 系統將會建立臨時表，並在 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a> 結構中描述遍歷臨時表所需的資訊。 如需詳細資訊，請參閱 <a href="gg269348(v=exchg.10).md">JET_OBJECTLIST</a>。 JET_ObjInfoListNoStats 與 JET_ObjInfoList 相同，不同之處在于報告記錄數目 (<em>columnidcRecord</em>) 和頁面 (<em>columnidcPage</em>) 的資料行將不會更新。</p> | 
| <p>JET_ObjInfoMax</p> | <p><em>pvResult</em> 會被解釋為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>。 物件的大小上限為頁面。 目前只會傳回資料表。</p> | 
| <p>JET_ObjInfoNoStats</p> | <p><em>pvResult</em> 會被解釋為 <a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>。 只會抓取 <em>szObjectName</em> 中指定之物件的相關資訊。</p><p><a href="gg269353(v=exchg.10).md">JET_OBJECTINFO</a>結構將會填入與<em>szObjectName</em>中所命名物件相關的資訊。</p><p>JET_ObjInfoNoStats 與 JET_ObjInfo 相同，不同之處在于報告記錄和頁面數目的欄位會設定為零。</p> | 
| <p>JET_ObjInfoRulesLoaded</p> | <p>已淘汰，目前不支援。</p> | 
| <p>JET_ObjInfoSysTabCursor</p> | <p>已淘汰，目前不支援。</p> | 
| <p>JET_ObjInfoSysTabReadOnly</p> | <p>已淘汰，目前不支援。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p><em>CbMax</em>中提供的緩衝區大小太小，無法容納所需的資訊。</p> | 
| <p>JET_errInvalidName</p> | <p><em>SzObjectName</em>或<em>szContainerName</em>中提供了不正確名稱。</p> | 
| <p>JET_errInvalidParameter</p> | <p>指定了不正確的參數。 可能會有不正確的層級傳遞至 <em>InfoLevel</em>。</p> | 



#### <a name="remarks"></a>備註

如果 **JetGetObjectInfo** 成功建立臨時表 (例如，JET_ObjInfoList 或 JET_ObjInfoNoStats) ，則呼叫端會負責以 [JetCloseTable](./jetclosetable-function.md)關閉臨時表。

**JetGetObjectInfo** 目前僅支援抓取資料表的相關資訊。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetObjectInfoW</strong> (Unicode) 和 <strong>JetGetObjectInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetGetTableInfo](./jetgettableinfo-function.md)
