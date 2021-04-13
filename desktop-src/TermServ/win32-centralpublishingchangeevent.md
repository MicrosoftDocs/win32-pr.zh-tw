---
title: Win32_CentralPublishingChangeEvent 類別
description: 代表中央 RDV 設定變更的事件。
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent 類別遠端桌面服務
- Win32_CentralPublishingChangeEvent 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465777"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="e5234-105">Win32 \_ CentralPublishingChangeEvent 類別</span><span class="sxs-lookup"><span data-stu-id="e5234-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="e5234-106">代表中央 RDV 設定變更的事件。</span><span class="sxs-lookup"><span data-stu-id="e5234-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="e5234-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="e5234-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5234-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5234-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="e5234-109">成員</span><span class="sxs-lookup"><span data-stu-id="e5234-109">Members</span></span>

<span data-ttu-id="e5234-110">**Win32 \_ CentralPublishingChangeEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e5234-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="e5234-111">屬性</span><span class="sxs-lookup"><span data-stu-id="e5234-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5234-112">屬性</span><span class="sxs-lookup"><span data-stu-id="e5234-112">Properties</span></span>

<span data-ttu-id="e5234-113">**Win32 \_ CentralPublishingChangeEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e5234-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5234-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="e5234-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5234-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5234-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5234-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5234-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5234-117">對應至事件的作業類型。</span><span class="sxs-lookup"><span data-stu-id="e5234-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="e5234-118">**建立** (0) </span><span class="sxs-lookup"><span data-stu-id="e5234-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="e5234-119">**修改** (1) </span><span class="sxs-lookup"><span data-stu-id="e5234-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="e5234-120">**刪除** (2) </span><span class="sxs-lookup"><span data-stu-id="e5234-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5234-121">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="e5234-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5234-122">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="e5234-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e5234-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5234-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5234-124">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="e5234-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="e5234-125">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="e5234-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="e5234-126">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。</span><span class="sxs-lookup"><span data-stu-id="e5234-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="e5234-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="e5234-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5234-128">資料類型： **物件**</span><span class="sxs-lookup"><span data-stu-id="e5234-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="e5234-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5234-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5234-130">由對應至事件的作業所變更的物件。</span><span class="sxs-lookup"><span data-stu-id="e5234-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="e5234-131">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="e5234-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5234-132">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="e5234-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e5234-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="e5234-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5234-134">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="e5234-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="e5234-135">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="e5234-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="e5234-136">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="e5234-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="e5234-137">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="e5234-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="e5234-138">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e5234-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5234-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5234-139">Requirements</span></span>



| <span data-ttu-id="e5234-140">需求</span><span class="sxs-lookup"><span data-stu-id="e5234-140">Requirement</span></span> | <span data-ttu-id="e5234-141">值</span><span class="sxs-lookup"><span data-stu-id="e5234-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5234-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5234-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e5234-143">都不支援</span><span class="sxs-lookup"><span data-stu-id="e5234-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e5234-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5234-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e5234-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5234-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e5234-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5234-146">Namespace</span></span><br/>                | <span data-ttu-id="e5234-147">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e5234-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e5234-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e5234-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5234-149"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5234-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="e5234-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e5234-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5234-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5234-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

