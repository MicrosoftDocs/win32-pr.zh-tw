---
title: MDM_Policy_Result01_Browser02 類別
description: MDM \_ Policy \_ Result01 \_ Browser02 類別代表可用的瀏覽器原則。MDM \_ Policy \_ Result01 \_ Browser02 類別代表可用的瀏覽器原則。
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- MDM_Policy_Result01_Browser02 類別
- MDM_Policy_Result01_Browser02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843132"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="13457-105">MDM \_ 原則 \_ Result01 \_ Browser02 類別</span><span class="sxs-lookup"><span data-stu-id="13457-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="13457-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="13457-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="13457-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="13457-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="13457-108">**MDM \_ Policy \_ Result01 \_ Browser02** 類別代表可用的瀏覽器原則。</span><span class="sxs-lookup"><span data-stu-id="13457-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="13457-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="13457-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13457-110">語法</span><span class="sxs-lookup"><span data-stu-id="13457-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
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

## <a name="members"></a><span data-ttu-id="13457-111">成員</span><span class="sxs-lookup"><span data-stu-id="13457-111">Members</span></span>

<span data-ttu-id="13457-112">**MDM \_ Policy \_ Result01 \_ Browser02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="13457-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="13457-113">屬性</span><span class="sxs-lookup"><span data-stu-id="13457-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13457-114">屬性</span><span class="sxs-lookup"><span data-stu-id="13457-114">Properties</span></span>

<span data-ttu-id="13457-115">**MDM \_ Policy \_ Result01 \_ Browser02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="13457-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="13457-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="13457-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="13457-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="13457-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="13457-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="13457-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="13457-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="13457-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="13457-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="13457-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="13457-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="13457-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="13457-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="13457-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="13457-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="13457-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="13457-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="13457-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="13457-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="13457-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="13457-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="13457-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-179">主頁</span><span class="sxs-lookup"><span data-stu-id="13457-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13457-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13457-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-183">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-184">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13457-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13457-185">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13457-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13457-186">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="13457-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="13457-187">此類別的字串為 "Browser"。</span><span class="sxs-lookup"><span data-stu-id="13457-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="13457-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="13457-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13457-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="13457-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="13457-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13457-194">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13457-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13457-195">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="13457-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="13457-196">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="13457-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="13457-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="13457-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-198">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="13457-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-201">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="13457-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-204">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="13457-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-207">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="13457-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-210">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="13457-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-213">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="13457-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="13457-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-219">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="13457-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="13457-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13457-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="13457-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-225">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13457-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="13457-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13457-228">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="13457-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13457-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="13457-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13457-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="13457-230">Requirements</span></span>



| <span data-ttu-id="13457-231">需求</span><span class="sxs-lookup"><span data-stu-id="13457-231">Requirement</span></span> | <span data-ttu-id="13457-232">值</span><span class="sxs-lookup"><span data-stu-id="13457-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13457-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13457-233">Minimum supported client</span></span><br/> | <span data-ttu-id="13457-234">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13457-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13457-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13457-235">Minimum supported server</span></span><br/> | <span data-ttu-id="13457-236">都不支援</span><span class="sxs-lookup"><span data-stu-id="13457-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="13457-237">命名空間</span><span class="sxs-lookup"><span data-stu-id="13457-237">Namespace</span></span><br/>                | <span data-ttu-id="13457-238">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="13457-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="13457-239">MOF</span><span class="sxs-lookup"><span data-stu-id="13457-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13457-240"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="13457-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="13457-241">DLL</span><span class="sxs-lookup"><span data-stu-id="13457-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13457-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13457-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13457-243">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13457-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13457-244">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="13457-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

