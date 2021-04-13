---
title: Win32_RDCentralPublishedRemoteDesktop 類別
description: 在另一部電腦上發佈的桌面，可透過終端機服務進行遠端使用。
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteDesktop 類別遠端桌面服務
- Win32_RDCentralPublishedRemoteDesktop 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464969"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="103be-105">Win32 \_ RDCentralPublishedRemoteDesktop 類別</span><span class="sxs-lookup"><span data-stu-id="103be-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="103be-106">在另一部電腦上發佈的桌面，可透過終端機服務進行遠端使用</span><span class="sxs-lookup"><span data-stu-id="103be-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="103be-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="103be-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="103be-108">語法</span><span class="sxs-lookup"><span data-stu-id="103be-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="103be-109">成員</span><span class="sxs-lookup"><span data-stu-id="103be-109">Members</span></span>

<span data-ttu-id="103be-110">**Win32 \_ RDCentralPublishedRemoteDesktop** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="103be-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="103be-111">屬性</span><span class="sxs-lookup"><span data-stu-id="103be-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="103be-112">屬性</span><span class="sxs-lookup"><span data-stu-id="103be-112">Properties</span></span>

<span data-ttu-id="103be-113">**Win32 \_ RDCentralPublishedRemoteDesktop** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="103be-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="103be-114">**別名**</span><span class="sxs-lookup"><span data-stu-id="103be-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103be-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="103be-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103be-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="103be-118">桌面的別名。</span><span class="sxs-lookup"><span data-stu-id="103be-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="103be-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="103be-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103be-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="103be-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="103be-123">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="103be-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="103be-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="103be-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="103be-125">**說明**</span><span class="sxs-lookup"><span data-stu-id="103be-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="103be-128">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="103be-128">Description of the object.</span></span>

<span data-ttu-id="103be-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="103be-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="103be-130">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="103be-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-131">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="103be-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="103be-132">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103be-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="103be-133">應顯示此資源的資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="103be-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="103be-134">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="103be-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-135">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="103be-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="103be-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103be-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="103be-137">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="103be-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="103be-138">對應到應用程式的圖示內容。</span><span class="sxs-lookup"><span data-stu-id="103be-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="103be-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="103be-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-140">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="103be-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="103be-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103be-142">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="103be-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="103be-143">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="103be-143">The date the object was installed.</span></span> <span data-ttu-id="103be-144">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="103be-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="103be-145">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="103be-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="103be-146">**名稱**</span><span class="sxs-lookup"><span data-stu-id="103be-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="103be-149">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="103be-149">The name of the object.</span></span>

<span data-ttu-id="103be-150">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="103be-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="103be-151">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="103be-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103be-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="103be-154">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="103be-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="103be-155">發佈桌面之伺服器陣列的別名。</span><span class="sxs-lookup"><span data-stu-id="103be-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="103be-156">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="103be-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="103be-159">對應于桌面之 RDP 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="103be-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="103be-160">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="103be-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-161">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="103be-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="103be-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="103be-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="103be-163">如果此應用程式應該顯示在 TS Web 存取中，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="103be-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="103be-164">**狀態**</span><span class="sxs-lookup"><span data-stu-id="103be-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="103be-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="103be-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="103be-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="103be-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="103be-167">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="103be-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="103be-168">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="103be-168">Current status of the object.</span></span> <span data-ttu-id="103be-169">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="103be-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="103be-170">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="103be-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="103be-171">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="103be-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="103be-172">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="103be-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="103be-173">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="103be-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="103be-174">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="103be-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="103be-175"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="103be-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-176"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-177"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-178"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-179"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-180"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-181"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="103be-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="103be-182"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="103be-182">("Service")</span></span>


<span data-ttu-id="103be-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="103be-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="103be-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="103be-184">Requirements</span></span>



| <span data-ttu-id="103be-185">需求</span><span class="sxs-lookup"><span data-stu-id="103be-185">Requirement</span></span> | <span data-ttu-id="103be-186">值</span><span class="sxs-lookup"><span data-stu-id="103be-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="103be-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="103be-187">Minimum supported client</span></span><br/> | <span data-ttu-id="103be-188">都不支援</span><span class="sxs-lookup"><span data-stu-id="103be-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="103be-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="103be-189">Minimum supported server</span></span><br/> | <span data-ttu-id="103be-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="103be-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="103be-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="103be-191">Namespace</span></span><br/>                | <span data-ttu-id="103be-192">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="103be-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="103be-193">MOF</span><span class="sxs-lookup"><span data-stu-id="103be-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="103be-194"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="103be-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="103be-195">DLL</span><span class="sxs-lookup"><span data-stu-id="103be-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="103be-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103be-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

