---
description: 深入瞭解： JET_RETRIEVECOLUMN 屬性
title: JET_RETRIEVECOLUMN 屬性
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c1e902b7e79111f3e9d9bf0160880d95c3957804de981fd56bbc36db5a9c3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107342"
---
# <a name="jet_retrievecolumn-properties"></a>JET_RETRIEVECOLUMN 屬性

包含受保護的成員  
包含繼承的成員  

[JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)類型會公開下列成員。

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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>取得抓取資料行作業抓取之資料的大小（以位元組為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>取得或設定 <a href="dn351040(v=exchg.10).md">pvData</a> 緩衝區的大小（以位元組為單位）。 抓取資料行作業將不會在 pvData 中儲存比 cbData 更多的資料。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>取得或設定要取得之資料行的資料行識別碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>藉由將0傳遞為 columnid，取得已標記、多重值或稀疏資料行的 columnid。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">犯 錯</a></td>
<td>取得從資料行抓取傳回的警告。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>取得或設定資料行抓取的選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>取得或設定資料將儲存在緩衝區中的位移。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>取得或設定要從 <a href="hh577895(v=exchg.10).md">LongBinary</a> 或 <a href="hh577895(v=exchg.10).md">LongText</a>類型的資料行中抓取之第一個位元組的位移。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>取得或設定包含在多值資料行中之值的序號。 如果 itagSequence 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>取得或設定將儲存從資料行取出之資料的緩衝區。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_RETRIEVECOLUMN 類別](./jet-retrievecolumn-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
