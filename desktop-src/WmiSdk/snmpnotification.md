---
description: SnmpNotification 類別會從通知類型宏對應到封裝的 CIM 類別。
ms.assetid: b90d8bab-7cae-4dbe-9f6e-daba4e68a10a
ms.tgt_platform: multiple
title: SnmpNotification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpNotification
- Root\snmp\localhost.SnmpNotification.SECURITY_DESCRIPTOR
- Root\snmp\localhost.SnmpNotification.TIME_CREATED
- Root\snmp\localhost.SnmpNotification.AgentAddress
- Root\snmp\localhost.SnmpNotification.AgentTransport
- Root\snmp\localhost.SnmpNotification.AgentTransportAddress
- Root\snmp\localhost.SnmpNotification.Community
- Root\snmp\localhost.SnmpNotification.Identification
- Root\snmp\localhost.SnmpNotification.TimeStamp
- Root\snmp\localhost.SnmpNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\localhost
ms.openlocfilehash: 89b50d04b435f862a329953f14b47646937a1d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514133"
---
# <a name="snmpnotification-class"></a><span data-ttu-id="c281c-103">SnmpNotification 類別</span><span class="sxs-lookup"><span data-stu-id="c281c-103">SnmpNotification class</span></span>

<span data-ttu-id="c281c-104">**SnmpNotification** 類別會從 [通知類型](notification-type-macro.md)宏對應到封裝的 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="c281c-104">The **SnmpNotification** class maps from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class.</span></span> <span data-ttu-id="c281c-105">它是 snmp [提供](snmp-provider.md) 者所使用的基類，用於從 [通知類型](notification-type-macro.md) 宏對應到封裝 CIM 類別的任何類別。</span><span class="sxs-lookup"><span data-stu-id="c281c-105">It is a base class used by the [SNMP Provider](snmp-provider.md) for any class mapped from the [NOTIFICATION-TYPE](notification-type-macro.md) macro to an encapsulated CIM class by the SNMP Provider.</span></span>

> [!Note]  
> <span data-ttu-id="c281c-106">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="c281c-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c281c-107">語法</span><span class="sxs-lookup"><span data-stu-id="c281c-107">Syntax</span></span>

