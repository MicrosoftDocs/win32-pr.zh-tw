---
description: 通知類型宏包含下列元素。
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: 通知類型宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979747"
---
# <a name="notification-type-macro"></a><span data-ttu-id="d52cf-103">通知類型宏</span><span class="sxs-lookup"><span data-stu-id="d52cf-103">NOTIFICATION-TYPE Macro</span></span>

<span data-ttu-id="d52cf-104">通知類型宏包含下列元素。</span><span class="sxs-lookup"><span data-stu-id="d52cf-104">The NOTIFICATION-TYPE macro contains the following elements.</span></span>

> [!Note]  
> <span data-ttu-id="d52cf-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="d52cf-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="d52cf-106">單元</span><span class="sxs-lookup"><span data-stu-id="d52cf-106">Components</span></span>

<dl> <dt>

<span data-ttu-id="d52cf-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>物件描述元</span><span class="sxs-lookup"><span data-stu-id="d52cf-107"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="d52cf-108">將名稱附加至通知類型宏中的 SNMP 事件。</span><span class="sxs-lookup"><span data-stu-id="d52cf-108">Attaches a name to an SNMP event in a NOTIFICATION-TYPE macro.</span></span> <span data-ttu-id="d52cf-109">下列清單列出對應物件描述項的規則。</span><span class="sxs-lookup"><span data-stu-id="d52cf-109">The following list lists the rules for mapping the object descriptor.</span></span>



| <span data-ttu-id="d52cf-110">類型</span><span class="sxs-lookup"><span data-stu-id="d52cf-110">Type</span></span>                        | <span data-ttu-id="d52cf-111">Concatenate</span><span class="sxs-lookup"><span data-stu-id="d52cf-111">Concatenate</span></span>                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52cf-112">封裝的 CIM 類別名稱</span><span class="sxs-lookup"><span data-stu-id="d52cf-112">Encapsulated CIM class name</span></span> | <span data-ttu-id="d52cf-113">「SNMP \_ 」</span><span class="sxs-lookup"><span data-stu-id="d52cf-113">"SNMP\_"</span></span><br/> <span data-ttu-id="d52cf-114">MIB 模組身分識別名稱</span><span class="sxs-lookup"><span data-stu-id="d52cf-114">MIB module identity name</span></span><br/> <span data-ttu-id="d52cf-115">底線 (\_) </span><span class="sxs-lookup"><span data-stu-id="d52cf-115">underscore (\_)</span></span><br/> <span data-ttu-id="d52cf-116">物件描述元</span><span class="sxs-lookup"><span data-stu-id="d52cf-116">object descriptor</span></span><br/> <span data-ttu-id="d52cf-117">「 \_ 通知」</span><span class="sxs-lookup"><span data-stu-id="d52cf-117">"\_Notification"</span></span><br/> <span data-ttu-id="d52cf-118">範例：來自 **CISCO-VTP-MIB** 的 **vtpServerDisabled** 通知會對應到 **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ 通知**。</span><span class="sxs-lookup"><span data-stu-id="d52cf-118">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_Notification**.</span></span><br/>                 |
| <span data-ttu-id="d52cf-119">引用 CIM 類別名稱</span><span class="sxs-lookup"><span data-stu-id="d52cf-119">Referent CIM class name</span></span>     | <span data-ttu-id="d52cf-120">「SNMP \_ 」</span><span class="sxs-lookup"><span data-stu-id="d52cf-120">"SNMP\_"</span></span><br/> <span data-ttu-id="d52cf-121">MIB 模組身分識別名稱</span><span class="sxs-lookup"><span data-stu-id="d52cf-121">MIB module identity name</span></span><br/> <span data-ttu-id="d52cf-122">底線 (\_) </span><span class="sxs-lookup"><span data-stu-id="d52cf-122">underscore (\_)</span></span><br/> <span data-ttu-id="d52cf-123">物件描述元</span><span class="sxs-lookup"><span data-stu-id="d52cf-123">object descriptor</span></span><br/> <span data-ttu-id="d52cf-124">" \_ ExtendedNotification"</span><span class="sxs-lookup"><span data-stu-id="d52cf-124">"\_ExtendedNotification"</span></span><br/> <span data-ttu-id="d52cf-125">範例：來自 **CISCO-VTP-MIB** 的 **vtpServerDisabled** 通知會對應到 **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**。</span><span class="sxs-lookup"><span data-stu-id="d52cf-125">Example: The **vtpServerDisabled** notification from the **CISCO-VTP-MIB** maps to **SNMP\_CISCO\_VTP\_MIB\_vtpServerDisabled\_ExtendedNotification**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d52cf-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS 子句</span><span class="sxs-lookup"><span data-stu-id="d52cf-126"><span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS clause</span></span>
</dt> <dd>

<span data-ttu-id="d52cf-127">列舉與通知物件相關聯的物件集合。</span><span class="sxs-lookup"><span data-stu-id="d52cf-127">Enumerates the set of objects associated with the notification object.</span></span>

</dd> <dt>

<span data-ttu-id="d52cf-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE 子句</span><span class="sxs-lookup"><span data-stu-id="d52cf-128"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="d52cf-129">指的是包含物件之詳細資訊的另一份檔。</span><span class="sxs-lookup"><span data-stu-id="d52cf-129">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="d52cf-130">它會對應到 CIM 類別限定詞 **參考**，它是字串類型。</span><span class="sxs-lookup"><span data-stu-id="d52cf-130">It maps to the CIM class qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="d52cf-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION 子句</span><span class="sxs-lookup"><span data-stu-id="d52cf-131"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="d52cf-132">描述有問題的物件。</span><span class="sxs-lookup"><span data-stu-id="d52cf-132">Describes the object in question.</span></span> <span data-ttu-id="d52cf-133">它會對應至 CIM 類別限定詞 **描述**，其為字串類型</span><span class="sxs-lookup"><span data-stu-id="d52cf-133">It maps to the CIM class qualifier **Description**, which is of type string</span></span>

