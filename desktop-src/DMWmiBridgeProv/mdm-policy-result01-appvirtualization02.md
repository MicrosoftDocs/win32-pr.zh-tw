---
title: MDM_Policy_Result01_AppVirtualization02 類別
description: MDM \_ Policy \_ Result01 \_ AppVirtualization02 類別代表可用的應用程式虛擬化原則。
ms.assetid: fc28646f-f4b9-4648-a22d-b90d32ff888f
keywords:
- MDM_Policy_Result01_AppVirtualization02 類別
- MDM_Policy_Result01_AppVirtualization02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02.InstanceID
- MDM_Policy_Result01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968c4718d7978bdf6770bdf8f828e6ef268cd32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465685"
---
# <a name="mdm_policy_result01_appvirtualization02-class"></a><span data-ttu-id="a2406-105">MDM \_ 原則 \_ Result01 \_ AppVirtualization02 類別</span><span class="sxs-lookup"><span data-stu-id="a2406-105">MDM\_Policy\_Result01\_AppVirtualization02 class</span></span>

<span data-ttu-id="a2406-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a2406-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a2406-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a2406-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a2406-108">MDM \_ Policy \_ Result01 \_ AppVirtualization02 類別代表可用的應用程式虛擬化原則。</span><span class="sxs-lookup"><span data-stu-id="a2406-108">The MDM\_Policy\_Result01\_AppVirtualization02 class represents the available app virtualization policies.</span></span>

<span data-ttu-id="a2406-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a2406-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2406-110">語法</span><span class="sxs-lookup"><span data-stu-id="a2406-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AppVirtualization02
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

## <a name="members"></a><span data-ttu-id="a2406-111">成員</span><span class="sxs-lookup"><span data-stu-id="a2406-111">Members</span></span>

<span data-ttu-id="a2406-112">**MDM \_ Policy \_ Result01 \_ AppVirtualization02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a2406-112">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="a2406-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a2406-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2406-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a2406-114">Properties</span></span>

<span data-ttu-id="a2406-115">**MDM \_ Policy \_ Result01 \_ AppVirtualization02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a2406-115">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a2406-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="a2406-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="a2406-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="a2406-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="a2406-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="a2406-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="a2406-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="a2406-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="a2406-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="a2406-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="a2406-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2406-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a2406-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2406-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2406-149">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2406-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="a2406-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="a2406-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2406-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a2406-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a2406-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2406-159">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a2406-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="a2406-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="a2406-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="a2406-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="a2406-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-171">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="a2406-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-175">StreamingAllowCertificateFilterForClient \_ SSL</span><span class="sxs-lookup"><span data-stu-id="a2406-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-176">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-177">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="a2406-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-180">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="a2406-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="a2406-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-186">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="a2406-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-188">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-189">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="a2406-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-191">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-192">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="a2406-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-195">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="a2406-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-197">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="a2406-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-200">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="a2406-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-203">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-204">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a2406-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="a2406-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2406-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a2406-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2406-207">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a2406-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2406-208">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2406-208">Requirements</span></span>



| <span data-ttu-id="a2406-209">需求</span><span class="sxs-lookup"><span data-stu-id="a2406-209">Requirement</span></span> | <span data-ttu-id="a2406-210">值</span><span class="sxs-lookup"><span data-stu-id="a2406-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2406-211">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2406-211">Minimum supported client</span></span><br/> | <span data-ttu-id="a2406-212">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2406-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2406-213">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2406-213">Minimum supported server</span></span><br/> | <span data-ttu-id="a2406-214">都不支援</span><span class="sxs-lookup"><span data-stu-id="a2406-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a2406-215">命名空間</span><span class="sxs-lookup"><span data-stu-id="a2406-215">Namespace</span></span><br/>                | <span data-ttu-id="a2406-216">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a2406-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a2406-217">MOF</span><span class="sxs-lookup"><span data-stu-id="a2406-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2406-218"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2406-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2406-219">DLL</span><span class="sxs-lookup"><span data-stu-id="a2406-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2406-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2406-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

