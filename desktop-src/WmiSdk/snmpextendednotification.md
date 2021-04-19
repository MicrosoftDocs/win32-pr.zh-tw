---
description: SnmpExtendedNotification 類別是 SNMP 提供者從通知類型宏對應到 CIM 類別之任何類別的基類。
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981490"
---
# <a name="snmpextendednotification-class"></a><span data-ttu-id="53e2c-103">SnmpExtendedNotification 類別</span><span class="sxs-lookup"><span data-stu-id="53e2c-103">SnmpExtendedNotification class</span></span>

<span data-ttu-id="53e2c-104">**SnmpExtendedNotification** 類別是 [SNMP 提供者](snmp-provider.md)從 [通知類型](notification-type-macro.md)宏對應到 CIM 類別之任何類別的基類。</span><span class="sxs-lookup"><span data-stu-id="53e2c-104">The **SnmpExtendedNotification** class is the base class for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to a CIM class by the [SNMP Provider](snmp-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="53e2c-105">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="53e2c-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="53e2c-106">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="53e2c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="53e2c-107">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="53e2c-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e2c-108">語法</span><span class="sxs-lookup"><span data-stu-id="53e2c-108">Syntax</span></span>

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="53e2c-109">成員</span><span class="sxs-lookup"><span data-stu-id="53e2c-109">Members</span></span>

<span data-ttu-id="53e2c-110">**SnmpExtendedNotification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="53e2c-110">The **SnmpExtendedNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="53e2c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="53e2c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53e2c-112">屬性</span><span class="sxs-lookup"><span data-stu-id="53e2c-112">Properties</span></span>

<span data-ttu-id="53e2c-113">**SnmpExtendedNotification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="53e2c-113">The **SnmpExtendedNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53e2c-114">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="53e2c-114">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-117">建立通知之實體的網路位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-117">Network address of the entity that created the notification.</span></span> <span data-ttu-id="53e2c-118">這是裝置的實際位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-118">This is the actual address of the device.</span></span> <span data-ttu-id="53e2c-119">當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-119">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="53e2c-120">當管理實體使用 SNMP over IPX 時，傳輸位址會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="53e2c-120">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="53e2c-121">這個屬性僅適用于 SNMPv1。</span><span class="sxs-lookup"><span data-stu-id="53e2c-121">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-122">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="53e2c-122">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-125">傳送實體所使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="53e2c-125">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="53e2c-126">這個屬性對 SNMPv1 和 SNMPv2C 有效。</span><span class="sxs-lookup"><span data-stu-id="53e2c-126">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-127">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="53e2c-127">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-130">傳送通知之實體的網路位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-130">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="53e2c-131">這是轉送通知的最後一個實體的位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-131">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="53e2c-132">當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-132">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="53e2c-133">當管理實體將 SNMP 用於 IPX 時，傳輸位址會參考 IPX 位址。</span><span class="sxs-lookup"><span data-stu-id="53e2c-133">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="53e2c-134">這個屬性對 SNMPv1 和 SNMPv2C 有效。</span><span class="sxs-lookup"><span data-stu-id="53e2c-134">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-135">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="53e2c-135">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-138">傳送實體所使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="53e2c-138">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-139">**社群**</span><span class="sxs-lookup"><span data-stu-id="53e2c-139">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-142">與 PDU 實例相關聯的群體名稱。</span><span class="sxs-lookup"><span data-stu-id="53e2c-142">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="53e2c-143">群體名稱會驗證 PDU 的建立者。</span><span class="sxs-lookup"><span data-stu-id="53e2c-143">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="53e2c-144">這個屬性對 SNMPv1 和 SNMPv2C 都有效。</span><span class="sxs-lookup"><span data-stu-id="53e2c-144">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-145">**識別**</span><span class="sxs-lookup"><span data-stu-id="53e2c-145">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-148">限定詞： **文字 \_ 慣例** ( "OBJECTIDENTIFIER" ) ， **編碼** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 語法** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 識別碼** ( "1.3.6.1.6.3.1.1.4.1" ) </span><span class="sxs-lookup"><span data-stu-id="53e2c-148">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-149">此通知的授權識別。</span><span class="sxs-lookup"><span data-stu-id="53e2c-149">Authoritative identification of this notification.</span></span> <span data-ttu-id="53e2c-150">直接對應到 MIB 專案 SnmpTrapOID 變數系結。</span><span class="sxs-lookup"><span data-stu-id="53e2c-150">Maps directly to the MIB entry SnmpTrapOID variable binding.</span></span> <span data-ttu-id="53e2c-151">這個屬性僅適用于 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="53e2c-151">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-152">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="53e2c-152">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-153">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="53e2c-153">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-155">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="53e2c-155">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="53e2c-156">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="53e2c-156">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="53e2c-157">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="53e2c-157">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-158">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="53e2c-158">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-159">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="53e2c-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-161">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="53e2c-161">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="53e2c-162">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="53e2c-162">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="53e2c-163">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="53e2c-163">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="53e2c-164">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="53e2c-164">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="53e2c-165">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="53e2c-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="53e2c-166">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="53e2c-166">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53e2c-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="53e2c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="53e2c-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53e2c-169">限定詞： **文字 \_ 慣例** ( "TimeTicks" ) ， **編碼** ( "TimeTicks" ) ， **物件 \_ 語法** ( "TimeTicks" ) ， **物件 \_ 識別碼** ( "1.3.6.1.2.1.1.3" ) </span><span class="sxs-lookup"><span data-stu-id="53e2c-169">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="53e2c-170">上次重新初始化代理程式的網路管理部分之後的時間（百分之一秒）。</span><span class="sxs-lookup"><span data-stu-id="53e2c-170">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="53e2c-171">這會對應到 MIB 變數 sysUptime 0，其類型為 **INTEGER32**。</span><span class="sxs-lookup"><span data-stu-id="53e2c-171">This maps to the MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="53e2c-172">這個屬性會對應至屬於 **uint32** 類型的 CIM 類別屬性 **時間戳記**。</span><span class="sxs-lookup"><span data-stu-id="53e2c-172">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="53e2c-173">這個屬性僅適用于 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="53e2c-173">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53e2c-174">備註</span><span class="sxs-lookup"><span data-stu-id="53e2c-174">Remarks</span></span>

<span data-ttu-id="53e2c-175">包含名為 **TimeStamp** 或 **識別** 之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。</span><span class="sxs-lookup"><span data-stu-id="53e2c-175">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="53e2c-176">如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。</span><span class="sxs-lookup"><span data-stu-id="53e2c-176">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="53e2c-177">包含名為「**社區**」之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。</span><span class="sxs-lookup"><span data-stu-id="53e2c-177">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="53e2c-178">如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。</span><span class="sxs-lookup"><span data-stu-id="53e2c-178">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="53e2c-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="53e2c-179">Requirements</span></span>



| <span data-ttu-id="53e2c-180">需求</span><span class="sxs-lookup"><span data-stu-id="53e2c-180">Requirement</span></span> | <span data-ttu-id="53e2c-181">值</span><span class="sxs-lookup"><span data-stu-id="53e2c-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53e2c-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53e2c-182">Minimum supported client</span></span><br/> | <span data-ttu-id="53e2c-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53e2c-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53e2c-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53e2c-184">Minimum supported server</span></span><br/> | <span data-ttu-id="53e2c-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53e2c-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53e2c-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="53e2c-186">Namespace</span></span><br/>                | <span data-ttu-id="53e2c-187">根 \\ snmp \\ SMIR</span><span class="sxs-lookup"><span data-stu-id="53e2c-187">Root\\snmp\\SMIR</span></span><br/>                                                             |
| <span data-ttu-id="53e2c-188">MOF</span><span class="sxs-lookup"><span data-stu-id="53e2c-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53e2c-189"><dt>SnmpSmiR mof</dt></span><span class="sxs-lookup"><span data-stu-id="53e2c-189"><dt>SnmpSmiR.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e2c-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53e2c-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e2c-191">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="53e2c-191">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="53e2c-192">通知類型宏</span><span class="sxs-lookup"><span data-stu-id="53e2c-192">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