``` syntax
class SnmpNotification : __ExtrinsicEvent
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

## <a name="members"></a><span data-ttu-id="c281c-108">成員</span><span class="sxs-lookup"><span data-stu-id="c281c-108">Members</span></span>

<span data-ttu-id="c281c-109">**SnmpNotification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c281c-109">The **SnmpNotification** class has these types of members:</span></span>

-   [<span data-ttu-id="c281c-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c281c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c281c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c281c-111">Properties</span></span>

<span data-ttu-id="c281c-112">**SnmpNotification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c281c-112">The **SnmpNotification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c281c-113">**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="c281c-113">**AgentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-116">建立通知之實體的網路位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-116">Network address of the entity that created the notification.</span></span> <span data-ttu-id="c281c-117">這是裝置的實際位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-117">This is the actual address of the device.</span></span> <span data-ttu-id="c281c-118">當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-118">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="c281c-119">當管理實體使用 SNMP over IPX 時，傳輸位址會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c281c-119">When the management entity uses SNMP over IPX, the transport address is set to **NULL**.</span></span> <span data-ttu-id="c281c-120">這個屬性僅適用于 SNMPv1。</span><span class="sxs-lookup"><span data-stu-id="c281c-120">This property is valid for SNMPv1 only.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-121">**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="c281c-121">**AgentTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-124">傳送實體所使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c281c-124">Transport protocol used by the sending entity.</span></span> <span data-ttu-id="c281c-125">這個屬性對 SNMPv1 和 SNMPv2C 有效。</span><span class="sxs-lookup"><span data-stu-id="c281c-125">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-126">**AgentTransportAddress**</span><span class="sxs-lookup"><span data-stu-id="c281c-126">**AgentTransportAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-127">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-129">傳送通知之實體的網路位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-129">Network address of the entity that sent the notification.</span></span> <span data-ttu-id="c281c-130">這是轉送通知的最後一個實體的位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-130">This is the address of the last entity that forwarded the notification.</span></span> <span data-ttu-id="c281c-131">當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-131">When the management entity uses SNMP over UDP, the transport address refers to an IP address.</span></span> <span data-ttu-id="c281c-132">當管理實體將 SNMP 用於 IPX 時，傳輸位址會參考 IPX 位址。</span><span class="sxs-lookup"><span data-stu-id="c281c-132">When the management entity uses SNMP over IPX, the transport address refers to an IPX address.</span></span> <span data-ttu-id="c281c-133">這個屬性對 SNMPv1 和 SNMPv2C 有效。</span><span class="sxs-lookup"><span data-stu-id="c281c-133">This property is valid for SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-134">**AgentTransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="c281c-134">**AgentTransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-137">傳送實體所使用的傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c281c-137">The transport protocol used by the sending entity.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-138">**社群**</span><span class="sxs-lookup"><span data-stu-id="c281c-138">**Community**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-141">與 PDU 實例相關聯的群體名稱。</span><span class="sxs-lookup"><span data-stu-id="c281c-141">Community name associated with an instance of the PDU.</span></span> <span data-ttu-id="c281c-142">群體名稱會驗證 PDU 的建立者。</span><span class="sxs-lookup"><span data-stu-id="c281c-142">The community name authenticates the originator of the PDU.</span></span> <span data-ttu-id="c281c-143">這個屬性對 SNMPv1 和 SNMPv2C 都有效。</span><span class="sxs-lookup"><span data-stu-id="c281c-143">This property is valid for both SNMPv1 and SNMPv2C.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-144">**識別**</span><span class="sxs-lookup"><span data-stu-id="c281c-144">**Identification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c281c-147">限定詞： **文字 \_ 慣例** ( "OBJECTIDENTIFIER" ) ， **編碼** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 語法** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 識別碼** ( "1.3.6.1.6.3.1.1.4.1" ) </span><span class="sxs-lookup"><span data-stu-id="c281c-147">Qualifiers: **textual\_convention** ("OBJECTIDENTIFIER"), **encoding** ("OBJECTIDENTIFIER"), **object\_syntax** ("OBJECTIDENTIFIER"), **object\_identifier** ("1.3.6.1.6.3.1.1.4.1")</span></span>
</dt> </dl>

<span data-ttu-id="c281c-148">此通知的授權識別。</span><span class="sxs-lookup"><span data-stu-id="c281c-148">Authoritative identification of this notification.</span></span> <span data-ttu-id="c281c-149">直接對應至 SnmpTrapOID 變數系結。</span><span class="sxs-lookup"><span data-stu-id="c281c-149">Maps directly to the SnmpTrapOID variable binding.</span></span> <span data-ttu-id="c281c-150">這個屬性僅適用于 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="c281c-150">This property is valid for SNMPv2C only.</span></span>

</dd> <dt>

<span data-ttu-id="c281c-151">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="c281c-151">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-152">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="c281c-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c281c-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-154">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="c281c-154">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c281c-155">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="c281c-155">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="c281c-156">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="c281c-156">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c281c-157">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="c281c-157">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-158">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c281c-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c281c-160">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="c281c-160">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c281c-161">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="c281c-161">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c281c-162">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="c281c-162">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="c281c-163">這個屬性繼承自 [**\_ \_ 事件**](--event.md)。</span><span class="sxs-lookup"><span data-stu-id="c281c-163">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="c281c-164">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="c281c-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="c281c-165">**時間 戳**</span><span class="sxs-lookup"><span data-stu-id="c281c-165">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c281c-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c281c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c281c-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c281c-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c281c-168">限定詞： **文字 \_ 慣例** ( "TimeTicks" ) ， **編碼** ( "TimeTicks" ) ， **物件 \_ 語法** ( "TimeTicks" ) ， **物件 \_ 識別碼** ( "1.3.6.1.2.1.1.3" ) </span><span class="sxs-lookup"><span data-stu-id="c281c-168">Qualifiers: **textual\_convention** ("TimeTicks"), **encoding** ("TimeTicks"), **object\_syntax** ("TimeTicks"), **object\_identifier** ("1.3.6.1.2.1.1.3")</span></span>
</dt> </dl>

<span data-ttu-id="c281c-169">上次重新初始化代理程式的網路管理部分之後的時間（百分之一秒）。</span><span class="sxs-lookup"><span data-stu-id="c281c-169">Time in hundredths of a second since the network management portion of the agent was last re-initialized.</span></span> <span data-ttu-id="c281c-170">MIB 變數 sysUptime 0，其類型為 **INTEGER32**。</span><span class="sxs-lookup"><span data-stu-id="c281c-170">MIB variable sysUptime.0, which is of type **INTEGER32**.</span></span> <span data-ttu-id="c281c-171">這個屬性會對應至屬於 **uint32** 類型的 CIM 類別屬性 **時間戳記**。</span><span class="sxs-lookup"><span data-stu-id="c281c-171">This property maps to the CIM class property **TimeStamp**, which is of type **uint32**.</span></span> <span data-ttu-id="c281c-172">這個屬性僅適用于 SNMPv2C。</span><span class="sxs-lookup"><span data-stu-id="c281c-172">This property is valid for SNMPv2C only.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c281c-173">備註</span><span class="sxs-lookup"><span data-stu-id="c281c-173">Remarks</span></span>

<span data-ttu-id="c281c-174">包含名為 **TimeStamp** 或 **識別** 之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。</span><span class="sxs-lookup"><span data-stu-id="c281c-174">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **TimeStamp** or **Identification** causes a mapping conflict.</span></span> <span data-ttu-id="c281c-175">如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。</span><span class="sxs-lookup"><span data-stu-id="c281c-175">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

<span data-ttu-id="c281c-176">包含名為「**社區**」之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。</span><span class="sxs-lookup"><span data-stu-id="c281c-176">A [NOTIFICATION-TYPE](notification-type-macro.md) macro that contains references to an [OBJECT-TYPE](object-type-macro.md) macro named **Community** causes a mapping conflict.</span></span> <span data-ttu-id="c281c-177">如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。</span><span class="sxs-lookup"><span data-stu-id="c281c-177">If this conflict occurs, the required properties take precedence and the conflicting references must be renamed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c281c-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="c281c-178">Requirements</span></span>



| <span data-ttu-id="c281c-179">需求</span><span class="sxs-lookup"><span data-stu-id="c281c-179">Requirement</span></span> | <span data-ttu-id="c281c-180">值</span><span class="sxs-lookup"><span data-stu-id="c281c-180">Value</span></span> |
|-------------------------------------|----------------------------------|
| <span data-ttu-id="c281c-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c281c-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c281c-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c281c-182">Windows Vista</span></span><br/>         |
| <span data-ttu-id="c281c-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c281c-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c281c-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c281c-184">Windows Server 2008</span></span><br/>   |
| <span data-ttu-id="c281c-185">命名空間</span><span class="sxs-lookup"><span data-stu-id="c281c-185">Namespace</span></span><br/>                | <span data-ttu-id="c281c-186">根 \\ snmp \\ localhost</span><span class="sxs-lookup"><span data-stu-id="c281c-186">Root\\snmp\\localhost</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c281c-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c281c-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c281c-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="c281c-188">**\_\_ExtrinsicEvent**</span></span>](--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="c281c-189">通知類型宏</span><span class="sxs-lookup"><span data-stu-id="c281c-189">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)
</dt> </dl>

 

