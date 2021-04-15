---
title: 判斷與物件實例相關聯的類別
description: Active Directory Domain Services 中的每個物件都有兩個屬性，其值可識別物件為其實例的物件類別階層架構。
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462052"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="8ba38-103">判斷與物件實例相關聯的類別</span><span class="sxs-lookup"><span data-stu-id="8ba38-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="8ba38-104">Active Directory Domain Services 中的每個物件都有兩個屬性，其值可識別物件為其實例的物件類別階層架構。</span><span class="sxs-lookup"><span data-stu-id="8ba38-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ba38-105">屬性</span><span class="sxs-lookup"><span data-stu-id="8ba38-105">Attribute</span></span></th>
<th><span data-ttu-id="8ba38-106">描述</span><span class="sxs-lookup"><span data-stu-id="8ba38-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ba38-107"><strong>structuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="8ba38-108">識別物件為其實例的結構化和抽象類別。</span><span class="sxs-lookup"><span data-stu-id="8ba38-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="8ba38-109">例如，使用者物件的值可以是：</span><span class="sxs-lookup"><span data-stu-id="8ba38-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="8ba38-110"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="8ba38-111"><strong>人</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="8ba38-112"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="8ba38-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba38-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="8ba38-115">識別包含在 <strong>structuralObjectClass</strong>中的類別，再加上任何動態附加的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="8ba38-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="8ba38-116">例如，如果 &quot; 車輛 &quot; 輔助類別附加至使用者物件，則這些值可以是：</span><span class="sxs-lookup"><span data-stu-id="8ba38-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="8ba38-117"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="8ba38-118"><strong>車輛</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="8ba38-119"><strong>人</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="8ba38-120"><strong>organizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="8ba38-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="8ba38-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8ba38-122">請注意，這兩個屬性都不包括以靜態方式連結化物件為實例之物件類別的輔助類別。</span><span class="sxs-lookup"><span data-stu-id="8ba38-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="8ba38-123">例如， **securityPrincipal** 輔助類別會以靜態方式連結至 **使用者** 類別，因為它包含在使用者 **classSchema** 物件的 **systemAuxiliaryClass** 值中。它不會包含在 user 類別實例的 **objectClass** 或 **structuralObjectClass** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="8ba38-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