</dd> <dt>

<span data-ttu-id="d52cf-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS 子句</span><span class="sxs-lookup"><span data-stu-id="d52cf-134"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="d52cf-135">指出是否必須支援此物件。</span><span class="sxs-lookup"><span data-stu-id="d52cf-135">Indicates whether the object must be supported.</span></span> <span data-ttu-id="d52cf-136">當狀態為「已 **淘汰** 」 **或「已淘汰」** 時，會從對應中捨棄通知。</span><span class="sxs-lookup"><span data-stu-id="d52cf-136">When the status is either **obsolete** or **deprecated**, the notification is discarded from the mapping.</span></span> <span data-ttu-id="d52cf-137">否則，此子句會對應到 CIM 類別限定詞 **狀態**，其為 **字串** 類型。</span><span class="sxs-lookup"><span data-stu-id="d52cf-137">Otherwise, this clause maps to the CIM class qualifier **Status**, which is of type **string**.</span></span>

<span data-ttu-id="d52cf-138">針對 SNMPv1，[ **狀態** ] 的慣用值是 [ **強制** ] 或 [ **選擇性**]，但辨識符號可以包含其他一些值。</span><span class="sxs-lookup"><span data-stu-id="d52cf-138">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="d52cf-139">若為 SNMPv2C，則 [ **狀態** ] 的慣用值為 [ **目前** ] 或 [已 **淘汰**]，但辨識符號可以包含其他一些值。</span><span class="sxs-lookup"><span data-stu-id="d52cf-139">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d52cf-140">備註</span><span class="sxs-lookup"><span data-stu-id="d52cf-140">Remarks</span></span>

<span data-ttu-id="d52cf-141">SNMP 提供者會將 **通知類型** 宏對應至已封裝或引用的類別定義。</span><span class="sxs-lookup"><span data-stu-id="d52cf-141">The SNMP provider maps the **NOTIFICATION-TYPE** macro to either an encapsulated or referent class definition.</span></span>

<span data-ttu-id="d52cf-142">封裝的類別定義不會公開與 MIB 物件相關聯的實例資訊。</span><span class="sxs-lookup"><span data-stu-id="d52cf-142">An encapsulated class definition does not expose the instance information associated with the MIB object.</span></span> <span data-ttu-id="d52cf-143">相反地，類別定義會將 OBJECTS 子句編碼為 CIM 事件類別的一連串屬性。</span><span class="sxs-lookup"><span data-stu-id="d52cf-143">Instead, the class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="d52cf-144">每個 CIM 屬性都會反映 OBJECTS 子句中對應 MIB 物件的名稱、類型和值。</span><span class="sxs-lookup"><span data-stu-id="d52cf-144">Each CIM property reflects the name, type, and value of the corresponding MIB object in the OBJECTS clause.</span></span> <span data-ttu-id="d52cf-145">如果您需要實例資訊，則必須對應至引用類別。</span><span class="sxs-lookup"><span data-stu-id="d52cf-145">If you require instance information, you must map to a referent class.</span></span> <span data-ttu-id="d52cf-146">封裝的類別定義會對應至 [SnmpNotification](snmpnotification.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="d52cf-146">An encapsulated class definition maps to the [SnmpNotification](snmpnotification.md) class.</span></span>

<span data-ttu-id="d52cf-147">引用類別會定義 MIB 物件，以及用來取得物件的實例資訊。</span><span class="sxs-lookup"><span data-stu-id="d52cf-147">A referent class defines an MIB object and the instance information used to obtain the object.</span></span> <span data-ttu-id="d52cf-148">類別定義會將 OBJECTS 子句編碼為 CIM 事件類別的一連串屬性。</span><span class="sxs-lookup"><span data-stu-id="d52cf-148">The class definition encodes the OBJECTS clause as a series of properties of the CIM event class.</span></span> <span data-ttu-id="d52cf-149">每個 CIM 屬性都會反映 OBJECTS 子句中對應的 MIB 物件的名稱，而類型則會反映與該 MIB 物件相關聯之類別實例的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="d52cf-149">Each CIM property reflects the name of the corresponding MIB object in the OBJECTS clause and the type as an embedded object that reflects an instance of the class associated with that MIB object.</span></span> <span data-ttu-id="d52cf-150">然後，提供者會產生與 MIB 物件相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="d52cf-150">The provider then generates a class associated with the MIB object.</span></span> <span data-ttu-id="d52cf-151">例如， **ifIndex** 會對應到名為 **SNMP \_ RFC1213 \_ MIB \_ ifIndex** 的內嵌類別。</span><span class="sxs-lookup"><span data-stu-id="d52cf-151">For example, **ifIndex** maps to an embedded class named **SNMP\_RFC1213\_MIB\_ifIndex**.</span></span> <span data-ttu-id="d52cf-152">如需這種類別類別的詳細資訊，請參閱 [OBJECT Type 宏](object-type-macro.md)。</span><span class="sxs-lookup"><span data-stu-id="d52cf-152">For more information about this type of class, see [OBJECT-TYPE Macro](object-type-macro.md).</span></span>

 

 




