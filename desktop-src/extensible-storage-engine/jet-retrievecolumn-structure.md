---
description: 深入瞭解： JET_RETRIEVECOLUMN 結構
title: JET_RETRIEVECOLUMN 結構
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
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
ms.openlocfilehash: 4f29f3c6a9ca3262b3cd09d726634afd70db9c6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471454"
---
# <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_retrievecolumn-structure"></a>JET_RETRIEVECOLUMN 結構

**JET_RETRIEVECOLUMN** 結構包含 [JetRetrieveColumns](./jetretrievecolumns-function.md)的輸入和輸出參數。 結構中的欄位描述要取出的資料行值、如何取出它，以及要儲存結果的位置。

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>成員

**columnid**

要取得之資料行的資料行識別碼。

**pvData**

開始儲存從資料行值取出之資料的指標。

**cbData**

從 **pvData** 開始的配置大小（以位元組為單位）。 抓取資料行作業將不會在 **pvData** 上儲存比 **cbData** 更多的資料。

**cbActual**

抓取資料行作業取出的資料大小（以位元組為單位）。

**grbit**

包含資料行抓取選項的位群組，其中包含零或多個下列值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>抓取修改過的值，而不是原始的值。 如果尚未修改此值，則會取出原始值。 如此一來，插入或更新記錄時，即可抓取尚未插入或更新的值。</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>盡可能從索引中抓取資料行值，而不存取記錄。 如此一來，當索引項目本身有需要的資料時，就可以避免不必要的記錄載入。 在無法從索引中取出原始資料行值的情況下，因為無法復原的轉換或資料截斷，將會存取記錄，並以一般方式抓取資料。 這是效能選項，只有在可能會從索引中抓取資料行值時才會指定。 如果目前的索引是叢集索引，則不應指定此選項，因為叢集或主要索引的索引項目目是記錄本身。 如果也設定 JET_bitRetrieveFromPrimaryBookmark，則無法設定此位。</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>從索引書簽抓取資料行值，而且當資料行同時出現在主要索引和目前索引中時，可以與索引值不同。 如果目前的索引是叢集或主要索引，則不應指定此選項。 如果也設定 JET_bitRetrieveFromIndex，則無法設定此位。</p> | 
| <p>JET_bitRetrieveTag</p> | <p>捕獲 pretinfo-itagSequence 中多重值資料行值的序號 &gt; 。 ItagSequence 欄位通常是用來從記錄中取出多值資料行值的輸入。 不過，從索引中抓取值時，您也可以將索引項目與特定序號建立關聯，並取出此序號。 抓取序號可能是成本高昂的作業，而且只在必要時才執行。</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>捕獲多重值資料行 Null 值。 如果未指定此選項，則會自動略過多重值資料行的 Null 值。</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>當要求的序號為1，而且記錄中的資料行沒有設定值時，會傳回 Null 值。 此選項只會影響多重值資料行。</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>此旗標僅供內部使用，不適合在您的應用程式中使用。</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>此旗標僅供內部使用，不適合在您的應用程式中使用。</p> | 



**ibLongValue**

要從類型 [JET_coltypLongBinary](./jet-coltyp.md) 或 [JET_coltypLongText](./jet-coltyp.md)的資料行中抓取之第一個位元組的位移。

**itagSequence**

多值資料行中所包含之值的序號。 **JET_RETRIEVECOLUMN** 中的 **itagSequence** 可以是0。 如果 **itagSequence** 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。 **ItagSequence** 值0不能用在 [JetRetrieveColumn](./jetretrievecolumn-function.md)的呼叫中。

**columnidNextTagged**

當所有標記的資料行都透過傳遞0做為 [JetRetrieveColumn](./jetretrievecolumn-function.md)的 **columnid** 時，已標記、多重值或稀疏資料行的 **columnid** 。

**犯 錯**

從資料行抓取傳回的錯誤碼和警告。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
