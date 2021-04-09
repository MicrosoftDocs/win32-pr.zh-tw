---
description: 深入瞭解： Server2003Grbits 成員
title: Server2003Grbits 成員 (Server2003) 的成員
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849538"
---
# <a name="server2003grbits-members"></a>Server2003Grbits 成員

包含受保護的成員  
包含繼承的成員  

已新增至 Windows Server 2003 版 ESENT 的 Grbits。

[Server2003Grbits](./server2003grbits-class.md)類型會公開下列成員。

## <a name="fields"></a>欄位

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
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。 此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>如果臨時表管理員可以使用針對中繼查詢結果優化的執行，此選項會要求只建立臨時表。 如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。 此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。 如需詳細資訊，請參閱 <a href="hh558517(v=exchg.10).md">唯一</a> 的。</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="公用欄位" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="靜態成員" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>所有先前由尚未排清至交易記錄檔的會話所認可的交易，都會立即進行清除。 此 API 會等到交易已排清之後，再返回呼叫端。 即使會話目前不在交易中，也可以使用此選項。 此選項不能與任何其他選項搭配使用。</td>
</tr>
</tbody>
</table>


頁首

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Server2003Grbits 類別](./server2003grbits-class.md)

[Server2003 命名空間。](./microsoft.isam.esent.interop.server2003-namespace.md)
