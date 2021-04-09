---
title: 'EAP 相關的錯誤和資訊常數 (Eaphosterror .h) '
description: 所有 EAPHost API 技術通用的 EAP 相關錯誤和資訊常數的個別群組。
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025186"
---
# <a name="eap-related-error-and-information-constants"></a><span data-ttu-id="95172-103">EAP 相關的錯誤和資訊常數</span><span class="sxs-lookup"><span data-stu-id="95172-103">EAP Related Error and Information Constants</span></span>

<span data-ttu-id="95172-104">所有 EAPHost API 技術通用的 EAP 相關錯誤和資訊常數的個別群組。</span><span class="sxs-lookup"><span data-stu-id="95172-104">Individual groups of EAP related error and information constants common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="95172-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ FIRST**</span><span class="sxs-lookup"><span data-stu-id="95172-105"><span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP\_E\_EAPHOST\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-106">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="95172-106">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="95172-107">定義錯誤報表的界限;在 **eap \_ e \_ EAPHost \_ FIRST** 和 **eap \_ e \_ EAPHost \_** 之間，會發生任何 EAPHost 相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-107">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST \_ LAST**</span><span class="sxs-lookup"><span data-stu-id="95172-108"><span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP\_E\_EAPHOST\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-109">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="95172-109">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-110">定義錯誤報表的界限;在 **eap \_ e \_ EAPHost \_ FIRST** 和 **eap \_ e \_ EAPHost \_** 之間，會發生任何 EAPHost 相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-110">Defines the boundary of error reports; any EAPHost related error will occur between **EAP\_E\_EAPHOST\_FIRST** and **EAP\_E\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST \_ FIRST**</span><span class="sxs-lookup"><span data-stu-id="95172-111"><span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP\_I\_EAPHOST\_FIRST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-112">0x80420000L</span><span class="sxs-lookup"><span data-stu-id="95172-112">0x80420000L</span></span>
</dt> <dt>



<span data-ttu-id="95172-113">定義資訊報告的界限;所有 EAPHost 相關的資訊事件記錄都會出現在 **EAP \_ i \_ EAPHost \_ FIRST** 和 **eap EAPHost 的 \_ \_ \_ 最後**。</span><span class="sxs-lookup"><span data-stu-id="95172-113">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**\_ \_ EAPHOST \_ 前的 EAP**</span><span class="sxs-lookup"><span data-stu-id="95172-114"><span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP\_I\_EAPHOST\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-115">0x804200FFL</span><span class="sxs-lookup"><span data-stu-id="95172-115">0x804200FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-116">定義資訊報告的界限;所有 EAPHost 相關的資訊事件記錄都會出現在 **EAP \_ i \_ EAPHost \_ FIRST** 和 **eap EAPHost 的 \_ \_ \_ 最後**。</span><span class="sxs-lookup"><span data-stu-id="95172-116">Defines the boundary of information reports; any EAPHost related informational event logging will occur between **EAP\_I\_EAPHOST\_FIRST** and **EAP\_I\_EAPHOST\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_無法存取 EAP E \_ CERT \_ STORE \_**</span><span class="sxs-lookup"><span data-stu-id="95172-117"><span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**EAP\_E\_CERT\_STORE\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-118">0x80420011</span><span class="sxs-lookup"><span data-stu-id="95172-118">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="95172-119">驗證者或對等都不能存取證書存儲。</span><span class="sxs-lookup"><span data-stu-id="95172-119">Neither the authenticator or peer can access the certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ \_ \_ 未安裝 EAP E EAPHOST \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="95172-120"><span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**EAP\_E\_EAPHOST\_METHOD\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-121">0x80420011</span><span class="sxs-lookup"><span data-stu-id="95172-121">0x80420011</span></span>
</dt> <dt>



<span data-ttu-id="95172-122">未安裝要求的 EAP 方法。</span><span class="sxs-lookup"><span data-stu-id="95172-122">The requested EAP method is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP \_ E \_ EAPHOST \_ THIRDPARTY \_ 方法 \_ 主機 \_ 重設**</span><span class="sxs-lookup"><span data-stu-id="95172-123"><span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**EAP\_E\_EAPHOST\_THIRDPARTY\_METHOD\_HOST\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-124">0x80420012</span><span class="sxs-lookup"><span data-stu-id="95172-124">0x80420012</span></span>
</dt> <dt>



