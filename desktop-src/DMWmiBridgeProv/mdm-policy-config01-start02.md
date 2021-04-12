---
title: MDM_Policy_Config01_Start02 類別
description: MDM \_ Policy \_ Config01 \_ Start02 類別代表可用的開始畫面原則。
ms.assetid: 2aef29c8-164a-4111-9c1a-e63eeec2531e
keywords:
- MDM_Policy_Config01_Start02 類別
- MDM_Policy_Config01_Start02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Start02
- MDM_Policy_Config01_Start02.InstanceID
- MDM_Policy_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9095fcf1611ef106fed5ad93f059e165ebcac15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465449"
---
# <a name="mdm_policy_config01_start02-class"></a><span data-ttu-id="5fee2-105">MDM \_ 原則 \_ Config01 \_ Start02 類別</span><span class="sxs-lookup"><span data-stu-id="5fee2-105">MDM\_Policy\_Config01\_Start02 class</span></span>

<span data-ttu-id="5fee2-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5fee2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5fee2-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5fee2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5fee2-108">**MDM \_ Policy \_ Config01 \_ Start02** 類別代表可用的開始畫面原則。</span><span class="sxs-lookup"><span data-stu-id="5fee2-108">The **MDM\_Policy\_Config01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="5fee2-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5fee2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fee2-110">語法</span><span class="sxs-lookup"><span data-stu-id="5fee2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Start02
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

## <a name="members"></a><span data-ttu-id="5fee2-111">成員</span><span class="sxs-lookup"><span data-stu-id="5fee2-111">Members</span></span>

<span data-ttu-id="5fee2-112">**MDM \_ Policy \_ Config01 \_ Start02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5fee2-112">The **MDM\_Policy\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="5fee2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5fee2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fee2-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5fee2-114">Properties</span></span>

<span data-ttu-id="5fee2-115">**MDM \_ Policy \_ Config01 \_ Start02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5fee2-115">The **MDM\_Policy\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5fee2-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="5fee2-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="5fee2-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="5fee2-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="5fee2-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="5fee2-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="5fee2-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="5fee2-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="5fee2-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="5fee2-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="5fee2-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="5fee2-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="5fee2-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="5fee2-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="5fee2-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="5fee2-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="5fee2-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="5fee2-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="5fee2-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="5fee2-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="5fee2-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-174">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="5fee2-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-177">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="5fee2-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-180">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="5fee2-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="5fee2-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-186">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="5fee2-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5fee2-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="5fee2-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5fee2-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fee2-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5fee2-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5fee2-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5fee2-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-197">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fee2-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fee2-198">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fee2-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="5fee2-199">此類別的字串為 "Start"</span><span class="sxs-lookup"><span data-stu-id="5fee2-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="5fee2-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="5fee2-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-201">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fee2-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5fee2-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5fee2-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5fee2-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5fee2-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-206">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fee2-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fee2-207">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5fee2-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="5fee2-208">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="5fee2-208">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="5fee2-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="5fee2-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fee2-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5fee2-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fee2-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5fee2-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fee2-212">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fee2-212">Requirements</span></span>



| <span data-ttu-id="5fee2-213">需求</span><span class="sxs-lookup"><span data-stu-id="5fee2-213">Requirement</span></span> | <span data-ttu-id="5fee2-214">值</span><span class="sxs-lookup"><span data-stu-id="5fee2-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fee2-215">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fee2-215">Minimum supported client</span></span><br/> | <span data-ttu-id="5fee2-216">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fee2-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fee2-217">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fee2-217">Minimum supported server</span></span><br/> | <span data-ttu-id="5fee2-218">都不支援</span><span class="sxs-lookup"><span data-stu-id="5fee2-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5fee2-219">命名空間</span><span class="sxs-lookup"><span data-stu-id="5fee2-219">Namespace</span></span><br/>                | <span data-ttu-id="5fee2-220">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="5fee2-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5fee2-221">MOF</span><span class="sxs-lookup"><span data-stu-id="5fee2-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fee2-222"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fee2-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fee2-223">DLL</span><span class="sxs-lookup"><span data-stu-id="5fee2-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fee2-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fee2-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fee2-225">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fee2-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fee2-226">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="5fee2-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

