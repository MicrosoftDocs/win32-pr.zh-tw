---
title: Win32_RDPersonalDesktopAssignment 類別
description: 個人桌面指派清單。
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Win32_RDPersonalDesktopAssignment 類別遠端桌面服務
- Win32_RDPersonalDesktopAssignment 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995577"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="d453a-105">Win32 \_ RDPersonalDesktopAssignment 類別</span><span class="sxs-lookup"><span data-stu-id="d453a-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="d453a-106">個人桌面指派清單。</span><span class="sxs-lookup"><span data-stu-id="d453a-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="d453a-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d453a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d453a-108">語法</span><span class="sxs-lookup"><span data-stu-id="d453a-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="d453a-109">成員</span><span class="sxs-lookup"><span data-stu-id="d453a-109">Members</span></span>

<span data-ttu-id="d453a-110">**Win32 \_ RDPersonalDesktopAssignment** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d453a-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="d453a-111">屬性</span><span class="sxs-lookup"><span data-stu-id="d453a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d453a-112">屬性</span><span class="sxs-lookup"><span data-stu-id="d453a-112">Properties</span></span>

<span data-ttu-id="d453a-113">**Win32 \_ RDPersonalDesktopAssignment** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d453a-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d453a-114">**標題**</span><span class="sxs-lookup"><span data-stu-id="d453a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-116">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d453a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d453a-117">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d453a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d453a-118">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="d453a-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d453a-119">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d453a-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d453a-120">**說明**</span><span class="sxs-lookup"><span data-stu-id="d453a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d453a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d453a-123">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d453a-123">Description of the object.</span></span>

<span data-ttu-id="d453a-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d453a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d453a-125">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="d453a-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d453a-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d453a-128">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d453a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d453a-129">使用者的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="d453a-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="d453a-130">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="d453a-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d453a-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d453a-133">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d453a-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d453a-134">已指派個人桌面的伺服器陣列。</span><span class="sxs-lookup"><span data-stu-id="d453a-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="d453a-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d453a-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-136">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d453a-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d453a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d453a-138">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="d453a-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d453a-139">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="d453a-139">The date the object was installed.</span></span> <span data-ttu-id="d453a-140">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d453a-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d453a-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d453a-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d453a-142">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d453a-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d453a-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d453a-145">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d453a-145">The name of the object.</span></span>

<span data-ttu-id="d453a-146">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d453a-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d453a-147">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d453a-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d453a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d453a-150">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="d453a-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d453a-151">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d453a-151">Current status of the object.</span></span> <span data-ttu-id="d453a-152">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d453a-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d453a-153">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d453a-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d453a-154">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d453a-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d453a-155">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d453a-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d453a-156">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d453a-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d453a-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d453a-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d453a-158"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d453a-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-159"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-160"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-161"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-162"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-163"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-164"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d453a-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d453a-165"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="d453a-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d453a-166">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="d453a-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d453a-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d453a-169">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d453a-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d453a-170">個人桌面已指派的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d453a-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="d453a-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="d453a-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d453a-172">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d453a-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d453a-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d453a-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d453a-174">指派的 VM 名稱。</span><span class="sxs-lookup"><span data-stu-id="d453a-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d453a-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="d453a-175">Requirements</span></span>



| <span data-ttu-id="d453a-176">需求</span><span class="sxs-lookup"><span data-stu-id="d453a-176">Requirement</span></span> | <span data-ttu-id="d453a-177">值</span><span class="sxs-lookup"><span data-stu-id="d453a-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d453a-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d453a-178">Minimum supported client</span></span><br/> | <span data-ttu-id="d453a-179">都不支援</span><span class="sxs-lookup"><span data-stu-id="d453a-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d453a-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d453a-180">Minimum supported server</span></span><br/> | <span data-ttu-id="d453a-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d453a-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="d453a-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="d453a-182">Namespace</span></span><br/>                | <span data-ttu-id="d453a-183">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d453a-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d453a-184">MOF</span><span class="sxs-lookup"><span data-stu-id="d453a-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d453a-185"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="d453a-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="d453a-186">DLL</span><span class="sxs-lookup"><span data-stu-id="d453a-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d453a-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d453a-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