<span data-ttu-id="95172-125">協力廠商方法的主機沒有回應，且已自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="95172-125">The host of the third party method is not responding and was restarted automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**\_無法存取 EAP E \_ EAPHOST \_ EAPQEC \_**</span><span class="sxs-lookup"><span data-stu-id="95172-126"><span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP\_E\_EAPHOST\_EAPQEC\_INACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-127">0x80420013</span><span class="sxs-lookup"><span data-stu-id="95172-127">0x80420013</span></span>
</dt> <dt>



<span data-ttu-id="95172-128">EAPHost 無法與 EAP [隔離強制用戶端](/windows/desktop/NAP/nap-client-architecture) 通訊 (QEC) 在 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) 上 (NAP) 啟用的用戶端。</span><span class="sxs-lookup"><span data-stu-id="95172-128">EAPHost not able to communicate with EAP [quarantine enforcement client](/windows/desktop/NAP/nap-client-architecture) (QEC) on a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) enabled client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP \_ E \_ EAPHOST 身分 \_ 識別 \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="95172-129"><span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**EAP\_E\_EAPHOST\_IDENTITY\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-130">0x80420014</span><span class="sxs-lookup"><span data-stu-id="95172-130">0x80420014</span></span>
</dt> <dt>



<span data-ttu-id="95172-131">如果驗證器在送出對等身分識別之後驗證失敗，EAPHost 就會傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-131">EAPHost returns this error if the authenticator fails the authentication after the peer identity was submitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP \_ E \_ 驗證 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="95172-132"><span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**EAP\_E\_AUTHENTICATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-133">0x80420015</span><span class="sxs-lookup"><span data-stu-id="95172-133">0x80420015</span></span> 
</dt> <dt>



<span data-ttu-id="95172-134">EAPHost 會在驗證失敗時傳回這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-134">EAPHost returns this error on authentication failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP \_ I \_ EAPHOST \_ EAP \_ 協商 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="95172-135"><span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**EAP\_I\_EAPHOST\_EAP\_NEGOTIATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-136">0x40420016</span><span class="sxs-lookup"><span data-stu-id="95172-136">0x40420016</span></span>
</dt> <dt>



<span data-ttu-id="95172-137">當用戶端和伺服器未設定相容的 EAP 類型時，EAPHost 會記錄此資訊事件。</span><span class="sxs-lookup"><span data-stu-id="95172-137">EAPHost logs this information event when the client and server aren't configured with compatible EAP types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP \_ E \_ EAPHOST \_ 方法 \_ 不正確封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="95172-138"><span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-139">0x80420017</span><span class="sxs-lookup"><span data-stu-id="95172-139">0x80420017</span></span>
</dt> <dt>



<span data-ttu-id="95172-140">EAP 方法收到無法處理的 EAP 封包。</span><span class="sxs-lookup"><span data-stu-id="95172-140">An EAP method received an EAP packet that cannot be processed.</span></span> <span data-ttu-id="95172-141">**Eap \_ E \_ EAPHOST \_ 方法 \_ \_** 的另一個名稱不正確封包是 **eap \_ 方法 \_ 無效 \_** 的封包。</span><span class="sxs-lookup"><span data-stu-id="95172-141">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP \_ E \_ EAPHOST \_ 遠端 \_ 不正確封 \_ 包**</span><span class="sxs-lookup"><span data-stu-id="95172-142"><span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-143">0x80420018</span><span class="sxs-lookup"><span data-stu-id="95172-143">0x80420018</span></span>
</dt> <dt>



