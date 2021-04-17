---
description: 深入瞭解： JET_RETINFO 屬性
title: JET_RETINFO 屬性
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565416"
---
# <a name="jet_retinfo-properties"></a>JET_RETINFO 屬性

包含受保護的成員  
包含繼承的成員  

[JET_RETINFO](./jet-retinfo-class.md)類型會公開下列成員。

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
<td><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></td>
<td>藉由將0傳遞為 JetRetrieveColumn 的 columnid，來取得所有標記的資料行時，取得已標記、多重值或稀疏資料行的 columnid。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335220(v=exchg.10).md">ibLongValue</a></td>
<td>取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a>或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351035(v=exchg.10).md">itagSequence</a></td>
<td>取得或設定多重值資料行中值的序號。 值的陣列是以一為基礎。 第一個值是 sequence 1，不是0。 如果 [記錄] 資料行只有一個值，則應該以 itagSequence 的形式傳遞1。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETINFO 類別](./jet-retinfo-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
