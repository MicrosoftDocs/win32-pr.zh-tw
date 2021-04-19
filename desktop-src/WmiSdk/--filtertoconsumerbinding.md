---
description: 用於註冊永久事件取用者，以便將 EventConsumer 的實例與 >eventfilter 的實例產生關聯 \_ \_ \_ \_ 。
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985491"
---
# <a name="__filtertoconsumerbinding-class"></a><span data-ttu-id="1bf18-103">\_\_FilterToConsumerBinding 類別</span><span class="sxs-lookup"><span data-stu-id="1bf18-103">\_\_FilterToConsumerBinding class</span></span>

<span data-ttu-id="1bf18-104">**\_ \_ FilterToConsumerBinding** 系統類別用於註冊永久事件取用者，以便將 [**\_ \_ EventConsumer**](--eventconsumer.md)的實例與 [**\_ \_ >eventfilter**](--eventfilter.md)的實例產生關聯。**\_ \_FilterToConsumerBinding** 是關聯類別。</span><span class="sxs-lookup"><span data-stu-id="1bf18-104">The **\_\_FilterToConsumerBinding** system class is used in the registration of permanent event consumers to relate an instance of the [**\_\_EventConsumer**](--eventconsumer.md) to an instance of [**\_\_EventFilter**](--eventfilter.md).**\_\_FilterToConsumerBinding** is an association class.</span></span>

<span data-ttu-id="1bf18-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1bf18-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1bf18-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1bf18-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf18-107">語法</span><span class="sxs-lookup"><span data-stu-id="1bf18-107">Syntax</span></span>

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a><span data-ttu-id="1bf18-108">成員</span><span class="sxs-lookup"><span data-stu-id="1bf18-108">Members</span></span>

<span data-ttu-id="1bf18-109">**\_ \_ FilterToConsumerBinding** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1bf18-109">The **\_\_FilterToConsumerBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf18-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1bf18-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf18-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1bf18-111">Properties</span></span>

<span data-ttu-id="1bf18-112">**\_ \_ FilterToConsumerBinding** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1bf18-112">The **\_\_FilterToConsumerBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bf18-113">**消費者**</span><span class="sxs-lookup"><span data-stu-id="1bf18-113">**Consumer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-114">資料類型： **\_ \_ EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="1bf18-114">Data type: **\_\_EventConsumer**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-116">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1bf18-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-117">[**\_ \_ EventConsumer**](--eventconsumer.md)實例的參考，代表邏輯取用者的物件路徑，也就是事件的收件者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-117">Reference to an instance of [**\_\_EventConsumer**](--eventconsumer.md) that represents the object path to a logical consumer, the recipient of an event.</span></span> <span data-ttu-id="1bf18-118">邏輯取用者是衍生自 **\_ \_ EventConsumer** 之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1bf18-118">A logical consumer is an instance of a class derived from **\_\_EventConsumer**.</span></span>

</dd> <dt>

