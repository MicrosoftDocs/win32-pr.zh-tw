---
description: 深入瞭解： JET_UNICODEINDEX 結構
title: JET_UNICODEINDEX 結構
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: 544438541affba1121850d5ad5a7a60d54d398bd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471384"
---
# <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_unicodeindex-structure"></a>JET_UNICODEINDEX 結構

**JET_UNICODEINDEX** 結構自訂在 unicode 資料行上建立索引時，如何將 Unicode 資料正規化。

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a>成員

**lcid**

正規化資料時要使用的地區設定識別碼。 只要電腦上已安裝適當的語言套件，即可使用任何地區設定。 其中一個例外狀況是，非語言相關地區設定 (LCID 為零) 不合法。

**dwMapFlags**

當 Unicode 資料正規化至索引鍵時，這些旗標會傳遞至 [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) ，如此可讓使用者定義旗標覆寫預設值。

**Windows 2000**： **dwFlags** 的唯一兩個合法值為：

  -  ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH |NORM_IGNORENONSPACE ) 

<!-- end list -->

  -  ( LCMAP_SORTKEY |NORM_IGNORECASE |NORM_IGNOREKANATYPE |NORM_IGNOREWIDTH ) 

**dwMapFlags** 具有下列限制。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>LCMAP_SORTKEY</p> | <p>Mandatory。</p> | 
| <p>LCMAP_BYTEREV</p> | <p>選擇性。</p> | 
| <p>NORM_IGNORECASE</p> | <p>選擇性。</p> | 
| <p>NORM_IGNORENONSPACE</p> | <p>選擇性。</p> | 
| <p>NORM_IGNORESYMBOLS</p> | <p>選擇性。</p> | 
| <p>NORM_IGNOREKANATYPE</p> | <p>選擇性。</p> | 
| <p>NORM_IGNOREWIDTH</p> | <p>選擇性。</p> | 
| <p>SORT_STRINGSORT</p> | <p>選擇性。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)
