---
title: Win32_RDMSPublishedApplication 類別
description: 管理已發佈的應用程式。
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication 類別遠端桌面服務
- Win32_RDMSPublishedApplication 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317427"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="fd640-105">Win32 \_ RDMSPublishedApplication 類別</span><span class="sxs-lookup"><span data-stu-id="fd640-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="fd640-106">管理已發佈的應用程式。</span><span class="sxs-lookup"><span data-stu-id="fd640-106">Manages a published application.</span></span>

<span data-ttu-id="fd640-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd640-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd640-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="fd640-109">成員</span><span class="sxs-lookup"><span data-stu-id="fd640-109">Members</span></span>

<span data-ttu-id="fd640-110">**Win32 \_ RDMSPublishedApplication** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fd640-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="fd640-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fd640-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd640-112">屬性</span><span class="sxs-lookup"><span data-stu-id="fd640-112">Properties</span></span>

<span data-ttu-id="fd640-113">**Win32 \_ RDMSPublishedApplication** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fd640-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd640-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="fd640-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-115">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-116">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd640-117">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd640-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd640-118">取得和設定應用程式的別名。</span><span class="sxs-lookup"><span data-stu-id="fd640-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="fd640-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-122">取得和設定應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="fd640-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-123">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="fd640-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fd640-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-126">取得和設定應用程式的命令列設定。</span><span class="sxs-lookup"><span data-stu-id="fd640-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="fd640-127">這個屬性可以設定為下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="fd640-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="fd640-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0) </span><span class="sxs-lookup"><span data-stu-id="fd640-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fd640-129">不允許命令列引數。</span><span class="sxs-lookup"><span data-stu-id="fd640-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="fd640-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**允許** (1) </span><span class="sxs-lookup"><span data-stu-id="fd640-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fd640-131">允許命令列引數。</span><span class="sxs-lookup"><span data-stu-id="fd640-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="fd640-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**需要** (2) </span><span class="sxs-lookup"><span data-stu-id="fd640-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fd640-133">需要命令列引數。</span><span class="sxs-lookup"><span data-stu-id="fd640-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd640-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="fd640-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-137">取得和設定應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="fd640-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-138">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="fd640-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-139">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-141">取得和設定應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="fd640-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-142">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="fd640-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-143">資料類型： **uint8** 陣列</span><span class="sxs-lookup"><span data-stu-id="fd640-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fd640-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-145">取得和設定包含應用程式圖示的陣列。</span><span class="sxs-lookup"><span data-stu-id="fd640-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-146">**>iconindex**</span><span class="sxs-lookup"><span data-stu-id="fd640-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="fd640-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-149">取得和設定應用程式圖示的索引。</span><span class="sxs-lookup"><span data-stu-id="fd640-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-150">**>iconpath**</span><span class="sxs-lookup"><span data-stu-id="fd640-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-153">取得並設定此應用程式圖示的路徑。</span><span class="sxs-lookup"><span data-stu-id="fd640-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="fd640-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-155">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd640-157">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd640-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd640-158">取得和設定應用程式的應用程式集區名稱。</span><span class="sxs-lookup"><span data-stu-id="fd640-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-159">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="fd640-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-161">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-162">取得和設定應用程式所需的命令列引數</span><span class="sxs-lookup"><span data-stu-id="fd640-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="fd640-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fd640-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd640-166">限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fd640-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fd640-167">取得和設定安全描述項，以安全描述項定義語言 (SDDL) 格式來控制應用程式的存取。</span><span class="sxs-lookup"><span data-stu-id="fd640-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-168">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="fd640-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-169">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="fd640-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-171">指出是否要在終端機服務中顯示應用程式 Web 存取 (TS Web 存取) 。</span><span class="sxs-lookup"><span data-stu-id="fd640-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="fd640-172">**TRUE** 表示在 TS Web 存取中顯示應用程式;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fd640-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fd640-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="fd640-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd640-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fd640-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd640-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fd640-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd640-176">取得和設定應用程式的虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="fd640-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd640-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd640-177">Requirements</span></span>



| <span data-ttu-id="fd640-178">需求</span><span class="sxs-lookup"><span data-stu-id="fd640-178">Requirement</span></span> | <span data-ttu-id="fd640-179">值</span><span class="sxs-lookup"><span data-stu-id="fd640-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd640-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd640-180">Minimum supported client</span></span><br/> | <span data-ttu-id="fd640-181">都不支援</span><span class="sxs-lookup"><span data-stu-id="fd640-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fd640-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd640-182">Minimum supported server</span></span><br/> | <span data-ttu-id="fd640-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd640-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fd640-184">命名空間</span><span class="sxs-lookup"><span data-stu-id="fd640-184">Namespace</span></span><br/>                | <span data-ttu-id="fd640-185">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="fd640-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fd640-186">MOF</span><span class="sxs-lookup"><span data-stu-id="fd640-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd640-187"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd640-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd640-188">DLL</span><span class="sxs-lookup"><span data-stu-id="fd640-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd640-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd640-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fd640-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd640-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd640-191">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="fd640-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