<span data-ttu-id="95172-144">EAPHost 收到無法處理的封包。</span><span class="sxs-lookup"><span data-stu-id="95172-144">EAPHost received a packet that cannot be processed.</span></span> <span data-ttu-id="95172-145">**Eap \_ E \_ EAPHOST \_ 遠端 \_ 無效封 \_ 包** 的另一個名稱是 **eap \_ 無效 \_** 的封包。</span><span class="sxs-lookup"><span data-stu-id="95172-145">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP \_ E \_ EAPHOST \_ XML \_ 格式不正確**</span><span class="sxs-lookup"><span data-stu-id="95172-146"><span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**EAP\_E\_EAPHOST\_XML\_MALFORMED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-147">0x80420019</span><span class="sxs-lookup"><span data-stu-id="95172-147">0x80420019</span></span>
</dt> <dt>



<span data-ttu-id="95172-148">EAPHost 設定架構驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="95172-148">The EAPHost configuration schema validation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP \_ E \_ 方法設定不 \_ \_ \_ \_ 支援 \_ SSO**</span><span class="sxs-lookup"><span data-stu-id="95172-149"><span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**EAP\_E\_METHOD\_CONFIG\_DOES\_NOT\_SUPPORT\_SSO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-150">0x8042001A</span><span class="sxs-lookup"><span data-stu-id="95172-150">0x8042001A</span></span>
</dt> <dt>



<span data-ttu-id="95172-151">Windows 7 或更新版本： EAP 方法不支援針對提供的設定 (SSO) 的單一登入。</span><span class="sxs-lookup"><span data-stu-id="95172-151">Windows 7 or later: The EAP method does not support single sign on (SSO) for the provided configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_ \_ 不支援 EAP E EAPHOST \_ 方法 \_ 操作 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95172-152"><span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**EAP\_E\_EAPHOST\_METHOD\_OPERATION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-153">0x80420020</span><span class="sxs-lookup"><span data-stu-id="95172-153">0x80420020</span></span>
</dt> <dt>



<span data-ttu-id="95172-154">當設定的 EAP 方法不支援要求的作業時，EAPHost 會傳回此錯誤 (程序呼叫) 。</span><span class="sxs-lookup"><span data-stu-id="95172-154">EAPHost returns this error when a configured EAP method does not support a requested operation (procedure call).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ 電子 \_ 使用者 \_ 第一**</span><span class="sxs-lookup"><span data-stu-id="95172-155"><span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP\_E\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-156">0x80420100L</span><span class="sxs-lookup"><span data-stu-id="95172-156">0x80420100L</span></span>
</dt> <dt>



<span data-ttu-id="95172-157">定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 第一次** 與 **eap \_ e \_ 使用者 \_** 之間，會發生任何使用者相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-157">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ 使用者 \_ 上次**</span><span class="sxs-lookup"><span data-stu-id="95172-158"><span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP\_E\_USER\_LAST**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-159">0x804201FFL</span><span class="sxs-lookup"><span data-stu-id="95172-159">0x804201FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-160">定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 第一次** 與 **eap \_ e \_ 使用者 \_** 之間，會發生任何使用者相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-160">Defines the boundary of error reports; any user related error will occur between **EAP\_E\_USER\_FIRST** and **EAP\_E\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ 使用者 \_ 優先**</span><span class="sxs-lookup"><span data-stu-id="95172-161"><span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP\_I\_USER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-162">0x40420100L</span><span class="sxs-lookup"><span data-stu-id="95172-162">0x40420100L</span></span>
</dt> <dt>



<span data-ttu-id="95172-163">定義資訊報告的界限;任何 EAP 相關的資訊事件記錄都會出現在 **eap \_ i \_ 使用者 \_ 第一次** 與 **eap \_ i \_ 使用者 \_** 之間。</span><span class="sxs-lookup"><span data-stu-id="95172-163">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**最近的 EAP \_ \_ 使用者 \_**</span><span class="sxs-lookup"><span data-stu-id="95172-164"><span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP\_I\_USER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-165">0x404201FFL</span><span class="sxs-lookup"><span data-stu-id="95172-165">0x404201FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-166">定義資訊報告的界限;任何 EAP 相關的資訊事件記錄都會出現在 **eap \_ i \_ 使用者 \_ 第一次** 與 **eap \_ i \_ 使用者 \_** 之間。</span><span class="sxs-lookup"><span data-stu-id="95172-166">Defines the boundary of information reports; any EAP related informational event logging will occur between **EAP\_I\_USER\_FIRST** and **EAP\_I\_USER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ \_ \_ \_ 找不到 EAP 電子使用者憑證**</span><span class="sxs-lookup"><span data-stu-id="95172-167"><span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**EAP\_E\_USER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-168">0x80420100</span><span class="sxs-lookup"><span data-stu-id="95172-168">0x80420100</span></span>
</dt> <dt>



