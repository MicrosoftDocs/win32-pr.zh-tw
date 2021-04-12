---
title: 'EAP 方法旗標 (Eaptypes .h) '
description: EAP 方法旗標用於要求者、驗證器和對等函式中，以指定 EAP 驗證會話的行為。
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464177"
---
# <a name="eap-method-flags"></a><span data-ttu-id="e9c32-103">EAP 方法旗標</span><span class="sxs-lookup"><span data-stu-id="e9c32-103">EAP Method Flags</span></span>

<span data-ttu-id="e9c32-104">EAP 方法旗標用於要求者、驗證器和對等函式中，以指定 EAP 驗證會話的行為。</span><span class="sxs-lookup"><span data-stu-id="e9c32-104">The EAP method flags are used within the supplicant, authenticator, and peer functions to specify behaviors of an EAP authentication session.</span></span>

<dl> <dt>

<span data-ttu-id="e9c32-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP \_ 旗標 \_ Reserved1**</span><span class="sxs-lookup"><span data-stu-id="e9c32-105"><span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP\_FLAG\_Reserved1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e9c32-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-107">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-107">Do not use.</span></span> <span data-ttu-id="e9c32-108">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-108">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP \_ 旗標 \_ 非 \_ 互動式**</span><span class="sxs-lookup"><span data-stu-id="e9c32-109"><span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP\_FLAG\_NON\_INTERACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-110">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e9c32-110">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-111">請勿顯示 (UI) 的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e9c32-111">Do not display a user interface (UI).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP \_ 旗標 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="e9c32-112"><span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**EAP\_FLAG\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-113">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e9c32-113">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-114">使用者資料是從 Windows 登入取得的。</span><span class="sxs-lookup"><span data-stu-id="e9c32-114">User data was obtained from Windows logon.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP \_ 旗標 \_ 預覽**</span><span class="sxs-lookup"><span data-stu-id="e9c32-115"><span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**EAP\_FLAG\_PREVIEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-116">0x00000008</span><span class="sxs-lookup"><span data-stu-id="e9c32-116">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-117">在驗證之前顯示認證 UI，即使快取的認證存在也一樣。</span><span class="sxs-lookup"><span data-stu-id="e9c32-117">Show credentials UI before authenticating, even if cached credentials are present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_旗標 \_ Reserved2**</span><span class="sxs-lookup"><span data-stu-id="e9c32-118"><span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span> **EAP\_FLAG\_Reserved2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9c32-119">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-120">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-120">Do not use.</span></span> <span data-ttu-id="e9c32-121">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-121">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP \_ 旗標 \_ 電腦 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="e9c32-122"><span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**EAP\_FLAG\_MACHINE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-123">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e9c32-123">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-124">使用機器層級驗證;未設定此旗標表示正在使用使用者層級驗證。</span><span class="sxs-lookup"><span data-stu-id="e9c32-124">Use machine level authentication; not setting this flag indicates user level authentication is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP \_ 旗標 \_ 來賓 \_ 存取**</span><span class="sxs-lookup"><span data-stu-id="e9c32-125"><span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**EAP\_FLAG\_GUEST\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9c32-126">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e9c32-126">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-127">表示提供來賓存取權的要求。</span><span class="sxs-lookup"><span data-stu-id="e9c32-127">Indicates a request to provide guest access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP \_ 旗標 \_ Reserved3**</span><span class="sxs-lookup"><span data-stu-id="e9c32-128"><span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP\_FLAG\_Reserved3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-129">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e9c32-129">0x00000080</span></span> 
</dt> <dt>



<span data-ttu-id="e9c32-130">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-130">Do not use.</span></span> <span data-ttu-id="e9c32-131">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-131">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_旗標 \_ Reserved4**</span><span class="sxs-lookup"><span data-stu-id="e9c32-132"><span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span> **EAP\_FLAG\_Reserved4**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-133">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e9c32-133">0x00000100</span></span> 
</dt> <dt>



