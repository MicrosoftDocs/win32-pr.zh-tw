---
title: Win32_TSRemoteControlSetting 類別
description: 定義 Win32 終端機類別的遠端控制設定 \_ 。
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteControlSetting 類別遠端桌面服務
- Win32_TSRemoteControlSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465545"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="f15cd-105">Win32 \_ TSRemoteControlSetting 類別</span><span class="sxs-lookup"><span data-stu-id="f15cd-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="f15cd-106">**Win32 \_ TSRemoteControlSetting** WMI 類別會定義 [**win32 \_ 終端**](win32-terminal.md)機類別的遠端控制設定。</span><span class="sxs-lookup"><span data-stu-id="f15cd-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="f15cd-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f15cd-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f15cd-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="f15cd-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15cd-109">語法</span><span class="sxs-lookup"><span data-stu-id="f15cd-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="f15cd-110">成員</span><span class="sxs-lookup"><span data-stu-id="f15cd-110">Members</span></span>

<span data-ttu-id="f15cd-111">**Win32 \_ TSRemoteControlSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f15cd-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f15cd-112">方法</span><span class="sxs-lookup"><span data-stu-id="f15cd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f15cd-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f15cd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f15cd-114">方法</span><span class="sxs-lookup"><span data-stu-id="f15cd-114">Methods</span></span>

<span data-ttu-id="f15cd-115">**Win32 \_ TSRemoteControlSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f15cd-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="f15cd-116">方法</span><span class="sxs-lookup"><span data-stu-id="f15cd-116">Method</span></span>                                                              | <span data-ttu-id="f15cd-117">描述</span><span class="sxs-lookup"><span data-stu-id="f15cd-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="f15cd-118">**RemoteControl**</span><span class="sxs-lookup"><span data-stu-id="f15cd-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="f15cd-119">設定這個類別的 **LevelOfControl** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f15cd-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f15cd-120">屬性</span><span class="sxs-lookup"><span data-stu-id="f15cd-120">Properties</span></span>

<span data-ttu-id="f15cd-121">**Win32 \_ TSRemoteControlSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f15cd-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f15cd-122">**標題**</span><span class="sxs-lookup"><span data-stu-id="f15cd-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f15cd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-125">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f15cd-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-126">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="f15cd-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f15cd-127">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-128">**說明**</span><span class="sxs-lookup"><span data-stu-id="f15cd-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f15cd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-131">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f15cd-131">Description of the object.</span></span>

<span data-ttu-id="f15cd-132">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f15cd-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-134">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f15cd-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-136">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="f15cd-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-137">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="f15cd-137">The date the object was installed.</span></span> <span data-ttu-id="f15cd-138">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f15cd-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f15cd-139">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-140">**LevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="f15cd-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-141">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f15cd-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-143">會話的控制層級，指定會話是否只會由遠端使用者查看，或透過鍵盤和滑鼠來查看及控制。</span><span class="sxs-lookup"><span data-stu-id="f15cd-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="f15cd-144">如需詳細資訊，請參閱 [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) 方法的備註一節。</span><span class="sxs-lookup"><span data-stu-id="f15cd-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="f15cd-145">支援下列值。</span><span class="sxs-lookup"><span data-stu-id="f15cd-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="f15cd-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (0) </span><span class="sxs-lookup"><span data-stu-id="f15cd-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-147">遠端控制已停用。</span><span class="sxs-lookup"><span data-stu-id="f15cd-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="f15cd-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1) </span><span class="sxs-lookup"><span data-stu-id="f15cd-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-149">遠端控制的使用者可以完全掌控使用者的會話，以及使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="f15cd-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="f15cd-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2) </span><span class="sxs-lookup"><span data-stu-id="f15cd-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-151">遠端控制的使用者可以完全掌控使用者的會話;不需要使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="f15cd-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="f15cd-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3) </span><span class="sxs-lookup"><span data-stu-id="f15cd-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-153">遠端控制的使用者可以從遠端使用使用者的許可權來查看會話;遠端使用者無法主動控制會話。</span><span class="sxs-lookup"><span data-stu-id="f15cd-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="f15cd-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4) </span><span class="sxs-lookup"><span data-stu-id="f15cd-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-155">遠端控制的使用者可以從遠端查看會話，但不能主動控制會話;不需要使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="f15cd-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f15cd-156">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f15cd-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f15cd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-159">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f15cd-159">The name of the object.</span></span>

