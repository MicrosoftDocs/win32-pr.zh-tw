---
title: Win32_TSVmMetadataItem 類別
description: 代表遠端桌面虛擬機器的中繼資料專案。
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataItem 類別遠端桌面服務
- Win32_TSVmMetadataItem 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933973"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="0de79-105">Win32 \_ TSVmMetadataItem 類別</span><span class="sxs-lookup"><span data-stu-id="0de79-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="0de79-106">代表遠端桌面虛擬機器的中繼資料專案。</span><span class="sxs-lookup"><span data-stu-id="0de79-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="0de79-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0de79-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de79-108">語法</span><span class="sxs-lookup"><span data-stu-id="0de79-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="0de79-109">成員</span><span class="sxs-lookup"><span data-stu-id="0de79-109">Members</span></span>

<span data-ttu-id="0de79-110">**Win32 \_ TSVmMetadataItem** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0de79-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="0de79-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0de79-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0de79-112">屬性</span><span class="sxs-lookup"><span data-stu-id="0de79-112">Properties</span></span>

<span data-ttu-id="0de79-113">**Win32 \_ TSVmMetadataItem** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0de79-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0de79-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="0de79-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0de79-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="0de79-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0de79-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="0de79-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0de79-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0de79-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de79-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="0de79-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de79-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0de79-123">Description of the object.</span></span>

<span data-ttu-id="0de79-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0de79-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de79-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0de79-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-126">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="0de79-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0de79-128">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="0de79-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0de79-129">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="0de79-129">The date the object was installed.</span></span> <span data-ttu-id="0de79-130">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="0de79-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0de79-131">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0de79-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de79-132">**名稱**</span><span class="sxs-lookup"><span data-stu-id="0de79-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0de79-135">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="0de79-135">The name of the object.</span></span>

<span data-ttu-id="0de79-136">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0de79-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de79-137">**SectionId**</span><span class="sxs-lookup"><span data-stu-id="0de79-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="0de79-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0de79-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0de79-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0de79-141">指定此專案所在之中繼資料內的區段。</span><span class="sxs-lookup"><span data-stu-id="0de79-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="0de79-142">0</span><span class="sxs-lookup"><span data-stu-id="0de79-142">0</span></span>
</dt> <dd>

<span data-ttu-id="0de79-143">設定區段。</span><span class="sxs-lookup"><span data-stu-id="0de79-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-144">1</span><span class="sxs-lookup"><span data-stu-id="0de79-144">1</span></span>
</dt> <dd>

<span data-ttu-id="0de79-145">啟蒙設定] 區段。</span><span class="sxs-lookup"><span data-stu-id="0de79-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0de79-146">**狀態**</span><span class="sxs-lookup"><span data-stu-id="0de79-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0de79-149">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="0de79-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0de79-150">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="0de79-150">Current status of the object.</span></span> <span data-ttu-id="0de79-151">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="0de79-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0de79-152">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="0de79-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0de79-153">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="0de79-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0de79-154">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="0de79-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0de79-155">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="0de79-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0de79-156">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="0de79-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0de79-157"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="0de79-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-158"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-159"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-160"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-161"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-162"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-163"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="0de79-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0de79-164"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="0de79-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0de79-165">**值**</span><span class="sxs-lookup"><span data-stu-id="0de79-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0de79-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0de79-168">屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0de79-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="0de79-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="0de79-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de79-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0de79-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0de79-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0de79-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0de79-172">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0de79-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0de79-173">虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="0de79-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0de79-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="0de79-174">Requirements</span></span>



| <span data-ttu-id="0de79-175">需求</span><span class="sxs-lookup"><span data-stu-id="0de79-175">Requirement</span></span> | <span data-ttu-id="0de79-176">值</span><span class="sxs-lookup"><span data-stu-id="0de79-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0de79-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0de79-177">Minimum supported client</span></span><br/> | <span data-ttu-id="0de79-178">都不支援</span><span class="sxs-lookup"><span data-stu-id="0de79-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="0de79-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0de79-179">Minimum supported server</span></span><br/> | <span data-ttu-id="0de79-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0de79-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="0de79-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="0de79-181">Namespace</span></span><br/>                | <span data-ttu-id="0de79-182">根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0de79-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="0de79-183">MOF</span><span class="sxs-lookup"><span data-stu-id="0de79-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0de79-184"><dt>TSVmHost mof</dt></span><span class="sxs-lookup"><span data-stu-id="0de79-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0de79-185">DLL</span><span class="sxs-lookup"><span data-stu-id="0de79-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0de79-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0de79-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

