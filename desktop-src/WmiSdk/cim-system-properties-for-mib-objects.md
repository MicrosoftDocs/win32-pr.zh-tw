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
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="ca7d4-103">MIB 物件的 CIM 系統屬性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="ca7d4-104">WMI 會定義一組系統屬性，這些與類別和類別的實例相關聯，除了類別特有的屬性之外。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="ca7d4-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="ca7d4-106">當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 系統屬性。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="ca7d4-107">SNMP 提供者必須要有必要的屬性，才能完全解析群組物件。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="ca7d4-108">無法定義強制屬性會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ca7d4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-109">Property</span></span></th>
<th><span data-ttu-id="ca7d4-110">描述</span><span class="sxs-lookup"><span data-stu-id="ca7d4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca7d4-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="ca7d4-112"><strong>字串</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-113">針對實例，此物件所屬的類別。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="ca7d4-114">針對類別，這是類別名稱。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca7d4-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="ca7d4-116"><strong>字串</strong>選</span><span class="sxs-lookup"><span data-stu-id="ca7d4-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="ca7d4-117">類別的名稱，這個類別是目前物件的最終基類 (不是它的直屬父類別) 。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca7d4-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="ca7d4-119"><strong>uint32</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-120">物件的類型。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-120">Type of object.</span></span> <span data-ttu-id="ca7d4-121">值為：</span><span class="sxs-lookup"><span data-stu-id="ca7d4-121">Values are:</span></span><br/> <dl> <span data-ttu-id="ca7d4-122">1 = 類別</span><span class="sxs-lookup"><span data-stu-id="ca7d4-122">1 = class</span></span><br />
<span data-ttu-id="ca7d4-123">2 = 實例</span><span class="sxs-lookup"><span data-stu-id="ca7d4-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca7d4-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="ca7d4-125"><strong>字串</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-126">物件所在的命名空間。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca7d4-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="ca7d4-128"><strong>字串</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-129">物件的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca7d4-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="ca7d4-131"><strong>uint32</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-132">為物件定義的非系統屬性數目。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca7d4-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="ca7d4-134"><strong>字串</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-135">物件的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca7d4-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="ca7d4-137"><strong>字串</strong>強制性</span><span class="sxs-lookup"><span data-stu-id="ca7d4-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="ca7d4-138">提供物件的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca7d4-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="ca7d4-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="ca7d4-140"><strong>字串</strong>選</span><span class="sxs-lookup"><span data-stu-id="ca7d4-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="ca7d4-141">物件的直屬父類別。</span><span class="sxs-lookup"><span data-stu-id="ca7d4-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




