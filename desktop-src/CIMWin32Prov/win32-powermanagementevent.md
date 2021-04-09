---
description: Win32 \_ PowerManagementEvent &\# 32;WMI 類別代表電源管理事件，由電源狀態變更所造成。
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110728"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="afced-103">Win32 \_ PowerManagementEvent 類別</span><span class="sxs-lookup"><span data-stu-id="afced-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="afced-104">**Win32 \_ PowerManagementEvent** [WMI 類別](../wmisdk/retrieving-a-class.md)代表電源管理事件，由電源狀態變更所造成。</span><span class="sxs-lookup"><span data-stu-id="afced-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="afced-105">這些狀態變更與 Advanced 電源管理 (APM) 或進階組態與電源介面 (ACPI) 系統管理通訊協定相關聯。</span><span class="sxs-lookup"><span data-stu-id="afced-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="afced-106">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="afced-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="afced-107">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="afced-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="afced-108">語法</span><span class="sxs-lookup"><span data-stu-id="afced-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="afced-109">成員</span><span class="sxs-lookup"><span data-stu-id="afced-109">Members</span></span>

<span data-ttu-id="afced-110">**Win32 \_ PowerManagementEvent** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="afced-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="afced-111">屬性</span><span class="sxs-lookup"><span data-stu-id="afced-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afced-112">屬性</span><span class="sxs-lookup"><span data-stu-id="afced-112">Properties</span></span>

<span data-ttu-id="afced-113">**Win32 \_ PowerManagementEvent** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="afced-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afced-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="afced-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afced-115">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="afced-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afced-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afced-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afced-117">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 電源管理事件" ) </span><span class="sxs-lookup"><span data-stu-id="afced-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="afced-118">系統電源狀態的變更類型。</span><span class="sxs-lookup"><span data-stu-id="afced-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="afced-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**進入暫** 止 (4) </span><span class="sxs-lookup"><span data-stu-id="afced-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="afced-120">暫止時，電腦會顯示為關閉;不過，它可以「喚醒」以回應各種事件，包括使用者輸入 (例如移動滑鼠或按鍵盤上的按鍵) 。</span><span class="sxs-lookup"><span data-stu-id="afced-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="afced-121">當電腦暫停時，會根據系統的使用方式，將耗電量縮減為數個層級的其中一個。</span><span class="sxs-lookup"><span data-stu-id="afced-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="afced-122">功率耗用量越低，系統就會花更多時間回到工作狀態。</span><span class="sxs-lookup"><span data-stu-id="afced-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="afced-123">當電腦進入暫停狀態時，會鎖定桌面，您必須按 CTRL + ALT + DELETE，並提供有效的使用者名稱和密碼，才能繼續作業</span><span class="sxs-lookup"><span data-stu-id="afced-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="afced-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**從暫** 止 (7) 繼續</span><span class="sxs-lookup"><span data-stu-id="afced-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="afced-125">表示已傳送暫停訊息的 Resume，讓電腦恢復正常的電源狀態。</span><span class="sxs-lookup"><span data-stu-id="afced-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="afced-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**電源狀態變更** (10) </span><span class="sxs-lookup"><span data-stu-id="afced-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="afced-127">指出電腦電源狀態的變更，例如從電池電力切換至 AC，或從 AC 切換至不斷電供應系統。</span><span class="sxs-lookup"><span data-stu-id="afced-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="afced-128">當剩餘電池的電力下滑至使用者所指定的臨界值之下，或是如果電池的電力由指定百分比來變更時，系統也會廣播這個事件。</span><span class="sxs-lookup"><span data-stu-id="afced-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="afced-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM 事件** (11) </span><span class="sxs-lookup"><span data-stu-id="afced-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="afced-130">指出 Advanced 電源管理 (APM) BIOS 已傳送 OEM 事件。</span><span class="sxs-lookup"><span data-stu-id="afced-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="afced-131">事件的值將會在 **OEMEventCode** 屬性中捕捉。</span><span class="sxs-lookup"><span data-stu-id="afced-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="afced-132">因為某些 APM BIOS 的執行不會提供 OEM 事件通知，所以在某些電腦上可能永遠不會廣播此事件。</span><span class="sxs-lookup"><span data-stu-id="afced-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="afced-133">APM 是舊版的電源管理配置。</span><span class="sxs-lookup"><span data-stu-id="afced-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="afced-134">雖然仍然受支援，但 (進階組態與電源介面) 中，大部分的 APM 都已由 ACPI 取代。</span><span class="sxs-lookup"><span data-stu-id="afced-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="afced-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**繼續** (18) </span><span class="sxs-lookup"><span data-stu-id="afced-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="afced-136">指出電腦已喚醒以回應事件。</span><span class="sxs-lookup"><span data-stu-id="afced-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="afced-137">如果系統偵測到使用者活動 (例如滑鼠按一下) ，ResumeSuspend 訊息將會廣播，讓應用程式知道他們可以繼續與使用者進行完全互動。</span><span class="sxs-lookup"><span data-stu-id="afced-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="afced-138">**OEMEventCode**</span><span class="sxs-lookup"><span data-stu-id="afced-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afced-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="afced-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="afced-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afced-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afced-141">限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 電源管理事件" ) </span><span class="sxs-lookup"><span data-stu-id="afced-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="afced-142">由原始設備製造商所定義的系統電源狀態 (OEM) 當此類別的 [ **事件** 類型] 屬性設為 [oem] (OEM 事件) ;否則，此屬性會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="afced-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="afced-143">當 APM BIOS 發出 APM OEM 事件的信號時，會產生 OEM 事件。</span><span class="sxs-lookup"><span data-stu-id="afced-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="afced-144">OEM 事件碼位於 0x0200h-0x02FFh 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="afced-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="afced-145">**安全 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="afced-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afced-146">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="afced-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="afced-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afced-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afced-148">事件提供者用來判斷哪些使用者可以接收事件的描述項。</span><span class="sxs-lookup"><span data-stu-id="afced-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="afced-149">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="afced-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="afced-150">如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](../wmisdk/wmi-security-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="afced-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="afced-151">**\_建立時間**</span><span class="sxs-lookup"><span data-stu-id="afced-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afced-152">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="afced-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afced-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="afced-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afced-154">唯一值，指出產生事件的時間。</span><span class="sxs-lookup"><span data-stu-id="afced-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="afced-155">這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。</span><span class="sxs-lookup"><span data-stu-id="afced-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="afced-156">此資訊採用國際標準時間 (UTC) 格式。</span><span class="sxs-lookup"><span data-stu-id="afced-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="afced-157">這個屬性繼承自 [**\_ \_ 事件**](../wmisdk/--event.md)。</span><span class="sxs-lookup"><span data-stu-id="afced-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="afced-158">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](../wmisdk/creating-a-wmi-script.md)。</span><span class="sxs-lookup"><span data-stu-id="afced-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afced-159">備註</span><span class="sxs-lookup"><span data-stu-id="afced-159">Remarks</span></span>

