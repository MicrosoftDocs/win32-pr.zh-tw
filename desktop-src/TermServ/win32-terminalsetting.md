---
title: Win32_TerminalSetting 類別
description: 表示可以套用至終端機的設定。
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Win32_TerminalSetting 類別遠端桌面服務
- Win32_TerminalSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968789"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="5bd74-105">Win32 \_ TerminalSetting 類別</span><span class="sxs-lookup"><span data-stu-id="5bd74-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="5bd74-106">**Win32 \_ TerminalSetting** WMI 類別代表可以套用至終端機的設定。</span><span class="sxs-lookup"><span data-stu-id="5bd74-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="5bd74-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd74-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd74-108">語法</span><span class="sxs-lookup"><span data-stu-id="5bd74-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="5bd74-109">成員</span><span class="sxs-lookup"><span data-stu-id="5bd74-109">Members</span></span>

<span data-ttu-id="5bd74-110">**Win32 \_ TerminalSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5bd74-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="5bd74-111">屬性</span><span class="sxs-lookup"><span data-stu-id="5bd74-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bd74-112">屬性</span><span class="sxs-lookup"><span data-stu-id="5bd74-112">Properties</span></span>

<span data-ttu-id="5bd74-113">**Win32 \_ TerminalSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5bd74-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bd74-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="5bd74-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd74-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="5bd74-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="5bd74-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5bd74-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bd74-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="5bd74-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd74-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="5bd74-123">Description of the object.</span></span>

<span data-ttu-id="5bd74-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bd74-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5bd74-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="5bd74-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="5bd74-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="5bd74-129">The date the object was installed.</span></span> <span data-ttu-id="5bd74-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="5bd74-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5bd74-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bd74-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="5bd74-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd74-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd74-135">The name of the object.</span></span>

<span data-ttu-id="5bd74-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bd74-137">**狀態**</span><span class="sxs-lookup"><span data-stu-id="5bd74-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd74-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-140">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="5bd74-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-141">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="5bd74-141">Current status of the object.</span></span> <span data-ttu-id="5bd74-142">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="5bd74-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5bd74-143">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="5bd74-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5bd74-144">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="5bd74-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5bd74-145">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="5bd74-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5bd74-146">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="5bd74-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5bd74-147">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5bd74-148"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-149"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-150"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-151"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-152"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-153"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-154"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5bd74-155"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="5bd74-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bd74-156">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="5bd74-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bd74-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5bd74-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bd74-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5bd74-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bd74-159">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd74-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bd74-160">備註</span><span class="sxs-lookup"><span data-stu-id="5bd74-160">Remarks</span></span>

<span data-ttu-id="5bd74-161">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5bd74-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5bd74-162">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5bd74-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5bd74-163">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5bd74-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5bd74-164">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="5bd74-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd74-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bd74-165">Requirements</span></span>



| <span data-ttu-id="5bd74-166">需求</span><span class="sxs-lookup"><span data-stu-id="5bd74-166">Requirement</span></span> | <span data-ttu-id="5bd74-167">值</span><span class="sxs-lookup"><span data-stu-id="5bd74-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd74-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5bd74-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd74-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bd74-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5bd74-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5bd74-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd74-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bd74-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5bd74-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="5bd74-172">Namespace</span></span><br/>                | <span data-ttu-id="5bd74-173">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="5bd74-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5bd74-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5bd74-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bd74-175"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bd74-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bd74-176">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd74-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd74-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bd74-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd74-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bd74-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd74-179">**CIM \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="5bd74-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="5bd74-180">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="5bd74-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5bd74-181">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="5bd74-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