<span data-ttu-id="95172-169">EAPHost 找不到使用者憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="95172-169">EAPHost could not find a user certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP \_ E \_ 使用者 \_ 憑證 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="95172-170"><span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**EAP\_E\_USER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-171">0x80420101</span><span class="sxs-lookup"><span data-stu-id="95172-171">0x80420101</span></span>
</dt> <dt>



<span data-ttu-id="95172-172">要驗證使用者的使用者憑證沒有適當的擴充金鑰使用方法 (EKU) 集。</span><span class="sxs-lookup"><span data-stu-id="95172-172">The user certificate being user for authentication does not have proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP \_ E \_ 使用者憑證已 \_ \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="95172-173"><span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**EAP\_E\_USER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-174">0x80420102</span><span class="sxs-lookup"><span data-stu-id="95172-174">0x80420102</span></span>
</dt> <dt>



<span data-ttu-id="95172-175">EAPhost 找到過期的使用者憑證。</span><span class="sxs-lookup"><span data-stu-id="95172-175">EAPhost found an expired user certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP \_ E \_ 使用者憑證已 \_ \_ 撤銷**</span><span class="sxs-lookup"><span data-stu-id="95172-176"><span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**EAP\_E\_USER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-177">0x80420103</span><span class="sxs-lookup"><span data-stu-id="95172-177">0x80420103</span></span>
</dt> <dt>



<span data-ttu-id="95172-178">用於驗證的使用者憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="95172-178">The user certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP \_ E \_ 使用者 \_ 憑證 \_ 其他 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="95172-179"><span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP\_E\_USER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-180">0x80420104</span><span class="sxs-lookup"><span data-stu-id="95172-180">0x80420104</span></span>
</dt> <dt>



<span data-ttu-id="95172-181">使用使用者認證進行驗證時發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-181">An unknown error occurred with the user certification being used for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_拒絕 EAP 電子 \_ 使用者憑證 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="95172-182"><span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**EAP\_E\_USER\_CERT\_REJECTED**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-183">0x80420105</span><span class="sxs-lookup"><span data-stu-id="95172-183">0x80420105</span></span>
</dt> <dt>



<span data-ttu-id="95172-184">驗證者拒絕了使用者認證。</span><span class="sxs-lookup"><span data-stu-id="95172-184">The authenticator rejected the user certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP \_ 我的 \_ 使用者 \_ 帳戶 \_ 其他 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="95172-185"><span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP\_I\_USER\_ACCOUNT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-186">0x40420110</span><span class="sxs-lookup"><span data-stu-id="95172-186">0x40420110</span></span>
</dt> <dt>



<span data-ttu-id="95172-187">識別交換之後收到 EAP 失敗，指出驗證使用者帳戶發生問題的可能性。</span><span class="sxs-lookup"><span data-stu-id="95172-187">An EAP failure was received after an identity exchange, indicating the likelihood of a problem with the authenticating user's account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_拒絕 EAP 電子 \_ 使用者 \_ 認證 \_**</span><span class="sxs-lookup"><span data-stu-id="95172-188"><span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**EAP\_E\_USER\_CREDENTIALS\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-189">0x80420111</span><span class="sxs-lookup"><span data-stu-id="95172-189">0x80420111</span></span>
</dt> <dt>



<span data-ttu-id="95172-190">驗證器已拒絕驗證的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="95172-190">The authenticator rejected user credentials for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**拒絕的 EAP \_ 電子 \_ 使用者 \_ 名稱 \_ 密碼 \_**</span><span class="sxs-lookup"><span data-stu-id="95172-191"><span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**EAP\_E\_USER\_NAME\_PASSWORD\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-192">0x80420112</span><span class="sxs-lookup"><span data-stu-id="95172-192">0x80420112</span></span>
</dt> <dt>



