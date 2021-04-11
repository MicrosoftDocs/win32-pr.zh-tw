---
description: 下圖顯示用於事件的 WMI 安全性常數。 它們是用來在用於事件或接收的安全描述項)  (Ace 設定存取控制專案。
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: '事件安全性常數 (Wbemcli .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115040"
---
# <a name="event-security-constants"></a><span data-ttu-id="0ba29-104">事件安全性常數</span><span class="sxs-lookup"><span data-stu-id="0ba29-104">Event Security Constants</span></span>

<span data-ttu-id="0ba29-105">下圖顯示用於事件的 WMI 安全性常數。</span><span class="sxs-lookup"><span data-stu-id="0ba29-105">The following shows the WMI security constants used for events.</span></span> <span data-ttu-id="0ba29-106">它們是用來在用於事件或接收的安全描述項)  (Ace 設定存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="0ba29-106">They are used to set access control entries (ACEs) in security descriptors used for events or sinks.</span></span>

<dl> <dt>

<span data-ttu-id="0ba29-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM \_ 正確 \_ 發佈**</span><span class="sxs-lookup"><span data-stu-id="0ba29-107"><span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**WBEM\_RIGHT\_PUBLISH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba29-108">128 (0x80) </span><span class="sxs-lookup"><span data-stu-id="0ba29-108">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="0ba29-109">指定帳戶可以將事件發佈至定義永久性取用者之事件篩選器的 [**\_ \_ >eventfilter**](--eventfilter.md)實例。</span><span class="sxs-lookup"><span data-stu-id="0ba29-109">Specifies that the account can publish events to the instance of [**\_\_EventFilter**](--eventfilter.md) that defines the event filter for a permanent consumer.</span></span> <span data-ttu-id="0ba29-110">可在 wbemcli 中取得。</span><span class="sxs-lookup"><span data-stu-id="0ba29-110">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ba29-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM \_ 正確 \_ 訂閱**</span><span class="sxs-lookup"><span data-stu-id="0ba29-111"><span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**WBEM\_RIGHT\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba29-112">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="0ba29-112">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="0ba29-113">指定取用者可以訂閱傳遞給接收的事件。</span><span class="sxs-lookup"><span data-stu-id="0ba29-113">Specifies that a consumer can subscribe to the events delivered to a sink.</span></span> <span data-ttu-id="0ba29-114">用於 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)。</span><span class="sxs-lookup"><span data-stu-id="0ba29-114">Used in [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity).</span></span> <span data-ttu-id="0ba29-115">可在 wbemcli 中取得。</span><span class="sxs-lookup"><span data-stu-id="0ba29-115">Available in wbemcli.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0ba29-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM \_ \_ 受限於 \_ \_ SDS**</span><span class="sxs-lookup"><span data-stu-id="0ba29-116"><span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**WBEM\_S\_SUBJECT\_TO\_SDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ba29-117">274435 (0x43003) </span><span class="sxs-lookup"><span data-stu-id="0ba29-117">274435 (0x43003)</span></span>
</dt> <dt>



<span data-ttu-id="0ba29-118">事件提供者指出 WMI 會檢查每個事件中的 **安全 \_ 描述項** 屬性 (繼承自 [**\_ \_ 事件**](--event.md)) ，而且只會將事件傳送給具有適當存取權限的取用者。</span><span class="sxs-lookup"><span data-stu-id="0ba29-118">Event provider indicates that WMI checks the **SECURITY\_DESCRIPTOR** property in each event (inherited from [**\_\_Event**](--event.md)), and only sends events to consumers with the appropriate access permissions.</span></span> <span data-ttu-id="0ba29-119">可在 wbemprov 中取得。</span><span class="sxs-lookup"><span data-stu-id="0ba29-119">Available in wbemprov.h.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ba29-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ba29-120">Requirements</span></span>



| <span data-ttu-id="0ba29-121">需求</span><span class="sxs-lookup"><span data-stu-id="0ba29-121">Requirement</span></span> | <span data-ttu-id="0ba29-122">值</span><span class="sxs-lookup"><span data-stu-id="0ba29-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba29-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ba29-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba29-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ba29-124">Windows Vista</span></span><br/>                                                                                                                               |
| <span data-ttu-id="0ba29-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ba29-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba29-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba29-126">Windows Server 2008</span></span><br/>                                                                                                                         |
| <span data-ttu-id="0ba29-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0ba29-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ba29-128"><dt>Wbemcli .h;</dt><dt>Wbemprov .h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba29-128"><dt>Wbemcli.h; </dt> <dt>Wbemprov.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba29-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ba29-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba29-130">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="0ba29-130">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="0ba29-131">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="0ba29-131">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="0ba29-132">保護 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="0ba29-132">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> </dl>

 

 




