---
title: MDM_Policy_Config01_Browser02 類別
description: MDM \_ Policy \_ Config01 \_ Browser02 類別代表可用的瀏覽器原則。
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- MDM_Policy_Config01_Browser02 類別
- MDM_Policy_Config01_Browser02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024904"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="ca240-105">MDM \_ 原則 \_ Config01 \_ Browser02 類別</span><span class="sxs-lookup"><span data-stu-id="ca240-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="ca240-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ca240-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca240-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ca240-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca240-108">**MDM \_ Policy \_ Config01 \_ Browser02** 類別代表可用的瀏覽器原則。</span><span class="sxs-lookup"><span data-stu-id="ca240-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="ca240-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ca240-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca240-110">語法</span><span class="sxs-lookup"><span data-stu-id="ca240-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="ca240-111">成員</span><span class="sxs-lookup"><span data-stu-id="ca240-111">Members</span></span>

<span data-ttu-id="ca240-112">**MDM \_ Policy \_ Config01 \_ Browser02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ca240-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="ca240-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ca240-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca240-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ca240-114">Properties</span></span>

<span data-ttu-id="ca240-115">**MDM \_ Policy \_ Config01 \_ Browser02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ca240-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ca240-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="ca240-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="ca240-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="ca240-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="ca240-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="ca240-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="ca240-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="ca240-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="ca240-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="ca240-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="ca240-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="ca240-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="ca240-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="ca240-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="ca240-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="ca240-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="ca240-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="ca240-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="ca240-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="ca240-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="ca240-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="ca240-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-179">主頁</span><span class="sxs-lookup"><span data-stu-id="ca240-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca240-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca240-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca240-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca240-185">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca240-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca240-186">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca240-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="ca240-187">此類別的字串為 "Browser"。</span><span class="sxs-lookup"><span data-stu-id="ca240-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="ca240-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="ca240-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca240-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ca240-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ca240-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca240-194">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca240-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca240-195">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ca240-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="ca240-196">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="ca240-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="ca240-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ca240-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-198">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="ca240-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-201">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="ca240-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-204">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="ca240-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-207">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="ca240-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-210">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="ca240-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-213">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="ca240-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="ca240-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-219">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="ca240-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ca240-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="ca240-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-225">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca240-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="ca240-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca240-228">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca240-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca240-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ca240-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca240-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca240-230">Requirements</span></span>



| <span data-ttu-id="ca240-231">需求</span><span class="sxs-lookup"><span data-stu-id="ca240-231">Requirement</span></span> | <span data-ttu-id="ca240-232">值</span><span class="sxs-lookup"><span data-stu-id="ca240-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca240-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca240-233">Minimum supported client</span></span><br/> | <span data-ttu-id="ca240-234">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca240-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca240-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca240-235">Minimum supported server</span></span><br/> | <span data-ttu-id="ca240-236">都不支援</span><span class="sxs-lookup"><span data-stu-id="ca240-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca240-237">命名空間</span><span class="sxs-lookup"><span data-stu-id="ca240-237">Namespace</span></span><br/>                | <span data-ttu-id="ca240-238">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="ca240-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ca240-239">MOF</span><span class="sxs-lookup"><span data-stu-id="ca240-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca240-240"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca240-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca240-241">DLL</span><span class="sxs-lookup"><span data-stu-id="ca240-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca240-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca240-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca240-243">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca240-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca240-244">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="ca240-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