<span data-ttu-id="95172-193">Windows 7 或更新版本：驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="95172-193">Windows 7 or later: Authentication failed.</span></span> <span data-ttu-id="95172-194">驗證者拒絕了使用者認證。</span><span class="sxs-lookup"><span data-stu-id="95172-194">The authenticator rejected the user credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ 電子 \_ 沒有 \_ 智慧 \_ 卡 \_ 讀卡機**</span><span class="sxs-lookup"><span data-stu-id="95172-195"><span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP\_E\_NO\_SMART\_CARD\_READER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-196">0x80420113</span><span class="sxs-lookup"><span data-stu-id="95172-196">0x80420113</span></span>
</dt> <dt>



<span data-ttu-id="95172-197">Windows 7 或更新版本：找不到智慧卡讀卡機。</span><span class="sxs-lookup"><span data-stu-id="95172-197">Windows 7 or later: No smart card reader found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ SERVER \_ FIRST**</span><span class="sxs-lookup"><span data-stu-id="95172-198"><span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP\_E\_SERVER\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-199">0x80420200L</span><span class="sxs-lookup"><span data-stu-id="95172-199">0x80420200L</span></span>
</dt> <dt>



<span data-ttu-id="95172-200">定義錯誤報表的界限;在 **eap \_ e \_ Server \_ FIRST** 與 **eap \_ e \_ server \_** 之間，會發生任何伺服器相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-200">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**</span><span class="sxs-lookup"><span data-stu-id="95172-201"><span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP\_E\_SERVER\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-202">0x804202FFL</span><span class="sxs-lookup"><span data-stu-id="95172-202">0x804202FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-203">定義錯誤報表的界限;在 **eap \_ e \_ Server \_ FIRST** 與 **eap \_ e \_ server \_** 之間，會發生任何伺服器相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-203">Defines the boundary of error reports; any server related error will occur between **EAP\_E\_SERVER\_FIRST** and **EAP\_E\_SERVER\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ \_ \_ \_ 找不到 EAP 電子伺服器憑證**</span><span class="sxs-lookup"><span data-stu-id="95172-204"><span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**EAP\_E\_SERVER\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-205">0x80420200</span><span class="sxs-lookup"><span data-stu-id="95172-205">0x80420200</span></span>
</dt> <dt>



<span data-ttu-id="95172-206">EAPHost 找不到伺服器憑證以進行驗證。</span><span class="sxs-lookup"><span data-stu-id="95172-206">EAPHost could not find the server certificate for authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP \_ E \_ 伺服器 \_ 證書 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="95172-207"><span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**EAP\_E\_SERVER\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-208">0x80420201</span><span class="sxs-lookup"><span data-stu-id="95172-208">0x80420201</span></span>
</dt> <dt>



<span data-ttu-id="95172-209">用來驗證使用者的伺服器憑證沒有適當的擴充金鑰使用方式 (EKU) 集。</span><span class="sxs-lookup"><span data-stu-id="95172-209">The server certificate being user for authentication does not have a proper extended key usage (EKU) set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP \_ E \_ 伺服器 \_ 證書已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="95172-210"><span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**EAP\_E\_SERVER\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-211">0x80420202</span><span class="sxs-lookup"><span data-stu-id="95172-211">0x80420202</span></span>
</dt> <dt>



<span data-ttu-id="95172-212">EAPhost 找到過期的伺服器憑證。</span><span class="sxs-lookup"><span data-stu-id="95172-212">EAPhost found an expired server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP \_ E \_ 伺服器 \_ 證書已 \_ 撤銷**</span><span class="sxs-lookup"><span data-stu-id="95172-213"><span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**EAP\_E\_SERVER\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-214">0x80420203</span><span class="sxs-lookup"><span data-stu-id="95172-214">0x80420203</span></span>
</dt> <dt>



