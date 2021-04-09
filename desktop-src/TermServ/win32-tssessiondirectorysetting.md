---
title: Win32_TSSessionDirectorySetting 類別
description: 表示 Win32 \_ TerminalService 類別的實例與 win32 TSSessionDirectory 類別的實例之間的關聯 \_ 。
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectorySetting 類別遠端桌面服務
- Win32_TSSessionDirectorySetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024684"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="f3173-105">Win32 \_ TSSessionDirectorySetting 類別</span><span class="sxs-lookup"><span data-stu-id="f3173-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="f3173-106">表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 類別的實例與 [**win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) 類別的實例之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="f3173-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="f3173-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3173-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3173-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3173-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="f3173-109">成員</span><span class="sxs-lookup"><span data-stu-id="f3173-109">Members</span></span>

<span data-ttu-id="f3173-110">**Win32 \_ TSSessionDirectorySetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3173-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f3173-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f3173-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3173-112">屬性</span><span class="sxs-lookup"><span data-stu-id="f3173-112">Properties</span></span>

<span data-ttu-id="f3173-113">**Win32 \_ TSSessionDirectorySetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3173-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3173-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="f3173-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3173-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3173-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="f3173-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3173-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="f3173-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f3173-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3173-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3173-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="f3173-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3173-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3173-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="f3173-123">Description of the object.</span></span>

<span data-ttu-id="f3173-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3173-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3173-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3173-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-126">資料類型： **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="f3173-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3173-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3173-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3173-129">表示可以使用 **設定** 屬性設定的 **Win32 \_ TerminalService** 實例。</span><span class="sxs-lookup"><span data-stu-id="f3173-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="f3173-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3173-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="f3173-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3173-133">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="f3173-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f3173-134">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="f3173-134">The date the object was installed.</span></span> <span data-ttu-id="f3173-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="f3173-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3173-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3173-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3173-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f3173-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3173-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3173-140">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3173-140">The name of the object.</span></span>

<span data-ttu-id="f3173-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3173-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3173-142">**設定**</span><span class="sxs-lookup"><span data-stu-id="f3173-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-143">資料類型： **Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="f3173-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3173-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3173-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3173-146">表示可以套用至相關聯 RD 工作階段主機伺服器的 RD 連線代理人設定。</span><span class="sxs-lookup"><span data-stu-id="f3173-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="f3173-147">**狀態**</span><span class="sxs-lookup"><span data-stu-id="f3173-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3173-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3173-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3173-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3173-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3173-150">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="f3173-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f3173-151">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="f3173-151">Current status of the object.</span></span> <span data-ttu-id="f3173-152">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="f3173-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f3173-153">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="f3173-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f3173-154">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="f3173-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3173-155">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="f3173-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3173-156">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="f3173-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3173-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="f3173-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f3173-158"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="f3173-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-159"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-160"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-161"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-162"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-163"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-164"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="f3173-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3173-165"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="f3173-165">("Service")</span></span>


<span data-ttu-id="f3173-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f3173-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f3173-167">備註</span><span class="sxs-lookup"><span data-stu-id="f3173-167">Remarks</span></span>

<span data-ttu-id="f3173-168">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f3173-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3173-169">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f3173-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3173-170">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f3173-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3173-171">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="f3173-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3173-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3173-172">Requirements</span></span>



| <span data-ttu-id="f3173-173">需求</span><span class="sxs-lookup"><span data-stu-id="f3173-173">Requirement</span></span> | <span data-ttu-id="f3173-174">值</span><span class="sxs-lookup"><span data-stu-id="f3173-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3173-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3173-175">Minimum supported client</span></span><br/> | <span data-ttu-id="f3173-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3173-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3173-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3173-177">Minimum supported server</span></span><br/> | <span data-ttu-id="f3173-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3173-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3173-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3173-179">Namespace</span></span><br/>                | <span data-ttu-id="f3173-180">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f3173-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="f3173-181">MOF</span><span class="sxs-lookup"><span data-stu-id="f3173-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3173-182"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3173-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3173-183">DLL</span><span class="sxs-lookup"><span data-stu-id="f3173-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3173-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3173-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3173-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3173-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3173-186">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="f3173-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="f3173-187">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="f3173-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f3173-188">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="f3173-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

