---
title: Win32_TSSystemInfo 類別
description: 代表集中式發佈伺服器資訊服務。
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Win32_TSSystemInfo 類別遠端桌面服務
- Win32_TSSystemInfo 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464960"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="62ab5-105">Win32 \_ TSSystemInfo 類別</span><span class="sxs-lookup"><span data-stu-id="62ab5-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="62ab5-106">代表集中式發佈伺服器資訊服務</span><span class="sxs-lookup"><span data-stu-id="62ab5-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="62ab5-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="62ab5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ab5-108">語法</span><span class="sxs-lookup"><span data-stu-id="62ab5-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="62ab5-109">成員</span><span class="sxs-lookup"><span data-stu-id="62ab5-109">Members</span></span>

<span data-ttu-id="62ab5-110">**Win32 \_ TSSystemInfo** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="62ab5-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="62ab5-111">屬性</span><span class="sxs-lookup"><span data-stu-id="62ab5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62ab5-112">屬性</span><span class="sxs-lookup"><span data-stu-id="62ab5-112">Properties</span></span>

<span data-ttu-id="62ab5-113">**Win32 \_ TSSystemInfo** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="62ab5-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62ab5-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="62ab5-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62ab5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="62ab5-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="62ab5-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="62ab5-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62ab5-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="62ab5-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62ab5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="62ab5-123">Description of the object.</span></span>

<span data-ttu-id="62ab5-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62ab5-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62ab5-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="62ab5-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="62ab5-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="62ab5-129">The date the object was installed.</span></span> <span data-ttu-id="62ab5-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="62ab5-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="62ab5-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62ab5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="62ab5-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62ab5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="62ab5-135">The name of the object.</span></span>

<span data-ttu-id="62ab5-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62ab5-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="62ab5-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-138">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="62ab5-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-140">這個 WMI 提供者的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="62ab5-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-141">**RDUGroup**</span><span class="sxs-lookup"><span data-stu-id="62ab5-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62ab5-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-144">安全描述項定義語言 (SDDL) 格式的遠端桌面使用者群組。</span><span class="sxs-lookup"><span data-stu-id="62ab5-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="62ab5-145">**狀態**</span><span class="sxs-lookup"><span data-stu-id="62ab5-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62ab5-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="62ab5-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="62ab5-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62ab5-148">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="62ab5-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="62ab5-149">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="62ab5-149">Current status of the object.</span></span> <span data-ttu-id="62ab5-150">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="62ab5-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="62ab5-151">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="62ab5-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="62ab5-152">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="62ab5-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="62ab5-153">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="62ab5-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="62ab5-154">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="62ab5-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="62ab5-155">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="62ab5-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="62ab5-156"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-157"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-158"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-159"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-160"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-161"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-162"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="62ab5-163"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="62ab5-163">("Service")</span></span>


<span data-ttu-id="62ab5-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="62ab5-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="62ab5-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="62ab5-165">Requirements</span></span>



| <span data-ttu-id="62ab5-166">需求</span><span class="sxs-lookup"><span data-stu-id="62ab5-166">Requirement</span></span> | <span data-ttu-id="62ab5-167">值</span><span class="sxs-lookup"><span data-stu-id="62ab5-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ab5-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62ab5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="62ab5-169">都不支援</span><span class="sxs-lookup"><span data-stu-id="62ab5-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="62ab5-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62ab5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="62ab5-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62ab5-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="62ab5-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="62ab5-172">Namespace</span></span><br/>                | <span data-ttu-id="62ab5-173">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="62ab5-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="62ab5-174">MOF</span><span class="sxs-lookup"><span data-stu-id="62ab5-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ab5-175"><dt>TsAllow mof</dt></span><span class="sxs-lookup"><span data-stu-id="62ab5-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="62ab5-176">DLL</span><span class="sxs-lookup"><span data-stu-id="62ab5-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ab5-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ab5-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