<span data-ttu-id="95172-215">用於驗證的伺服器憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="95172-215">The server certificate being used for authentication has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP \_ E \_ SERVER \_ CERT \_ 其他 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="95172-216"><span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**EAP\_E\_SERVER\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-217">0x80420204</span><span class="sxs-lookup"><span data-stu-id="95172-217">0x80420204</span></span>
</dt> <dt>



<span data-ttu-id="95172-218">伺服器憑證發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-218">An unknown error occurred with the server certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ FIRST**</span><span class="sxs-lookup"><span data-stu-id="95172-219"><span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP\_E\_USER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-220">0x80420300L</span><span class="sxs-lookup"><span data-stu-id="95172-220">0x80420300L</span></span>
</dt> <dt>



<span data-ttu-id="95172-221">定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 根憑證 \_ \_ 第一** 次與 **eap \_ e \_ 使用者 \_ 跟 \_ 證書 \_** 之間，會發生任何使用者根憑證相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-221">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ LAST**</span><span class="sxs-lookup"><span data-stu-id="95172-222"><span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP\_E\_USER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-223">0x804203FFL</span><span class="sxs-lookup"><span data-stu-id="95172-223">0x804203FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-224">定義錯誤報表的界限;在 **eap \_ e \_ 使用者 \_ 根憑證 \_ \_ 第一** 次與 **eap \_ e \_ 使用者 \_ 跟 \_ 證書 \_** 之間，會發生任何使用者根憑證相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-224">Defines the boundary of error reports; any user root certificate related error will occur between **EAP\_E\_USER\_ROOT\_CERT\_FIRST** and **EAP\_E\_USER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 EAP E 使用者根憑證**</span><span class="sxs-lookup"><span data-stu-id="95172-225"><span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**EAP\_E\_USER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-226">0x80420300</span><span class="sxs-lookup"><span data-stu-id="95172-226">0x80420300</span></span>
</dt> <dt>



<span data-ttu-id="95172-227">EAPHost 在受信任的根憑證存放區中找不到用於使用者認證驗證的憑證。</span><span class="sxs-lookup"><span data-stu-id="95172-227">EAPHost could not find a certificate in a trusted root certificate store for user certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="95172-228"><span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**EAP\_E\_USER\_ROOT\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-229">0x80420301</span><span class="sxs-lookup"><span data-stu-id="95172-229">0x80420301</span></span>
</dt> <dt>



<span data-ttu-id="95172-230">驗證失敗，因為用於此網路的根憑證無效。</span><span class="sxs-lookup"><span data-stu-id="95172-230">The authentication failed because the root certificate used for this network is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP \_ E \_ 使用者 \_ 跟 \_ 證書已 \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="95172-231"><span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**EAP\_E\_USER\_ROOT\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-232">0x80420302</span><span class="sxs-lookup"><span data-stu-id="95172-232">0x80420302</span></span>
</dt> <dt>



<span data-ttu-id="95172-233">使用者憑證驗證所需的受信任根憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="95172-233">The trusted root certificate needed for user certificate validation has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 第一個**</span><span class="sxs-lookup"><span data-stu-id="95172-234"><span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-235">0x80420400L</span><span class="sxs-lookup"><span data-stu-id="95172-235">0x80420400L</span></span>
</dt> <dt>



<span data-ttu-id="95172-236">定義錯誤報表的界限;系統會先將 **eap \_ e \_ server \_ 根憑證 \_ \_ 第一個** 與 **eap \_ e \_ server \_ 跟 \_ \_** 證書之間發生任何伺服器根憑證相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-236">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 最後**</span><span class="sxs-lookup"><span data-stu-id="95172-237"><span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-238">0x804204FFL</span><span class="sxs-lookup"><span data-stu-id="95172-238">0x804204FFL</span></span>
</dt> <dt>



