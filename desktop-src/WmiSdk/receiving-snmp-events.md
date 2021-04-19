---
description: SNMP 事件提供者支援 SNMPv1 陷阱和 SNMPv2 通知。
ms.assetid: 715b2925-b01d-4631-86e3-a6239ff1dba7
ms.tgt_platform: multiple
title: 接收 SNMP 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f718d2bcea85d0ee942050108f337f8ecb78e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980540"
---
# <a name="receiving-snmp-events"></a><span data-ttu-id="8c121-103">接收 SNMP 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-103">Receiving SNMP Events</span></span>

<span data-ttu-id="8c121-104">SNMP 事件提供者支援 SNMPv1 陷阱和 SNMPv2 通知。</span><span class="sxs-lookup"><span data-stu-id="8c121-104">The SNMP event providers support SNMPv1 traps and SNMPv2 notifications.</span></span>

<span data-ttu-id="8c121-105">支援下列三種類型的 SNMPv1 陷阱和 SNMPv2 通知：</span><span class="sxs-lookup"><span data-stu-id="8c121-105">The following three types of SNMPv1 traps and SNMPv2 notifications are supported:</span></span>

-   <span data-ttu-id="8c121-106">泛型</span><span class="sxs-lookup"><span data-stu-id="8c121-106">Generic</span></span>

    <span data-ttu-id="8c121-107">泛型陷阱和通知會對應到已命名的事件，例如連結和冷啟動。</span><span class="sxs-lookup"><span data-stu-id="8c121-107">Generic traps and notifications correspond to named events such as link up and cold start.</span></span> <span data-ttu-id="8c121-108">泛型陷阱和通知會以類別（例如 **SnmpLinkUpNotification** 和 **SnmpWarmStartExtendedNotification**）來表示，而這些類別會在類別名稱中包含陷阱的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c121-108">Generic traps and notifications are represented by classes, such as **SnmpLinkUpNotification** and **SnmpWarmStartExtendedNotification**, that contain the name of the trap in the class name.</span></span> <span data-ttu-id="8c121-109">這些類別是 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)的子類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-109">These classes are subclasses of [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span>

-   <span data-ttu-id="8c121-110">企業專用</span><span class="sxs-lookup"><span data-stu-id="8c121-110">Enterprise-specific</span></span>

    <span data-ttu-id="8c121-111">企業特定的陷阱和通知會對應至 WMI 類別所代表的事件，而該 WMI 類別不是 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md)的子類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-111">Enterprise specific traps and notifications correspond to events that are represented by a WMI class that is not a subclass of [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="8c121-112">若要支援企業特定的陷阱和通知，取用者必須藉由使用 SNMP MIB 編譯器編譯 MIB 定義來定義類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-112">To support enterprise specific traps and notifications, a consumer must define classes by compiling MIB definitions using the SNMP MIB compiler.</span></span>

-   <span data-ttu-id="8c121-113">企業-非特定</span><span class="sxs-lookup"><span data-stu-id="8c121-113">Enterprise-nonspecific</span></span>

    <span data-ttu-id="8c121-114">Nonenterprise 特定的陷阱和通知不會對應到任何一般事件種類或企業特定的事件種類。</span><span class="sxs-lookup"><span data-stu-id="8c121-114">Nonenterprise-specific traps and notifications do not correspond to any of the generic event types or enterprise-specific event types.</span></span> <span data-ttu-id="8c121-115">Nonenterprise 特定的陷阱和通知未將其 MIB 定義編譯成 SMIR。</span><span class="sxs-lookup"><span data-stu-id="8c121-115">Nonenterprise-specific traps and notifications have not had their MIB definitions compiled into the SMIR.</span></span> <span data-ttu-id="8c121-116">它們是由衍生自 SnmpNotification 和 [SnmpExtendedNotification](snmpextendednotification.md)的 [SnmpNotification](snmpnotification.md)、 **SnmpV2Notification**、 **SnmpV1ExtendedNotification** 和 **SnmpV2ExtendedNotification** 類別表示。</span><span class="sxs-lookup"><span data-stu-id="8c121-116">They are represented by the [SnmpNotification](snmpnotification.md), **SnmpV2Notification**, **SnmpV1ExtendedNotification**, and **SnmpV2ExtendedNotification** classes derived from SnmpNotification and [SnmpExtendedNotification](snmpextendednotification.md).</span></span>

