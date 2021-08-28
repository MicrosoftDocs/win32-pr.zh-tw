---
description: 驅動程式功能旗標。
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627994"
---
# <a name="d3denum"></a>D3DENUM

驅動程式功能旗標。



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#定義</td>
<td>值</td>
<td>描述</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Microsoft Windows 硬體品質實驗室 (的 WHQL) 驅動程式測試。 這是一項耗時的測試，需要一秒或兩秒的時間才會受到影響。 <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>的 WHQLLevel 成員會使用這個常數。<br/> 
<table>
<tbody>
<tr class="odd">
<td>Direct3D 9 與 Direct3D 9Ex 之間的差異：<br/> D3DENUM_WHQL_LEVEL 已被取代為在 Windows Vista、Windows Server 2008、Windows 7 和 Windows Server 2008 R2 (或更新的作業系統) 上執行的 Direct3D9Ex。 其中任何一個作業系統都會針對 WHQL 等級傳回1，而不會檢查驅動程式的狀態。 <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3d9。h     |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 常數](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




