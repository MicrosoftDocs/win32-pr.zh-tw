---
title: MDM_HealthAttestation 類別
description: MDM \_ HealthAttestation 類別可讓企業 IT 管理員評估受管理裝置的健全狀況，並採取企業原則動作。
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation 類別
- MDM_HealthAttestation 類別，描述
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464857"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="687da-105">MDM \_ HealthAttestation 類別</span><span class="sxs-lookup"><span data-stu-id="687da-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="687da-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="687da-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="687da-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="687da-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="687da-108">**MDM \_ HealthAttestation** 類別可讓企業 IT 管理員評估受管理裝置的健全狀況，並採取企業原則動作。</span><span class="sxs-lookup"><span data-stu-id="687da-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="687da-109">以下是 HealthAttestation CSP 所執行的函式清單：</span><span class="sxs-lookup"><span data-stu-id="687da-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="687da-110">收集用來驗證裝置健康情況狀態的資料</span><span class="sxs-lookup"><span data-stu-id="687da-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="687da-111">將資料轉送到「健康情況證明服務」(HAS)</span><span class="sxs-lookup"><span data-stu-id="687da-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="687da-112">布建從中接收的健康情況證明憑證</span><span class="sxs-lookup"><span data-stu-id="687da-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="687da-113">在要求時，會將接收自的健康情況證明 (憑證轉寄) ，並將相關的執行時間資訊轉送至 MDM 伺服器以進行驗證</span><span class="sxs-lookup"><span data-stu-id="687da-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="687da-114">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="687da-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="687da-115">語法</span><span class="sxs-lookup"><span data-stu-id="687da-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="687da-116">成員</span><span class="sxs-lookup"><span data-stu-id="687da-116">Members</span></span>

<span data-ttu-id="687da-117">**MDM \_ HealthAttestation** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="687da-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="687da-118">方法</span><span class="sxs-lookup"><span data-stu-id="687da-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="687da-119">屬性</span><span class="sxs-lookup"><span data-stu-id="687da-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="687da-120">方法</span><span class="sxs-lookup"><span data-stu-id="687da-120">Methods</span></span>

<span data-ttu-id="687da-121">**MDM \_ HealthAttestation** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="687da-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="687da-122">方法</span><span class="sxs-lookup"><span data-stu-id="687da-122">Method</span></span>                                                                 | <span data-ttu-id="687da-123">描述</span><span class="sxs-lookup"><span data-stu-id="687da-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="687da-124">**VerifyHealthMethod**</span><span class="sxs-lookup"><span data-stu-id="687da-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="687da-125">通知裝置以準備健康情況憑證驗證要求的方法。</span><span class="sxs-lookup"><span data-stu-id="687da-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="687da-126">屬性</span><span class="sxs-lookup"><span data-stu-id="687da-126">Properties</span></span>

<span data-ttu-id="687da-127">**MDM \_ HealthAttestation** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="687da-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687da-128">[[MSSQLSERVER 的通訊協定內容]](/windows/client-management/mdm/healthattestation-csp)</span><span class="sxs-lookup"><span data-stu-id="687da-128">[Certificate](/windows/client-management/mdm/healthattestation-csp)</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="687da-131">限定詞： **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="687da-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="687da-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="687da-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687da-135">**CurrentProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="687da-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-136">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="687da-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="687da-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="687da-138">TBD</span><span class="sxs-lookup"><span data-stu-id="687da-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="687da-139">ForceRetrieve</span><span class="sxs-lookup"><span data-stu-id="687da-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-140">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="687da-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="687da-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="687da-142">HASEndpoint</span><span class="sxs-lookup"><span data-stu-id="687da-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-143">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-144">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687da-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="687da-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687da-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687da-148">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="687da-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="687da-149">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="687da-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="687da-150">此類別的字串為 "HealthAttestation"。</span><span class="sxs-lookup"><span data-stu-id="687da-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="687da-151">**MaxSupportedProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="687da-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-152">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="687da-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="687da-153">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="687da-154">TBD</span><span class="sxs-lookup"><span data-stu-id="687da-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="687da-155">Nonce</span><span class="sxs-lookup"><span data-stu-id="687da-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687da-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="687da-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="687da-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687da-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="687da-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687da-161">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="687da-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="687da-162">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="687da-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="687da-163">此類別的字串為 "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="687da-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="687da-164">**PreferredMaxProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="687da-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="687da-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="687da-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="687da-167">TBD</span><span class="sxs-lookup"><span data-stu-id="687da-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="687da-168">狀態</span><span class="sxs-lookup"><span data-stu-id="687da-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-169">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="687da-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="687da-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="687da-171">TpmReadyStatus</span><span class="sxs-lookup"><span data-stu-id="687da-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="687da-172">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="687da-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="687da-173">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="687da-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="687da-174">規格需求</span><span class="sxs-lookup"><span data-stu-id="687da-174">Requirements</span></span>



| <span data-ttu-id="687da-175">需求</span><span class="sxs-lookup"><span data-stu-id="687da-175">Requirement</span></span> | <span data-ttu-id="687da-176">值</span><span class="sxs-lookup"><span data-stu-id="687da-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="687da-177">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="687da-177">Minimum supported client</span></span><br/> | <span data-ttu-id="687da-178">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="687da-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="687da-179">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="687da-179">Minimum supported server</span></span><br/> | <span data-ttu-id="687da-180">都不支援</span><span class="sxs-lookup"><span data-stu-id="687da-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="687da-181">命名空間</span><span class="sxs-lookup"><span data-stu-id="687da-181">Namespace</span></span><br/>                | <span data-ttu-id="687da-182">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="687da-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="687da-183">MOF</span><span class="sxs-lookup"><span data-stu-id="687da-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687da-184"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="687da-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="687da-185">DLL</span><span class="sxs-lookup"><span data-stu-id="687da-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687da-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="687da-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="687da-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="687da-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687da-188">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="687da-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

