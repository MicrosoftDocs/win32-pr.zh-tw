---
title: Win32_RDCentralPublishedRemoteApplication 類別
description: 描述在另一部電腦上發佈的應用程式，以透過終端機服務進行遠端使用。
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteApplication 類別遠端桌面服務
- Win32_RDCentralPublishedRemoteApplication 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934240"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="35a07-105">Win32 \_ RDCentralPublishedRemoteApplication 類別</span><span class="sxs-lookup"><span data-stu-id="35a07-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="35a07-106">描述在另一部電腦上發佈的應用程式，以透過終端機服務進行遠端使用。</span><span class="sxs-lookup"><span data-stu-id="35a07-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="35a07-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35a07-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a07-108">語法</span><span class="sxs-lookup"><span data-stu-id="35a07-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="35a07-109">成員</span><span class="sxs-lookup"><span data-stu-id="35a07-109">Members</span></span>

<span data-ttu-id="35a07-110">**Win32 \_ RDCentralPublishedRemoteApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35a07-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="35a07-111">屬性</span><span class="sxs-lookup"><span data-stu-id="35a07-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35a07-112">屬性</span><span class="sxs-lookup"><span data-stu-id="35a07-112">Properties</span></span>

<span data-ttu-id="35a07-113">**Win32 \_ RDCentralPublishedRemoteApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35a07-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35a07-114">**別名**</span><span class="sxs-lookup"><span data-stu-id="35a07-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35a07-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35a07-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-118">應用程式的別名。</span><span class="sxs-lookup"><span data-stu-id="35a07-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="35a07-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-122">AppID 可用來在用戶端上進行釘選。</span><span class="sxs-lookup"><span data-stu-id="35a07-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-123">**標題**</span><span class="sxs-lookup"><span data-stu-id="35a07-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a07-126">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="35a07-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-127">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="35a07-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="35a07-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a07-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a07-129">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="35a07-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="35a07-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-132">此應用程式是否需要命令列引數。</span><span class="sxs-lookup"><span data-stu-id="35a07-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="35a07-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0) </span><span class="sxs-lookup"><span data-stu-id="35a07-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="35a07-134">不允許</span><span class="sxs-lookup"><span data-stu-id="35a07-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="35a07-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**允許** (1) </span><span class="sxs-lookup"><span data-stu-id="35a07-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="35a07-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**需要** (2) </span><span class="sxs-lookup"><span data-stu-id="35a07-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35a07-137">**說明**</span><span class="sxs-lookup"><span data-stu-id="35a07-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35a07-140">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="35a07-140">Description of the object.</span></span>

<span data-ttu-id="35a07-141">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a07-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a07-142">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="35a07-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-143">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="35a07-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35a07-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-145">應顯示此資源的資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="35a07-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-146">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="35a07-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-147">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="35a07-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="35a07-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35a07-149">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35a07-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-150">對應到應用程式的圖示內容。</span><span class="sxs-lookup"><span data-stu-id="35a07-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35a07-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-152">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="35a07-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a07-154">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="35a07-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="35a07-155">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="35a07-155">The date the object was installed.</span></span> <span data-ttu-id="35a07-156">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="35a07-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="35a07-157">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a07-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a07-158">**名稱**</span><span class="sxs-lookup"><span data-stu-id="35a07-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35a07-161">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="35a07-161">The name of the object.</span></span>

<span data-ttu-id="35a07-162">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a07-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a07-163">**路徑**</span><span class="sxs-lookup"><span data-stu-id="35a07-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-166">應用程式的路徑</span><span class="sxs-lookup"><span data-stu-id="35a07-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="35a07-167">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="35a07-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35a07-170">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35a07-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-171">發佈應用程式之伺服器陣列的別名</span><span class="sxs-lookup"><span data-stu-id="35a07-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="35a07-172">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="35a07-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35a07-175">對應于應用程式之 RDP 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="35a07-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-176">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="35a07-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-179">此應用程式所需的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="35a07-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="35a07-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-181">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-182">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35a07-183">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="35a07-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-184">控制應用程式存取的安全描述項（SDDL 格式）。</span><span class="sxs-lookup"><span data-stu-id="35a07-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="35a07-185">空字串表示允許所有存取。</span><span class="sxs-lookup"><span data-stu-id="35a07-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-186">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="35a07-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-187">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="35a07-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-188">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-189">如果此應用程式應該顯示在 TS Web 存取中，則 **為 true** ;否則 **為 false**。</span><span class="sxs-lookup"><span data-stu-id="35a07-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="35a07-190">**狀態**</span><span class="sxs-lookup"><span data-stu-id="35a07-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-192">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35a07-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35a07-193">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="35a07-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="35a07-194">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="35a07-194">Current status of the object.</span></span> <span data-ttu-id="35a07-195">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="35a07-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="35a07-196">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="35a07-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="35a07-197">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="35a07-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35a07-198">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="35a07-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35a07-199">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="35a07-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35a07-200">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="35a07-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="35a07-201"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="35a07-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-202"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-203"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-204"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-205"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-206"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-207"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="35a07-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="35a07-208"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="35a07-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35a07-209">**VPath**</span><span class="sxs-lookup"><span data-stu-id="35a07-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35a07-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35a07-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35a07-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35a07-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35a07-212">應用程式的虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="35a07-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35a07-213">規格需求</span><span class="sxs-lookup"><span data-stu-id="35a07-213">Requirements</span></span>



| <span data-ttu-id="35a07-214">需求</span><span class="sxs-lookup"><span data-stu-id="35a07-214">Requirement</span></span> | <span data-ttu-id="35a07-215">值</span><span class="sxs-lookup"><span data-stu-id="35a07-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a07-216">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35a07-216">Minimum supported client</span></span><br/> | <span data-ttu-id="35a07-217">都不支援</span><span class="sxs-lookup"><span data-stu-id="35a07-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="35a07-218">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35a07-218">Minimum supported server</span></span><br/> | <span data-ttu-id="35a07-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35a07-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="35a07-220">命名空間</span><span class="sxs-lookup"><span data-stu-id="35a07-220">Namespace</span></span><br/>                | <span data-ttu-id="35a07-221">根 \\ cimv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="35a07-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="35a07-222">MOF</span><span class="sxs-lookup"><span data-stu-id="35a07-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35a07-223"><dt>Tscpub mof</dt></span><span class="sxs-lookup"><span data-stu-id="35a07-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="35a07-224">DLL</span><span class="sxs-lookup"><span data-stu-id="35a07-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35a07-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35a07-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

