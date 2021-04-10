---
title: MDM_Policy_Result01_Search02 類別
description: MDM \_ Policy \_ Result01 \_ Search02 類別代表可用的搜尋原則。
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- MDM_Policy_Result01_Search02 類別
- MDM_Policy_Result01_Search02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024794"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="33cbe-105">MDM \_ 原則 \_ Result01 \_ Search02 類別</span><span class="sxs-lookup"><span data-stu-id="33cbe-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="33cbe-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="33cbe-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33cbe-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="33cbe-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33cbe-108">**MDM \_ Policy \_ Result01 \_ Search02** 類別代表可用的搜尋原則。</span><span class="sxs-lookup"><span data-stu-id="33cbe-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="33cbe-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="33cbe-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33cbe-110">語法</span><span class="sxs-lookup"><span data-stu-id="33cbe-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
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

## <a name="members"></a><span data-ttu-id="33cbe-111">成員</span><span class="sxs-lookup"><span data-stu-id="33cbe-111">Members</span></span>

<span data-ttu-id="33cbe-112">**MDM \_ Policy \_ Result01 \_ Search02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="33cbe-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="33cbe-113">屬性</span><span class="sxs-lookup"><span data-stu-id="33cbe-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33cbe-114">屬性</span><span class="sxs-lookup"><span data-stu-id="33cbe-114">Properties</span></span>

<span data-ttu-id="33cbe-115">**MDM \_ Policy \_ Result01 \_ Search02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="33cbe-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33cbe-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="33cbe-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="33cbe-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="33cbe-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="33cbe-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="33cbe-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="33cbe-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="33cbe-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="33cbe-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="33cbe-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33cbe-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33cbe-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33cbe-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="33cbe-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-146">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33cbe-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33cbe-147">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="33cbe-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="33cbe-148">此類別的字串為 "Search"。</span><span class="sxs-lookup"><span data-stu-id="33cbe-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="33cbe-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="33cbe-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="33cbe-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="33cbe-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33cbe-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33cbe-153">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="33cbe-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="33cbe-154">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="33cbe-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="33cbe-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="33cbe-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33cbe-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="33cbe-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33cbe-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="33cbe-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33cbe-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="33cbe-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33cbe-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="33cbe-161">Requirements</span></span>



| <span data-ttu-id="33cbe-162">需求</span><span class="sxs-lookup"><span data-stu-id="33cbe-162">Requirement</span></span> | <span data-ttu-id="33cbe-163">值</span><span class="sxs-lookup"><span data-stu-id="33cbe-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33cbe-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33cbe-164">Minimum supported client</span></span><br/> | <span data-ttu-id="33cbe-165">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33cbe-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33cbe-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33cbe-166">Minimum supported server</span></span><br/> | <span data-ttu-id="33cbe-167">都不支援</span><span class="sxs-lookup"><span data-stu-id="33cbe-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="33cbe-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="33cbe-168">Namespace</span></span><br/>                | <span data-ttu-id="33cbe-169">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="33cbe-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="33cbe-170">MOF</span><span class="sxs-lookup"><span data-stu-id="33cbe-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33cbe-171"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="33cbe-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="33cbe-172">DLL</span><span class="sxs-lookup"><span data-stu-id="33cbe-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33cbe-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33cbe-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33cbe-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33cbe-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33cbe-175">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="33cbe-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

