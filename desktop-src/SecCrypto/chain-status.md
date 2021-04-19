---
description: 抓取鏈的有效狀態或鏈中的特定憑證。
title: IChain2：： Status 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Status
- IChain.Status
- Chain.Status
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23673289e2ff39d4180a4be8dc0be61f4a5cffc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987174"
---
# <a name="ichain2status-property"></a><span data-ttu-id="25a87-103">IChain2：： Status 屬性</span><span class="sxs-lookup"><span data-stu-id="25a87-103">IChain2::Status property</span></span>

<span data-ttu-id="25a87-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="25a87-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="25a87-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="25a87-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="25a87-106">**Status** 屬性會抓取鏈的有效狀態或鏈中的特定憑證。</span><span class="sxs-lookup"><span data-stu-id="25a87-106">The **Status** property retrieves the validity status of the chain or a specific certificate in the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="25a87-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="25a87-107">Syntax</span></span>


```VB
Chain.Status( _
  ByVal Index _
) As Long
```



## <a name="property-value"></a><span data-ttu-id="25a87-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="25a87-108">Property value</span></span>

<span data-ttu-id="25a87-109">**LONG** 值，表示鏈或指定憑證的有效狀態指標。</span><span class="sxs-lookup"><span data-stu-id="25a87-109">A **LONG** value that represents the validity status indicator of the chain or the specified certificate.</span></span> <span data-ttu-id="25a87-110">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="25a87-110">The following table shows the possible values.</span></span> <span data-ttu-id="25a87-111">如果鏈或指定的憑證有效，則這個屬性會包含零。</span><span class="sxs-lookup"><span data-stu-id="25a87-111">This property will contain zero if the chain or specified certificate is valid.</span></span> <span data-ttu-id="25a87-112">否則，此屬性會包含一或多個下列值的組合。</span><span class="sxs-lookup"><span data-stu-id="25a87-112">Otherwise, this property will contain a combination of one or more of the following values.</span></span>

<dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>

<span data-ttu-id="25a87-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 時間 \_ 有效** (&H00000001) </span><span class="sxs-lookup"><span data-stu-id="25a87-113"><span id="CAPICOM_TRUST_IS_NOT_TIME_VALID"></span><span id="capicom_trust_is_not_time_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_VALID** (&H00000001)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-114">此憑證或憑證鏈中的其中一個憑證的時間無效。</span><span class="sxs-lookup"><span data-stu-id="25a87-114">This certificate or one of the certificates in the certificate chain is not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>

<span data-ttu-id="25a87-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 時間 \_ 嵌套** (&H00000002) </span><span class="sxs-lookup"><span data-stu-id="25a87-115"><span id="CAPICOM_TRUST_IS_NOT_TIME_NESTED"></span><span id="capicom_trust_is_not_time_nested"></span>**CAPICOM\_TRUST\_IS\_NOT\_TIME\_NESTED** (&H00000002)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-116">鏈中的憑證未正確地進行時間嵌套。</span><span class="sxs-lookup"><span data-stu-id="25a87-116">Certificates in the chain are not properly time nested.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>

<span data-ttu-id="25a87-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM \_ (&\_ H00000004 \_ 撤銷信任**) </span><span class="sxs-lookup"><span data-stu-id="25a87-117"><span id="CAPICOM_TRUST_IS_REVOKED"></span><span id="capicom_trust_is_revoked"></span>**CAPICOM\_TRUST\_IS\_REVOKED** (&H00000004)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-118">此憑證的信任或憑證鏈中的其中一個憑證已遭撤銷。</span><span class="sxs-lookup"><span data-stu-id="25a87-118">Trust for this certificate or one of the certificates in the certificate chain has been revoked.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>

<span data-ttu-id="25a87-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM \_信任 \_ 不 \_ 是 \_ 簽名碼 \_ 有效** (&H00000008) </span><span class="sxs-lookup"><span data-stu-id="25a87-119"><span id="CAPICOM_TRUST_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_is_not_signature_valid"></span>**CAPICOM\_TRUST\_IS\_NOT\_SIGNATURE\_VALID** (&H00000008)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-120">憑證或憑證鏈中的其中一個憑證沒有有效的簽章。</span><span class="sxs-lookup"><span data-stu-id="25a87-120">The certificate or one of the certificates in the certificate chain does not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>

<span data-ttu-id="25a87-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM \_信任 \_ 對 (&H00000010 \_ \_ \_ 的 \_ 使用** 方式無效) </span><span class="sxs-lookup"><span data-stu-id="25a87-121"><span id="CAPICOM_TRUST_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00000010)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-122">憑證或憑證鏈的建議使用方式無效。</span><span class="sxs-lookup"><span data-stu-id="25a87-122">The certificate or certificate chain is not valid for its proposed usage.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>

