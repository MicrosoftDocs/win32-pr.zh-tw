---
title: MDM_Policy_Result01_Start02 類別
description: MDM \_ Policy \_ Result01 \_ Start02 類別代表可用的開始畫面原則。
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- MDM_Policy_Result01_Start02 類別
- MDM_Policy_Result01_Start02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024976"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="51993-105">MDM \_ 原則 \_ Result01 \_ Start02 類別</span><span class="sxs-lookup"><span data-stu-id="51993-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="51993-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="51993-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="51993-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="51993-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="51993-108">**MDM \_ Policy \_ Result01 \_ Start02** 類別代表可用的開始畫面原則。</span><span class="sxs-lookup"><span data-stu-id="51993-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="51993-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="51993-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51993-110">語法</span><span class="sxs-lookup"><span data-stu-id="51993-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="51993-111">成員</span><span class="sxs-lookup"><span data-stu-id="51993-111">Members</span></span>

<span data-ttu-id="51993-112">**MDM \_ Policy \_ Result01 \_ Start02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="51993-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="51993-113">屬性</span><span class="sxs-lookup"><span data-stu-id="51993-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51993-114">屬性</span><span class="sxs-lookup"><span data-stu-id="51993-114">Properties</span></span>

<span data-ttu-id="51993-115">**MDM \_ Policy \_ Result01 \_ Start02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="51993-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="51993-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="51993-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="51993-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="51993-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="51993-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="51993-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="51993-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="51993-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="51993-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="51993-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="51993-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="51993-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="51993-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="51993-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="51993-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="51993-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="51993-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="51993-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="51993-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="51993-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="51993-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-174">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="51993-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-177">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="51993-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-180">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="51993-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="51993-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-186">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="51993-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="51993-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="51993-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="51993-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51993-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51993-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51993-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="51993-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51993-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="51993-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51993-197">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51993-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51993-198">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="51993-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="51993-199">此類別的字串為 "Start"</span><span class="sxs-lookup"><span data-stu-id="51993-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="51993-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="51993-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-201">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="51993-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51993-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51993-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="51993-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="51993-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51993-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="51993-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51993-206">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51993-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51993-207">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="51993-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="51993-208">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="51993-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="51993-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="51993-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51993-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="51993-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51993-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="51993-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51993-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="51993-212">Requirements</span></span>



| <span data-ttu-id="51993-213">需求</span><span class="sxs-lookup"><span data-stu-id="51993-213">Requirement</span></span> | <span data-ttu-id="51993-214">值</span><span class="sxs-lookup"><span data-stu-id="51993-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51993-215">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51993-215">Minimum supported client</span></span><br/> | <span data-ttu-id="51993-216">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51993-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51993-217">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51993-217">Minimum supported server</span></span><br/> | <span data-ttu-id="51993-218">都不支援</span><span class="sxs-lookup"><span data-stu-id="51993-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="51993-219">命名空間</span><span class="sxs-lookup"><span data-stu-id="51993-219">Namespace</span></span><br/>                | <span data-ttu-id="51993-220">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="51993-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="51993-221">MOF</span><span class="sxs-lookup"><span data-stu-id="51993-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51993-222"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="51993-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="51993-223">DLL</span><span class="sxs-lookup"><span data-stu-id="51993-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51993-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51993-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51993-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51993-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51993-226">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="51993-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

