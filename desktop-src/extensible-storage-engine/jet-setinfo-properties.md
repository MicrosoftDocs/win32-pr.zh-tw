---
description: 深入瞭解： JET_SETINFO 屬性
title: JET_SETINFO 屬性
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112532"
---
# <a name="jet_setinfo-properties"></a>JET_SETINFO 屬性

包含受保護的成員  
包含繼承的成員  

[JET_SETINFO](./jet-setinfo-class.md)類型會公開下列成員。

## <a name="properties"></a>屬性

<table>
<thead>
<tr class="header">
<th> </th>
<th>名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351064(v=exchg.10).md">ibLongValue</a></td>
<td>取得或設定要在 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中設定之第一個位元組的位移。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351037(v=exchg.10).md">itagSequence</a></td>
<td>取得或設定要設定之多重值資料行中的值順序。 值的陣列是以一為基礎。 第一個值是 sequence 1，而不是 0 (零) 。 如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。 值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_SETINFO 類別](./jet-setinfo-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
