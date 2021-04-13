---
title: Win32_TerminalServiceToSetting 類別
description: 表示 Win32 \_ TerminalService 類別的實例與特定 Win32 TerminalServiceSetting 屬性的設定之間的關聯 \_ 。
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceToSetting 類別遠端桌面服務
- Win32_TerminalServiceToSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384538"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="80436-105">Win32 \_ TerminalServiceToSetting 類別</span><span class="sxs-lookup"><span data-stu-id="80436-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="80436-106">**Win32 \_ TerminalServiceToSetting** WMI 類別代表 [**win32 \_ TerminalService**](win32-terminalservice.md)類別的實例與特定 [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)屬性的設定之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="80436-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="80436-107">設定包括遠端桌面工作階段主機 (RD 工作階段主機) 伺服器模式、授權、Active Desktop、許可權功能、刪除暫存資料夾和暫存資料夾（每個會話）。</span><span class="sxs-lookup"><span data-stu-id="80436-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="80436-108">下列語法已從 MOF 程式碼簡化，並包含所有已定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="80436-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80436-109">語法</span><span class="sxs-lookup"><span data-stu-id="80436-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="80436-110">成員</span><span class="sxs-lookup"><span data-stu-id="80436-110">Members</span></span>

<span data-ttu-id="80436-111">**Win32 \_ TerminalServiceToSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="80436-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="80436-112">屬性</span><span class="sxs-lookup"><span data-stu-id="80436-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80436-113">屬性</span><span class="sxs-lookup"><span data-stu-id="80436-113">Properties</span></span>

<span data-ttu-id="80436-114">**Win32 \_ TerminalServiceToSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="80436-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80436-115">**標題**</span><span class="sxs-lookup"><span data-stu-id="80436-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80436-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80436-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80436-118">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="80436-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="80436-119">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="80436-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="80436-120">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="80436-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80436-121">**說明**</span><span class="sxs-lookup"><span data-stu-id="80436-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-122">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80436-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80436-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80436-124">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="80436-124">Description of the object.</span></span>

<span data-ttu-id="80436-125">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="80436-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80436-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="80436-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-127">資料類型： **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="80436-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="80436-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80436-129">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80436-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80436-130">表示可以使用 **設定** 屬性設定的 [**Win32 \_ TerminalService**](win32-terminalservice.md)實例。</span><span class="sxs-lookup"><span data-stu-id="80436-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="80436-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="80436-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-132">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="80436-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80436-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80436-134">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="80436-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="80436-135">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="80436-135">The date the object was installed.</span></span> <span data-ttu-id="80436-136">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="80436-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="80436-137">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="80436-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80436-138">**名稱**</span><span class="sxs-lookup"><span data-stu-id="80436-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80436-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80436-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80436-141">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="80436-141">The name of the object.</span></span>

<span data-ttu-id="80436-142">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="80436-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80436-143">**設定**</span><span class="sxs-lookup"><span data-stu-id="80436-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-144">資料類型： **Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="80436-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="80436-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80436-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80436-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80436-147">表示可以套用至相關聯 RD 工作階段主機伺服器的遠端桌面服務設定。</span><span class="sxs-lookup"><span data-stu-id="80436-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="80436-148">**狀態**</span><span class="sxs-lookup"><span data-stu-id="80436-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80436-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="80436-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80436-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="80436-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80436-151">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="80436-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="80436-152">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="80436-152">Current status of the object.</span></span> <span data-ttu-id="80436-153">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="80436-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="80436-154">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="80436-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="80436-155">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="80436-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="80436-156">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="80436-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="80436-157">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="80436-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="80436-158">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="80436-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="80436-159"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="80436-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-160"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-161"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-162"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-163"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-164"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-165"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="80436-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="80436-166"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="80436-166">("Service")</span></span>


<span data-ttu-id="80436-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80436-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="80436-168">備註</span><span class="sxs-lookup"><span data-stu-id="80436-168">Remarks</span></span>

<span data-ttu-id="80436-169">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="80436-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="80436-170">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="80436-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="80436-171">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="80436-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="80436-172">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="80436-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="80436-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="80436-173">Requirements</span></span>



| <span data-ttu-id="80436-174">需求</span><span class="sxs-lookup"><span data-stu-id="80436-174">Requirement</span></span> | <span data-ttu-id="80436-175">值</span><span class="sxs-lookup"><span data-stu-id="80436-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80436-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80436-176">Minimum supported client</span></span><br/> | <span data-ttu-id="80436-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80436-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80436-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80436-178">Minimum supported server</span></span><br/> | <span data-ttu-id="80436-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80436-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80436-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="80436-180">Namespace</span></span><br/>                | <span data-ttu-id="80436-181">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="80436-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="80436-182">MOF</span><span class="sxs-lookup"><span data-stu-id="80436-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80436-183"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="80436-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="80436-184">DLL</span><span class="sxs-lookup"><span data-stu-id="80436-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80436-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80436-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80436-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80436-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80436-187">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="80436-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="80436-188">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="80436-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="80436-189">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="80436-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="80436-190">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="80436-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

