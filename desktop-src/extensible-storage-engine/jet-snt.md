---
description: 深入瞭解： JET_SNT
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191133"
---
# <a name="jet_snt"></a>JET_SNT


_**適用于：** Windows |Windows Server_

## <a name="jet_snt"></a>JET_SNT

[JET_SNT]()的常數群組描述作業的進度點，這是在呼叫[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函數時所要求的資訊。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常數/值</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_sntBegin<br />
5</p></td>
<td><p>作業的開頭</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>不支援。</p>
<p><strong>Windows 2000 伺服器：</strong>  作業已啟動。 在此情況下，回呼函式的最後一個參數應該是指向 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的有效指標，指出要執行的單位總數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>完成的單位數和尚未完成的單位數。 這項資訊會在 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的成員中傳回。</p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>作業完成。</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>作業失敗。</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>操作的復原控制。</p>
<div class="alert">

> [!NOTE]
> <P>此值不適用於從 Windows 8 開始的 Windows 作業系統版本。</P>


</div></td>
</tr>
</tbody>
</table>


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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
