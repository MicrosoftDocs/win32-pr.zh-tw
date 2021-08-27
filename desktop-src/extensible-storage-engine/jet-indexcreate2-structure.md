---
description: 深入瞭解： JET_INDEXCREATE2 結構
title: JET_INDEXCREATE2 結構
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00d5a788113b7427fb96a4f270478c1dd7572d54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473204"
---
# <a name="jet_indexcreate2-structure"></a>JET_INDEXCREATE2 結構


_**適用于：** Windows |Windows伺服器_

**JET_INDEXCREATE2** 結構包含對可延伸的儲存體引擎 (ESE) 資料庫中的資料建立索引所需的資訊。 結構是由函式（例如 [JetCreateIndex2](./jetcreateindex2-function.md)）和結構（例如 [JET_TABLECREATE](./jet-tablecreate-structure.md) 和 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)）所使用。

Windows 7 作業系統引進了 **JET_INDEXCREATE2** 結構。

```cpp
typedef struct tagJET_INDEXCREATE2 {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
    unsigned long cbKeyMost;
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小（以位元組為單位）。 將這個成員設定為 sizeof ( JET_INDEXCREATE2 ) 。

**szIndexName**

要建立之索引的名稱。

此名稱應符合下列條件：

  - 它應該小於 JET_cbNameMost，不包括終止的 null。

  - 它必須由下列一組字元組成： 0 (零) 到9、A 到 Z、a 到 z，以及 "" 以外的所有其他標點符號 \!  (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。

  - 不得以空格開頭。

  - 它至少必須包含一個非空白字元。

**szKey**

以 null 分隔之標記的雙 null 結束字串指標。

每個權杖的格式為 " \<direction-specifier\> \<column-name\> "，其中的方向規格為 "+" 或 "-"。 例如，"+  abc \\ 0-def \\ 0 + Ghi 0" 的 szKey \\ 會以遞增順序來編制三個數據行 "abc" (的索引) 、"def" (以遞減順序) 和 "ghi" (遞增順序) 。 在 C 語言中，字串常值具有隱含的 **Null** 結束字元，因此上述字串將以雙 Null 結束。

在 **szKey** 中指定的資料行數目不能超過與版本相依的常數)  (JET_ccolKeyMost。

至少必須在 **szKey** 中命名一個資料行。

過時行為：在雙 Null 結束字元之後，您可以指定語言識別項， (傳遞到 MAKELCID ( langid 中的文字，SORT_DEFAULT ) ) 做為指定索引之 LCID 的方式。 在 *grbit*) 中設定 JET_bitIndexUnicode，在 **szKey** 中指定語言識別項和 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (中的 LCID 是不合法的。

已淘汰：在語言識別項之後，可以將 **cbVarSegMac** 傳遞為 **USHORT** 資料類型。 如果在 **szKey** 中同時設定 USHORT，以及在結構中設定 **cbVarSegMac** ，則行為會是未定義的。

**cbKey**

**SzKey** 的長度（以位元組為單位），包括兩個終止的 null。

**grbit**

包含零或多個值選項的位群組，這些選項列于下表中。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitIndexUnique</p> | <p>不允許有重複的索引項目 (索引鍵) 。 呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 時，不會強制執行這項功能，而不是在呼叫 <a href="gg294137(v=exchg.10).md">JetSetColumn</a> 時強制執行。</p> | 
| <p>JET_bitIndexPrimary</p> | <p>索引是主要 (叢集) 索引。 每個資料表都必須只有一個主要索引。 如果未在資料表上明確定義主要索引，database engine 將會建立自己的主要索引。</p> | 
| <p>JET_bitIndexDisallowNull</p> | <p>建立索引的資料行都不能包含 <strong>Null</strong> 值。</p> | 
| <p>JET_bitIndexIgnoreNull</p> | <p>如果要編制索引的所有資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</p> | 
| <p>JET_bitIndexIgnoreAnyNull</p> | <p>如果要編制索引的任何資料行都是 <strong>Null</strong>，請勿加入資料列的索引項目。</p> | 
| <p>JET_bitIndexIgnoreFirstNull</p> | <p>如果要編制索引的第一個資料行是 <strong>Null</strong>，請勿加入資料列的索引項目。</p> | 
| <p>JET_bitIndexLazyFlush</p> | <p>指定將延遲記錄索引作業。</p><p>JET_bitIndexLazyFlush 不會影響資料更新的酷。 如果處理常式終止時，索引作業中斷，軟復原仍能讓資料庫處於一致的狀態，但索引可能不存在。</p> | 
| <p>JET_bitIndexEmpty</p> | <p>請勿嘗試建立索引，因為所有專案都會評估為 <strong>Null</strong>。 <strong>grbit</strong> 傳遞 JET_bitIndexEmpty 時，也必須指定 JET_bitIgnoreAnyNull。 這是一項效能增強功能。 例如，如果新的資料行加入至資料表，然後在這個新加入的資料行上建立索引，則會掃描資料表中的所有記錄，即使這些記錄未加入至索引也一樣。 指定 JET_bitIndexEmpty 會略過資料表掃描，這可能會花費很長的時間。</p> | 
| <p>JET_bitIndexUnversioned</p> | <p>JET_bitIndexUnversioned 會導致其他交易看到索引建立。 一般來說，交易中的會話將無法在另一個會話中看到索引建立作業。 如果另一個交易可能建立相同的索引，則此旗標很有用。 第二個索引建立將會失敗，而不是可能導致許多不必要的資料庫作業。 第二筆交易可能無法立即使用索引。 索引建立作業必須先完成，才可供使用。 會話目前不能在交易中建立索引，而不需要版本資訊。</p> | 
| <p>JET_bitIndexSortNullsHigh</p> | <p>指定此旗標會在索引中的所有資料行資料之後，將 <strong>Null</strong> 值排序。</p> | 
| <p>JET_bitIndexUnicode</p> | <p>指定此旗標會影響結構中 lcid/pidxunicde 聯集欄位的解釋。 設定位表示 pidxunicode 欄位實際上會指向 <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> 結構。 不需要 JET_bitIndexUnicode 來編制 Unicode 資料的索引。 只需要自訂 Unicode 資料的正規化。</p> | 
| <p>JET_bitIndexTuples</p> | <p>指定索引為元組索引。 如需元組索引的描述，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 。</p><p>Windows XP 作業系統引進了 JET_bitIndexTuples 的值。</p> | 
| <p>JET_bitIndexTupleLimits</p> | <p>指定此旗標會影響結構中 <strong>cbVarSegMac/ptuplelimits</strong> 聯集欄位的解釋。 設定此位表示 <strong>ptuplelimits</strong> 欄位實際上會指向 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，以允許自訂元組索引限制 (暗示 JET_bitIndexTuples) 。</p><p><strong>JET_bitIndexTupleLimits</strong>值是在 Windows Server 2003 作業系統中引進。</p> | 
| <p>JET_bitIndexCrossProduct<br />0x00004000</p> | <p>針對具有多值資料行之多個索引鍵資料行的索引指定此旗標，會導致針對這些索引鍵資料行中的所有值交叉乘積的每個結果建立索引項目。 否則，索引在最重要的索引鍵資料行中，每個多重值都只會有一個專案，這是多值資料行，而每個索引項目會使用任何其他索引鍵資料行中的第一個多重值資料行值。</p><p>例如，如果您在資料行 A 上針對具有值 "1" 和 "2" 的資料行 A 指定此旗標，則會建立下列索引項目： "red"、"1"、"red"、"2"、"blue"、"1"、"blue"、"2"。 否則，將會建立下列索引項目： "red"、"1"、"blue"、"1"。</p><p>Windows Vista 引進了<strong>JET_bitIndexCrossProduct</strong>的值。</p> | 
| <p>JET_bitIndexKeyMost<br />0x00008000</p> | <p>指定此旗標將會導致索引使用結構中 <strong>cbKeyMost</strong> 欄位指定的最大索引鍵大小。 否則，索引會使用 JET_cbKeyMost (255) 做為其最大索引鍵大小。</p><p>Windows Vista 引進了<strong>JET_bitIndexKeyMost</strong>的值。</p> | 
| <p>JET_bitIndexDisallowTruncation<br />0x00010000</p> | <p>指定此旗標會導致索引的任何更新會導致截斷的金鑰失敗，並產生 JET_errKeyTruncated 的回應碼。 否則，將會以無訊息方式截斷金鑰。 如需有關金鑰截斷的詳細資訊，請參閱 <a href="gg269329(v=exchg.10).md">JetMakeKey</a>。</p><p>Windows Vista 引進了<strong>JET_bitIndexDisallowTruncation</strong>的值。</p> | 



**ulDensity**

初始索引 B + 樹狀結構的百分比密度。 指定小於100的數位，一開始就會使用較多的空間來建立索引，但允許未來的索引成長，進而避免發生內部片段。

**lcid**

地區設定識別碼 (LCID) 在 *grbit* 參數中未指定 JET_bitIndexUnicode 值時正規化資料時所要使用的值。 如果索引是透過 Unicode 資料行，則 LCID 會影響正規化。

**pidxunicode**

如果在 *grbit* 參數中指定了 JET_bitIndexUnicode 值，則為 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md)結構的指標。 這可讓使用者指定在 Unicode 正規化期間傳遞至 [LCMapString](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) 函數的自訂旗標。

**cbVarSegMac**

*Grbit* 參數中未指定 JET_bitIndexTupleLimits 值時，每個資料行要儲存在索引中的最大長度（以位元組為單位）。

將此欄位的值指定為 0 (零) 相當於下列專案：

  - 指定主要索引的 JET_cbPrimaryKeyMost。

  - 指定次要索引的 JET_cbSecondaryKeyMost。

**ptuplelimits**

如果在 *grbit* 參數中指定了 JET_bitIndexTupleLimits 值，則為 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md)結構的指標。

**ptuplelimits** 是在 Windows Server 2003 中引進。

**rgconditionalcolumn**

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)結構陣列的選擇性參數，用來指定索引中的條件資料行。

**cConditionalColumn**

**Rgconditionalcolumn** 陣列中的結構計數。

**犯 錯**

包含用來建立此索引的傳回碼。

**cbKeyMost**

針對索引中的索引鍵，指定允許的最大大小（以位元組為單位）。 如果未在 *grbit* 參數中指定 JET_bitIndexKeyMost，則會忽略此參數。 如果這個參數設定為零，且 *grbit* 成員中指定了 JET_bitIndexKeyMost，呼叫的函式將會失敗併發生 JET_err_InvalidDef。

最小支援的金鑰大小為 JET_cbKeyMostMin (255) ，也就是舊版的最大索引鍵大小。

金鑰大小上限取決於資料庫頁面大小 (JET_paramDatabasePageSize) 如下所示：

  - 如果 JET_paramDatabasePageSize = 2048，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost2KBytePage (500) 

  - 如果 JET_paramDatabasePageSize = 4096，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost4KBytePage (1000) 

  - 如果 JET_paramDatabasePageSize = 8192，則 JET_cbKeyMostMin (255) \< =  **cbKeyMost** \< = JET_cbKeyMost8KBytePage (2000) 

您也可以從 JET_paramKeyMost 系統參數讀取實例的最大支援索引鍵大小上限。

**cbKeyMost** 是在 Windows Vista 中引進的。

**pSpacehints**

[JET_SPACEHINTS](./jet-spacehints-structure.md)結構的指標。

**pSpacehints** 是在 Windows 7 中引進。

### <a name="remarks"></a>備註

ESE 支援在包含多個值的索引鍵資料行上編制索引。 若要使用這項功能，資料行必須是標記的資料行類型 (JET_bitColumnTagged) ，且必須加上旗標，以 JET_bitColumnMultiValued 為其建立多個值。 在 Windows Vista 之前的 Windows 版本中，只有索引中的第一個多重值索引鍵資料行會在索引中展開其值。 所有其他多值和標記的資料行只會在索引中展開其第一個值。

假設資料表中有下列資料列 (資料行 Alpha 不是多重值，而資料行 Beta、Gamma 和 Delta 是多重值) ，而且索引建立為 "+ Alpha \\ 0 + Beta \\ 0 + Gamma \\ 0 + Delta \\ 0 \\ 0"：


| <p>Alpha</p> | <p>Beta</p> | <p>色差補正</p> | <p>差異</p> | 
|--------------|-------------|--------------|--------------|
| <p>1</p> | <p>ABC<br />GHI<br />JKL</p> | <p>MNO<br />PQR<br />斯圖</p> | <p>VWX<br />YZ</p> | 
| <p>2</p> | <p>，</p> | <p>雨<br />西班牙</p> | <p>IN<br />瀑布</p> | 



將會儲存下列索引元組：

{1，ABC，MNO，VWX}  
{1，GHI，MNO，VWX}  
{1，JKL，MNO，VWX}  
{2，，雨，IN}

請注意，雖然第二個數據列中的 Alpha 資料行會有單一多重值，但不會儲存 {2，，西班牙，IN}。

從 Windows Vista 開始的 Windows 版本中，您可以藉由指定 JET_bitIndexCrossProduct，在索引中展開所有多重值資料行。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JET_ INDEXCREATE2_W</strong> (Unicode) 和 <strong>JET_</strong> INDEXCREATE2_A (ANSI) 。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
