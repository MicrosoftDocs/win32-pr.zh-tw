---
description: 深入瞭解： JET_GRBIT
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 2b54ed8a95d81c148b68727384dd76fba3d2dc8b1f9d6452c2105bc45f015646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362278"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**適用于：** Windows |Windows伺服器_

## <a name="jet_grbit"></a>JET_GRBIT

**JET_GRBIT** 資料類型是一組位，其中包含所使用之函式和結構的特定常數。

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>資料類型

JET_GRBIT

一般情況下，用來做為此資料類型之值的常數會反映其使用所在的 API 元素名稱。 例如，所有傳遞給 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的常數都以 "JET_bitRetrieve" 開頭。 同樣地，傳遞給 [JetSetColumn](./jetsetcolumn-function.md) 的所有常數都以 "JET_bitSet" 開頭。

值為零會導致忽略參數。

### <a name="remarks"></a>備註

如需詳細資訊，請參閱特定的函數或結構。 這些選項通常會以一組可以合併的旗標形式傳遞。

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
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
