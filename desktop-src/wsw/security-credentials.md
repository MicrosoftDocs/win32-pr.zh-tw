---
title: 安全性認證
description: 安全性認證是通訊物件所擁有的一項辨識項，可用來建立或取得安全性權杖。
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- 適用于 Windows 的安全性認證 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106969125"
---
# <a name="security-credentials"></a><span data-ttu-id="3b670-106">安全性認證</span><span class="sxs-lookup"><span data-stu-id="3b670-106">Security Credentials</span></span>

<span data-ttu-id="3b670-107">安全性認證是通訊物件所擁有的一項辨識項，可用來建立或取得安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="3b670-107">Security credentials are a piece of evidence that a communicating party possesses that can be used to create or obtain a security token.</span></span> <span data-ttu-id="3b670-108">因此，認證通常比安全性權杖長，且安全性權杖可視為安全性認證的運行時程表現。</span><span class="sxs-lookup"><span data-stu-id="3b670-108">Thus, credentials are typically longer-lived than security tokens, and a security token can be viewed as the runtime manifestation of the security credentials.</span></span> <span data-ttu-id="3b670-109">認證的範例包括電腦憑證 (可在執行時間將其轉換成 x.509 安全性權杖) 或在網域的使用者名稱/密碼組 (，可用來取得) 的 Kerberos 安全性權杖。</span><span class="sxs-lookup"><span data-stu-id="3b670-109">Example of credentials include a machine certificate (which can be converted into an X.509 security token at runtime) or a username/password pair for a domain (which can be used to obtain a Kerberos security token).</span></span>


<span data-ttu-id="3b670-110">認證會指定為 [安全性](security-bindings.md)系結的一部分。</span><span class="sxs-lookup"><span data-stu-id="3b670-110">Credentials are specified as part of the [security bindings](security-bindings.md).</span></span>

<span data-ttu-id="3b670-111">下列 API 元素會搭配安全性認證使用。</span><span class="sxs-lookup"><span data-stu-id="3b670-111">The following API elements are used with security credentials.</span></span>

