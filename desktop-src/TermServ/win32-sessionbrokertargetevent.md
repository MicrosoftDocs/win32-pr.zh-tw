---
title: Win32_SessionBrokerTargetEvent 類別
description: 代表會話 broker 目標的變更。
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerTargetEvent 類別遠端桌面服務
- Win32_SessionBrokerTargetEvent 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685708"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="1caf5-105">Win32 \_ SessionBrokerTargetEvent 類別</span><span class="sxs-lookup"><span data-stu-id="1caf5-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="1caf5-106">代表會話 broker 目標的變更。</span><span class="sxs-lookup"><span data-stu-id="1caf5-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="1caf5-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1caf5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caf5-108">語法</span><span class="sxs-lookup"><span data-stu-id="1caf5-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="1caf5-109">成員</span><span class="sxs-lookup"><span data-stu-id="1caf5-109">Members</span></span>

<span data-ttu-id="1caf5-110">**Win32 \_ SessionBrokerTargetEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1caf5-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1caf5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="1caf5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1caf5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1caf5-112">Properties</span></span>

<span data-ttu-id="1caf5-113">**Win32 \_ SessionBrokerTargetEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1caf5-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1caf5-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="1caf5-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-115">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1caf5-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-117">指定發生的變更。</span><span class="sxs-lookup"><span data-stu-id="1caf5-117">Specifies the change that occurred.</span></span> <span data-ttu-id="1caf5-118">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1caf5-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1caf5-119">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="1caf5-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-120">未指定變更的類型。</span><span class="sxs-lookup"><span data-stu-id="1caf5-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-121">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="1caf5-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-122">外部 IP 位址已變更。</span><span class="sxs-lookup"><span data-stu-id="1caf5-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-123">4 (0x4) </span><span class="sxs-lookup"><span data-stu-id="1caf5-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-124">內部 IP 位址已變更。</span><span class="sxs-lookup"><span data-stu-id="1caf5-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-125">8 (0x8) </span><span class="sxs-lookup"><span data-stu-id="1caf5-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-126">目標已聯結。</span><span class="sxs-lookup"><span data-stu-id="1caf5-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-127">16 (0x10) </span><span class="sxs-lookup"><span data-stu-id="1caf5-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-128">已移除目標。</span><span class="sxs-lookup"><span data-stu-id="1caf5-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-129">32 (0x20) </span><span class="sxs-lookup"><span data-stu-id="1caf5-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-130">目標的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="1caf5-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-131">64 (0x40) </span><span class="sxs-lookup"><span data-stu-id="1caf5-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="1caf5-132">目標為閒置。</span><span class="sxs-lookup"><span data-stu-id="1caf5-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1caf5-133">**環境**</span><span class="sxs-lookup"><span data-stu-id="1caf5-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1caf5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-136">環境名稱。</span><span class="sxs-lookup"><span data-stu-id="1caf5-136">The environment name.</span></span> <span data-ttu-id="1caf5-137">如果虛擬機器 (VM) 目標，這可能是 VM 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="1caf5-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="1caf5-138">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="1caf5-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-139">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="1caf5-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1caf5-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-142">目標所屬伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="1caf5-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="1caf5-143">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="1caf5-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-144">**Guid**</span><span class="sxs-lookup"><span data-stu-id="1caf5-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1caf5-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-147">目標的 GUID。</span><span class="sxs-lookup"><span data-stu-id="1caf5-147">The GUID of the target.</span></span>

<span data-ttu-id="1caf5-148">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="1caf5-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="1caf5-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1caf5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-152">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1caf5-152">The name of the plug-in.</span></span>

<span data-ttu-id="1caf5-153">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="1caf5-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-154">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="1caf5-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-155">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="1caf5-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-157">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="1caf5-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="1caf5-158">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="1caf5-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="1caf5-159">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](/windows/desktop/WmiSdk/wmi-security-constants)。</span><span class="sxs-lookup"><span data-stu-id="1caf5-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="1caf5-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1caf5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-163">目標的名稱。</span><span class="sxs-lookup"><span data-stu-id="1caf5-163">The name of the target.</span></span>

<span data-ttu-id="1caf5-164">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="1caf5-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1caf5-165">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="1caf5-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1caf5-166">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1caf5-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1caf5-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1caf5-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1caf5-168">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="1caf5-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="1caf5-169">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="1caf5-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1caf5-170">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="1caf5-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="1caf5-171">這個屬性繼承自 [**\_ \_ 事件**](/windows/desktop/WmiSdk/--event)。</span><span class="sxs-lookup"><span data-stu-id="1caf5-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="1caf5-172">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1caf5-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1caf5-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="1caf5-173">Requirements</span></span>



| <span data-ttu-id="1caf5-174">需求</span><span class="sxs-lookup"><span data-stu-id="1caf5-174">Requirement</span></span> | <span data-ttu-id="1caf5-175">值</span><span class="sxs-lookup"><span data-stu-id="1caf5-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1caf5-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1caf5-176">Minimum supported client</span></span><br/> | <span data-ttu-id="1caf5-177">都不支援</span><span class="sxs-lookup"><span data-stu-id="1caf5-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1caf5-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1caf5-178">Minimum supported server</span></span><br/> | <span data-ttu-id="1caf5-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1caf5-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1caf5-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="1caf5-180">Namespace</span></span><br/>                | <span data-ttu-id="1caf5-181">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1caf5-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="1caf5-182">MOF</span><span class="sxs-lookup"><span data-stu-id="1caf5-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1caf5-183"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="1caf5-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1caf5-184">DLL</span><span class="sxs-lookup"><span data-stu-id="1caf5-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1caf5-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1caf5-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

