---
description: 深入瞭解： JET_TUPLELIMITS 結構
title: JET_TUPLELIMITS 結構
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: dc5a71328681e1ce415b1a34e9c8f718b460e7f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471774"
---
# <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_tuplelimits-structure"></a>JET_TUPLELIMITS 結構

**JET_TUPLELIMITS** 結構允許使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)，針對每個索引（而不是每個實例）自訂元組索引特性。

**Windows Server 2003：****JET_TUPLELIMITS** 結構是在 Windows Server 2003 中引進。

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>成員

**chLengthMin**

元組的最小長度。 預設值是 3。

**chLengthMax**

元組的最大長度。 預設值是 10。

**chToIndexMax**

要編制索引之字串的最大長度。 例如，如果資料行的長度為100個字元，且 **chToIndexMax** 設定為60，則只會編制資料行的前60個字元的索引。 預設值為32767。

**cchIncrement**

這可讓您根據每個索引來設定 stride。

**Windows Vista：****cchIncrement** 成員是在 Windows Vista 中引進。 在 Windows Vista 之前，將視窗移 (「stride」 ) 的數量一律為1，如「備註」一節中的範例所示。

**ichStart**

從值開始抓取元組的值位移。

**Windows Vista：****ichStart** 成員是在 Windows Vista 中引進。

### <a name="remarks"></a>備註

元組索引會引導字串，並編制其所有可能的 **chLengthMax** 子字串的索引。 在字串的結尾 (或位置 **chToIndexMax**（以第一個) 發生者為准），將會編制至少 **chLengthMin** 的子字串索引。

元組索引可以用來搜尋具有開頭和尾端萬用字元的字串。

假設有一個資料列的文字欄位為 "RAIN IN 西班牙 \! "，且如果元組索引是以參數 **chLengthMin**= 2 和 **chLengthMax**= 3 建立的，則索引中會建立下列專案：

"RAI"  
AIN  
在  
"N I"  
在  
在  
"N S"  
SP-1  
SPA  
PAI  
AIN  
"IN \! "  
"N \! "

請注意，"IN" 發生兩次，而且最後一個專案 ( "N \! " ) 小於 3 (**chLengthMax**) 。 另請注意，分割演算法不會察覺空格或單字，並將所有字元視為相同。

**Windows xp：** Windows xp 支援元組索引，但沒有 **JET_TUPLELIMITS**。 資料庫引擎會使用預設值 (**chLengthMin**= 3、 **chLengthMax**= 10、 **chToIndexMax**= 32767) 。 您仍然可以變更這些值，但會使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramIndexTuplesLengthMin](./index-parameters.md)、 [JET_paramIndexTuplesLengthMax](./index-parameters.md)和 [JET_paramIndexTuplesToIndexMax](./index-parameters.md)，以每個實例為基礎設定這些值。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008，Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
