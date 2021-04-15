---
description: 深入瞭解： JET_ENUMCOLUMNID 屬性
title: JET_ENUMCOLUMNID 屬性
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510938"
---
# <a name="jet_enumcolumnid-properties"></a>JET_ENUMCOLUMNID 屬性

包含受保護的成員  
包含繼承的成員  

[JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)類型會公開下列成員。

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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>取得或設定要列舉的 columnid 識別碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>取得或設定以一為基礎的索引) 所 (的資料行值計數，以列舉指定的資料行識別碼。 如果 ctagSequence 為 0 (零) 則會忽略 rgtagSequence，並且會列舉指定之資料行識別碼的所有資料行值。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>取得或設定指定資料行的資料行值陣列中，以一個為基底的索引陣列。 單一元素是 JET_RETRIEVECOLUMN 中定義的 itagSequence。 ItagSequence 0 (零) 表示 &quot; skip &quot; 。 1的 itagSequence 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_ENUMCOLUMNID 類別](./jet-enumcolumnid-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
