---
title: MDM_Policy_Config01_Search02 類別
description: MDM \_ Policy \_ Config01 \_ Search02 類別代表可用的搜尋原則。
ms.assetid: 0ae4876c-3584-4b22-be02-a499443f5df0
keywords:
- MDM_Policy_Config01_Search02 類別
- MDM_Policy_Config01_Search02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Search02
- MDM_Policy_Config01_Search02.InstanceID
- MDM_Policy_Config01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f3517cacf1fd9af6b37f64a0cbbc8294916cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465452"
---
# <a name="mdm_policy_config01_search02-class"></a><span data-ttu-id="b54e2-105">MDM \_ 原則 \_ Config01 \_ Search02 類別</span><span class="sxs-lookup"><span data-stu-id="b54e2-105">MDM\_Policy\_Config01\_Search02 class</span></span>

<span data-ttu-id="b54e2-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b54e2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b54e2-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b54e2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b54e2-108">**MDM \_ Policy \_ Config01 \_ Search02** 類別代表可用的搜尋原則。</span><span class="sxs-lookup"><span data-stu-id="b54e2-108">The **MDM\_Policy\_Config01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="b54e2-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b54e2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b54e2-110">語法</span><span class="sxs-lookup"><span data-stu-id="b54e2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="b54e2-111">成員</span><span class="sxs-lookup"><span data-stu-id="b54e2-111">Members</span></span>

<span data-ttu-id="b54e2-112">**MDM \_ Policy \_ Config01 \_ Search02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b54e2-112">The **MDM\_Policy\_Config01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="b54e2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b54e2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b54e2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="b54e2-114">Properties</span></span>

<span data-ttu-id="b54e2-115">**MDM \_ Policy \_ Config01 \_ Search02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b54e2-115">The **MDM\_Policy\_Config01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b54e2-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="b54e2-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="b54e2-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="b54e2-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="b54e2-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="b54e2-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="b54e2-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="b54e2-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="b54e2-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="b54e2-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b54e2-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b54e2-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b54e2-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b54e2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b54e2-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b54e2-147">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b54e2-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="b54e2-148">此類別的字串為 "Search"。</span><span class="sxs-lookup"><span data-stu-id="b54e2-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="b54e2-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b54e2-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b54e2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b54e2-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b54e2-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b54e2-153">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b54e2-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="b54e2-154">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="b54e2-154">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="b54e2-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="b54e2-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b54e2-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="b54e2-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b54e2-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="b54e2-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b54e2-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b54e2-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b54e2-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="b54e2-161">Requirements</span></span>



| <span data-ttu-id="b54e2-162">需求</span><span class="sxs-lookup"><span data-stu-id="b54e2-162">Requirement</span></span> | <span data-ttu-id="b54e2-163">值</span><span class="sxs-lookup"><span data-stu-id="b54e2-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54e2-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b54e2-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b54e2-165">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b54e2-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b54e2-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b54e2-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b54e2-167">都不支援</span><span class="sxs-lookup"><span data-stu-id="b54e2-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b54e2-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="b54e2-168">Namespace</span></span><br/>                | <span data-ttu-id="b54e2-169">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="b54e2-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b54e2-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b54e2-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b54e2-171"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b54e2-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b54e2-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b54e2-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b54e2-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b54e2-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b54e2-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b54e2-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b54e2-175">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="b54e2-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

