---
title: Win32_TerminalTerminalSetting 類別
description: 表示終端機與其設定之間的關聯。
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Win32_TerminalTerminalSetting 類別遠端桌面服務
- Win32_TerminalTerminalSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465096"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="934b6-105">Win32 \_ TerminalTerminalSetting 類別</span><span class="sxs-lookup"><span data-stu-id="934b6-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="934b6-106">**Win32 \_ TerminalTerminalSetting** WMI 類別代表終端機與其配置設定之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="934b6-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="934b6-107">下列語法已從 MOF 程式碼簡化，並包含所有已定義的屬性。</span><span class="sxs-lookup"><span data-stu-id="934b6-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="934b6-108">語法</span><span class="sxs-lookup"><span data-stu-id="934b6-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="934b6-109">成員</span><span class="sxs-lookup"><span data-stu-id="934b6-109">Members</span></span>

<span data-ttu-id="934b6-110">**Win32 \_ TerminalTerminalSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="934b6-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="934b6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="934b6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="934b6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="934b6-112">Properties</span></span>

<span data-ttu-id="934b6-113">**Win32 \_ TerminalTerminalSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="934b6-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="934b6-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="934b6-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="934b6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934b6-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="934b6-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="934b6-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="934b6-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="934b6-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="934b6-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="934b6-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="934b6-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="934b6-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934b6-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="934b6-123">Description of the object.</span></span>

<span data-ttu-id="934b6-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="934b6-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="934b6-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="934b6-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-126">資料類型： **Win32 \_ 終端** 機</span><span class="sxs-lookup"><span data-stu-id="934b6-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934b6-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="934b6-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="934b6-129">表示可以透過 **設定** 屬性設定的終端機。</span><span class="sxs-lookup"><span data-stu-id="934b6-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="934b6-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="934b6-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="934b6-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934b6-133">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="934b6-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="934b6-134">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="934b6-134">The date the object was installed.</span></span> <span data-ttu-id="934b6-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="934b6-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="934b6-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="934b6-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="934b6-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="934b6-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="934b6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="934b6-140">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="934b6-140">The name of the object.</span></span>

<span data-ttu-id="934b6-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="934b6-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="934b6-142">**設定**</span><span class="sxs-lookup"><span data-stu-id="934b6-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-143">資料類型： **Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="934b6-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934b6-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="934b6-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="934b6-146">表示可以套用至指定之終端機的設定。</span><span class="sxs-lookup"><span data-stu-id="934b6-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="934b6-147">**狀態**</span><span class="sxs-lookup"><span data-stu-id="934b6-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="934b6-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="934b6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="934b6-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="934b6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="934b6-150">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="934b6-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="934b6-151">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="934b6-151">Current status of the object.</span></span> <span data-ttu-id="934b6-152">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="934b6-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="934b6-153">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="934b6-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="934b6-154">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="934b6-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="934b6-155">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="934b6-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="934b6-156">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="934b6-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="934b6-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="934b6-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="934b6-158"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="934b6-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-159"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-160"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-161"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-162"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-163"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-164"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="934b6-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="934b6-165"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="934b6-165">("Service")</span></span>


<span data-ttu-id="934b6-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="934b6-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="934b6-167">備註</span><span class="sxs-lookup"><span data-stu-id="934b6-167">Remarks</span></span>

<span data-ttu-id="934b6-168">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="934b6-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="934b6-169">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="934b6-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="934b6-170">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="934b6-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="934b6-171">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="934b6-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="934b6-172">規格需求</span><span class="sxs-lookup"><span data-stu-id="934b6-172">Requirements</span></span>



| <span data-ttu-id="934b6-173">需求</span><span class="sxs-lookup"><span data-stu-id="934b6-173">Requirement</span></span> | <span data-ttu-id="934b6-174">值</span><span class="sxs-lookup"><span data-stu-id="934b6-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="934b6-175">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="934b6-175">Minimum supported client</span></span><br/> | <span data-ttu-id="934b6-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="934b6-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="934b6-177">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="934b6-177">Minimum supported server</span></span><br/> | <span data-ttu-id="934b6-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="934b6-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="934b6-179">命名空間</span><span class="sxs-lookup"><span data-stu-id="934b6-179">Namespace</span></span><br/>                | <span data-ttu-id="934b6-180">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="934b6-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="934b6-181">MOF</span><span class="sxs-lookup"><span data-stu-id="934b6-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="934b6-182"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="934b6-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="934b6-183">DLL</span><span class="sxs-lookup"><span data-stu-id="934b6-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="934b6-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="934b6-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="934b6-185">另請參閱</span><span class="sxs-lookup"><span data-stu-id="934b6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="934b6-186">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="934b6-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="934b6-187">**Win32 \_ 終端機**</span><span class="sxs-lookup"><span data-stu-id="934b6-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="934b6-188">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="934b6-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