| <span data-ttu-id="3b670-112">回呼</span><span class="sxs-lookup"><span data-stu-id="3b670-112">Callback</span></span>                                                                  | <span data-ttu-id="3b670-113">Description</span><span class="sxs-lookup"><span data-stu-id="3b670-113">Description</span></span>                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="3b670-114">**WS \_ GET \_ CERT \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="3b670-114">**WS\_GET\_CERT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | <span data-ttu-id="3b670-115">提供憑證給安全性執行時間。</span><span class="sxs-lookup"><span data-stu-id="3b670-115">Provides a certificate to the security runtime.</span></span>          |
| [<span data-ttu-id="3b670-116">**WS \_ 驗證 \_ 密碼 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="3b670-116">**WS\_VALIDATE\_PASSWORD\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | <span data-ttu-id="3b670-117">驗證接收者端的使用者名稱/密碼組。</span><span class="sxs-lookup"><span data-stu-id="3b670-117">Validates a username/password pair on the receiver side.</span></span> |



 



| <span data-ttu-id="3b670-118">列舉型別</span><span class="sxs-lookup"><span data-stu-id="3b670-118">Enumeration</span></span>                                                                                           | <span data-ttu-id="3b670-119">描述</span><span class="sxs-lookup"><span data-stu-id="3b670-119">Description</span></span>                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="3b670-120">**WS \_ CERT \_ 認證 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3b670-120">**WS\_CERT\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | <span data-ttu-id="3b670-121">憑證認證的類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-121">The type of the certificate credential.</span></span>                       |
| [<span data-ttu-id="3b670-122">**WS 使用者 \_ 名稱 \_ 認證 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3b670-122">**WS\_USERNAME\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | <span data-ttu-id="3b670-123">使用者名稱/密碼認證的類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-123">The type of the username/password credential.</span></span>                 |
| [<span data-ttu-id="3b670-124">**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="3b670-124">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | <span data-ttu-id="3b670-125">「Windows 整合式驗證」認證的類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-125">The type of the Windows Integrated Authentication credential.</span></span> |



 



| <span data-ttu-id="3b670-126">結構</span><span class="sxs-lookup"><span data-stu-id="3b670-126">Structure</span></span>                                                                                                   | <span data-ttu-id="3b670-127">Description</span><span class="sxs-lookup"><span data-stu-id="3b670-127">Description</span></span>                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b670-128">**WS \_ CERT \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-128">**WS\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | <span data-ttu-id="3b670-129">所有憑證認證類型的抽象基底類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-129">The abstract base type for all certificate credential types.</span></span>                                                          |
| [<span data-ttu-id="3b670-130">**WS \_ 自 \_ 定義 \_ 憑證認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-130">**WS\_CUSTOM\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | <span data-ttu-id="3b670-131">型別，用來指定要由回呼提供給應用程式的憑證認證。</span><span class="sxs-lookup"><span data-stu-id="3b670-131">The type for specifying a certificate credential that is to be supplied by a callback to the application.</span></span>             |
| [<span data-ttu-id="3b670-132">**WS \_ 預設 \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-132">**WS\_DEFAULT\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | <span data-ttu-id="3b670-133">輸入，以根據目前的執行緒 token 提供 Windows 整合式驗證認證。</span><span class="sxs-lookup"><span data-stu-id="3b670-133">Type for supplying a Windows Integrated Authentication credential based on the current thread token.</span></span>                  |
| [<span data-ttu-id="3b670-134">**WS 不 \_ 透明的 \_ WINDOWS 整合式 \_ \_ 驗證 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-134">**WS\_OPAQUE\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | <span data-ttu-id="3b670-135">提供 Windows 整合式驗證認證的類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-135">Type for supplying a Windows Integrated Authentication credential.</span></span>                                                    |
| [<span data-ttu-id="3b670-136">**WS \_ 字串使用者 \_ 名稱 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-136">**WS\_STRING\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | <span data-ttu-id="3b670-137">提供以字串形式提供使用者名稱/密碼組的型別。</span><span class="sxs-lookup"><span data-stu-id="3b670-137">The type for supplying a username/password pair as strings.</span></span>                                                           |
| [<span data-ttu-id="3b670-138">**WS \_ 字串 \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-138">**WS\_STRING\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | <span data-ttu-id="3b670-139">以使用者名稱、密碼、網域字串提供 Windows 認證的類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-139">Type for supplying a Windows credential as username, password, domain strings.</span></span>                                        |
| [<span data-ttu-id="3b670-140">**WS \_ 主體 \_ 名稱 \_ \_ 憑證認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-140">**WS\_SUBJECT\_NAME\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | <span data-ttu-id="3b670-141">使用憑證的主體名稱、存放區位置和存放區名稱來指定憑證認證的型別。</span><span class="sxs-lookup"><span data-stu-id="3b670-141">The type for specifying a certificate credential using the certificate's subject name, store location and store name.</span></span> |
| [<span data-ttu-id="3b670-142">**WS \_ 指紋 \_ \_ 憑證認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-142">**WS\_THUMBPRINT\_CERT\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | <span data-ttu-id="3b670-143">類型，用來指定使用憑證指紋的憑證認證、儲存位置和存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="3b670-143">The type for specifying a certificate credential using the certificate's thumbprint, store location and store name.</span></span>   |
| [<span data-ttu-id="3b670-144">**WS 使用者 \_ 名稱 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-144">**WS\_USERNAME\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | <span data-ttu-id="3b670-145">所有使用者名稱/密碼認證的抽象基底類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-145">The abstract base type for all username/password credentials.</span></span>                                                         |
| [<span data-ttu-id="3b670-146">**WS \_ WINDOWS \_ 整合式 \_ 驗證 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="3b670-146">**WS\_WINDOWS\_INTEGRATED\_AUTH\_CREDENTIAL**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | <span data-ttu-id="3b670-147">所有與 Windows 整合式驗證搭配使用之認證類型的抽象基底類型。</span><span class="sxs-lookup"><span data-stu-id="3b670-147">The abstract base type for all credential types used with Windows Integrated Authentication.</span></span>                          |



 

 

 




