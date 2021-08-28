---
description: 深入瞭解： JetAddColumn 函數
title: JetAddColumn 函式
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1f59d4bb49145dd897994bebb776249a55e14d8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466375"
---
# <a name="jetaddcolumn-function"></a>JetAddColumn 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetaddcolumn-function"></a>JetAddColumn 函式

**JetAddColumn** 函數會將新的資料行加入至 ESE 資料庫中的現有資料表。

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

要加入資料行的資料表。

*szColumnName*

要加入之資料行的名稱。 此名稱必須符合下列準則：

  - 長度必須少於 JET_cbNameMost 個字元，不包括終止的 **Null**。

  - 它必須只包含下列集合中的字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () ， \] 也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。

  - 它不能以空格開頭。

  - 它至少必須包含一個非空白字元。

*pcolumndef*

[JET_COLUMNDEF](./jet-columndef-structure.md)結構的指標，此結構會定義可儲存在資料行中的資料。

*pvDefault*

緩衝區的指標，其中包含資料行的預設值。 緩衝區的長度為 **cbDefault**。 如果沒有預設值，請將 **pvDefault** 設定為 **Null** ，並將 **cbDefault** 設定為零。 固定資料行的預設值不能大於 JET_cbColumnMost 個位元組，或 long 值的 JET_cbLVDefaultValueMost 個位元組。 如果預設值大於該值，則會以無訊息模式截斷。

如果 *grbit* 已設定 JET_bitColumnUserDefinedDefault， **pvDefault** 將會被解釋為 [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) 結構的指標。

*cbDefault*

在 **pvDefault** 中指定的緩衝區大小（以位元組為單位）。

*>ekind*

[JET_COLUMNID](./jet-columnid.md)結構的指標，在成功的情況下，將會接收新建立之資料行的識別碼。 失敗時，值為未定義。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業成功。</p> | 
| <p>JET_errFixedDDL</p> | <p>嘗試修改固定 DDL 資料表的資料定義。 具有固定 DDL 的資料表範例是範本資料表。</p> | 
| <p>JET_errInvalidParameter</p> | <p>傳遞至 API 的參數無效。 以下是無效參數的一些範例：</p><ul><li><p>在其<em>cbStruct</em>成員中傳遞錯誤的<a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構大小。</p></li><li><p>傳入 JET_bitColumnUserDefinedDefault，但未將 <strong>cbDefault</strong> 設定為 sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) 。</p></li></ul> | 
| <p>JET_errInTransaction</p> | <p>嘗試加入具有 JET_bitColumnUnversioned 位集的資料行，但該會話目前位於交易中。</p> | 
| <p>JET_errColumnDuplicate</p> | <p>資料行已經存在。 嘗試加入沒有版本資訊的資料行，而且該資料行已經存在。</p> | 
| <p>JET_errTableNotEmpty</p> | <p>資料表包含資料。 您只能將 [保管更新] 資料行新增至空白資料表。</p> | 
| <p>JET_errRecordTooBig</p> | <p>記錄太大。 固定資料行之 <strong>cbMax</strong> 參數的總和不得超過某個值。</p> | 
| <p>JET_errTooManyColumns</p> | <p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p> | 
| <p>JET_errColumnRedundant</p> | <p>嘗試加入重複的資料行。 應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>無法解析回呼函數。 可能找不到 DLL，或可能找不到 DLL 中的函數。 如果啟用了足夠的記錄，事件記錄檔將會提供更多詳細資料。</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>指出固定或變數資料行 (<strong>cbMax</strong>) 長度上限大於 JET_cbColumnMost 的警告。 這項限制不適用於 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 和 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 的 Long 值 (。</p> | 
| <p>JET_errInvalidName</p> | <p>傳遞的名稱無效，因為 <strong>szColumnName</strong>。 如需有關限制的詳細資訊，請參閱 <strong>szColumnName</strong>的準則。</p> | 
| <p>JET_errInvalidColumnType</p> | <p><strong>Coltyp</strong>欄位未設定為有效的資料行類型。</p> | 
| <p>JET_errInvalidCodePage</p> | <p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>cp</strong>參數未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p> | 
| <p>JET_errTaggedNotNull</p> | <p>JET_bitColumnNotNull 不能與加上標籤、Long 值或 SLV 資料行一起使用。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>指定了不正確 <em>grbits</em> 組合。 此錯誤的部分原因如下：</p><ul><li><p>JET_bitColumnFixed 用於已標記、Long 值或 SLV 資料行。</p></li><li><p>JET_bitColumnEscrowUpdate 用於不是 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>類型的資料行。</p></li><li><p>JET_bitColumnEscrowUpdate 用於 (JET_bitColumnVersion) 的版本資料行。</p></li><li><p>JET_bitColumnEscrowUpdate 用在 AutoIncrememnt 資料行上 (JET_bitColumnAutoincrement) 。</p></li><li><p>JET_bitColumnEscrowUpdate 在沒有預設值的資料行上使用 (<strong>cbDefault</strong> 等於零) 。</p></li><li><p>JET_bitColumnFinalize 用在非「正在進行」更新資料行的資料行上， (JET_bitColumnEscrowUpdate 未設定) 。</p></li><li><p>JET_bitColumnDeleteOnZero 用在非「正在進行」更新資料行的資料行上， (JET_bitColumnEscrowUpdate 未設定) 。</p></li><li><p>JET_bitColumnAutoincrement 用於未 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>的資料行。</p><p><strong>Windows 2000：</strong>錯誤碼的這個原因只用于 Windows 2000。</p><p>JET_bitColumnAutoincrement 用於不是 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>的資料行。</p><p><strong>Windows XP：</strong>此錯誤碼的原因是用於 Windows XP 和更新版本的作業系統。</p></li><li><p>JET_bitColumnVersion 用於未 <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>的資料行。</p></li><li><p>自動遞增資料行使用了 JET_bitColumnVersion。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnFixed 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnNotNull 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnVersion 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnAutoincrement 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnUpdatable 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnEscrowUpdate 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnFinalize 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnDeleteOnZero 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 與 JET_bitColumnMaybeNull 一起使用。</p></li><li><p>JET_bitColumnUserDefinedDefault 是用於固定或變數) 的未標記資料行 (。</p></li></ul> | 
| <p>JET_errMultiValuedColumnMustBeTagged</p> | <p>多值資料行 (JET_bitColumnMultiValued) 只能用在已加上標籤或 Long 值 (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 資料行中。</p> | 
| <p>JET_errCannotBeTagged</p> | <p>嘗試在資料行可能未標記時使用標記的資料行。 禁止標記的資料行的部分條件約束為：</p><ul><li><p> (JET_bitColumnEscrowUpdate) 的「保管更新資料行」不能用在已標記或長的值 (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 資料行。</p></li><li><p>自動遞增資料行可能未標記。</p></li><li><p>可能未標記版本資料行。</p></li></ul> | 
| <p>JET_errExclusiveTableLockRequired</p> | <p>此作業需要資料表的獨佔鎖定。</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>指出固定或變數資料行 (<em>cbMax</em>) 長度上限大於 JET_cbColumnMost 的警告。 這項限制不適用於 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> 和 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) 的 Long 值 (。</p> | 



#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetAddColumnW</strong> (Unicode) 和 <strong>JetAddColumnA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
