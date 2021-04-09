---
title: MDM_Policy_Result01_Connectivity02 類別
description: MDM \_ Policy \_ Result01 \_ Connectivity02 類別代表可用的連接原則。
ms.assetid: af5f21f8-8010-4e5a-b75f-30032333d87d
keywords:
- MDM_Policy_Result01_Connectivity02 類別
- MDM_Policy_Result01_Connectivity02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Connectivity02
- MDM_Policy_Result01_Connectivity02.InstanceID
- MDM_Policy_Result01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723e8fa3287f99994d45fcc0a8bc5a09473a7563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843240"
---
# <a name="mdm_policy_result01_connectivity02-class"></a><span data-ttu-id="5413e-105">MDM \_ 原則 \_ Result01 \_ Connectivity02 類別</span><span class="sxs-lookup"><span data-stu-id="5413e-105">MDM\_Policy\_Result01\_Connectivity02 class</span></span>

<span data-ttu-id="5413e-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="5413e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5413e-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="5413e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5413e-108">**MDM \_ Policy \_ Result01 \_ Connectivity02** 類別代表可用的連接原則。</span><span class="sxs-lookup"><span data-stu-id="5413e-108">The **MDM\_Policy\_Result01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="5413e-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="5413e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5413e-110">語法</span><span class="sxs-lookup"><span data-stu-id="5413e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="5413e-111">成員</span><span class="sxs-lookup"><span data-stu-id="5413e-111">Members</span></span>

<span data-ttu-id="5413e-112">**MDM \_ Policy \_ Result01 \_ Connectivity02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5413e-112">The **MDM\_Policy\_Result01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="5413e-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5413e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5413e-114">屬性</span><span class="sxs-lookup"><span data-stu-id="5413e-114">Properties</span></span>

<span data-ttu-id="5413e-115">**MDM \_ Policy \_ Result01 \_ Connectivity02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5413e-115">The **MDM\_Policy\_Result01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5413e-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="5413e-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="5413e-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="5413e-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="5413e-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="5413e-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="5413e-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="5413e-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="5413e-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="5413e-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="5413e-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="5413e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5413e-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="5413e-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5413e-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5413e-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5413e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5413e-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5413e-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5413e-153">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5413e-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="5413e-154">此類別的字串為 "Connectivity"。</span><span class="sxs-lookup"><span data-stu-id="5413e-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="5413e-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5413e-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-157">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="5413e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5413e-158">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5413e-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5413e-159">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5413e-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="5413e-160">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="5413e-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="5413e-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="5413e-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5413e-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="5413e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5413e-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="5413e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5413e-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="5413e-164">Requirements</span></span>



| <span data-ttu-id="5413e-165">需求</span><span class="sxs-lookup"><span data-stu-id="5413e-165">Requirement</span></span> | <span data-ttu-id="5413e-166">值</span><span class="sxs-lookup"><span data-stu-id="5413e-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5413e-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5413e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="5413e-168">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5413e-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5413e-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5413e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="5413e-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="5413e-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5413e-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="5413e-171">Namespace</span></span><br/>                | <span data-ttu-id="5413e-172">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="5413e-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5413e-173">MOF</span><span class="sxs-lookup"><span data-stu-id="5413e-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5413e-174"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="5413e-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5413e-175">DLL</span><span class="sxs-lookup"><span data-stu-id="5413e-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5413e-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5413e-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5413e-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5413e-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5413e-178">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="5413e-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

