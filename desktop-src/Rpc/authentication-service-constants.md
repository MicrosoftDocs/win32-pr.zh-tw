---
title: 'Authentication-Service 常數 (Rpcdce) '
description: 驗證服務常數代表傳遞給各種執行時間函數的驗證服務。
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
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
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509207"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="8d85a-103">Authentication-Service 常數</span><span class="sxs-lookup"><span data-stu-id="8d85a-103">Authentication-Service Constants</span></span>

<span data-ttu-id="8d85a-104">驗證服務常數代表傳遞給各種執行時間函數的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="8d85a-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="8d85a-105">下列常數是 *AuthnSvc* 參數的有效值。</span><span class="sxs-lookup"><span data-stu-id="8d85a-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="8d85a-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="8d85a-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="8d85a-107">Description</span><span class="sxs-lookup"><span data-stu-id="8d85a-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="8d85a-108"><dt>**RPC \_C \_ 驗證 \_ 無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="8d85a-109">不需要驗證。</span><span class="sxs-lookup"><span data-stu-id="8d85a-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="8d85a-110"><dt>**RPC \_C \_ 驗證 \_ DCE \_ 私**</dt>用 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="8d85a-111">使用分散式運算環境 (DCE) 私密金鑰驗證。</span><span class="sxs-lookup"><span data-stu-id="8d85a-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="8d85a-112"><dt>**RPC \_C \_ 驗證 \_ DCE \_ PUBLIC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="8d85a-113">「DCE 公開金鑰驗證」 (保留供日後使用) 。</span><span class="sxs-lookup"><span data-stu-id="8d85a-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="8d85a-114"><dt>**RPC \_C \_ 驗證 \_ DEC \_ 公用**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="8d85a-115">DEC 公開金鑰驗證 (保留供日後使用) 。</span><span class="sxs-lookup"><span data-stu-id="8d85a-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="8d85a-116"><dt>**RPC \_C \_ 驗證 \_ GSS \_ 協商**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="8d85a-117">使用 [Microsoft NEGOTIATE SSP](/windows/desktop/SecAuthN/microsoft-negotiate)。</span><span class="sxs-lookup"><span data-stu-id="8d85a-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="8d85a-118">此 SSP 會在使用 NTLM 和 Kerberos 通訊協定安全性支援提供者 (SSP) 之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="8d85a-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="8d85a-119"><dt>**RPC \_C \_ 驗證 \_ WINNT**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="8d85a-120">使用 [MICROSOFT NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm)。</span><span class="sxs-lookup"><span data-stu-id="8d85a-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="8d85a-121"><dt>**RPC \_C \_ 驗證 \_ GSS \_ SCHANNEL**</dt>安全通道 <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="8d85a-122">使用 [SCHANNEL SSP](/windows/desktop/SecAuthN/secure-channel)。</span><span class="sxs-lookup"><span data-stu-id="8d85a-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="8d85a-123">此 SSP 支援安全通訊端層 (SSL) 、私用通訊技術 (PCT) ，以及傳輸層級安全性 (TLS) 。</span><span class="sxs-lookup"><span data-stu-id="8d85a-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="8d85a-124"><dt>**RPC \_C \_ 驗證 \_ GSS \_ KERBEROS**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="8d85a-125">使用 [Microsoft KERBEROS SSP](/windows/desktop/SecAuthN/microsoft-kerberos)。</span><span class="sxs-lookup"><span data-stu-id="8d85a-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="8d85a-126"><dt>**RPC \_C \_ 驗證 \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="8d85a-127">使用 (DPA) 的分散式密碼驗證。</span><span class="sxs-lookup"><span data-stu-id="8d85a-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="8d85a-128"><dt>**RPC \_C \_ 驗證 \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="8d85a-129">用於 Microsoft Network (MSN) 的驗證通訊協定 SSP。</span><span class="sxs-lookup"><span data-stu-id="8d85a-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="8d85a-130"><dt>**RPC \_C \_ 驗證 \_ 摘要**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="8d85a-131">Windows XP 或更新版本：使用 [MICROSOFT DIGEST SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="8d85a-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="8d85a-132"><dt>**RPC \_C \_ 驗證 \_ NEGO \_**</dt>擴充項 <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="8d85a-133">Windows 7 或更新版本：已保留。</span><span class="sxs-lookup"><span data-stu-id="8d85a-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="8d85a-134">請勿使用</span><span class="sxs-lookup"><span data-stu-id="8d85a-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="8d85a-135"><dt>**RPC \_C \_ 驗證 \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="8d85a-136">這個 SSP 會為 Microsoft 訊息佇列提供 SSPI 相容的包裝函式， (MSMQ) 傳輸層級的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8d85a-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="8d85a-137"><dt>**RPC \_C \_ 驗證 \_ 預設**</dt>為 <dt>0xffffffff</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="8d85a-138">使用預設驗證服務。</span><span class="sxs-lookup"><span data-stu-id="8d85a-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="8d85a-139">備註</span><span class="sxs-lookup"><span data-stu-id="8d85a-139">Remarks</span></span>

<span data-ttu-id="8d85a-140">針對透過系結 \_ \_ \_ 控制碼發出的遠端程序呼叫，指定 RPC C 驗證 NONE 來關閉驗證。</span><span class="sxs-lookup"><span data-stu-id="8d85a-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="8d85a-141">當您指定 RPC \_ c \_ 驗證 \_ 預設值時，rpc 執行時間程式庫會使用 rpc \_ c \_ 驗證 \_ WINNT 驗證服務來進行使用系結控制碼進行的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="8d85a-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d85a-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d85a-142">Requirements</span></span>



| <span data-ttu-id="8d85a-143">需求</span><span class="sxs-lookup"><span data-stu-id="8d85a-143">Requirement</span></span> | <span data-ttu-id="8d85a-144">值</span><span class="sxs-lookup"><span data-stu-id="8d85a-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8d85a-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d85a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8d85a-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d85a-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8d85a-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d85a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8d85a-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d85a-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8d85a-149">標頭</span><span class="sxs-lookup"><span data-stu-id="8d85a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d85a-150"><dt>Rpcdce。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d85a-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d85a-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d85a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d85a-152">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="8d85a-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="8d85a-153">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="8d85a-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="8d85a-154">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="8d85a-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="8d85a-155">**RpcBindingInqAuthClientEx**</span><span class="sxs-lookup"><span data-stu-id="8d85a-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="8d85a-156">**RpcBindingSetAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="8d85a-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="8d85a-157">**RpcBindingInqAuthInfoEx**</span><span class="sxs-lookup"><span data-stu-id="8d85a-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

