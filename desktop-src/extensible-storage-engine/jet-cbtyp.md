---
description: 深入瞭解： JET_CBTYP
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
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
ms.openlocfilehash: b0a2d8551ea0ac47f10cbd189114dde36f72c8b0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982951"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**適用于：** Windows |Windows伺服器_

## <a name="jet_cbtyp"></a>JET_CBTYP

**JET_CBTYP** 的常數群組會描述作業中的所有可能點，資料庫引擎會呼叫 [JET_CALLBACK](./jet-callback-callback-function.md)回呼函數來通知應用程式。 資料庫引擎會在回呼函數的 *cbtyp* 參數中傳遞這些常數的其中一個。 資料庫引擎在此呼叫中傳遞的其他參數的意義取決於傳遞的特定 **JET_CBTYP** 。

**Windows XP：** Windows XP 引進了 **JET_CBTYP** 的常數群組。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_cbtypNull<br />0x00000000</p> | <p>這是保留的回呼，而且一律視為無效。</p> | 
| <p>JET_cbtypFinalize<br />0x00000001</p> | <p>此回呼已保留供日後使用。</p> | 
| <p>JET_cbtypBeforeInsert<br />0x00000002</p> | <p>這項回呼會在透過呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a>將新的記錄插入資料表之前進行。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：要插入記錄的會話。</p></li><li><p><em>dbid</em>：包含要插入之記錄的資料表之資料庫識別碼。</p></li><li><p><em>tableid</em>：已備妥要插入新記錄的資料指標。 請務必注意，在此時間，任何版本或自動遞增資料行的值可能不正確。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</p></li></ul> | 
| <p>JET_cbtypAfterInsert<br />0x00000004</p> | <p>只要呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> ，但在 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 回到其呼叫端之前，新的記錄插入資料表中，就會發生此回呼。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：具有剛插入之記錄的會話。</p></li><li><p><em>dbid</em>：包含剛插入之記錄的資料表之資料庫識別碼。</p></li><li><p><em>tableid</em>：資料表上的資料指標，表示剛插入的記錄。 請注意，資料指標仍位於與 insert 回呼之前相同的索引項目。 此外也請注意，此索引項目可能不會以任何方式與插入的記錄相關。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則會忽略它。</p></li></ul> | 
| <p>JET_cbtypBeforeReplace<br />0x00000008</p> | <p>這項回呼會在 <a href="gg269288(v=exchg.10).md">JetUpdate</a>的呼叫變更資料表中的現有記錄之前發生。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：包含要變更之記錄的會話。</p></li><li><p><em>dbid</em>：包含要變更之記錄之資料表的資料庫識別碼。</p></li><li><p><em>tableid</em>：游標位於與要變更之記錄相關聯的索引項目上。 請務必注意，在此時間，任何版本或自動遞增資料行的值可能不正確。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</p></li></ul> | 
| <p>JET_cbtypAfterReplace<br />0x00000010</p> | <p>這項回呼會在資料表中的現有記錄已由呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> ，但在 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 返回其呼叫端之前發生。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：具有剛剛變更之記錄的會話。</p></li><li><p><em>dbid</em>：包含剛變更之記錄的資料表之資料庫識別碼。</p></li><li><p><em>tableid</em>：游標位於與剛剛變更之記錄相關聯的索引項目目上。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則會忽略它。</p></li></ul> | 
| <p>JET_cbtypBeforeDelete<br />0x00000020</p> | <p>這項回呼會在呼叫 <a href="gg269315(v=exchg.10).md">JetDelete</a>來刪除資料表中的現有記錄之前發生。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：具有要刪除之記錄的會話。</p></li><li><p><em>dbid</em>：包含要刪除之記錄的資料表之資料庫識別碼。</p></li><li><p><em>tableid</em>：游標位於與要刪除之記錄相關聯的索引項目上。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong> 如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</p></li></ul> | 
| <p>JET_cbtypAfterDelete<br />0x00000040</p> | <p>這項回呼會在呼叫 <a href="gg269315(v=exchg.10).md">JetDelete</a> 時，但在 <a href="gg269315(v=exchg.10).md">JetDelete</a> 傳回給其呼叫端之前，于資料表中的現有記錄已刪除的情況下發生。</p><p>此回呼原因的函式指標是透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>傳遞給<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> ，或是在執行時間透過<a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>來設定。 如需詳細資訊，請參閱 <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> 或 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：具有剛刪除記錄的會話。</p></li><li><p><em>dbid</em>：包含剛刪除記錄之資料表的資料庫識別碼。</p></li><li><p><em>tableid</em>：游標位於與剛刪除之記錄相關聯的索引項目上。</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>：傳遞至 <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> 或 <strong>Null</strong>的內容指標。</p></li><li><p><em>ulUnused</em>： <strong>Null</strong></p></li></ul><p>如果回呼傳回錯誤，則會忽略它。</p> | 
| <p>JET_cbtypUserDefinedDefaultValue<br />0x00000080</p> | <p>當引擎需要從應用程式取得使用者定義的資料行預設值時，就會發生此回呼。 此回呼基本上是由應用程式評估的 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 有限實作為。 最多可以針對使用者定義的預設值傳回一個資料行值。</p><p>此回呼原因的函式指標是透過<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>結構傳遞至<a href="gg294122(v=exchg.10).md">JetAddColumn</a> ，或透過<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構中<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>結構傳遞至<a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> 。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：正在計算使用者定義之預設值的會話</p></li><li><p><em>dbid</em>：包含使用者定義之預設值之資料表的資料庫識別碼</p></li><li><p><em>tableid</em>：位於記錄上的資料指標，該記錄會抓取使用者定義的預設值</p></li><li><p><em>pvArg1</em>：使用者定義之預設值的輸出緩衝區</p></li><li><p><em>pvArg2</em>：在輸入時，這是輸出緩衝區的大小。 在輸出時，這是使用者定義之預設值的實際大小。 在任一種情況下，大小為32位不帶正負號的整數。</p></li><li><p><em>pvCoNtext</em>：緩衝區的指標，其中包含建立資料行時在 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構中指定的使用者資料，如果未提供內容則為 Null。</p></li><li><p><em>ulUnused</em>：即將抓取使用者定義預設值之資料行的資料行識別碼。</p></li></ul><p>如果回呼傳回錯誤，則源自回呼的作業將會失敗，並出現該錯誤。</p><p>如果回呼傳回 JET_wrnBufferTruncated，作業將會繼續，但在回呼期間不會取出整個值。</p><p>如果回呼傳回 JET_wrnColumnNull，此作業將會繼續，但資料行的使用者定義預設值為 Null。</p> | 
| <p>JET_cbtypOnlineDefragCompleted<br />0x00000100</p> | <p>當 <a href="gg269317(v=exchg.10).md">JetDefragment</a> 所起始的資料庫線上磁碟重組已停止，因為進程已完成或達到時間限制時，就會發生此回呼。</p><p>此回呼原因的函式指標會傳遞至 <a href="gg269317(v=exchg.10).md">JetDefragment</a>。 如需詳細資訊，請參閱 <a href="gg269317(v=exchg.10).md">JetDefragment</a>。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>：用來對資料流程檔案執行資料庫或 JET_sesidNil 的線上磁碟重組的會話。</p></li><li><p><em>dbid</em>：要針對資料流程檔案進行磁碟重組或 JET_dbidNil 之資料庫的資料庫識別碼。</p></li><li><p><em>tableid</em>： JET_tableidNil</p></li><li><p><em>pvArg1</em>： <strong>Null</strong></p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>： <strong>Null</strong></p></li><li><p><em>ulUnused</em>： <strong>Null</strong></p></li></ul><p>如果回呼傳回錯誤，則會忽略它。</p> | 
| <p>JET_cbtypFreeCursorLS<br />0x00000200</p> | <p>當應用程式需要清除與資料庫引擎所釋放之資料指標相關聯的本機儲存體的內容控制碼時，就會發生此回呼。 如需詳細資訊，請參閱 <a href="gg269243(v=exchg.10).md">JetSetLS</a>。</p><p>此回呼原因的函式指標是透過<a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>的<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>： JET_sesidNil</p></li><li><p><em>dbid</em>： JET_dbidNil</p></li><li><p><em>tableid</em>： JET_tableidNil</p></li><li><p><em>pvArg1</em>：使用<a href="gg269243(v=exchg.10).md">JetSetLS</a>設定的內容控制碼</p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>： <strong>Null</strong></p></li><li><p><em>ulUnused</em>： <strong>Null</strong></p></li></ul><p>如果回呼傳回錯誤，則會忽略它。</p> | 
| <p>JET_cbtypFreeTableLS<br />0x00000400</p> | <p>這是因為應用程式必須清除與資料庫引擎所釋放之資料表相關聯之本機儲存體的內容控制碼，因此會發生此回呼。 如需詳細資訊，請參閱 <a href="gg269243(v=exchg.10).md">JetSetLS</a>。</p><p>此回呼原因的函式指標是透過<a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>的<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定。</p><p>回呼參數會有下列值：</p><ul><li><p><em>sesid</em>： JET_sesidNil</p></li><li><p><em>dbid</em>： JET_dbidNil</p></li><li><p><em>tableid</em>： JET_tableidNil</p></li><li><p><em>pvArg1</em>：使用 <a href="gg269243(v=exchg.10).md">JetSetLS</a>設定的內容控制碼。</p></li><li><p><em>pvArg2</em>： <strong>Null</strong></p></li><li><p><em>pvCoNtext</em>： <strong>Null</strong></p></li><li><p><em>ulUnused</em>： <strong>Null</strong></p></li></ul><p>如果回呼傳回錯誤，則會忽略它。</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)