<span data-ttu-id="95172-239">定義錯誤報表的界限;系統會先將 **eap \_ e \_ server \_ 根憑證 \_ \_ 第一個** 與 **eap \_ e \_ server \_ 跟 \_ \_** 證書之間發生任何伺服器根憑證相關的錯誤。</span><span class="sxs-lookup"><span data-stu-id="95172-239">Defines the boundary of error reports; any server root certificate related error will occur between **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST** and **EAP\_E\_SERVER\_ROOT\_CERT\_FIRST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ \_ \_ \_ \_ 找不到 EAP E 伺服器根憑證**</span><span class="sxs-lookup"><span data-stu-id="95172-240"><span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-241">0x80420400</span><span class="sxs-lookup"><span data-stu-id="95172-241">0x80420400</span></span>
</dt> <dt>



<span data-ttu-id="95172-242">EAPHost 在伺服器憑證驗證的受信任根憑證存放區中找不到根憑證。</span><span class="sxs-lookup"><span data-stu-id="95172-242">EAPHost could not find a root certificate in a trusted root certificate store for the server certification validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP \_ E \_ 伺服器 \_ 跟 \_ 證書 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="95172-243"><span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_INVALID**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-244">0x80420401</span><span class="sxs-lookup"><span data-stu-id="95172-244">0x80420401</span></span>
</dt> <dt>



<span data-ttu-id="95172-245">驗證失敗，因為伺服器電腦上此網路所需的伺服器憑證無效。</span><span class="sxs-lookup"><span data-stu-id="95172-245">The authentication failed because the server certificate required for this network on the server computer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="95172-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_需要 EAP E \_ 伺服器 \_ 跟 \_ 證書 \_ 名稱 \_**</span><span class="sxs-lookup"><span data-stu-id="95172-246"><span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**EAP\_E\_SERVER\_ROOT\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95172-247">0x80420406</span><span class="sxs-lookup"><span data-stu-id="95172-247">0x80420406</span></span>
</dt> <dt>



<span data-ttu-id="95172-248">驗證失敗，因為伺服器電腦上的憑證未指定伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="95172-248">The authentication failed because the certificate on the server computer does not have a server name specified.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95172-249">備註</span><span class="sxs-lookup"><span data-stu-id="95172-249">Remarks</span></span>

<span data-ttu-id="95172-250">某些錯誤有替代名稱：</span><span class="sxs-lookup"><span data-stu-id="95172-250">There are alternate names for certain errors:</span></span>

-   <span data-ttu-id="95172-251">**Eap \_ E \_ EAPHOST \_ 方法 \_ \_** 的另一個名稱不正確封包是 **eap \_ 方法 \_ 無效 \_** 的封包。</span><span class="sxs-lookup"><span data-stu-id="95172-251">Another name for **EAP\_E\_EAPHOST\_METHOD\_INVALID\_PACKET** is **EAP\_METHOD\_INVALID\_PACKET**.</span></span>
-   <span data-ttu-id="95172-252">**Eap \_ E \_ EAPHOST \_ 遠端 \_ 無效封 \_ 包** 的另一個名稱是 **eap \_ 無效 \_** 的封包。</span><span class="sxs-lookup"><span data-stu-id="95172-252">Another name for **EAP\_E\_EAPHOST\_REMOTE\_INVALID\_PACKET** is **EAP\_INVALID\_PACKET**.</span></span>

## <a name="requirements"></a><span data-ttu-id="95172-253">規格需求</span><span class="sxs-lookup"><span data-stu-id="95172-253">Requirements</span></span>



| <span data-ttu-id="95172-254">需求</span><span class="sxs-lookup"><span data-stu-id="95172-254">Requirement</span></span> | <span data-ttu-id="95172-255">值</span><span class="sxs-lookup"><span data-stu-id="95172-255">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="95172-256">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95172-256">Minimum supported client</span></span><br/> | <span data-ttu-id="95172-257">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95172-257">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="95172-258">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95172-258">Minimum supported server</span></span><br/> | <span data-ttu-id="95172-259">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95172-259">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="95172-260">標頭</span><span class="sxs-lookup"><span data-stu-id="95172-260">Header</span></span><br/>                   | <dl> <span data-ttu-id="95172-261"><dt>Eaphosterror。h</dt></span><span class="sxs-lookup"><span data-stu-id="95172-261"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95172-262">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95172-262">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95172-263">常見的 EAPHost 常數</span><span class="sxs-lookup"><span data-stu-id="95172-263">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