> [!Note]  
> <span data-ttu-id="8c121-117">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="8c121-117">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="8c121-118">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="8c121-118">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="8c121-119">接收一般 SNMP 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-119">Receiving Generic SNMP Events</span></span>](#receiving-generic-snmp-events)
-   [<span data-ttu-id="8c121-120">接收 Enterprise-Specific 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-120">Receiving Enterprise-Specific Events</span></span>](#receiving-enterprise-specific-events)
-   [<span data-ttu-id="8c121-121">接收 Enterprise-Nonspecific 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-121">Receiving Enterprise-Nonspecific Events</span></span>](#receiving-enterprise-nonspecific-events)

## <a name="receiving-generic-snmp-events"></a><span data-ttu-id="8c121-122">接收一般 SNMP 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-122">Receiving Generic SNMP Events</span></span>

<span data-ttu-id="8c121-123">滲入和 SREP 支援所有類型的泛型 SNMPv1 陷阱和 SNMPv2 通知。</span><span class="sxs-lookup"><span data-stu-id="8c121-123">The SEEP and SREP support all types of generic SNMPv1 traps and SNMPv2 notifications.</span></span> <span data-ttu-id="8c121-124">一般 SNMP 事件是以 [SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md) 類別的子類別表示。</span><span class="sxs-lookup"><span data-stu-id="8c121-124">Generic SNMP events are represented by subclasses of the [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span>

<span data-ttu-id="8c121-125">每個事件種類都是以一個滲入類別和一個 SREP 類別來表示。</span><span class="sxs-lookup"><span data-stu-id="8c121-125">Each event type is represented by one SEEP class and one SREP class.</span></span> <span data-ttu-id="8c121-126">滲入類別衍生自 [SnmpNotification](snmpnotification.md);SREP 類別衍生自 [SnmpExtendedNotification](snmpextendednotification.md)。</span><span class="sxs-lookup"><span data-stu-id="8c121-126">The SEEP classes derive from [SnmpNotification](snmpnotification.md); the SREP classes derive from [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="8c121-127">事件提供者需要不同的類別，因為它們在 SNMP 事件資料的呈現方式中使用不同的機制。</span><span class="sxs-lookup"><span data-stu-id="8c121-127">The event providers require different classes because they use different mechanisms in the presentation of the SNMP event data.</span></span>

<span data-ttu-id="8c121-128">滲入會將 SNMP 事件資料直接轉換成 WMI 類別屬性，而 SREP 則不會。</span><span class="sxs-lookup"><span data-stu-id="8c121-128">The SEEP converts the SNMP event data directly to WMI class properties, whereas the SREP does not.</span></span> <span data-ttu-id="8c121-129">SREP 會將間接取值層級新增至使用 WMI 屬性所需的解讀。</span><span class="sxs-lookup"><span data-stu-id="8c121-129">The SREP adds a level of indirection to the interpretation required to use the WMI properties.</span></span> <span data-ttu-id="8c121-130">SREP [SnmpExtendedNotification](snmpextendednotification.md) 子類別的屬性是 SNMP 類別的實例;滲入 [SnmpNotification](snmpnotification.md) 子類別的屬性是整數和字串。</span><span class="sxs-lookup"><span data-stu-id="8c121-130">The properties of the SREP [SnmpExtendedNotification](snmpextendednotification.md) subclasses are instances of SNMP classes; the properties of the SEEP [SnmpNotification](snmpnotification.md) subclasses are integers and strings.</span></span>

<span data-ttu-id="8c121-131">下表列出一般 SNMP 事件和相關事件類別的類型。</span><span class="sxs-lookup"><span data-stu-id="8c121-131">The following table lists the types of generic SNMP events and the associated event classes.</span></span>



| <span data-ttu-id="8c121-132">簡易網路管理通訊協定 (SNMP) 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-132">SNMP event</span></span>                                    | <span data-ttu-id="8c121-133">滲入類別</span><span class="sxs-lookup"><span data-stu-id="8c121-133">SEEP class</span></span>                                | <span data-ttu-id="8c121-134">SREP 類別</span><span class="sxs-lookup"><span data-stu-id="8c121-134">SREP class</span></span>                                        |
|-----------------------------------------------|-------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="8c121-135">驗證失敗</span><span class="sxs-lookup"><span data-stu-id="8c121-135">Authentication failure</span></span>                        | <span data-ttu-id="8c121-136">**SnmpAuthenticationFailureNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-136">**SnmpAuthenticationFailureNotification**</span></span> | <span data-ttu-id="8c121-137">**SnmpAuthenticationFailureExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-137">**SnmpAuthenticationFailureExtendedNotification**</span></span> |
| <span data-ttu-id="8c121-138">外部閘道協定 (EGP) 鄰居遺失</span><span class="sxs-lookup"><span data-stu-id="8c121-138">Exterior Gateway Protocol (EGP) neighbor loss</span></span> | <span data-ttu-id="8c121-139">**SnmpEGPNeighborLossNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-139">**SnmpEGPNeighborLossNotification**</span></span>       | <span data-ttu-id="8c121-140">**SnmpEGPNeighborLossExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-140">**SnmpEGPNeighborLossExtendedNotification**</span></span>       |
| <span data-ttu-id="8c121-141">冷啟動</span><span class="sxs-lookup"><span data-stu-id="8c121-141">Cold start</span></span>                                    | <span data-ttu-id="8c121-142">**SnmpColdStartNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-142">**SnmpColdStartNotification**</span></span>             | <span data-ttu-id="8c121-143">**SnmpColdStartExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-143">**SnmpColdStartExtendedNotification**</span></span>             |
| <span data-ttu-id="8c121-144">暖開機</span><span class="sxs-lookup"><span data-stu-id="8c121-144">Warm start</span></span>                                    | <span data-ttu-id="8c121-145">**SnmpWarmStartNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-145">**SnmpWarmStartNotification**</span></span>             | <span data-ttu-id="8c121-146">**SnmpWarmStartExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-146">**SnmpWarmStartExtendedNotification**</span></span>             |
| <span data-ttu-id="8c121-147">連結</span><span class="sxs-lookup"><span data-stu-id="8c121-147">Link up</span></span>                                       | <span data-ttu-id="8c121-148">**SnmpLinkUpNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-148">**SnmpLinkUpNotification**</span></span>                | <span data-ttu-id="8c121-149">**SnmpLinkUpExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-149">**SnmpLinkUpExtendedNotification**</span></span>                |
| <span data-ttu-id="8c121-150">連結下移</span><span class="sxs-lookup"><span data-stu-id="8c121-150">Link down</span></span>                                     | <span data-ttu-id="8c121-151">**SnmpLinkDownNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-151">**SnmpLinkDownNotification**</span></span>              | <span data-ttu-id="8c121-152">**SnmpLinkDownExtendedNotification**</span><span class="sxs-lookup"><span data-stu-id="8c121-152">**SnmpLinkDownExtendedNotification**</span></span>              |



 

<span data-ttu-id="8c121-153">例如， **SnmpLinkUpNotification** 和 **SnmpLinkUpExtendedNotification** 類別會描述連結事件。</span><span class="sxs-lookup"><span data-stu-id="8c121-153">For example, the **SnmpLinkUpNotification** and **SnmpLinkUpExtendedNotification** classes describe the link-up event.</span></span> <span data-ttu-id="8c121-154">這兩個類別都包含 **ifIndex**、 **ifAdminStatus** 和 **ifOperStatus** 屬性，但它們的類型非常不同。</span><span class="sxs-lookup"><span data-stu-id="8c121-154">Both classes include the **ifIndex**, **ifAdminStatus**, and **ifOperStatus** properties, but they have very different types.</span></span> <span data-ttu-id="8c121-155">**SnmpLinkUpNotification** 類別中的屬性是 SINT32 和 STRING 類型。</span><span class="sxs-lookup"><span data-stu-id="8c121-155">The properties in the **SnmpLinkUpNotification** class are of type SINT32 and STRING.</span></span> <span data-ttu-id="8c121-156">**SnmpLinkUpExtendedNotification** 類別中的屬性是內嵌物件類型 IETF \_ SNMP \_ RFC1213 \_ MIB \_ ifTable。</span><span class="sxs-lookup"><span data-stu-id="8c121-156">The properties in the **SnmpLinkUpExtendedNotification** class are the embedded object type IETF\_SNMP\_RFC1213\_MIB\_ifTable.</span></span>

## <a name="receiving-enterprise-specific-events"></a><span data-ttu-id="8c121-157">接收 Enterprise-Specific 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-157">Receiving Enterprise-Specific Events</span></span>

<span data-ttu-id="8c121-158">滲入和 SREP 支援您已編譯到 SMIR 中的任何企業特定陷阱和通知。</span><span class="sxs-lookup"><span data-stu-id="8c121-158">The SEEP and SREP support any enterprise-specific traps and notifications that you have compiled into the SMIR.</span></span>

<span data-ttu-id="8c121-159">下列程式描述如何接收企業特定的事件。</span><span class="sxs-lookup"><span data-stu-id="8c121-159">The following procedure describes how to receive enterprise-specific events.</span></span>

<span data-ttu-id="8c121-160">**接收企業特定事件**</span><span class="sxs-lookup"><span data-stu-id="8c121-160">**To receive enterprise-specific events**</span></span>

1.  <span data-ttu-id="8c121-161">從負責產生事件的裝置編譯 MIB 定義。</span><span class="sxs-lookup"><span data-stu-id="8c121-161">Compile the MIB definitions from the device responsible for generating the event.</span></span>

    <span data-ttu-id="8c121-162">您可以使用 SNMP MIB 編譯器編譯 MIB 定義。</span><span class="sxs-lookup"><span data-stu-id="8c121-162">You can compile the MIB definitions using the SNMP MIB compiler.</span></span> <span data-ttu-id="8c121-163">如需詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="8c121-163">For more information, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

2.  <span data-ttu-id="8c121-164">決定您想要對應至事件的類別類型。</span><span class="sxs-lookup"><span data-stu-id="8c121-164">Determine what types of classes you want mapping to the events.</span></span>

    <span data-ttu-id="8c121-165">當您針對企業特定事件編譯 MIB 定義時，您可以決定編譯器所產生的類別類型。</span><span class="sxs-lookup"><span data-stu-id="8c121-165">When you compile the MIB definition for an enterprise-specific event, you can determine what type of class the compiler generates.</span></span> <span data-ttu-id="8c121-166">具體來說，您可以指示編譯器建立下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="8c121-166">Specifically, you can instruct the compiler to create one of the following choices:</span></span>

    -   <span data-ttu-id="8c121-167">從定義[SnmpNotification](snmpnotification.md)子類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-167">[SnmpNotification](snmpnotification.md) subclasses from the definitions.</span></span>
    -   <span data-ttu-id="8c121-168">從定義[SnmpExtendedNotification](snmpextendednotification.md)子類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-168">[SnmpExtendedNotification](snmpextendednotification.md) subclasses from the definitions.</span></span>
    -   <span data-ttu-id="8c121-169">[SnmpNotification](snmpnotification.md) 和 [SnmpExtendedNotification](snmpextendednotification.md) 定義中的子類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-169">[SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md) subclasses from the definitions.</span></span>

    <span data-ttu-id="8c121-170">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="8c121-170">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="8c121-171">如果 SNMP 事件提供者收到沒有類別的特定陷阱或通知，則提供者會產生 nonenterprise 特定的事件。</span><span class="sxs-lookup"><span data-stu-id="8c121-171">If the SNMP event providers receive a specific trap or notification for which there is no class, the providers generate an nonenterprise-specific event.</span></span> <span data-ttu-id="8c121-172">如需詳細資訊，請參閱 [接收企業非特定事件](#receiving-enterprise-nonspecific-events)。</span><span class="sxs-lookup"><span data-stu-id="8c121-172">For more information, see [Receiving Enterprise Nonspecific Events](#receiving-enterprise-nonspecific-events).</span></span>

## <a name="receiving-enterprise-nonspecific-events"></a><span data-ttu-id="8c121-173">接收 Enterprise-Nonspecific 事件</span><span class="sxs-lookup"><span data-stu-id="8c121-173">Receiving Enterprise-Nonspecific Events</span></span>

<span data-ttu-id="8c121-174">企業非明確事件是指不會將 SNMPv1 陷阱或 SNMPv2 通知對應到 [SnmpNotification](snmpnotification.md) 或 [SnmpExtendedNotification](snmpextendednotification.md) 的任何子類別或代表企業事件的任何類別的事件。</span><span class="sxs-lookup"><span data-stu-id="8c121-174">An enterprise-nonspecific event is an event that does not map from an SNMPv1 trap or SNMPv2 notification to any of the subclasses of [SnmpNotification](snmpnotification.md) or [SnmpExtendedNotification](snmpextendednotification.md) or any class that represents an enterprise event.</span></span>

<span data-ttu-id="8c121-175">滲入會針對未明確的事件使用 **SNMPV1Notification** 或 **SNMPV2Notification** 類別，而 SREP 會使用 **SNMPv1ExtendedNotification** 和 **SNMPV2ExtendedNotification** 類別。</span><span class="sxs-lookup"><span data-stu-id="8c121-175">SEEP uses the **SNMPV1Notification** or **SNMPV2Notification** classes for nonspecific events, whereas SREP uses the **SNMPv1ExtendedNotification** and **SNMPV2ExtendedNotification** classes.</span></span>

<span data-ttu-id="8c121-176">所有四個企業明確的類別都衍生自 [SnmpNotification](snmpnotification.md) 或 [SnmpExtendedNotification](snmpextendednotification.md) 類別，而且具有相同的格式。</span><span class="sxs-lookup"><span data-stu-id="8c121-176">All four enterprise-nonspecific classes derive from either the [SnmpNotification](snmpnotification.md) or [SnmpExtendedNotification](snmpextendednotification.md) classes, and have the same format.</span></span> <span data-ttu-id="8c121-177">這兩個類別都具有單一屬性 **VarBindList**。</span><span class="sxs-lookup"><span data-stu-id="8c121-177">Both classes have the single property **VarBindList**.</span></span> <span data-ttu-id="8c121-178">**VarBindList** 是 **SnmpVarBind** 類別的實例陣列。</span><span class="sxs-lookup"><span data-stu-id="8c121-178">**VarBindList** is an array of instances of the **SnmpVarBind** class.</span></span> <span data-ttu-id="8c121-179">**SnmpVarBind** 是 snmp 事件提供者所支援的基類，用以代表 snmp 變數系結的實例。</span><span class="sxs-lookup"><span data-stu-id="8c121-179">**SnmpVarBind** is a base class supported by the SNMP event providers to represent an instance of an SNMP variable binding.</span></span> <span data-ttu-id="8c121-180">下表列出 **SnmpVarBind** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="8c121-180">The following table lists the properties of **SnmpVarBind**.</span></span>



| <span data-ttu-id="8c121-181">屬性</span><span class="sxs-lookup"><span data-stu-id="8c121-181">Property</span></span>         | <span data-ttu-id="8c121-182">描述</span><span class="sxs-lookup"><span data-stu-id="8c121-182">Description</span></span>                                                                                                    |
|------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c121-183">編碼</span><span class="sxs-lookup"><span data-stu-id="8c121-183">Encoding</span></span>         | <span data-ttu-id="8c121-184">字串，指出 **值** 屬性中變數的抽象語法標記法 (一)  (asn.1) 類型。</span><span class="sxs-lookup"><span data-stu-id="8c121-184">String that indicates the Abstract Syntax Notation One (ASN.1) type of the variable in the **Value** property.</span></span> |
| <span data-ttu-id="8c121-185">ObjectIdentifier</span><span class="sxs-lookup"><span data-stu-id="8c121-185">ObjectIdentifier</span></span> | <span data-ttu-id="8c121-186">在 **Value** 屬性中識別變數的字串。</span><span class="sxs-lookup"><span data-stu-id="8c121-186">String that identifies the variable in the **Value** property.</span></span>                                                 |
| <span data-ttu-id="8c121-187">值</span><span class="sxs-lookup"><span data-stu-id="8c121-187">Value</span></span>            | <span data-ttu-id="8c121-188">位元組中的原始資料。</span><span class="sxs-lookup"><span data-stu-id="8c121-188">Raw data in octets.</span></span>                                                                                            |



 

<span data-ttu-id="8c121-189">在 **SnmpV1Notification** 和 **SnmpV2Notification** 類別中，除了前兩個變數系結（TimeStamp 和 SnmpTrapOID）之外，已保留 SNMP 事件的變數系結順序。</span><span class="sxs-lookup"><span data-stu-id="8c121-189">In the **SnmpV1Notification** and **SnmpV2Notification** classes, the variable binding order from the SNMP event has been preserved except for the first two variable bindings, TimeStamp and SnmpTrapOID.</span></span> <span data-ttu-id="8c121-190">這些系結已移除，並儲存在 [SnmpNotification](snmpnotification.md)或 [SnmpExtendedNotification](snmpextendednotification.md)父類別的 **TimeStamp** 和 **id** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="8c121-190">These bindings have been removed and are stored in the **TimeStamp** and **Identification** properties of the [SnmpNotification](snmpnotification.md) or [SnmpExtendedNotification](snmpextendednotification.md) parent class.</span></span>

 

 



