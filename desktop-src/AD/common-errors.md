---
title: '常見的錯誤 (AD DS) '
description: 下表包含的常見錯誤清單，可能會根據所要嵌套之群組的範圍而發生。
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- 常見的錯誤廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/11/2019
ms.locfileid: "104462676"
---
# <a name="common-errors-ad-ds"></a>常見的錯誤 (AD DS) 

下表包含的常見錯誤清單，可能會根據所要嵌套之群組的範圍而發生。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001F</td>
<td>一般失敗。 如果您嘗試進行下列動作，就會發生此錯誤：
<ul>
<li>將網域本機群組新增至全域或萬用群組或另一個網域中的網域本機群組。 您只能將網域本機群組新增為相同網域中其他網域本機群組的成員。</li>
<li>將萬用群組新增至全域群組。 萬用群組可以新增至通用和網網域本機群組，但不能新增至全域群組。</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202F</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>。 如果您嘗試將安全性群組新增至以混合模式執行之網域中的另一個群組，就會發生此錯誤。 安全性群組無法以混合模式來嵌套;安全性群組只能以原生模式進行嵌套。</td>
</tr>
</tbody>
</table>



 

 

 




