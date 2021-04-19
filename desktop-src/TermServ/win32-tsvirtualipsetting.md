---
title: Win32_TSVirtualIPSetting 類別
description: 表示 Win32 \_ TerminalService 元素類別和 win32 \_ TSVirtualIP 設定類別之間的關聯。
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIPSetting 類別遠端桌面服務
- Win32_TSVirtualIPSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969138"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="32406-105">Win32 \_ TSVirtualIPSetting 類別</span><span class="sxs-lookup"><span data-stu-id="32406-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="32406-106">表示 [**win32 \_ TerminalService**](win32-terminalservice.md) 元素類別和 [**win32 \_ TSVirtualIP**](win32-tsvirtualip.md) 設定類別之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="32406-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="32406-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="32406-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32406-108">語法</span><span class="sxs-lookup"><span data-stu-id="32406-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="32406-109">成員</span><span class="sxs-lookup"><span data-stu-id="32406-109">Members</span></span>

<span data-ttu-id="32406-110">**Win32 \_ TSVirtualIPSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="32406-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="32406-111">屬性</span><span class="sxs-lookup"><span data-stu-id="32406-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32406-112">屬性</span><span class="sxs-lookup"><span data-stu-id="32406-112">Properties</span></span>

<span data-ttu-id="32406-113">**Win32 \_ TSVirtualIPSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="32406-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32406-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="32406-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="32406-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32406-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32406-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="32406-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="32406-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="32406-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="32406-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="32406-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32406-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="32406-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="32406-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32406-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32406-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="32406-123">Description of the object.</span></span>

<span data-ttu-id="32406-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="32406-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32406-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="32406-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-126">資料類型： **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="32406-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="32406-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32406-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32406-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32406-129">[**Win32 \_ TerminalService**](win32-terminalservice.md)物件的參考，這個物件是關聯的元素類別。</span><span class="sxs-lookup"><span data-stu-id="32406-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="32406-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="32406-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-131">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="32406-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="32406-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32406-133">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="32406-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="32406-134">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="32406-134">The date the object was installed.</span></span> <span data-ttu-id="32406-135">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="32406-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="32406-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="32406-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32406-137">**名稱**</span><span class="sxs-lookup"><span data-stu-id="32406-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="32406-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32406-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="32406-140">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="32406-140">The name of the object.</span></span>

<span data-ttu-id="32406-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="32406-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="32406-142">**設定**</span><span class="sxs-lookup"><span data-stu-id="32406-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-143">資料類型： **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="32406-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="32406-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32406-145">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32406-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32406-146">[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)物件的參考，這個物件是關聯的設定類別。</span><span class="sxs-lookup"><span data-stu-id="32406-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="32406-147">**狀態**</span><span class="sxs-lookup"><span data-stu-id="32406-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32406-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="32406-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32406-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="32406-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32406-150">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="32406-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="32406-151">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="32406-151">Current status of the object.</span></span> <span data-ttu-id="32406-152">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="32406-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="32406-153">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="32406-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="32406-154">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="32406-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="32406-155">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="32406-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="32406-156">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="32406-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="32406-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="32406-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="32406-158"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="32406-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-159"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-160"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-161"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-162"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-163"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-164"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="32406-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="32406-165"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="32406-165">("Service")</span></span>


<span data-ttu-id="32406-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="32406-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="32406-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="32406-167">Requirements</span></span>



| <span data-ttu-id="32406-168">需求</span><span class="sxs-lookup"><span data-stu-id="32406-168">Requirement</span></span> | <span data-ttu-id="32406-169">值</span><span class="sxs-lookup"><span data-stu-id="32406-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32406-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32406-170">Minimum supported client</span></span><br/> | <span data-ttu-id="32406-171">都不支援</span><span class="sxs-lookup"><span data-stu-id="32406-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="32406-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32406-172">Minimum supported server</span></span><br/> | <span data-ttu-id="32406-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32406-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="32406-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="32406-174">Namespace</span></span><br/>                | <span data-ttu-id="32406-175">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="32406-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="32406-176">MOF</span><span class="sxs-lookup"><span data-stu-id="32406-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32406-177"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="32406-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="32406-178">DLL</span><span class="sxs-lookup"><span data-stu-id="32406-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32406-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32406-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32406-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32406-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32406-181">**CIM \_ ElementSetting**</span><span class="sxs-lookup"><span data-stu-id="32406-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="32406-182">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="32406-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="32406-183">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="32406-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

