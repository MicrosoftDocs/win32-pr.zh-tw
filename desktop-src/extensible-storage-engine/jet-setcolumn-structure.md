---
description: 深入瞭解： JET_SETCOLUMN 結構
title: JET_SETCOLUMN 結構
TOCTitle: JET_SETCOLUMN Structure
ms:assetid: 3fdb8ec0-3c40-44f3-9859-72e22a504b90
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269233(v=EXCHG.10)
ms:contentKeyID: 32765535
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
ms.openlocfilehash: a170132fd4d832133e0f0bcad4a3499fa743db38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689936"
---
# <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_setcolumn-structure"></a>JET_SETCOLUMN 結構

**JET_SETCOLUMN** 結構包含 [JetSetColumns](./jetsetcolumns-function.md)的輸入和輸出參數。 結構中的欄位描述要設定的資料行值、如何設定它，以及要在哪裡取得資料行集資料。

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      const void* pvData;
      unsigned long cbData;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_ERR err;
    } JET_SETCOLUMN;
```

### <a name="members"></a>成員

**columnid**

要設定之資料行的資料行識別碼。

**pvData**

要設定為數據行的資料指標。

**cbData**

配置的大小（以位元組為單位），以位元組為單位從 **pvData** 開始。

**grbit**

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。

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
<td><p>JET_bitSetAppendLV</p></td>
<td><p>將資料附加至類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行。 您可以藉由判斷現有 long 值的大小，並在<strong>psetinfo</strong>中指定<strong>ibLongValue</strong> ，來達成相同的行為。 不過，使用此 <em>grbit</em>比較簡單，因為不需要知道現有資料行值的大小。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetOverwriteLV</p></td>
<td><p>以新資料取代現有的 long 值。 使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSizeLV</p></td>
<td><p>將輸入緩衝區轉譯為整數位節數，以將其設定為指定 columnid 所描述之 long 值的長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。 如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。 如果大小小於現有的資料行值，則會截斷此值。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetZeroLength</p></td>
<td><p>將值設定為零長度。 一般來說，藉由傳遞 cbMax 0 來將資料行值設定為 Null。 不過，對於某些類型而言（例如 <a href="gg269213(v=exchg.10).md">JET_coltypText</a>），資料行值的長度可以是0，而不是 null，而且此選項可用來區分 Null 和0長度。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetSeparateLV</p></td>
<td><p>強制將 long 值、類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行與記錄資料的其餘部分分開儲存。 這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。 不過，這個選項可以用來強制儲存較長的值。 請注意，在大小或較小的四個位元組之間，不能強制為個別的值。 在這種情況下，會忽略選項。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetUniqueMultiValues</p></td>
<td><p>強制多重值資料行中的相異值。 此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。 如果指定此選項，則也不能指定 JET_bitSetAppendLv、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetUniqueNormalizedMultiValues</p></td>
<td><p>強制多重值資料行中的相異值。 此選項會比較資料行資料的索引鍵正規化轉換與其他類似轉換的現有資料行值，如果找到重複的資料行，則會傳回錯誤。 如果指定此選項，則也不能指定 JET_bitSetAppendLv、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSetRevertToDefaultValue</p></td>
<td><p>導致資料行在後續的取出資料行作業上傳回預設資料行值。 移除所有現有的資料行值。 此選項僅適用于已標記、稀疏或多重值的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIntrinsicLV</p></td>
<td><p>盡可能保留最長的值、 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 JET_coltypeLongBinary 類型的資料行，並盡可能地儲存其他記錄資料。 一般情況下，長的資料行會在其長度超過1024個位元組時分開儲存，否則會導致記錄長度超過其頁面大小的相關大小限制。 但是，如果設定此選項，set 資料行作業會失敗並出現錯誤 JET_errColumnTooBig，而不是將此資料行值與其余記錄資料分開。</p></td>
</tr>
</tbody>
</table>


**ibLongValue**

從 [JET_coltypLongBinary](./jet-coltyp.md)或 [JET_coltypLongText](./jet-coltyp.md)類型的資料行抓取的第一個位元組位移。

**itagSequence**

描述多重值資料行中值的序號。 **ItagSequence** 為0表示應該將資料行值集加入為多重值資料行的新實例。

**犯 錯**

從集合資料行作業傳回的錯誤碼和警告。

### <a name="requirements"></a>規格需求

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
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetSetColumns](./jetsetcolumns-function.md)
