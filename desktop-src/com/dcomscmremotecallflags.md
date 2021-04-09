---
title: DCOMSCMRemoteCallFlags
description: 控制從本機 DCOM 服務控制管理員 (DCOMSCM) 至遠端 DCOMSCM 的呼叫行為。
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- DCOMSCMRemoteCallFlags 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024148"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="3adb9-104">DCOMSCMRemoteCallFlags</span><span class="sxs-lookup"><span data-stu-id="3adb9-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="3adb9-105">控制從本機 DCOM 服務控制管理員 (DCOMSCM) 至遠端 DCOMSCM 的呼叫行為。</span><span class="sxs-lookup"><span data-stu-id="3adb9-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3adb9-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="3adb9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="3adb9-107">備註</span><span class="sxs-lookup"><span data-stu-id="3adb9-107">Remarks</span></span>

<span data-ttu-id="3adb9-108">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="3adb9-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="3adb9-109">值</span><span class="sxs-lookup"><span data-stu-id="3adb9-109">Value</span></span> | <span data-ttu-id="3adb9-110">描述</span><span class="sxs-lookup"><span data-stu-id="3adb9-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="3adb9-111">0x1</span><span class="sxs-lookup"><span data-stu-id="3adb9-111">0x1</span></span>   | <span data-ttu-id="3adb9-112">**DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="3adb9-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="3adb9-113">0x2</span><span class="sxs-lookup"><span data-stu-id="3adb9-113">0x2</span></span>   | <span data-ttu-id="3adb9-114">**DCOMSCM \_ 啟用不 \_ 允許不安全的 \_ \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="3adb9-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="3adb9-115">0x4</span><span class="sxs-lookup"><span data-stu-id="3adb9-115">0x4</span></span>   | <span data-ttu-id="3adb9-116">**DCOMSCM \_ 解決 \_ 使用 \_ 所有 \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="3adb9-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="3adb9-117">0x8</span><span class="sxs-lookup"><span data-stu-id="3adb9-117">0x8</span></span>   | <span data-ttu-id="3adb9-118">**DCOMSCM \_ RESOLVE 不 \_ 允許不安全的 \_ \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="3adb9-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="3adb9-119">0x10</span><span class="sxs-lookup"><span data-stu-id="3adb9-119">0x10</span></span>  | <span data-ttu-id="3adb9-120">**DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE**</span><span class="sxs-lookup"><span data-stu-id="3adb9-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="3adb9-121">DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES 描述</span><span class="sxs-lookup"><span data-stu-id="3adb9-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="3adb9-122">當用戶端發出使用預設安全性設定的啟用要求時，本機 DCOMSCM 會在對遠端 DCOMSCM 進行啟用 RPC 呼叫時使用「協商驗證」服務。</span><span class="sxs-lookup"><span data-stu-id="3adb9-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="3adb9-123">如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的啟用 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="3adb9-124">**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的啟用 RPC 呼叫失敗，本機 DCOMSCM 會使用 Kerberos、NTLM 或其他已設定的安全性提供者來進行啟用 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="3adb9-125">如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會使用沒有安全性的啟用 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="3adb9-126">藉由設定此旗標，您可以在 Windows Vista 或更高版本上執行本機 DCOMSCM，使其行為類似于 Vista 之前的系統。</span><span class="sxs-lookup"><span data-stu-id="3adb9-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="3adb9-127">除非相容性原因需要，否則不建議設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="3adb9-128">DCOMSCM \_ 啟用不 \_ 允許不安全的 \_ \_ 呼叫描述</span><span class="sxs-lookup"><span data-stu-id="3adb9-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="3adb9-129">如果已設定 **DCOMSCM \_ 啟用不允許不安全的 \_ \_ \_ 呼叫** 旗標，則本機 DCOMSCM 不會進行不安全的啟用 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="3adb9-130">若要讓用戶端使用非預設安全性設定來提出啟用要求，請在進行啟用要求時指定 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="3adb9-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="3adb9-131">在此情況下， **DCOMSCM \_ 啟用 \_ 使用 \_ 所有 \_ AUTHNSERVICES** 和 DCOMSCM 啟用時，會忽略不 **\_ 安全的 \_ \_ \_ 呼叫** 旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="3adb9-132">除非網路中的所有用戶端和伺服器都經過完整驗證，否則不建議設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="3adb9-133">DCOMSCM \_ RESOLVE \_ USE \_ ALL \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="3adb9-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="3adb9-134">當用戶端拆收物件參考時，本機 DCOMSCM 會在對遠端 DCOMSCM 進行 OXID 解析 RPC 呼叫時，使用「協商驗證」服務。</span><span class="sxs-lookup"><span data-stu-id="3adb9-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="3adb9-135">如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的方式來進行 OXID 解析 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="3adb9-136">**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的 OXID 解析 RPC 呼叫失敗，本機 DCOMSCM 會使用 Kerberos、NTLM 或其他已設定的安全性提供者來進行 OXID 解析 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="3adb9-137">如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會使用沒有安全性的方式進行 OXID 解析 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="3adb9-138">藉由設定此旗標，您可以在 Windows Vista 或更高版本上執行本機 DCOMSCM，使其行為類似于 Vista 之前的系統。</span><span class="sxs-lookup"><span data-stu-id="3adb9-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="3adb9-139">除非相容性原因需要，否則不建議設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="3adb9-140">DCOMSCM \_ RESOLVE 不 \_ 允許不安全的 \_ \_ 通話描述</span><span class="sxs-lookup"><span data-stu-id="3adb9-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="3adb9-141">如果已設定 **DCOMSCM \_ RESOLVE 不允許不安全的 \_ \_ \_ 呼叫** 旗標，則本機 DCOMSCM 不會進行不安全的 OXID 解析 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="3adb9-142">此外，本機 DCOMSCM 不會進行不安全的垃圾收集 Ping RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="3adb9-143">除非網路中的所有用戶端和伺服器都經過完整驗證，否則不建議設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="3adb9-144">DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE 描述</span><span class="sxs-lookup"><span data-stu-id="3adb9-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="3adb9-145">本機 DCOMSCM 會在對遠端 DCOMSCM 進行垃圾收集 Ping RPC 呼叫時，使用「協商驗證」服務。</span><span class="sxs-lookup"><span data-stu-id="3adb9-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="3adb9-146">如果呼叫失敗，本機 DCOMSCM 會使用沒有安全性的進行垃圾收集 Ping RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="3adb9-147">**Windows Server 2003 和 WINDOWS XP/2000：** 如果使用「協商驗證」服務的垃圾收集 Ping RPC 呼叫失敗，則本機 DCOMSCM 會使用 Kerberos、NTLM 和其他已設定的安全性提供者，讓垃圾收集 Ping RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="3adb9-148">如果沒有任何安全性提供者可運作，則本機 DCOMSCM 會進行垃圾收集，而不使用安全性來 Ping RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="3adb9-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="3adb9-149">藉由設定此旗標，您可以在 Windows Vista 或更新版本上使用本機 DCOMSCM，使其行為類似于 Vista 之前的系統。</span><span class="sxs-lookup"><span data-stu-id="3adb9-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="3adb9-150">除非相容性原因需要，否則不建議將 **DCOMSCM \_ PING \_ 使用 \_ MID \_ AUTHNSERVICE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="3adb9-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3adb9-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="3adb9-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3adb9-152">遠端連線的驗證</span><span class="sxs-lookup"><span data-stu-id="3adb9-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="3adb9-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="3adb9-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="3adb9-154">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="3adb9-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="3adb9-155">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="3adb9-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 