<span data-ttu-id="afced-160">**Win32 \_ PowerManagementEvent** 類別衍生自 [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)。</span><span class="sxs-lookup"><span data-stu-id="afced-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="afced-161">電源狀態的變更通常表示電腦或其他受管理裝置發生問題。</span><span class="sxs-lookup"><span data-stu-id="afced-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="afced-162">如果伺服器突然從 AC 電源切換至不斷電供應系統，這項變更可能表示發生某種情況的電子問題，可能是電腦本身或電腦保留的房間內的電力系統所發生。</span><span class="sxs-lookup"><span data-stu-id="afced-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="afced-163">系統管理員需要監視這些變更的電源狀態，並立即收到這類變更的通知。</span><span class="sxs-lookup"><span data-stu-id="afced-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="afced-164">這可讓他們在裝置完全斷電之前採取動作。</span><span class="sxs-lookup"><span data-stu-id="afced-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="afced-165">例如， (的不斷電供應系統供應系統可能只會在15分鐘內執行，然後才關閉。 ) </span><span class="sxs-lookup"><span data-stu-id="afced-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="afced-166">**Win32 \_ PowerManagementEvent** 類別可以用來監視電腦電源狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="afced-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="afced-167">這些變更可能包括從某個電源來源切換到另一個電源，以及電腦電源狀態的變更 (例如，進入或離開暫停模式) 。</span><span class="sxs-lookup"><span data-stu-id="afced-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="afced-168">**Win32 \_ PowerManagementEvent** 類別只有兩個屬性： [事件種類]，用來表示發生的電源變更事件種類，以及 OEMEventType，供某些原始設備製造商用來定義其他的電源變更事件。</span><span class="sxs-lookup"><span data-stu-id="afced-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="afced-169">如需回應 Windows 電源事件的詳細資訊，請參閱「嘿！」上的「 [使用 PowerShell 監視及回應 Windows 電源事件](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) 」一文。</span><span class="sxs-lookup"><span data-stu-id="afced-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="afced-170">編寫專家的腳本！</span><span class="sxs-lookup"><span data-stu-id="afced-170">Scripting Guy!</span></span> <span data-ttu-id="afced-171">部落格。</span><span class="sxs-lookup"><span data-stu-id="afced-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="afced-172">範例</span><span class="sxs-lookup"><span data-stu-id="afced-172">Examples</span></span>

<span data-ttu-id="afced-173">下列 VBScript 會監視電腦電源狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="afced-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="afced-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="afced-174">Requirements</span></span>



| <span data-ttu-id="afced-175">需求</span><span class="sxs-lookup"><span data-stu-id="afced-175">Requirement</span></span> | <span data-ttu-id="afced-176">值</span><span class="sxs-lookup"><span data-stu-id="afced-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afced-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afced-177">Minimum supported client</span></span><br/> | <span data-ttu-id="afced-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afced-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afced-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afced-179">Minimum supported server</span></span><br/> | <span data-ttu-id="afced-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afced-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afced-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="afced-181">Namespace</span></span><br/>                | <span data-ttu-id="afced-182">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afced-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afced-183">MOF</span><span class="sxs-lookup"><span data-stu-id="afced-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afced-184"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="afced-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afced-185">DLL</span><span class="sxs-lookup"><span data-stu-id="afced-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afced-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afced-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afced-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afced-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afced-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="afced-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="afced-189">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="afced-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="afced-190">[監視電腦電源狀態的變更](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="afced-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
