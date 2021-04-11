---
title: MDM_Policy_Config01_DeliveryOptimization02 類別
description: MDM \_ Policy \_ Config01 \_ DeliveryOptimization02 類別表示可用的傳遞優化原則。
ms.assetid: 10dfb751-f044-4f30-90e0-af0fcb0931fb
keywords:
- MDM_Policy_Config01_DeliveryOptimization02 類別
- MDM_Policy_Config01_DeliveryOptimization02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeliveryOptimization02
- MDM_Policy_Config01_DeliveryOptimization02.InstanceID
- MDM_Policy_Config01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb9675f87a5bf9951e125bded69ae5eb10feb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094256"
---
# <a name="mdm_policy_config01_deliveryoptimization02-class"></a><span data-ttu-id="17f12-105">MDM \_ 原則 \_ Config01 \_ DeliveryOptimization02 類別</span><span class="sxs-lookup"><span data-stu-id="17f12-105">MDM\_Policy\_Config01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="17f12-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="17f12-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="17f12-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="17f12-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="17f12-108">**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別表示可用的傳遞優化原則。</span><span class="sxs-lookup"><span data-stu-id="17f12-108">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="17f12-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="17f12-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17f12-110">語法</span><span class="sxs-lookup"><span data-stu-id="17f12-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="17f12-111">成員</span><span class="sxs-lookup"><span data-stu-id="17f12-111">Members</span></span>

<span data-ttu-id="17f12-112">**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="17f12-112">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="17f12-113">屬性</span><span class="sxs-lookup"><span data-stu-id="17f12-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17f12-114">屬性</span><span class="sxs-lookup"><span data-stu-id="17f12-114">Properties</span></span>

<span data-ttu-id="17f12-115">**MDM \_ Policy \_ Config01 \_ DeliveryOptimization02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="17f12-115">The **MDM\_Policy\_Config01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="17f12-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="17f12-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="17f12-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="17f12-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17f12-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="17f12-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="17f12-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17f12-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="17f12-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="17f12-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="17f12-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="17f12-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="17f12-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="17f12-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="17f12-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="17f12-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="17f12-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="17f12-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17f12-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="17f12-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17f12-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="17f12-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="17f12-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="17f12-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17f12-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17f12-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17f12-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-169">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17f12-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17f12-170">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17f12-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17f12-171">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="17f12-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="17f12-172">此類別的字串為 ">deliveryoptimization"。</span><span class="sxs-lookup"><span data-stu-id="17f12-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="17f12-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="17f12-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17f12-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="17f12-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17f12-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="17f12-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17f12-176">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17f12-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="17f12-177">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="17f12-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="17f12-178">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="17f12-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17f12-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="17f12-179">Requirements</span></span>



| <span data-ttu-id="17f12-180">需求</span><span class="sxs-lookup"><span data-stu-id="17f12-180">Requirement</span></span> | <span data-ttu-id="17f12-181">值</span><span class="sxs-lookup"><span data-stu-id="17f12-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17f12-182">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17f12-182">Minimum supported client</span></span><br/> | <span data-ttu-id="17f12-183">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17f12-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17f12-184">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17f12-184">Minimum supported server</span></span><br/> | <span data-ttu-id="17f12-185">都不支援</span><span class="sxs-lookup"><span data-stu-id="17f12-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="17f12-186">命名空間</span><span class="sxs-lookup"><span data-stu-id="17f12-186">Namespace</span></span><br/>                | <span data-ttu-id="17f12-187">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="17f12-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="17f12-188">MOF</span><span class="sxs-lookup"><span data-stu-id="17f12-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17f12-189"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="17f12-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17f12-190">DLL</span><span class="sxs-lookup"><span data-stu-id="17f12-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17f12-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17f12-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f12-192">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17f12-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f12-193">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="17f12-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