<span data-ttu-id="1bf18-119">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="1bf18-119">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-120">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="1bf18-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-122">安全識別碼 (SID) ，可唯一識別建立系結的使用者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-122">Security identifier (SID) that uniquely identifies the user who created the binding.</span></span> <span data-ttu-id="1bf18-123">根據作業系統，WMI 會儲存系統管理員 sid 或建立 **\_ \_ FilterToConsumerBinding** 實例之使用者的 sid。</span><span class="sxs-lookup"><span data-stu-id="1bf18-123">Depending on the operating system, WMI stores the Administrator SID or the SID of the user that creates an instance of **\_\_FilterToConsumerBinding**.</span></span> <span data-ttu-id="1bf18-124">如需詳細資訊，請參閱使用邏輯取用者來系結 [事件篩選器](binding-an-event-filter-with-a-logical-consumer.md) ，以及 [使用標準取用者來監視和回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="1bf18-124">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bf18-125">**DeliverSynchronously**</span><span class="sxs-lookup"><span data-stu-id="1bf18-125">**DeliverSynchronously**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bf18-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-128">已過時。</span><span class="sxs-lookup"><span data-stu-id="1bf18-128">Obsolete.</span></span> <span data-ttu-id="1bf18-129">請改為使用 **DeliveryQoS** 屬性來取代這個屬性，因為如果 **DeliverSynchronously** 設定為 **True** ，則會覆寫 **DeliveryQoS** 屬性的設定。</span><span class="sxs-lookup"><span data-stu-id="1bf18-129">Instead use the **DeliveryQoS** property in place of this property, because if **DeliverSynchronously** is set to **True** it overrides the setting of the **DeliveryQoS** property.</span></span>

</dd> <dt>

<span data-ttu-id="1bf18-130">**DeliveryQoS**</span><span class="sxs-lookup"><span data-stu-id="1bf18-130">**DeliveryQoS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1bf18-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-133">訂用帳戶的服務品質。</span><span class="sxs-lookup"><span data-stu-id="1bf18-133">Quality of service for a subscription.</span></span> <span data-ttu-id="1bf18-134">如果 **DeliverSynchronously** 屬性設定為 **True**，它會覆寫 **DeliveryQoS** 屬性的設定。</span><span class="sxs-lookup"><span data-stu-id="1bf18-134">If the **DeliverSynchronously** property is set to **True**, it overrides the setting of the **DeliveryQoS** property.</span></span>

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span data-ttu-id="1bf18-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_旗標 \_ QOS \_ 同步** (0) </span><span class="sxs-lookup"><span data-stu-id="1bf18-135"><span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG\_FLAG\_QOS\_SYNCHRONOUS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1bf18-136">同步傳遞</span><span class="sxs-lookup"><span data-stu-id="1bf18-136">Synchronous delivery</span></span>

<span data-ttu-id="1bf18-137">**False**：</span><span class="sxs-lookup"><span data-stu-id="1bf18-137">**False**.</span></span> <span data-ttu-id="1bf18-138">事件會以同步方式傳遞給邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-138">The event is delivered to the logical consumer synchronously.</span></span>

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span data-ttu-id="1bf18-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_標示 \_ QOS \_ EXPRESS** (1) </span><span class="sxs-lookup"><span data-stu-id="1bf18-139"><span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG\_FLAG\_QOS\_EXPRESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1bf18-140">快遞</span><span class="sxs-lookup"><span data-stu-id="1bf18-140">Express delivery</span></span>

<span data-ttu-id="1bf18-141">**True**。</span><span class="sxs-lookup"><span data-stu-id="1bf18-141">**True**.</span></span> <span data-ttu-id="1bf18-142">事件會以非同步方式傳遞給邏輯取用者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-142">The event is delivered to the logical consumer asynchronously.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1bf18-143">**Filter**</span><span class="sxs-lookup"><span data-stu-id="1bf18-143">**Filter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-144">資料類型： **\_ \_ >eventfilter**</span><span class="sxs-lookup"><span data-stu-id="1bf18-144">Data type: **\_\_EventFilter**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-146">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1bf18-146">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-147">[**\_ \_ >eventfilter**](--eventfilter.md)實例的參考，代表事件篩選器的物件路徑，這是指定要接收之事件種類的查詢。</span><span class="sxs-lookup"><span data-stu-id="1bf18-147">Reference to an instance of [**\_\_EventFilter**](--eventfilter.md) that represents the object path to an event filter which is a query that specifies the type of event to be received.</span></span>

</dd> <dt>

<span data-ttu-id="1bf18-148">**MaintainSecurityCoNtext**</span><span class="sxs-lookup"><span data-stu-id="1bf18-148">**MaintainSecurityContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-149">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bf18-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-151">若 **為 True**，則會以提供者提供的相同安全性內容來傳遞事件。</span><span class="sxs-lookup"><span data-stu-id="1bf18-151">If **True**, the events are delivered in the same security context that the provider was in when it provided them.</span></span>

> [!Note]  
> <span data-ttu-id="1bf18-152">只有實作為 DLL 的取用者 (同進程取用者) 可以接收提供者之安全性內容中的事件。</span><span class="sxs-lookup"><span data-stu-id="1bf18-152">Only a consumer implemented as a DLL (an in-process consumer) can receive events in the security context of the provider.</span></span> <span data-ttu-id="1bf18-153">如需有關同進程提供者和安全性的詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="1bf18-153">For more information about in-process providers and security, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="1bf18-154">如需詳細資訊和範例，請參閱取代：[安全地接收事件](receiving-events-securely.md)。</span><span class="sxs-lookup"><span data-stu-id="1bf18-154">For more information and examples, see replace:[Receiving Events Securely](receiving-events-securely.md).</span></span>

 

</dd> <dt>

<span data-ttu-id="1bf18-155">**SlowDownProviders**</span><span class="sxs-lookup"><span data-stu-id="1bf18-155">**SlowDownProviders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf18-156">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1bf18-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1bf18-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1bf18-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1bf18-158">若 **為 True**，則在此取用者無法趕上時，提供者會變慢。</span><span class="sxs-lookup"><span data-stu-id="1bf18-158">If **True**, providers are slowed down if this consumer cannot keep up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1bf18-159">備註</span><span class="sxs-lookup"><span data-stu-id="1bf18-159">Remarks</span></span>

<span data-ttu-id="1bf18-160">**\_ \_ FilterToConsumerBinding** 類別衍生自 [**\_ \_ IndicationRelated**](--indicationrelated.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="1bf18-160">The **\_\_FilterToConsumerBinding** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="1bf18-161">永久事件取用者會使用 **\_ \_ FilterToConsumerBinding** 系統類別，將事件篩選器系結至最終取用者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-161">Permanent event consumers use the **\_\_FilterToConsumerBinding** system class to bind event filters to final consumers.</span></span> <span data-ttu-id="1bf18-162">將篩選和取用者系結在一起之後，WMI 可以將符合篩選準則的事件轉送到對應的取用者。</span><span class="sxs-lookup"><span data-stu-id="1bf18-162">After the filter and consumer are bound together, WMI can forward events that match the filter to the corresponding consumer.</span></span>

## <a name="examples"></a><span data-ttu-id="1bf18-163">範例</span><span class="sxs-lookup"><span data-stu-id="1bf18-163">Examples</span></span>

<span data-ttu-id="1bf18-164">在 TechNet 資源庫上 [建立永久性 wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2)檔案 PowerShell 範例使用 **\_ \_ FilterToConsumerBinding** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。</span><span class="sxs-lookup"><span data-stu-id="1bf18-164">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_FilterToConsumerBinding** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf18-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bf18-165">Requirements</span></span>



| <span data-ttu-id="1bf18-166">需求</span><span class="sxs-lookup"><span data-stu-id="1bf18-166">Requirement</span></span> | <span data-ttu-id="1bf18-167">值</span><span class="sxs-lookup"><span data-stu-id="1bf18-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1bf18-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bf18-168">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf18-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bf18-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1bf18-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bf18-170">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf18-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bf18-171">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1bf18-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="1bf18-172">Namespace</span></span><br/>                | <span data-ttu-id="1bf18-173">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="1bf18-173">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1bf18-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bf18-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf18-175">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="1bf18-175">**\_\_IndicationRelated**</span></span>](--indicationrelated.md)
</dt> <dt>

[<span data-ttu-id="1bf18-176">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="1bf18-176">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1bf18-177">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="1bf18-177">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="1bf18-178">監視事件</span><span class="sxs-lookup"><span data-stu-id="1bf18-178">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="1bf18-179">建立事件篩選器</span><span class="sxs-lookup"><span data-stu-id="1bf18-179">Creating an Event Filter</span></span>](creating-an-event-filter.md)
</dt> <dt>

[<span data-ttu-id="1bf18-180">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="1bf18-180">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




