---
description: WMI 會定義一組系統屬性，這些與類別和類別的實例相關聯，除了類別特有的屬性之外。
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: MIB 物件的 CIM 系統屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981611"
---
# <a name="cim-system-properties-for-mib-objects"></a>MIB 物件的 CIM 系統屬性

WMI 會定義一組系統屬性，這些與類別和類別的實例相關聯，除了類別特有的屬性之外。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 系統屬性。 SNMP 提供者必須要有必要的屬性，才能完全解析群組物件。 無法定義強制屬性會傳回錯誤。



<table>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>字串</strong>強制性<br/> 針對實例，此物件所屬的類別。 針對類別，這是類別名稱。<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>字串</strong>選<br/> 類別的名稱，這個類別是目前物件的最終基類 (不是它的直屬父類別) 。<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>uint32</strong>強制性<br/> 物件的類型。 值為：<br/> <dl> 1 = 類別<br />
2 = 實例<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>字串</strong>強制性<br/> 物件所在的命名空間。<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>字串</strong>強制性<br/> 物件的絕對路徑。<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>uint32</strong>強制性<br/> 為物件定義的非系統屬性數目。<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>字串</strong>強制性<br/> 物件的相對路徑。<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>字串</strong>強制性<br/> 提供物件的伺服器。<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>字串</strong>選<br/> 物件的直屬父類別。<br/></td>
</tr>
</tbody>
</table>



 

 

 




