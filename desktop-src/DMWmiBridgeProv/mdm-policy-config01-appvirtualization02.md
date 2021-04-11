---
title: MDM_Policy_Config01_AppVirtualization02 類別
description: MDM \_ Policy \_ Config01 AppVirtualization02 類別會設定 \_ 可用的應用程式虛擬化原則。
ms.assetid: d270704c-8652-4f97-89f7-fcb6e68ee6fe
keywords:
- MDM_Policy_Config01_AppVirtualization02 類別
- MDM_Policy_Config01_AppVirtualization02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AppVirtualization02
- MDM_Policy_Config01_AppVirtualization02.InstanceID
- MDM_Policy_Config01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871d09b306cff2833601100d9a645cde5c59e33f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094275"
---
# <a name="mdm_policy_config01_appvirtualization02-class"></a><span data-ttu-id="aad26-105">MDM \_ 原則 \_ Config01 \_ AppVirtualization02 類別</span><span class="sxs-lookup"><span data-stu-id="aad26-105">MDM\_Policy\_Config01\_AppVirtualization02 class</span></span>

<span data-ttu-id="aad26-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="aad26-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aad26-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="aad26-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aad26-108">MDM \_ Policy \_ Config01 AppVirtualization02 類別會設定 \_ 可用的應用程式虛擬化原則。</span><span class="sxs-lookup"><span data-stu-id="aad26-108">The MDM\_Policy\_Config01\_AppVirtualization02 class configures the available app virtualization policies.</span></span>

<span data-ttu-id="aad26-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="aad26-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad26-110">語法</span><span class="sxs-lookup"><span data-stu-id="aad26-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="aad26-111">成員</span><span class="sxs-lookup"><span data-stu-id="aad26-111">Members</span></span>

<span data-ttu-id="aad26-112">**MDM \_ Policy \_ Config01 \_ AppVirtualization02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="aad26-112">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="aad26-113">屬性</span><span class="sxs-lookup"><span data-stu-id="aad26-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aad26-114">屬性</span><span class="sxs-lookup"><span data-stu-id="aad26-114">Properties</span></span>

<span data-ttu-id="aad26-115">**MDM \_ Policy \_ Config01 \_ AppVirtualization02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="aad26-115">The **MDM\_Policy\_Config01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aad26-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="aad26-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="aad26-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="aad26-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="aad26-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="aad26-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="aad26-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="aad26-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="aad26-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="aad26-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="aad26-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aad26-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aad26-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad26-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad26-149">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aad26-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="aad26-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="aad26-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aad26-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="aad26-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="aad26-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad26-159">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aad26-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="aad26-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="aad26-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="aad26-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="aad26-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="aad26-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-175">StreamingAllowCertificateFilterForClient \_ SSL</span><span class="sxs-lookup"><span data-stu-id="aad26-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-177">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="aad26-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="aad26-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="aad26-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-186">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="aad26-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-189">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="aad26-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="aad26-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-195">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="aad26-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="aad26-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="aad26-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-204">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aad26-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="aad26-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad26-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="aad26-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad26-207">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="aad26-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aad26-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="aad26-208">Requirements</span></span>



| <span data-ttu-id="aad26-209">需求</span><span class="sxs-lookup"><span data-stu-id="aad26-209">Requirement</span></span> | <span data-ttu-id="aad26-210">值</span><span class="sxs-lookup"><span data-stu-id="aad26-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aad26-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aad26-211">Minimum supported client</span></span><br/> | <span data-ttu-id="aad26-212">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aad26-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aad26-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aad26-213">Minimum supported server</span></span><br/> | <span data-ttu-id="aad26-214">都不支援</span><span class="sxs-lookup"><span data-stu-id="aad26-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aad26-215">命名空間</span><span class="sxs-lookup"><span data-stu-id="aad26-215">Namespace</span></span><br/>                | <span data-ttu-id="aad26-216">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="aad26-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aad26-217">MOF</span><span class="sxs-lookup"><span data-stu-id="aad26-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aad26-218"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="aad26-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aad26-219">DLL</span><span class="sxs-lookup"><span data-stu-id="aad26-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aad26-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aad26-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