<span data-ttu-id="25a87-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM \_信任 \_ 是不 \_ 受信任的 \_ 根** (&H00000020) </span><span class="sxs-lookup"><span data-stu-id="25a87-123"><span id="CAPICOM_TRUST_IS_UNTRUSTED_ROOT"></span><span id="capicom_trust_is_untrusted_root"></span>**CAPICOM\_TRUST\_IS\_UNTRUSTED\_ROOT** (&H00000020)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-124">憑證或憑證鏈是以不受信任的根目錄為基礎。</span><span class="sxs-lookup"><span data-stu-id="25a87-124">The certificate or certificate chain is based on an untrusted root.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>

<span data-ttu-id="25a87-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM \_信任 \_ 撤銷 \_ 狀態 \_ 不明** (&H00000040) </span><span class="sxs-lookup"><span data-stu-id="25a87-125"><span id="CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN"></span><span id="capicom_trust_revocation_status_unknown"></span>**CAPICOM\_TRUST\_REVOCATION\_STATUS\_UNKNOWN** (&H00000040)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-126">憑證或憑證鏈中的其中一個憑證的撤銷狀態不明。</span><span class="sxs-lookup"><span data-stu-id="25a87-126">The revocation status of the certificate or one of the certificates in the certificate chain is unknown.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>

<span data-ttu-id="25a87-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM \_信任 \_ 是 \_ 迴圈** (&H00000080) </span><span class="sxs-lookup"><span data-stu-id="25a87-127"><span id="CAPICOM_TRUST_IS_CYCLIC"></span><span id="capicom_trust_is_cyclic"></span>**CAPICOM\_TRUST\_IS\_CYCLIC** (&H00000080)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-128">鏈中的其中一個憑證是由原始憑證已認證的 [*憑證授權單位*](../secgloss/c-gly.md) 單位所發出。</span><span class="sxs-lookup"><span data-stu-id="25a87-128">One of the certificates in the chain was issued by a [*certification authority*](../secgloss/c-gly.md) that the original certificate had certified.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>

<span data-ttu-id="25a87-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM \_信任 \_ 不正確 \_ 延伸** 模組 (&H00000100) </span><span class="sxs-lookup"><span data-stu-id="25a87-129"><span id="CAPICOM_TRUST_INVALID_EXTENSION"></span><span id="capicom_trust_invalid_extension"></span>**CAPICOM\_TRUST\_INVALID\_EXTENSION** (&H00000100)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-130">其中一個憑證具有不正確延伸模組。</span><span class="sxs-lookup"><span data-stu-id="25a87-130">One of the certificates has an extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>

<span data-ttu-id="25a87-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM \_ (&H00000200) 信任 \_ 不正確 \_ 原則 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="25a87-131"><span id="CAPICOM_TRUST_INVALID_POLICY_CONSTRAINTS"></span><span id="capicom_trust_invalid_policy_constraints"></span>**CAPICOM\_TRUST\_INVALID\_POLICY\_CONSTRAINTS** (&H00000200)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-132">憑證或憑證鏈中的其中一個憑證具有原則條件約束延伸，而其中一個已發行的憑證有不允許的原則對應延伸，或沒有必要的發佈原則延伸。</span><span class="sxs-lookup"><span data-stu-id="25a87-132">The certificate or one of the certificates in the certificate chain has a policy constraints extension, and one of the issued certificates has a disallowed policy mapping extension or does not have a required issuance policies extension.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>

<span data-ttu-id="25a87-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM \_信任 \_ 不正確 \_ 基本 \_ 條件約束** (&H00000400) </span><span class="sxs-lookup"><span data-stu-id="25a87-133"><span id="CAPICOM_TRUST_INVALID_BASIC_CONSTRAINTS"></span><span id="capicom_trust_invalid_basic_constraints"></span>**CAPICOM\_TRUST\_INVALID\_BASIC\_CONSTRAINTS** (&H00000400)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-134">憑證或憑證鏈中的其中一個憑證具有基本的限制延伸，而憑證無法用來發行其他憑證，或已超過鏈路徑長度。</span><span class="sxs-lookup"><span data-stu-id="25a87-134">The certificate or one of the certificates in the certificate chain has a basic constraints extension, and either the certificate cannot be used to issue other certificates, or the chain path length has been exceeded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>

<span data-ttu-id="25a87-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM \_信任 \_ 不正確 \_ 名稱 \_ 條件約束** (&H00000800) </span><span class="sxs-lookup"><span data-stu-id="25a87-135"><span id="CAPICOM_TRUST_INVALID_NAME_CONSTRAINTS"></span><span id="capicom_trust_invalid_name_constraints"></span>**CAPICOM\_TRUST\_INVALID\_NAME\_CONSTRAINTS** (&H00000800)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-136">憑證或憑證鏈中的其中一個憑證具有不正確名稱限制延伸。</span><span class="sxs-lookup"><span data-stu-id="25a87-136">The certificate or one of the certificates in the certificate chain has a name constraints extension that is not valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>

