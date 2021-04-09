---
title: Win32_Terminal 類別
description: 表示終端。
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal 類別遠端桌面服務
- Win32_Terminal 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094096"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="f2de7-105">Win32 \_ 終端機類別</span><span class="sxs-lookup"><span data-stu-id="f2de7-105">Win32\_Terminal class</span></span>

<span data-ttu-id="f2de7-106">**Win32 \_ 終端** 機 WMI 類別代表終端機。</span><span class="sxs-lookup"><span data-stu-id="f2de7-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="f2de7-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f2de7-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f2de7-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="f2de7-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2de7-109">語法</span><span class="sxs-lookup"><span data-stu-id="f2de7-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="f2de7-110">成員</span><span class="sxs-lookup"><span data-stu-id="f2de7-110">Members</span></span>

<span data-ttu-id="f2de7-111">**Win32 \_ 終端** 機類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f2de7-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="f2de7-112">方法</span><span class="sxs-lookup"><span data-stu-id="f2de7-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f2de7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f2de7-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f2de7-114">方法</span><span class="sxs-lookup"><span data-stu-id="f2de7-114">Methods</span></span>

<span data-ttu-id="f2de7-115">**Win32 \_ 終端** 機類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f2de7-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="f2de7-116">方法</span><span class="sxs-lookup"><span data-stu-id="f2de7-116">Method</span></span>                                  | <span data-ttu-id="f2de7-117">描述</span><span class="sxs-lookup"><span data-stu-id="f2de7-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2de7-118">**創建**</span><span class="sxs-lookup"><span data-stu-id="f2de7-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="f2de7-119">使用 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) 類別的屬性和方法，建立具有預設設定的終端機，這些設定可以自訂。</span><span class="sxs-lookup"><span data-stu-id="f2de7-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="f2de7-120">**刪除**</span><span class="sxs-lookup"><span data-stu-id="f2de7-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="f2de7-121">刪除指定的終端機。</span><span class="sxs-lookup"><span data-stu-id="f2de7-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="f2de7-122">**啟用**</span><span class="sxs-lookup"><span data-stu-id="f2de7-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="f2de7-123">停用或啟用終端機。</span><span class="sxs-lookup"><span data-stu-id="f2de7-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="f2de7-124">**重新命名**</span><span class="sxs-lookup"><span data-stu-id="f2de7-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="f2de7-125">重新命名終端機。</span><span class="sxs-lookup"><span data-stu-id="f2de7-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="f2de7-126">屬性</span><span class="sxs-lookup"><span data-stu-id="f2de7-126">Properties</span></span>

<span data-ttu-id="f2de7-127">**Win32 \_ 終端** 機類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f2de7-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2de7-128">**標題**</span><span class="sxs-lookup"><span data-stu-id="f2de7-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2de7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-131">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f2de7-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-132">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="f2de7-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f2de7-133">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2de7-134">**說明**</span><span class="sxs-lookup"><span data-stu-id="f2de7-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2de7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-137">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f2de7-137">Description of the object.</span></span>

<span data-ttu-id="f2de7-138">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2de7-139">**fEnableTerminal**</span><span class="sxs-lookup"><span data-stu-id="f2de7-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f2de7-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-142">指定指定的終端機是否已停用或啟用。</span><span class="sxs-lookup"><span data-stu-id="f2de7-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="f2de7-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0) </span><span class="sxs-lookup"><span data-stu-id="f2de7-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f2de7-144">終端機已停用。</span><span class="sxs-lookup"><span data-stu-id="f2de7-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="f2de7-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1) </span><span class="sxs-lookup"><span data-stu-id="f2de7-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f2de7-146">終端機已啟用。</span><span class="sxs-lookup"><span data-stu-id="f2de7-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f2de7-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f2de7-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-148">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f2de7-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-150">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="f2de7-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-151">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="f2de7-151">The date the object was installed.</span></span> <span data-ttu-id="f2de7-152">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f2de7-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f2de7-153">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2de7-154">**LoggedOnUsers**</span><span class="sxs-lookup"><span data-stu-id="f2de7-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-155">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f2de7-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-156">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-157">終端機的已登入會話數目。</span><span class="sxs-lookup"><span data-stu-id="f2de7-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="f2de7-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f2de7-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2de7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-161">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2de7-161">The name of the object.</span></span>

<span data-ttu-id="f2de7-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2de7-163">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f2de7-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2de7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-166">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="f2de7-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-167">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f2de7-167">Current status of the object.</span></span> <span data-ttu-id="f2de7-168">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f2de7-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f2de7-169">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f2de7-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f2de7-170">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f2de7-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f2de7-171">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f2de7-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f2de7-172">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f2de7-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f2de7-173">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f2de7-174"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-175"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-176"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-177"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-178"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-179"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-180"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f2de7-181"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="f2de7-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f2de7-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="f2de7-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2de7-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2de7-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f2de7-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2de7-185">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2de7-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2de7-186">識別終端機實例的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="f2de7-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2de7-187">備註</span><span class="sxs-lookup"><span data-stu-id="f2de7-187">Remarks</span></span>

<span data-ttu-id="f2de7-188">**Win32 \_終端** 機與 [**win32 \_ TerminalSetting**](win32-terminalsetting.md)相關聯，作為 [**win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md)關聯的 **Element** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f2de7-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="f2de7-189">下列類別是 **win32 \_ 終端** 機類別的子類別： [**win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)、 [**win32 \_ TSLogonSetting**](win32-tslogonsetting.md)、 [**win32 \_ TSSessionSetting**](win32-tssessionsetting.md)、 [**win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)、 [**win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md)、 [**win32 \_ TSClientSetting**](win32-tsclientsetting.md)、 [**win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)、 [**win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)、 [**win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)和 [**win32 \_ TSAccount**](win32-tsaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="f2de7-190">請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="f2de7-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="f2de7-191">如果嘗試將 "Console" 指定為 **TerminalName** 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="f2de7-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="f2de7-192">如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f2de7-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="f2de7-193">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="f2de7-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f2de7-194">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="f2de7-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f2de7-195">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="f2de7-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f2de7-196">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f2de7-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f2de7-197">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f2de7-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f2de7-198">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2de7-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f2de7-199">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f2de7-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f2de7-200">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f2de7-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2de7-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2de7-201">Requirements</span></span>



| <span data-ttu-id="f2de7-202">需求</span><span class="sxs-lookup"><span data-stu-id="f2de7-202">Requirement</span></span> | <span data-ttu-id="f2de7-203">值</span><span class="sxs-lookup"><span data-stu-id="f2de7-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2de7-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2de7-204">Minimum supported client</span></span><br/> | <span data-ttu-id="f2de7-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2de7-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2de7-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2de7-206">Minimum supported server</span></span><br/> | <span data-ttu-id="f2de7-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2de7-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2de7-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="f2de7-208">Namespace</span></span><br/>                | <span data-ttu-id="f2de7-209">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f2de7-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f2de7-210">MOF</span><span class="sxs-lookup"><span data-stu-id="f2de7-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2de7-211"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2de7-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2de7-212">DLL</span><span class="sxs-lookup"><span data-stu-id="f2de7-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2de7-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2de7-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2de7-214">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2de7-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2de7-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f2de7-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="f2de7-216">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="f2de7-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f2de7-217">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="f2de7-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 

