---
title: Win32_TSSessionSetting 類別
description: 定義 Win32 終端機類別的設定 \_ ，例如時間限制以及中斷連線和重新連接動作。
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting 類別遠端桌面服務
- Win32_TSSessionSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509375"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="1f6ca-105">Win32 \_ TSSessionSetting 類別</span><span class="sxs-lookup"><span data-stu-id="1f6ca-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="1f6ca-106">**Win32 \_ TSSessionSetting** WMI 類別會定義 [**win32 \_ 終端**](win32-terminal.md)機類別的設定，例如時間限制以及中斷連線和重新連接動作。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="1f6ca-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="1f6ca-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6ca-109">語法</span><span class="sxs-lookup"><span data-stu-id="1f6ca-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="1f6ca-110">成員</span><span class="sxs-lookup"><span data-stu-id="1f6ca-110">Members</span></span>

<span data-ttu-id="1f6ca-111">**Win32 \_ TSSessionSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1f6ca-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="1f6ca-112">方法</span><span class="sxs-lookup"><span data-stu-id="1f6ca-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f6ca-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1f6ca-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f6ca-114">方法</span><span class="sxs-lookup"><span data-stu-id="1f6ca-114">Methods</span></span>

<span data-ttu-id="1f6ca-115">**Win32 \_ TSSessionSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="1f6ca-116">方法</span><span class="sxs-lookup"><span data-stu-id="1f6ca-116">Method</span></span>                                                              | <span data-ttu-id="1f6ca-117">描述</span><span class="sxs-lookup"><span data-stu-id="1f6ca-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="1f6ca-118">**BrokenConnection**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="1f6ca-119">設定包含在此類別中的中斷連接屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="1f6ca-120">**TimeLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="1f6ca-121">設定這個類別中包含的時間限制屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="1f6ca-122">屬性</span><span class="sxs-lookup"><span data-stu-id="1f6ca-122">Properties</span></span>

<span data-ttu-id="1f6ca-123">**Win32 \_ TSSessionSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f6ca-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-125">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-127">配置給作用中會話的最大時間量（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="1f6ca-128">值為0會指定無限的時間量。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-132">當連線因為網路遺失或超過時間限制而中斷時，伺服器在會話上所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="1f6ca-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**中斷** (0) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-134">使用者已與會話中斷連線。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="1f6ca-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (1) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-136">從伺服器中永久刪除會話。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-137">**BrokenConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1f6ca-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-140">伺服器用來判斷何時中斷連線，因為網路遺失或超過時間限制的原則。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="1f6ca-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-142">伺服器會覆寫使用者的中斷連接原則設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="1f6ca-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-144">使用者的中斷連線原則設定有效。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-145">**標題**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-148">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-149">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1f6ca-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-151">**說明**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-154">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-154">Description of the object.</span></span>

<span data-ttu-id="1f6ca-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-159">中斷連線的會話終止的時間間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="1f6ca-160">值為0會指定無限的時間量。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-161">**EnableTimeoutWarning**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1f6ca-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-164">啟用超時警告。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-164">Enables the timeout warning.</span></span>

<span data-ttu-id="1f6ca-165">**Windows 7、Windows server 2008 R2、Windows Vista 和 Windows server 2008：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-167">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-169">閒置會話終止的時間間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="1f6ca-170">值為0會指定無限的時間量。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-172">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-174">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="1f6ca-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-175">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-175">The date the object was installed.</span></span> <span data-ttu-id="1f6ca-176">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1f6ca-177">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-178">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-181">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-181">The name of the object.</span></span>

