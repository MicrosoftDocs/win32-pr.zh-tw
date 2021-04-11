---
title: MDM_Policy_Config01_RemoteManagement02 類別
description: MDM \_ 原則 \_ Config01 \_ RemoteManagement02 遠端系統管理原則。
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- MDM_Policy_Config01_RemoteManagement02 類別
- MDM_Policy_Config01_RemoteManagement02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843539"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="0f94c-105">MDM \_ 原則 \_ Config01 \_ RemoteManagement02 類別</span><span class="sxs-lookup"><span data-stu-id="0f94c-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="0f94c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="0f94c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f94c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="0f94c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f94c-108">MDM \_ 原則 \_ Config01 \_ RemoteManagement02 遠端系統管理原則。</span><span class="sxs-lookup"><span data-stu-id="0f94c-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="0f94c-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0f94c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f94c-110">語法</span><span class="sxs-lookup"><span data-stu-id="0f94c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="0f94c-111">成員</span><span class="sxs-lookup"><span data-stu-id="0f94c-111">Members</span></span>

<span data-ttu-id="0f94c-112">**MDM \_ Policy \_ Config01 \_ RemoteManagement02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0f94c-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="0f94c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="0f94c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f94c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="0f94c-114">Properties</span></span>

<span data-ttu-id="0f94c-115">**MDM \_ Policy \_ Config01 \_ RemoteManagement02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0f94c-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0f94c-116">AllowBasicAuthentication \_ 用戶端</span><span class="sxs-lookup"><span data-stu-id="0f94c-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-119">AllowBasicAuthentication \_ 服務</span><span class="sxs-lookup"><span data-stu-id="0f94c-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-120">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="0f94c-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="0f94c-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-126">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="0f94c-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-131">AllowUnencryptedTraffic \_ 用戶端</span><span class="sxs-lookup"><span data-stu-id="0f94c-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-134">AllowUnencryptedTraffic \_ 服務</span><span class="sxs-lookup"><span data-stu-id="0f94c-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="0f94c-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="0f94c-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="0f94c-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="0f94c-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f94c-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0f94c-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0f94c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-152">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f94c-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f94c-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0f94c-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0f94c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-156">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f94c-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="0f94c-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-159">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="0f94c-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="0f94c-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0f94c-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="0f94c-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f94c-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0f94c-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f94c-168">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0f94c-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f94c-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f94c-169">Requirements</span></span>



| <span data-ttu-id="0f94c-170">需求</span><span class="sxs-lookup"><span data-stu-id="0f94c-170">Requirement</span></span> | <span data-ttu-id="0f94c-171">值</span><span class="sxs-lookup"><span data-stu-id="0f94c-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f94c-172">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f94c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0f94c-173">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f94c-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f94c-174">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f94c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0f94c-175">都不支援</span><span class="sxs-lookup"><span data-stu-id="0f94c-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0f94c-176">命名空間</span><span class="sxs-lookup"><span data-stu-id="0f94c-176">Namespace</span></span><br/>                | <span data-ttu-id="0f94c-177">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0f94c-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0f94c-178">MOF</span><span class="sxs-lookup"><span data-stu-id="0f94c-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f94c-179"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f94c-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f94c-180">DLL</span><span class="sxs-lookup"><span data-stu-id="0f94c-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f94c-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f94c-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

