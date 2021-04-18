---
title: Win32_TSPublishedApplication 類別
description: 定義可用來透過 Windows Server 2008 R2 RemoteApp 進行遠端使用的應用程式。
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplication 類別遠端桌面服務
- Win32_TSPublishedApplication 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965294"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="24659-105">Win32 \_ TSPublishedApplication 類別</span><span class="sxs-lookup"><span data-stu-id="24659-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="24659-106">定義可用來透過 Windows Server 2008 R2 RemoteApp 進行遠端使用的應用程式。</span><span class="sxs-lookup"><span data-stu-id="24659-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="24659-107">語法</span><span class="sxs-lookup"><span data-stu-id="24659-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="24659-108">成員</span><span class="sxs-lookup"><span data-stu-id="24659-108">Members</span></span>

<span data-ttu-id="24659-109">**Win32 \_ TSPublishedApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24659-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="24659-110">屬性</span><span class="sxs-lookup"><span data-stu-id="24659-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24659-111">屬性</span><span class="sxs-lookup"><span data-stu-id="24659-111">Properties</span></span>

<span data-ttu-id="24659-112">**Win32 \_ TSPublishedApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="24659-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24659-113">**別名**</span><span class="sxs-lookup"><span data-stu-id="24659-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="24659-116">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="24659-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="24659-117">應用程式的別名。</span><span class="sxs-lookup"><span data-stu-id="24659-117">The alias of the application.</span></span> <span data-ttu-id="24659-118">該別名是程式的唯一識別碼，預設值為程式的檔案名稱 (不含副檔名)。</span><span class="sxs-lookup"><span data-stu-id="24659-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="24659-119">**標題**</span><span class="sxs-lookup"><span data-stu-id="24659-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24659-122">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="24659-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="24659-123">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="24659-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="24659-124">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24659-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24659-125">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="24659-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-126">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="24659-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24659-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-128">應用程式的命令列引數設定。</span><span class="sxs-lookup"><span data-stu-id="24659-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="24659-129">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="24659-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="24659-130">0</span><span class="sxs-lookup"><span data-stu-id="24659-130">0</span></span>
</dt> <dd>

<span data-ttu-id="24659-131">不允許命令列引數。</span><span class="sxs-lookup"><span data-stu-id="24659-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="24659-132">1</span><span class="sxs-lookup"><span data-stu-id="24659-132">1</span></span>
</dt> <dd>

<span data-ttu-id="24659-133">允許任何命令列引數。</span><span class="sxs-lookup"><span data-stu-id="24659-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="24659-134">2</span><span class="sxs-lookup"><span data-stu-id="24659-134">2</span></span>
</dt> <dd>

<span data-ttu-id="24659-135">請一律使用 **RequiredCommandLine**) 中指定 (所需的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="24659-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="24659-136">**說明**</span><span class="sxs-lookup"><span data-stu-id="24659-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24659-139">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="24659-139">Description of the object.</span></span>

<span data-ttu-id="24659-140">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24659-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24659-141">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="24659-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-142">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="24659-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="24659-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24659-144">對應到應用程式之圖示的位元組內容。</span><span class="sxs-lookup"><span data-stu-id="24659-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="24659-145">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="24659-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-146">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="24659-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24659-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-148">圖示的索引或識別碼。</span><span class="sxs-lookup"><span data-stu-id="24659-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="24659-149">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="24659-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-152">應用程式圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="24659-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="24659-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="24659-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-154">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="24659-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24659-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24659-156">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="24659-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="24659-157">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="24659-157">The date the object was installed.</span></span> <span data-ttu-id="24659-158">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="24659-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="24659-159">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24659-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24659-160">**名稱**</span><span class="sxs-lookup"><span data-stu-id="24659-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24659-163">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="24659-163">The name of the object.</span></span>

<span data-ttu-id="24659-164">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24659-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24659-165">**路徑**</span><span class="sxs-lookup"><span data-stu-id="24659-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-167">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-168">應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="24659-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="24659-169">**PathExists**</span><span class="sxs-lookup"><span data-stu-id="24659-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-170">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24659-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24659-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24659-172">指出應用程式路徑是否有效。</span><span class="sxs-lookup"><span data-stu-id="24659-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="24659-173">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="24659-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-176">對應到應用程式之 RDP 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="24659-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="24659-177">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="24659-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-179">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-180">應用程式所需的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="24659-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="24659-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="24659-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-184">控制應用程式存取的安全描述項（SDDL 格式）。</span><span class="sxs-lookup"><span data-stu-id="24659-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="24659-185">空字串表示允許所有存取。</span><span class="sxs-lookup"><span data-stu-id="24659-185">An empty string implies allow all access.</span></span> <span data-ttu-id="24659-186">此安全描述項不支援拒絕 Ace 或參考非網域使用者或群組的 Ace。</span><span class="sxs-lookup"><span data-stu-id="24659-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="24659-187">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="24659-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-188">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="24659-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24659-189">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-190">指出應用程式是否應該在 RD Web 存取中顯示。</span><span class="sxs-lookup"><span data-stu-id="24659-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="24659-191">**狀態**</span><span class="sxs-lookup"><span data-stu-id="24659-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="24659-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24659-194">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="24659-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="24659-195">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="24659-195">Current status of the object.</span></span> <span data-ttu-id="24659-196">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="24659-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="24659-197">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="24659-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="24659-198">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="24659-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="24659-199">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="24659-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="24659-200">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="24659-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="24659-201">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="24659-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="24659-202"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="24659-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-203"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-204"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-205"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-206"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-207"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-208"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="24659-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="24659-209"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="24659-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24659-210">**VPath**</span><span class="sxs-lookup"><span data-stu-id="24659-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24659-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="24659-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24659-212">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="24659-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="24659-213">應用程式的虛擬路徑，這表示內含環境變數的路徑。</span><span class="sxs-lookup"><span data-stu-id="24659-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24659-214">備註</span><span class="sxs-lookup"><span data-stu-id="24659-214">Remarks</span></span>

<span data-ttu-id="24659-215">您必須是 Administrators 群組的成員，才能使用這個類別來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="24659-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="24659-216">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="24659-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="24659-217">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級，可以使用 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM 函式來設定。</span><span class="sxs-lookup"><span data-stu-id="24659-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="24659-218">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="24659-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="24659-219">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="24659-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="24659-220">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="24659-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="24659-221">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="24659-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="24659-222">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="24659-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="24659-223">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="24659-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="24659-224">規格需求</span><span class="sxs-lookup"><span data-stu-id="24659-224">Requirements</span></span>



| <span data-ttu-id="24659-225">需求</span><span class="sxs-lookup"><span data-stu-id="24659-225">Requirement</span></span> | <span data-ttu-id="24659-226">值</span><span class="sxs-lookup"><span data-stu-id="24659-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24659-227">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24659-227">Minimum supported client</span></span><br/> | <span data-ttu-id="24659-228">都不支援</span><span class="sxs-lookup"><span data-stu-id="24659-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24659-229">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24659-229">Minimum supported server</span></span><br/> | <span data-ttu-id="24659-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24659-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24659-231">命名空間</span><span class="sxs-lookup"><span data-stu-id="24659-231">Namespace</span></span><br/>                | <span data-ttu-id="24659-232">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="24659-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24659-233">MOF</span><span class="sxs-lookup"><span data-stu-id="24659-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24659-234"><dt>Tsallow mof</dt></span><span class="sxs-lookup"><span data-stu-id="24659-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="24659-235">DLL</span><span class="sxs-lookup"><span data-stu-id="24659-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24659-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24659-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