<span data-ttu-id="1f6ca-182">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-183">**PolicySourceActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-184">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-186">指出 **ActiveSessionLimit** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1f6ca-187">0</span><span class="sxs-lookup"><span data-stu-id="1f6ca-187">0</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-188">伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-189">1</span><span class="sxs-lookup"><span data-stu-id="1f6ca-189">1</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-190">群組原則</span><span class="sxs-lookup"><span data-stu-id="1f6ca-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-191">2</span><span class="sxs-lookup"><span data-stu-id="1f6ca-191">2</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-192">預設</span><span class="sxs-lookup"><span data-stu-id="1f6ca-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-194">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-196">指出 **BrokenConnectionAction** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1f6ca-197">0</span><span class="sxs-lookup"><span data-stu-id="1f6ca-197">0</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-198">伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-199">1</span><span class="sxs-lookup"><span data-stu-id="1f6ca-199">1</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-200">群組原則</span><span class="sxs-lookup"><span data-stu-id="1f6ca-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-201">2</span><span class="sxs-lookup"><span data-stu-id="1f6ca-201">2</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-202">預設</span><span class="sxs-lookup"><span data-stu-id="1f6ca-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-204">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-206">指出 **DisconnectedSessionLimit** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1f6ca-207">0</span><span class="sxs-lookup"><span data-stu-id="1f6ca-207">0</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-208">伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-209">1</span><span class="sxs-lookup"><span data-stu-id="1f6ca-209">1</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-210">群組原則</span><span class="sxs-lookup"><span data-stu-id="1f6ca-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-211">2</span><span class="sxs-lookup"><span data-stu-id="1f6ca-211">2</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-212">預設</span><span class="sxs-lookup"><span data-stu-id="1f6ca-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-213">**PolicySourceIdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-214">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-216">指出 **IdleSessionLimit** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1f6ca-217">0</span><span class="sxs-lookup"><span data-stu-id="1f6ca-217">0</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-218">伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-219">1</span><span class="sxs-lookup"><span data-stu-id="1f6ca-219">1</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-220">群組原則</span><span class="sxs-lookup"><span data-stu-id="1f6ca-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-221">2</span><span class="sxs-lookup"><span data-stu-id="1f6ca-221">2</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-222">預設</span><span class="sxs-lookup"><span data-stu-id="1f6ca-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-223">**PolicySourceReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-224">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-226">指出 **ReconnectPolicy** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="1f6ca-227">0</span><span class="sxs-lookup"><span data-stu-id="1f6ca-227">0</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-228">伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-229">1</span><span class="sxs-lookup"><span data-stu-id="1f6ca-229">1</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-230">群組原則</span><span class="sxs-lookup"><span data-stu-id="1f6ca-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-231">2</span><span class="sxs-lookup"><span data-stu-id="1f6ca-231">2</span></span>
</dt> <dd>

<span data-ttu-id="1f6ca-232">預設</span><span class="sxs-lookup"><span data-stu-id="1f6ca-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-233">**ReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-234">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1f6ca-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-236">指定使用者是否必須使用先前的用戶端重新連線至已中斷連線的會話。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="1f6ca-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**任何用戶端** (0) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-238">任何用戶端都將用來重新連接。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="1f6ca-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**先前的用戶端** (1) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-240">連接中使用的先前用戶端會用來重新連接。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-241">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-242">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-243">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-244">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-245">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-245">Current status of the object.</span></span> <span data-ttu-id="1f6ca-246">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1f6ca-247">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1f6ca-248">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1f6ca-249">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1f6ca-250">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1f6ca-251">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1f6ca-252"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-253"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-254"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-255"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-256"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-257"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-258"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1f6ca-259"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f6ca-260">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f6ca-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-263">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-263">The name of the terminal.</span></span>

<span data-ttu-id="1f6ca-264">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f6ca-265">**TimeLimitPolicy**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f6ca-266">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f6ca-267">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1f6ca-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1f6ca-268">伺服器用來判斷使用者會話時間限制的原則。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="1f6ca-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-270">使用者的時間限制原則設定生效。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="1f6ca-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**伺服器覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="1f6ca-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1f6ca-272">伺服器會覆寫使用者的時間限制原則設定。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f6ca-273">備註</span><span class="sxs-lookup"><span data-stu-id="1f6ca-273">Remarks</span></span>

<span data-ttu-id="1f6ca-274">請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="1f6ca-275">如果嘗試將 "Console" 指定為 TerminalName 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="1f6ca-276">如果視窗工作站嘗試呼叫此物件的方法，以新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，則也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="1f6ca-277">若要連接到「根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway」命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="1f6ca-278">針對 C/c + + 呼叫，這會是 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="1f6ca-279">針對 Visual Basic 和腳本呼叫，這會是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="1f6ca-280">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="1f6ca-281">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f6ca-282">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1f6ca-283">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f6ca-284">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="1f6ca-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6ca-285">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f6ca-285">Requirements</span></span>



| <span data-ttu-id="1f6ca-286">需求</span><span class="sxs-lookup"><span data-stu-id="1f6ca-286">Requirement</span></span> | <span data-ttu-id="1f6ca-287">值</span><span class="sxs-lookup"><span data-stu-id="1f6ca-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6ca-288">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f6ca-288">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6ca-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f6ca-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f6ca-290">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f6ca-290">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6ca-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f6ca-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f6ca-292">命名空間</span><span class="sxs-lookup"><span data-stu-id="1f6ca-292">Namespace</span></span><br/>                | <span data-ttu-id="1f6ca-293">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="1f6ca-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1f6ca-294">MOF</span><span class="sxs-lookup"><span data-stu-id="1f6ca-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f6ca-295"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ca-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f6ca-296">DLL</span><span class="sxs-lookup"><span data-stu-id="1f6ca-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f6ca-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ca-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6ca-298">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f6ca-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f6ca-299">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="1f6ca-300">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="1f6ca-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