<span data-ttu-id="f15cd-160">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-161">**PolicySourceLevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="f15cd-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-162">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f15cd-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-164">指出 **LevelOfControl** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="f15cd-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="f15cd-165">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="f15cd-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f15cd-166">伺服器</span><span class="sxs-lookup"><span data-stu-id="f15cd-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-167">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="f15cd-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f15cd-168">群組原則</span><span class="sxs-lookup"><span data-stu-id="f15cd-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="f15cd-169">2 (0x2) </span><span class="sxs-lookup"><span data-stu-id="f15cd-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f15cd-170">預設</span><span class="sxs-lookup"><span data-stu-id="f15cd-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f15cd-171">**RemoteControlPolicy**</span><span class="sxs-lookup"><span data-stu-id="f15cd-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f15cd-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f15cd-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-174">伺服器用來取得遠端控制設定的原則。</span><span class="sxs-lookup"><span data-stu-id="f15cd-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="f15cd-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="f15cd-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-176">使用者的遠端控制設定有效。</span><span class="sxs-lookup"><span data-stu-id="f15cd-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="f15cd-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="f15cd-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f15cd-178">伺服器會覆寫使用者的遠端控制設定。</span><span class="sxs-lookup"><span data-stu-id="f15cd-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f15cd-179">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f15cd-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f15cd-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-182">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="f15cd-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-183">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f15cd-183">Current status of the object.</span></span> <span data-ttu-id="f15cd-184">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f15cd-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f15cd-185">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f15cd-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f15cd-186">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f15cd-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f15cd-187">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f15cd-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f15cd-188">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f15cd-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f15cd-189">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f15cd-190"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-191"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-192"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-193"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-194"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-195"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-196"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f15cd-197"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="f15cd-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f15cd-198">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="f15cd-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f15cd-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f15cd-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f15cd-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f15cd-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f15cd-201">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="f15cd-201">The name of the terminal.</span></span>

<span data-ttu-id="f15cd-202">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f15cd-203">備註</span><span class="sxs-lookup"><span data-stu-id="f15cd-203">Remarks</span></span>

<span data-ttu-id="f15cd-204">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="f15cd-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f15cd-205">針對 C/c + + 呼叫，這會是 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="f15cd-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f15cd-206">針對 Visual Basic 和腳本呼叫，這會是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="f15cd-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f15cd-207">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="f15cd-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f15cd-208">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f15cd-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f15cd-209">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f15cd-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f15cd-210">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f15cd-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f15cd-211">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f15cd-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f15cd-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="f15cd-212">Requirements</span></span>



| <span data-ttu-id="f15cd-213">需求</span><span class="sxs-lookup"><span data-stu-id="f15cd-213">Requirement</span></span> | <span data-ttu-id="f15cd-214">值</span><span class="sxs-lookup"><span data-stu-id="f15cd-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f15cd-215">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f15cd-215">Minimum supported client</span></span><br/> | <span data-ttu-id="f15cd-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f15cd-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f15cd-217">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f15cd-217">Minimum supported server</span></span><br/> | <span data-ttu-id="f15cd-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f15cd-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f15cd-219">命名空間</span><span class="sxs-lookup"><span data-stu-id="f15cd-219">Namespace</span></span><br/>                | <span data-ttu-id="f15cd-220">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="f15cd-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f15cd-221">MOF</span><span class="sxs-lookup"><span data-stu-id="f15cd-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f15cd-222"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="f15cd-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f15cd-223">DLL</span><span class="sxs-lookup"><span data-stu-id="f15cd-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f15cd-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f15cd-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15cd-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f15cd-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15cd-226">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="f15cd-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="f15cd-227">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="f15cd-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