<span data-ttu-id="25a87-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM \_信任 \_ 不支援 (&H00001000) 的 \_ \_ \_ 名稱 \_ 條件約束**</span><span class="sxs-lookup"><span data-stu-id="25a87-137"><span id="CAPICOM_TRUST_HAS_NOT_SUPPORTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_supported_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_SUPPORTED\_NAME\_CONSTRAINT** (&H00001000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-138">憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，其包含不受支援的欄位。</span><span class="sxs-lookup"><span data-stu-id="25a87-138">The certificate or one of the certificates in the certificate chain has a name constraints extension that contains unsupported fields.</span></span> <span data-ttu-id="25a87-139">不支援最小和最大欄位。</span><span class="sxs-lookup"><span data-stu-id="25a87-139">The minimum and maximum fields are not supported.</span></span> <span data-ttu-id="25a87-140">因此，最小值必須一律為零，且最大值必須一律不存在。</span><span class="sxs-lookup"><span data-stu-id="25a87-140">Thus minimum must always be zero and maximum must always be absent.</span></span> <span data-ttu-id="25a87-141">僅支援其他名稱的 UPN。</span><span class="sxs-lookup"><span data-stu-id="25a87-141">Only UPN is supported for an Other Name.</span></span> <span data-ttu-id="25a87-142">不支援下列替代名稱選擇：</span><span class="sxs-lookup"><span data-stu-id="25a87-142">The following alternative name choices are not supported:</span></span>

-   <span data-ttu-id="25a87-143">X400 位址</span><span class="sxs-lookup"><span data-stu-id="25a87-143">X400 Address</span></span>
-   <span data-ttu-id="25a87-144">EDI 合作物件名稱</span><span class="sxs-lookup"><span data-stu-id="25a87-144">EDI Party Name</span></span>
-   <span data-ttu-id="25a87-145">註冊的識別碼</span><span class="sxs-lookup"><span data-stu-id="25a87-145">Registered Id</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>

<span data-ttu-id="25a87-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM \_信任 \_ \_ 未 \_ 定義 \_ 名稱 \_ 條件約束** (&H00002000) </span><span class="sxs-lookup"><span data-stu-id="25a87-146"><span id="CAPICOM_TRUST_HAS_NOT_DEFINED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_defined_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_DEFINED\_NAME\_CONSTRAINT** (&H00002000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-147">憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且在終端憑證中的其中一個名稱選擇缺少名稱條件約束。</span><span class="sxs-lookup"><span data-stu-id="25a87-147">The certificate or one of the certificates in the certificate chain has a name constraints extension, and a name constraint is missing for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>

<span data-ttu-id="25a87-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM \_信任在 H00004000 中 \_ \_ 不 \_ 允許 \_ 名稱 \_ 條件約束** (&) </span><span class="sxs-lookup"><span data-stu-id="25a87-148"><span id="CAPICOM_TRUST_HAS_NOT_PERMITTED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_not_permitted_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_NOT\_PERMITTED\_NAME\_CONSTRAINT** (&H00004000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-149">憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且在終端憑證中的其中一個名稱選擇不會有允許的名稱限制。</span><span class="sxs-lookup"><span data-stu-id="25a87-149">The certificate or one of the certificates in the certificate chain has a name constraints extension, and there is not a permitted name constraint for one of the name choices in the end certificate.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>

<span data-ttu-id="25a87-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM \_信任 \_ 已 \_ 排除 \_ 名稱 \_ 條件約束** (&H00008000) </span><span class="sxs-lookup"><span data-stu-id="25a87-150"><span id="CAPICOM_TRUST_HAS_EXCLUDED_NAME_CONSTRAINT"></span><span id="capicom_trust_has_excluded_name_constraint"></span>**CAPICOM\_TRUST\_HAS\_EXCLUDED\_NAME\_CONSTRAINT** (&H00008000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-151">憑證或憑證鏈中的其中一個憑證具有名稱限制延伸，而且會明確排除終端憑證中的其中一個名稱選擇。</span><span class="sxs-lookup"><span data-stu-id="25a87-151">The certificate or one of the certificates in the certificate chain has a name constraints extension, and one of the name choices in the end certificate is explicitly excluded.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>

<span data-ttu-id="25a87-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM \_信任 \_ \_ 離線 \_ 撤銷** (&H01000000) </span><span class="sxs-lookup"><span data-stu-id="25a87-152"><span id="CAPICOM_TRUST_IS_OFFLINE_REVOCATION"></span><span id="capicom_trust_is_offline_revocation"></span>**CAPICOM\_TRUST\_IS\_OFFLINE\_REVOCATION** (&H01000000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-153">憑證的撤銷狀態，或憑證鏈中的其中一個憑證已離線或過時。</span><span class="sxs-lookup"><span data-stu-id="25a87-153">The revocation status of the certificate or one of the certificates in the certificate chain is either offline or stale.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>

<span data-ttu-id="25a87-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM \_ (&H02000000) 信任 \_ 無 \_ 發佈 \_ 鏈 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="25a87-154"><span id="CAPICOM_TRUST_NO_ISSUANCE_CHAIN_POLICY"></span><span id="capicom_trust_no_issuance_chain_policy"></span>**CAPICOM\_TRUST\_NO\_ISSUANCE\_CHAIN\_POLICY** (&H02000000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-155">終端憑證沒有任何產生的發佈原則，而且其中一個發行 CA 憑證有需要的原則限制延伸。</span><span class="sxs-lookup"><span data-stu-id="25a87-155">The end certificate does not have any resultant issuance policies, and one of the issuing CA certificates has a policy constraints extension requiring it.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>

<span data-ttu-id="25a87-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM \_信任 \_ 是 (&H00010000 的 \_ 部分 \_ 鏈**) </span><span class="sxs-lookup"><span data-stu-id="25a87-156"><span id="CAPICOM_TRUST_IS_PARTIAL_CHAIN"></span><span id="capicom_trust_is_partial_chain"></span>**CAPICOM\_TRUST\_IS\_PARTIAL\_CHAIN** (&H00010000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-157">憑證鏈不會競爭。</span><span class="sxs-lookup"><span data-stu-id="25a87-157">The certificate chain is not compete.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>

<span data-ttu-id="25a87-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM \_信任 \_ CTL \_ \_ 不是 \_ 時間 \_ 有效** (&H00020000) </span><span class="sxs-lookup"><span data-stu-id="25a87-158"><span id="CAPICOM_TRUST_CTL_IS_NOT_TIME_VALID"></span><span id="capicom_trust_ctl_is_not_time_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_TIME\_VALID** (&H00020000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-159">用來建立此鏈的 CTL 沒有時間有效。</span><span class="sxs-lookup"><span data-stu-id="25a87-159">A CTL used to create this chain was not time valid.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>

<span data-ttu-id="25a87-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM \_信任 \_ CTL \_ \_ 不是 \_ \_** 簽章有效 (&H00040000) </span><span class="sxs-lookup"><span data-stu-id="25a87-160"><span id="CAPICOM_TRUST_CTL_IS_NOT_SIGNATURE_VALID"></span><span id="capicom_trust_ctl_is_not_signature_valid"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_SIGNATURE\_VALID** (&H00040000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-161">用來建立此鏈的 CTL 沒有有效的簽章。</span><span class="sxs-lookup"><span data-stu-id="25a87-161">A CTL used to create this chain did not have a valid signature.</span></span>

</dd> <dt>

<span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>

<span data-ttu-id="25a87-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM \_信賴 \_ CTL \_ 對 (&H00080000 \_ \_ \_ 的 \_ 使用** 方式無效) </span><span class="sxs-lookup"><span data-stu-id="25a87-162"><span id="CAPICOM_TRUST_CTL_IS_NOT_VALID_FOR_USAGE"></span><span id="capicom_trust_ctl_is_not_valid_for_usage"></span>**CAPICOM\_TRUST\_CTL\_IS\_NOT\_VALID\_FOR\_USAGE** (&H00080000)</span></span>


</dt> <dd>

<span data-ttu-id="25a87-163">用來建立此鏈的 CTL 對此使用方式無效。</span><span class="sxs-lookup"><span data-stu-id="25a87-163">A CTL used to create this chain is not valid for this usage.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25a87-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="25a87-164">Requirements</span></span>



| <span data-ttu-id="25a87-165">需求</span><span class="sxs-lookup"><span data-stu-id="25a87-165">Requirement</span></span> | <span data-ttu-id="25a87-166">值</span><span class="sxs-lookup"><span data-stu-id="25a87-166">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25a87-167">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="25a87-167">End of client support</span></span><br/> | <span data-ttu-id="25a87-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25a87-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="25a87-169">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="25a87-169">End of server support</span></span><br/> | <span data-ttu-id="25a87-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25a87-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="25a87-171">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="25a87-171">Redistributable</span></span><br/>       | <span data-ttu-id="25a87-172">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="25a87-172">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="25a87-173">DLL</span><span class="sxs-lookup"><span data-stu-id="25a87-173">DLL</span></span><br/>                   | <dl> <span data-ttu-id="25a87-174"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25a87-174"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