<span data-ttu-id="e9c32-134">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-134">Do not use.</span></span> <span data-ttu-id="e9c32-135">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-135">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP \_ 旗 \_ 標 \_ 從 \_ 休眠狀態繼續**</span><span class="sxs-lookup"><span data-stu-id="e9c32-136"><span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP\_FLAG\_RESUME\_FROM\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-137">0x00000200</span><span class="sxs-lookup"><span data-stu-id="e9c32-137">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-138">表示這是機器活動從休眠期間繼續進行的第一次呼叫。</span><span class="sxs-lookup"><span data-stu-id="e9c32-138">Indicates this is the first call after machine activity has resumed from a period of hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_旗標 \_ Reserved5**</span><span class="sxs-lookup"><span data-stu-id="e9c32-139"><span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span> **EAP\_FLAG\_Reserved5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-140">0x00000400</span><span class="sxs-lookup"><span data-stu-id="e9c32-140">0x00000400</span></span> 
</dt> <dt>



<span data-ttu-id="e9c32-141">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-141">Do not use.</span></span> <span data-ttu-id="e9c32-142">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-142">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP \_ 旗標 \_ Reserved6**</span><span class="sxs-lookup"><span data-stu-id="e9c32-143"><span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP\_FLAG\_Reserved6**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-144">0x00000800</span><span class="sxs-lookup"><span data-stu-id="e9c32-144">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-145">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-145">Do not use.</span></span> <span data-ttu-id="e9c32-146">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-146">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP \_ 旗標 \_ 完整 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="e9c32-147"><span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**EAP\_FLAG\_FULL\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-148">0x00001000</span><span class="sxs-lookup"><span data-stu-id="e9c32-148">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-149">表示通道方法應該執行完整驗證，而不是簡短版本，例如 [受保護的 EAP (PEAP) 快速重新](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10))連線。</span><span class="sxs-lookup"><span data-stu-id="e9c32-149">Indicates that tunnel methods should perform a full authentication instead of an abbreviated version, such as [Protected EAP (PEAP) Fast Reconnect](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP \_ 旗標 \_ 偏好 \_ 替換 \_ 認證**</span><span class="sxs-lookup"><span data-stu-id="e9c32-150"><span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**EAP\_FLAG\_PREFER\_ALT\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e9c32-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-152">指出所有其他形式的認證抓取都偏好傳遞至 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) 的認證，即使傳遞到目前函式的設定資料要求不同的認證抓取模式也是一樣。</span><span class="sxs-lookup"><span data-stu-id="e9c32-152">Indicates credentials passed into [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) are preferred to all other forms of credential retrieval, even if configuration data passed into the current function requests a different mode of credential retrieval.</span></span>

> [!Note]  
> <span data-ttu-id="e9c32-153">此旗標僅供 [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-153">This flag is only used by [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP \_ 旗標 \_ Reserved7**</span><span class="sxs-lookup"><span data-stu-id="e9c32-154"><span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP\_FLAG\_Reserved7**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-155">0x00004000</span><span class="sxs-lookup"><span data-stu-id="e9c32-155">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-156">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-156">Do not use.</span></span> <span data-ttu-id="e9c32-157">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-157">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP \_ 對等 \_ 旗標 \_ 健全狀況 \_ 狀態 \_ 變更**</span><span class="sxs-lookup"><span data-stu-id="e9c32-158"><span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**EAP\_PEER\_FLAG\_HEALTH\_STATE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-159">0x00008000</span><span class="sxs-lookup"><span data-stu-id="e9c32-159">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-160">指出重新驗證的原因是 (NAP) 回呼的 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) ;因為健全狀況狀態變更，所以 NAP 起始了驗證會話。</span><span class="sxs-lookup"><span data-stu-id="e9c32-160">Indicates the cause of re-authentication is a [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP) callback; NAP initiated the authentication session because the health state changed.</span></span> <span data-ttu-id="e9c32-161">只有當先前呼叫這個函式所提供的 NAP 特定 [*NotificationHandler*](/previous-versions/windows/desktop/api) 回呼呼叫這個函式時，才必須傳送此旗標。</span><span class="sxs-lookup"><span data-stu-id="e9c32-161">This flag must be sent only when this function is called by a NAP-specific [*NotificationHandler*](/previous-versions/windows/desktop/api) callback provided by a previous call to this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP \_ 旗標 \_ 抑制 \_ UI**</span><span class="sxs-lookup"><span data-stu-id="e9c32-162"><span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**EAP\_FLAG\_SUPRESS\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-163">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e9c32-163">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-164">繼續以可用資訊進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e9c32-164">Continue authentication with available information.</span></span> <span data-ttu-id="e9c32-165">如果驗證無法繼續，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="e9c32-165">If the authentication cannot proceed then fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP \_ 旗標 \_ 預先 \_ 登入**</span><span class="sxs-lookup"><span data-stu-id="e9c32-166"><span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**EAP\_FLAG\_PRE\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-167">0x00020000</span><span class="sxs-lookup"><span data-stu-id="e9c32-167">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-168">表示 EAPHost 應該提供單一登入 (SSO) 。</span><span class="sxs-lookup"><span data-stu-id="e9c32-168">Indicates that EAPHost should provide Single-Sign-On (SSO).</span></span> <span data-ttu-id="e9c32-169">如需詳細資訊，請參閱 [SSO 和 PLAP](understanding-sso-and-plap.md)。</span><span class="sxs-lookup"><span data-stu-id="e9c32-169">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP \_ 旗標 \_ 使用者 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="e9c32-170"><span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**EAP\_FLAG\_USER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-171">0x00040000</span><span class="sxs-lookup"><span data-stu-id="e9c32-171">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-172">表示無法設定 **EAP \_ 旗標 \_ 電腦 \_ 驗證** 之舊版方法的使用者層級驗證。</span><span class="sxs-lookup"><span data-stu-id="e9c32-172">Indicates user level authentication for legacy methods that cannot set **EAP\_FLAG\_MACHINE\_AUTH**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP \_ 旗標 \_ SAMPLEPAGE.DLL.CONFG \_ READONLY**</span><span class="sxs-lookup"><span data-stu-id="e9c32-173"><span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP\_FLAG\_CONFG\_READONLY**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9c32-174">0x00080000</span><span class="sxs-lookup"><span data-stu-id="e9c32-174">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-175">表示可查看但未更新的設定。</span><span class="sxs-lookup"><span data-stu-id="e9c32-175">Indicates the configuration can be viewed but not updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9c32-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP \_ 旗標 \_ Reserved8**</span><span class="sxs-lookup"><span data-stu-id="e9c32-176"><span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP\_FLAG\_Reserved8**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9c32-177">0x00100000</span><span class="sxs-lookup"><span data-stu-id="e9c32-177">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="e9c32-178">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-178">Do not use.</span></span> <span data-ttu-id="e9c32-179">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="e9c32-179">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9c32-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9c32-180">Requirements</span></span>



| <span data-ttu-id="e9c32-181">需求</span><span class="sxs-lookup"><span data-stu-id="e9c32-181">Requirement</span></span> | <span data-ttu-id="e9c32-182">值</span><span class="sxs-lookup"><span data-stu-id="e9c32-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c32-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9c32-183">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c32-184">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c32-184">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9c32-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9c32-185">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c32-186">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9c32-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9c32-187">標頭</span><span class="sxs-lookup"><span data-stu-id="e9c32-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c32-188"><dt>Eaptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c32-188"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9c32-189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9c32-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c32-190">常見的 EAPHost 常數</span><span class="sxs-lookup"><span data-stu-id="e9c32-190">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

