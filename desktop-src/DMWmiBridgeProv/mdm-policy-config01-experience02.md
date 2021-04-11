---
title: MDM_Policy_Config01_Experience02 類別
description: MDM \_ Policy \_ Config01 \_ Experience02 類別表示可用的體驗原則。
ms.assetid: 21052983-696c-4137-9c72-16ea3b4a1eb7
keywords:
- MDM_Policy_Config01_Experience02 類別
- MDM_Policy_Config01_Experience02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Experience02
- MDM_Policy_Config01_Experience02.InstanceID
- MDM_Policy_Config01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38885dbc22c51bfa9e1653f81dba38255f6ba6a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105720"
---
# <a name="mdm_policy_config01_experience02-class"></a><span data-ttu-id="b330d-105">MDM \_ 原則 \_ Config01 \_ Experience02 類別</span><span class="sxs-lookup"><span data-stu-id="b330d-105">MDM\_Policy\_Config01\_Experience02 class</span></span>

<span data-ttu-id="b330d-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b330d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b330d-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b330d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b330d-108">**MDM \_ Policy \_ Config01 \_ Experience02** 類別表示可用的體驗原則。</span><span class="sxs-lookup"><span data-stu-id="b330d-108">The **MDM\_Policy\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="b330d-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b330d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b330d-110">語法</span><span class="sxs-lookup"><span data-stu-id="b330d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="b330d-111">成員</span><span class="sxs-lookup"><span data-stu-id="b330d-111">Members</span></span>

<span data-ttu-id="b330d-112">**MDM \_ Policy \_ Config01 \_ Experience02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b330d-112">The **MDM\_Policy\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="b330d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b330d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b330d-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b330d-114">Properties</span></span>

<span data-ttu-id="b330d-115">**MDM \_ Policy \_ Config01 \_ Experience02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b330d-115">The **MDM\_Policy\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b330d-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="b330d-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="b330d-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="b330d-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="b330d-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="b330d-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b330d-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="b330d-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="b330d-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b330d-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="b330d-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="b330d-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="b330d-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b330d-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="b330d-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b330d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b330d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b330d-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b330d-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b330d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b330d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b330d-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b330d-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b330d-153">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b330d-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="b330d-154">針對此類別，字串為「經驗」。</span><span class="sxs-lookup"><span data-stu-id="b330d-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="b330d-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b330d-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b330d-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b330d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b330d-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b330d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b330d-158">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b330d-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b330d-159">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b330d-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="b330d-160">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="b330d-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b330d-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="b330d-161">Requirements</span></span>



| <span data-ttu-id="b330d-162">需求</span><span class="sxs-lookup"><span data-stu-id="b330d-162">Requirement</span></span> | <span data-ttu-id="b330d-163">值</span><span class="sxs-lookup"><span data-stu-id="b330d-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b330d-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b330d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b330d-165">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b330d-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b330d-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b330d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b330d-167">都不支援</span><span class="sxs-lookup"><span data-stu-id="b330d-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b330d-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="b330d-168">Namespace</span></span><br/>                | <span data-ttu-id="b330d-169">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="b330d-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b330d-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b330d-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b330d-171"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b330d-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b330d-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b330d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b330d-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b330d-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b330d-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b330d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b330d-175">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="b330d-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

