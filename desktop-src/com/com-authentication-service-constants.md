---
title: '驗證服務常數 (RpcDce .h) '
description: 藉由識別提供服務的安全性封裝（例如 NTLMSSP、Kerberos 或 Schannel）來定義驗證服務。
ms.assetid: c16a8e52-a7f9-40d9-99ef-10b382b5cb3c
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_KERNEL
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_PKU2U
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227d2accdf871c2e57a25661837d10089c983ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106319"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="ffe4c-103">驗證服務常數</span><span class="sxs-lookup"><span data-stu-id="ffe4c-103">Authentication Service Constants</span></span>

<span data-ttu-id="ffe4c-104">藉由識別提供服務的安全性封裝（例如 NTLMSSP、Kerberos 或 Schannel）來定義驗證服務。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-104">Defines authentication services by identifying the security package that provides the service, such as NTLMSSP, Kerberos, or Schannel.</span></span>



| <span data-ttu-id="ffe4c-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="ffe4c-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="ffe4c-106">Description</span><span class="sxs-lookup"><span data-stu-id="ffe4c-106">Description</span></span>                                                                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="ffe4c-107"><dt>**RPC \_C \_ 驗證 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-107"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="ffe4c-108">不需要驗證。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-108">No authentication.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="ffe4c-109"><dt>**RPC \_C \_ 驗證 \_ DCE \_ 私**</dt>用 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-109"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="ffe4c-110">DCE 私密金鑰驗證。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-110">DCE private key authentication.</span></span><br/>                                                                                                                                                                                                                                     |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="ffe4c-111"><dt>**RPC \_C \_ 驗證 \_ DCE \_ PUBLIC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-111"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="ffe4c-112">DCE 公開金鑰驗證。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-112">DCE public key authentication.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="ffe4c-113"><dt>**RPC \_C \_ 驗證 \_ DEC \_ 公用**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-113"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="ffe4c-114">DEC 公開金鑰驗證。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-114">DEC public key authentication.</span></span> <span data-ttu-id="ffe4c-115">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-115">Reserved for future use.</span></span><br/>                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="ffe4c-116"><dt>**RPC \_C \_ 驗證 \_ GSS \_ 協商**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="ffe4c-117">Snego 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-117">Snego security support provider.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="ffe4c-118"><dt>**RPC \_C \_ 驗證 \_ WINNT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-118"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="ffe4c-119">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="ffe4c-119">NTLMSSP</span></span><br/>                                                                                                                                                                                                                                                             |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="ffe4c-120"><dt>**RPC \_C \_ 驗證 \_ GSS \_ SCHANNEL**</dt>安全通道 <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-120"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="ffe4c-121">Schannel 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-121">Schannel security support provider.</span></span> <span data-ttu-id="ffe4c-122">此驗證服務支援 SSL 2.0、SSL 3.0、TLS 和 PCT。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-122">This authentication service supports SSL 2.0, SSL 3.0, TLS, and PCT.</span></span><br/>                                                                                                                                                            |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="ffe4c-123"><dt>**RPC \_C \_ 驗證 \_ GSS \_ KERBEROS**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-123"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="ffe4c-124">Kerberos 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-124">Kerberos security support provider.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="ffe4c-125"><dt>**RPC \_C \_ 驗證 \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-125"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="ffe4c-126">DPA 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-126">DPA security support provider.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="ffe4c-127"><dt>**RPC \_C \_ 驗證 \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-127"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="ffe4c-128">MSN 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-128">MSN security support provider.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="RPC_C_AUTHN_KERNEL"></span><span id="rpc_c_authn_kernel"></span><dl> <span data-ttu-id="ffe4c-129"><dt>**RPC \_C \_ 驗證 \_ 核心**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-129"><dt>**RPC\_C\_AUTHN\_KERNEL**</dt> <dt>20</dt></span></span> </dl>                       | <span data-ttu-id="ffe4c-130">核心安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-130">Kernel security support provider.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="ffe4c-131"><dt>**RPC \_C \_ 驗證 \_ 摘要**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-131"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="ffe4c-132">摘要式安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-132">Digest security support provider.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="ffe4c-133"><dt>**RPC \_C \_ 驗證 \_ NEGO \_**</dt>擴充項 <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-133"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="ffe4c-134">NEGO 擴充項安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-134">NEGO extender security support provider.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RPC_C_AUTHN_PKU2U"></span><span id="rpc_c_authn_pku2u"></span><dl> <span data-ttu-id="ffe4c-135"><dt>**RPC \_C \_ 驗證 \_ PKU2U**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-135"><dt>**RPC\_C\_AUTHN\_PKU2U**</dt> <dt>31</dt></span></span> </dl>                          | <span data-ttu-id="ffe4c-136">PKU2U 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-136">PKU2U security support provider.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="ffe4c-137"><dt>**RPC \_C \_ 驗證 \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-137"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="ffe4c-138">MQ 安全性支援提供者。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-138">MQ security support provider.</span></span><br/>                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="ffe4c-139"><dt>**RPC \_C \_ 驗證 \_ 預設**</dt> <dt>0xFFFFFFFFL</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-139"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xFFFFFFFFL</dt></span></span> </dl>           | <span data-ttu-id="ffe4c-140">系統預設驗證服務。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-140">The system default authentication service.</span></span> <span data-ttu-id="ffe4c-141">指定此值時，COM 會使用其一般安全性全面協商演算法來挑選驗證服務。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-141">When this value is specified, COM uses its normal security blanket negotiation algorithm to pick an authentication service.</span></span> <span data-ttu-id="ffe4c-142">如需詳細資訊，請參閱 [安全性綜合協商](security-blanket-negotiation.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-142">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="ffe4c-143">備註</span><span class="sxs-lookup"><span data-stu-id="ffe4c-143">Remarks</span></span>

<span data-ttu-id="ffe4c-144">這些常數會用於唯一的 [**\_ 驗證 \_ 服務**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) 和唯一的 [**\_ 驗證 \_ 資訊**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) 結構中。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-144">These constants are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) and the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structures.</span></span> <span data-ttu-id="ffe4c-145">**唯一的 \_ 驗證 \_ 服務** 結構會由伺服器傳遞至 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)函式，而且可以由 [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)函數抓取。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-145">The **SOLE\_AUTHENTICATION\_SERVICE** structure is passed by the server to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and can be retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="ffe4c-146">用戶端會將 **唯一 \_ 驗證 \_ 資訊** 結構的指標傳遞至 **CoInitializeSecurity**。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-146">A pointer to a **SOLE\_AUTHENTICATION\_INFO** structure is passed by the client to **CoInitializeSecurity**.</span></span> <span data-ttu-id="ffe4c-147">如需這些值（例如 NTLMSSP 和 Kerberos）所識別之安全性封裝的詳細資訊，請參閱 [COM 和安全性封裝](com-and-security-packages.md)。</span><span class="sxs-lookup"><span data-stu-id="ffe4c-147">For more information on the security packages identified by these values, such as NTLMSSP and Kerberos, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe4c-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffe4c-148">Requirements</span></span>



| <span data-ttu-id="ffe4c-149">需求</span><span class="sxs-lookup"><span data-stu-id="ffe4c-149">Requirement</span></span> | <span data-ttu-id="ffe4c-150">值</span><span class="sxs-lookup"><span data-stu-id="ffe4c-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe4c-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffe4c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe4c-152">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe4c-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ffe4c-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffe4c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe4c-154">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffe4c-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ffe4c-155">標頭</span><span class="sxs-lookup"><span data-stu-id="ffe4c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffe4c-156"><dt>RpcDce。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4c-156"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe4c-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffe4c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe4c-158">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-158">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="ffe4c-159">**CoQueryAuthenticationServices**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-159">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="ffe4c-160">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-160">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="ffe4c-161">**唯一 \_ 驗證 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-161">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="ffe4c-162">**唯一 \_ 驗證 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-162">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

