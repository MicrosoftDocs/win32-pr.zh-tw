---
description: 深入瞭解： JetRetrieveColumn 函數
title: JetRetrieveColumn 函式
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985352"
---
# <a name="jetretrievecolumn-function"></a>JetRetrieveColumn 函式


_**適用于：** Windows |Windows Server_

## <a name="jetretrievecolumn-function"></a>JetRetrieveColumn 函式

**JetRetrieveColumn** 函式會從目前的記錄抓取單一資料行值。 記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。 或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。 此函數也可以從參考目前記錄的索引項目抓取資料行資料。 除了取得實際的資料行值之外， **JetRetrieveColumn** 還可以用來取得資料行的大小，然後再抓取資料行資料本身，讓應用程式緩衝區可以適當地調整大小。

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*columnid*

要取出之資料行的 [JET_COLUMNID](./jet-columnid.md) 。

*Columnid* 值為 0 (零) 可以提供，而不會參考任何個別的資料行。 當 *columnid* 0 (零) 時，所有標記的資料行、稀疏和多重值資料行都會被視為單一資料行。 這有助於抓取記錄中所有的稀疏資料行。

*pvData*

接收資料行值的輸出緩衝區。

*cbData*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

接收資料行值的實際大小（以位元組為單位）。

如果此參數為 **Null**，則不會傳回資料行值的實際大小。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：

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
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>此旗標會使抓取資料行抓取修改過的值，而不是原始的值。 如果尚未修改此值，則會取出原始值。 如此一來，在插入或更新記錄的作業期間，可能會取出尚未插入或更新的值。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>此選項可用來從索引取出資料行值（如果可能的話），而不需要存取記錄。 如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。 在無法從索引中取出原始資料行值的情況下，因為無法復原的轉換或資料截斷，將會存取記錄，並以一般方式抓取資料。 這是效能選項，只有在可能會從索引中抓取資料行值時才會指定。 如果目前的索引是叢集索引，則不應指定此選項，因為叢集或主要索引的索引項目目是記錄本身。 如果也設定 JET_bitRetrieveFromPrimaryBookmark，則無法設定此位。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>此選項是用來從索引書簽中取出資料行值，而且當資料行同時出現在主要索引和目前索引中時，可能會與索引值不同。 如果目前的索引是叢集或主要索引，則不應指定此選項。 如果也設定 JET_bitRetrieveFromIndex，則無法設定此位。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>此選項可用來取出 pretinfo-itagSequence 中多重值資料行值的序號 &gt; 。 ItagSequence 欄位通常是用來從記錄中取出多重值資料行值的輸入。 不過，從索引中抓取值時，您也可以將索引項目與特定序號建立關聯，並取出此序號。 抓取序號可能是成本高昂的作業，而且只在必要時才執行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>此選項可用來取出多值資料行 <strong>Null</strong> 值。 如果未指定此選項，則會自動略過多重值資料行的 <strong>Null</strong> 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>此選項只會影響多重值資料行，而且當要求的序號為1，而且記錄中的資料行沒有設定值時，就會傳回 <strong>Null</strong> 值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>此旗標僅供內部使用，不適合在您的應用程式中使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>此旗標僅供內部使用，不適合在您的應用程式中使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>此旗標將允許抓取索引的元組區段。 您必須使用 JET_bitRetrieveFromIndex 指定此位。</p></td>
</tr>
</tbody>
</table>


*pretinfo*

如果 *pretinfo* 為 **Null** ，則函式的行為就如同 *ItagSequence* 為1，而 *ibLongValue* 為 0 (零) 。 這會導致資料行抓取抓取多重值資料行的第一個值，並在位移 0 (零) 取出長資料。

