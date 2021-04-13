---
title: IKE/AuthIP 結構
description: IKE/AuthIP 結構
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/27/2020
ms.locfileid: "104374681"
---
# <a name="ikeauthip-structures"></a><span data-ttu-id="bfa36-103">IKE/AuthIP 結構</span><span class="sxs-lookup"><span data-stu-id="bfa36-103">IKE/AuthIP Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bfa36-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="bfa36-104">In this section</span></span>

-   [<span data-ttu-id="bfa36-105">**IKEEXT \_ 驗證 \_ METHOD0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-105">**IKEEXT\_AUTHENTICATION\_METHOD0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [<span data-ttu-id="bfa36-106">**IKEEXT \_ 驗證 \_ METHOD1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-106">**IKEEXT\_AUTHENTICATION\_METHOD1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [<span data-ttu-id="bfa36-107">**IKEEXT \_ 驗證 \_ METHOD2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-107">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="bfa36-108">**IKEEXT \_ CERT \_ EKUS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-108">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="bfa36-109">**IKEEXT \_ CERT \_ .name0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-109">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="bfa36-110">**IKEEXT \_ 憑證 \_ 根 \_ CONFIG0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-110">**IKEEXT\_CERT\_ROOT\_CONFIG0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [<span data-ttu-id="bfa36-111">**IKEEXT \_ 憑證 \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-111">**IKEEXT\_CERTIFICATE\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [<span data-ttu-id="bfa36-112">**IKEEXT \_ 憑證 \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-112">**IKEEXT\_CERTIFICATE\_AUTHENTICATION1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [<span data-ttu-id="bfa36-113">**IKEEXT \_ 憑證 \_ AUTHENTICATION2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-113">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="bfa36-114">**IKEEXT \_ 憑證 \_ CREDENTIAL0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-114">**IKEEXT\_CERTIFICATE\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [<span data-ttu-id="bfa36-115">**IKEEXT \_ 憑證 \_ CREDENTIAL1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-115">**IKEEXT\_CERTIFICATE\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [<span data-ttu-id="bfa36-116">**IKEEXT \_ 憑證 \_ CRITERIA0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-116">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="bfa36-117">**IKEEXT \_ 加密 \_ ALGORITHM0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-117">**IKEEXT\_CIPHER\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [<span data-ttu-id="bfa36-118">**IKEEXT \_ 一般 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-118">**IKEEXT\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [<span data-ttu-id="bfa36-119">**IKEEXT \_ 一般 \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-119">**IKEEXT\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [<span data-ttu-id="bfa36-120">**IKEEXT \_ COOKIE \_ PAIR0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-120">**IKEEXT\_COOKIE\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [<span data-ttu-id="bfa36-121">**IKEEXT \_ CREDENTIAL0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-121">**IKEEXT\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [<span data-ttu-id="bfa36-122">**IKEEXT \_ CREDENTIAL1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-122">**IKEEXT\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [<span data-ttu-id="bfa36-123">**IKEEXT \_ CREDENTIAL2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-123">**IKEEXT\_CREDENTIAL2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [<span data-ttu-id="bfa36-124">**IKEEXT \_ CREDENTIALS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-124">**IKEEXT\_CREDENTIALS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [<span data-ttu-id="bfa36-125">**IKEEXT \_ CREDENTIALS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-125">**IKEEXT\_CREDENTIALS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [<span data-ttu-id="bfa36-126">**IKEEXT \_ CREDENTIALS2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-126">**IKEEXT\_CREDENTIALS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [<span data-ttu-id="bfa36-127">**IKEEXT \_ 認證 \_ PAIR0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-127">**IKEEXT\_CREDENTIAL\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [<span data-ttu-id="bfa36-128">**IKEEXT \_ 認證 \_ PAIR1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-128">**IKEEXT\_CREDENTIAL\_PAIR1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [<span data-ttu-id="bfa36-129">**IKEEXT \_ 認證 \_ PAIR2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-129">**IKEEXT\_CREDENTIAL\_PAIR2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [<span data-ttu-id="bfa36-130">**IKEEXT \_ EAP \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-130">**IKEEXT\_EAP\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [<span data-ttu-id="bfa36-131">**IKEEXT \_ EM \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-131">**IKEEXT\_EM\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [<span data-ttu-id="bfa36-132">**IKEEXT \_ EM \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-132">**IKEEXT\_EM\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [<span data-ttu-id="bfa36-133">**IKEEXT \_ EM \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-133">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="bfa36-134">**IKEEXT \_ 完整性 \_ ALGORITHM0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-134">**IKEEXT\_INTEGRITY\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [<span data-ttu-id="bfa36-135">**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ 通用 \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-135">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [<span data-ttu-id="bfa36-136">**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ 通用 \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-136">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [<span data-ttu-id="bfa36-137">**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-137">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [<span data-ttu-id="bfa36-138">**IKEEXT \_ IP \_ 版本 \_ 特定的 \_ KEYMODULE \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-138">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [<span data-ttu-id="bfa36-139">**IKEEXT \_ IPV6 \_ CGA \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-139">**IKEEXT\_IPV6\_CGA\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [<span data-ttu-id="bfa36-140">**IKEEXT \_ KERBEROS \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-140">**IKEEXT\_KERBEROS\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [<span data-ttu-id="bfa36-141">**IKEEXT \_ KERBEROS \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-141">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="bfa36-142">**IKEEXT \_ KEYMODULE \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-142">**IKEEXT\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [<span data-ttu-id="bfa36-143">**IKEEXT \_ KEYMODULE \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-143">**IKEEXT\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [<span data-ttu-id="bfa36-144">**IKEEXT \_ 名稱 \_ CREDENTIAL0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-144">**IKEEXT\_NAME\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [<span data-ttu-id="bfa36-145">**IKEEXT \_ NTLM \_ V2 \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-145">**IKEEXT\_NTLM\_V2\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [<span data-ttu-id="bfa36-146">**IKEEXT \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-146">**IKEEXT\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [<span data-ttu-id="bfa36-147">**IKEEXT \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-147">**IKEEXT\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [<span data-ttu-id="bfa36-148">**IKEEXT \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-148">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="bfa36-149">**IKEEXT \_ 預先共用 \_ 金鑰 \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-149">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [<span data-ttu-id="bfa36-150">**IKEEXT \_ 預先共用 \_ 金鑰 \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-150">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [<span data-ttu-id="bfa36-151">**IKEEXT \_ PROPOSAL0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-151">**IKEEXT\_PROPOSAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [<span data-ttu-id="bfa36-152">**IKEEXT \_ 保留的 \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-152">**IKEEXT\_RESERVED\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [<span data-ttu-id="bfa36-153">**IKEEXT \_ SA \_ DETAILS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-153">**IKEEXT\_SA\_DETAILS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [<span data-ttu-id="bfa36-154">**IKEEXT \_ SA \_ DETAILS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-154">**IKEEXT\_SA\_DETAILS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [<span data-ttu-id="bfa36-155">**IKEEXT \_ SA \_ DETAILS2**</span><span class="sxs-lookup"><span data-stu-id="bfa36-155">**IKEEXT\_SA\_DETAILS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [<span data-ttu-id="bfa36-156">**IKEEXT \_ SA \_ 列舉 \_ TEMPLATE0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-156">**IKEEXT\_SA\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [<span data-ttu-id="bfa36-157">**IKEEXT \_ STATISTICS0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-157">**IKEEXT\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [<span data-ttu-id="bfa36-158">**IKEEXT \_ STATISTICS1**</span><span class="sxs-lookup"><span data-stu-id="bfa36-158">**IKEEXT\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [<span data-ttu-id="bfa36-159">**IKEEXT \_ TRAFFIC0**</span><span class="sxs-lookup"><span data-stu-id="bfa36-159">**IKEEXT\_TRAFFIC0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




