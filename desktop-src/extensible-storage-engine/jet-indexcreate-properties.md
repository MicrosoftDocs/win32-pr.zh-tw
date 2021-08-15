---
description: 深入瞭解： JET_INDEXCREATE 屬性
title: JET_INDEXCREATE 屬性
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0669d00b9c28e5299c5b9f55f0931ec7d22921eddad5e2b6b4876199057d111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254265"
---
# <a name="jet_indexcreate-properties"></a>JET_INDEXCREATE 屬性

包含受保護的成員  
包含繼承的成員  

[JET_INDEXCREATE](./jet-indexcreate-class.md)類型會公開下列成員。

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>取得或設定 szKey 的長度（以字元為單位），包括兩個終止的 null。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>取得或設定索引中索引鍵允許的大小上限（以位元組為單位）。 最小支援的金鑰大小為 JET_cbKeyMostMin (255) 這是舊版的最大金鑰大小。 最大索引鍵大小取決於資料庫頁面大小 <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>。 您可以使用 <a href="dn351156(v=exchg.10).md">KeyMost</a>抓取最大的索引鍵大小。 Windows XP 和 Windows Server 2003 會忽略此參數。 不同于非受控 API，不需要 <strong>IndexKeyMost () </strong> (JET_bitIndexKeyMost) ，它會自動加入。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>取得或設定要儲存在索引中之每個資料行的最大長度（以位元組為單位）。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>取得或設定條件式資料行的數目。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">犯 錯</a></td>
<td>取得或設定建立此索引的錯誤碼。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>取得或設定索引建立選項。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>取得或設定選擇性的 unicode 比較選項。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>取得或設定空間配置、維護和使用方式提示。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>取得或設定選擇性的條件式資料行。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>取得或設定要建立之索引的名稱。</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>取得或設定索引鍵的描述。 這是以 null 分隔之標記的雙 null 結束字串。 每個標記的格式都是 [方向規範] [資料行名稱]，其中的方向規格為 &quot; + &quot; 或 &quot; - &quot; 。 例如， &quot; + abc\0-def\0 + ghi\0 的 szKey 會以 &quot; 遞增順序)  (的三個數據行來編制索引 &quot; &quot; ， &quot; &quot; 而 def (以遞減順序) 和 &quot; ghi &quot; (遞增順序) 。</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="公用屬性" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>取得或設定索引的密度。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_INDEXCREATE 類別](./jet-indexcreate-class.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
