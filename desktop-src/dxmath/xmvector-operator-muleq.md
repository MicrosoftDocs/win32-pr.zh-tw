---
description: 乘法指派運算子。
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operator * = 運算子
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13280fd5da109012ac90ff55a778f8f5cd6a5b95
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627724"
---
# <a name="operator--operators"></a>operator \* = 運算子

乘法指派運算子

### <a name="overload-list"></a>多載清單



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >運算子</th>
<th >描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR：： operator * = (XMVECTOR&，float) </strong></a></td>
<td >將 <code>XMVECTOR</code> 實例乘以浮點值，並傳回更新的實例的參考。 <br/> 會將 <code>operator *=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件乘以指定的浮點值，並傳回更新的目前實例的參考。 <br/>
<blockquote>
[!Note]<br />
此運算子僅適用于 c + +。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td ><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR：： operator * = (XMVECTOR&，XMVECTOR) </strong></a></td>
<td >將一個 <code>XMVECTOR</code> 實例乘以第二個實例，並傳回已更新之初始實例的參考。 <br/> 會將 <code>operator *=</code> <a href="xmvector-data-type.md"><strong>XMVECTOR 資料類型</strong></a> 之目前實例的每個元件乘以第二個指定之實例中的對應元件 <code>XMVECTOR</code> ，並傳回已更新之初始實例的參考。 <br/>
<blockquote>
[!Note]<br />
此運算子僅適用于 c + +。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XMVECTOR 運算子](ovw-xmvector-operators.md)
</dt> <dt>

**參考**
</dt> <dt>

[**XMVECTOR 資料類型**](xmvector-data-type.md)
</dt> </dl>

 

 