這個參數是用來提供下列一或多項：

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
<td><p>ibLongValue</p></td>
<td><p>在抓取資料行值的一部分時，將二進位位移提供給 long 資料行值。</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>提供所需多重值資料行值的序號。 請注意，只有在指定 JET_bitRetrieveTag 時，才會設定此欄位。 否則，它不會修改。</p></td>
</tr>
<tr class="odd">
<td><p>columnidNextTagged</p></td>
<td><p>當使用傳遞 <em>columnid</em> 0 (零) 來抓取所有標記、稀疏和多重值的資料行時，傳回所傳回之資料行值的資料行識別碼。</p></td>
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
<td><p>JET_errBadColumnId</p></td>
<td><p>提供的資料行識別碼超出資料行識別碼的合法限制。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadItagSequence</p></td>
<td><p>傳遞了不正確多重值資料行序號值給 pretinfo- &gt; itagSequence。 多重值資料行值序號的有效值為1或更大。 值為 0 (零) 對此函數無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>無法從索引中取出索引為子字串的資料行，因為只有資料行的一小部分通常會出現在每個索引項目目中。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>在某些情況下，為抓取資料行提供的緩衝區必須夠大，才能傳回任何數量的資料行值。 例如，將可更新的可更新資料行調整為在呼叫會話的交易內容中保持一致，而且這項調整需要呼叫端所提供的緩衝區。 如果提供的緩衝區空間不足，則會傳回 JET_errInvalidBufferSize，且不會傳回任何資料行資料。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>指定的一個或多個參數不正確。 如果 retinfo 的大小小於 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>的大小，就會發生這種情況。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>提供的選項未知，或已知位設定的不合法組合。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標未放置在記錄上。 此情況具有許多不同的原因。 例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</p></td>
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
<p><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>無法取出整個資料行值，因為指定的緩衝區小於資料行的大小。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>取出的資料行值為 <strong>Null</strong>。</p></td>
</tr>
</tbody>
</table>


成功時，會將指定資料行的資料行值複製到指定的緩衝區。 會傳回小於所有資料行值，並傳回警告 JET_wrnBufferTruncated。 如果指定了 *pcbActual* ，則會傳回資料行值的實際大小。 請注意， **Null** 值具有 0 (零) 長度，因此會將傳回的大小設定為 0 (零) 。 如果取出的資料行是多重值資料行，而且已指定 *pretinfo* ，而且 JET_bitReturnTag 設定為選項，則會在 pretinfo-itagSequence 中傳回資料行值的序號 \> 。

失敗時，資料指標位置會保持不變，且不會將任何資料複製到提供的緩衝區。

#### <a name="remarks"></a>備註

此呼叫只會用來針對非多重值資料行取出固定或已知大小的資料。 不過，當資料行資料的大小不明時，通常會使用這兩次呼叫。 首先會呼叫它來判斷資料的大小，讓它可以配置所需的儲存空間。 然後，再次進行相同的呼叫，以取得資料行資料。 當實際的值數目未知時，因為資料行是多重值，所以呼叫通常會使用三次。 首先，取得值的數目，然後再按兩次，以配置儲存體並取出實際的資料。

您可以使用 \> 從1開始的 pretinfo-itagSequence 值（從1開始，並在每個後續的呼叫中增加），來取得多重值資料行的所有值。 從函式傳回 JET_wrnColumnNull 時，已知會取出最後一個資料行值。 請注意，如果多重值資料行的值序列中設定了明確的 **Null** 值，則無法完成這個方法，因為這些值會被略過。 如果應用程式想要取出所有多重值的資料行值（包括明確設定為 **Null** 的值），則必須使用 [JetRetrieveColumns](./jetretrievecolumns-function.md) ，而不是 **JetRetrieveColumn**。 請注意，當 *itagSequence* 值為 0 (零) 時，此函數不會傳回多重值函數的值數目。 當 *itagSequence* 值為 0 (零) 時，只有 [JetRetrieveColumns](./jetretrievecolumns-function.md)會傳回資料行值的數目。

如果在交易層級0呼叫這個函式 (零) （例如，呼叫會話本身不在交易中），則會在函式中開啟和關閉交易。 這項功能的目的是要傳回一致的結果，以防長數值跨越資料庫頁面。 請注意，當會話不在交易中時，此交易會在函式呼叫和一系列的呼叫之間釋出，而交易中的會話可能會在第一次呼叫這個函數之後傳回資料更新。

除非設定了 JET_bitRetrieveIgnoreDefault 選項，否則當資料行尚未明確設定為另一個值時，將會取出預設資料行值。

在插入之前從複製緩衝區取出自動遞增資料行值，是在將正規化的資料插入多個資料表時，唯一用來識別連結之記錄的常見方式。 自動遞增值是在插入作業開始時配置，而且可以在更新完成之前，隨時從複製緩衝區中取出。

當您藉由將 *columnid* 設定為 0 (零) 來抓取所有標記、多重值和稀疏資料行時，資料行會以 *columnid* 順序從最低 *columnid* 到最高 *columnid* 進行取出。 每次抓取資料行值時，就會傳回相同的資料行值順序。 順序具決定性。

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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
