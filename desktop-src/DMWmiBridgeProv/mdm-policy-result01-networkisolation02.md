---
title: MDM_Policy_Result01_NetworkIsolation02 類別
description: MDM \_ Policy \_ Result01 \_ NetworkIsolation02 類別代表可用的瀏覽器原則。
ms.assetid: f44f43fb-813b-4d40-a56c-0c497e004a8a
keywords:
- MDM_Policy_Result01_NetworkIsolation02 類別
- MDM_Policy_Result01_NetworkIsolation02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02.InstanceID
- MDM_Policy_Result01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5611d7e00ab0fa5210a657b55a3f2990fdf40880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094403"
---
# <a name="mdm_policy_result01_networkisolation02-class"></a><span data-ttu-id="d533c-105">MDM \_ 原則 \_ Result01 \_ NetworkIsolation02 類別</span><span class="sxs-lookup"><span data-stu-id="d533c-105">MDM\_Policy\_Result01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="d533c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="d533c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d533c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="d533c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d533c-108">**MDM \_ Policy \_ Result01 \_ NetworkIsolation02** 類別代表可用的瀏覽器原則。</span><span class="sxs-lookup"><span data-stu-id="d533c-108">The **MDM\_Policy\_Result01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="d533c-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d533c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d533c-110">語法</span><span class="sxs-lookup"><span data-stu-id="d533c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
  string NeutralResources;
};
```

## <a name="members"></a><span data-ttu-id="d533c-111">成員</span><span class="sxs-lookup"><span data-stu-id="d533c-111">Members</span></span>

<span data-ttu-id="d533c-112">**MDM \_ Policy \_ Result01 \_ NetworkIsolation02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d533c-112">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="d533c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d533c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d533c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="d533c-114">Properties</span></span>

<span data-ttu-id="d533c-115">**MDM \_ Policy \_ Result01 \_ NetworkIsolation02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d533c-115">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d533c-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="d533c-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="d533c-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="d533c-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d533c-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d533c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="d533c-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="d533c-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d533c-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d533c-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="d533c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d533c-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d533c-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d533c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d533c-140">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d533c-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d533c-141">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d533c-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="d533c-142">此類別的字串為 "NetworkIsolation"。</span><span class="sxs-lookup"><span data-stu-id="d533c-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="d533c-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="d533c-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d533c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d533c-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d533c-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d533c-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d533c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d533c-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d533c-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d533c-149">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d533c-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d533c-150">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="d533c-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="d533c-151">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="d533c-151">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d533c-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="d533c-152">Requirements</span></span>



| <span data-ttu-id="d533c-153">需求</span><span class="sxs-lookup"><span data-stu-id="d533c-153">Requirement</span></span> | <span data-ttu-id="d533c-154">值</span><span class="sxs-lookup"><span data-stu-id="d533c-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d533c-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d533c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d533c-156">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d533c-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d533c-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d533c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d533c-158">都不支援</span><span class="sxs-lookup"><span data-stu-id="d533c-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d533c-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="d533c-159">Namespace</span></span><br/>                | <span data-ttu-id="d533c-160">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="d533c-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d533c-161">MOF</span><span class="sxs-lookup"><span data-stu-id="d533c-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d533c-162"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d533c-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d533c-163">DLL</span><span class="sxs-lookup"><span data-stu-id="d533c-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d533c-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d533c-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

