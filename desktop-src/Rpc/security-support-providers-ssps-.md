---
title: " (Ssp 的安全性支援提供者) "
description: 從 Windows 2000 開始，RPC 支援各種不同的安全性提供者和套件。
ms.assetid: f82eba3d-412e-4cb6-9353-2e66bd0f377a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cc5417dd6142c693005a1aab9d39738d108ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093188"
---
# <a name="security-support-providers-ssps"></a><span data-ttu-id="f45f0-103"> (Ssp 的安全性支援提供者) </span><span class="sxs-lookup"><span data-stu-id="f45f0-103">Security Support Providers (SSPs)</span></span>

<span data-ttu-id="f45f0-104">從 Windows 2000 開始，RPC 支援各種不同的安全性提供者和套件。</span><span class="sxs-lookup"><span data-stu-id="f45f0-104">Beginning with Windows 2000, RPC supports a variety of security providers and packages.</span></span> <span data-ttu-id="f45f0-105">這些包括：</span><span class="sxs-lookup"><span data-stu-id="f45f0-105">These include:</span></span>

-   <span data-ttu-id="f45f0-106">**Kerberos 通訊協定安全性封裝。**</span><span class="sxs-lookup"><span data-stu-id="f45f0-106">**Kerberos Protocol Security Package.**</span></span> <span data-ttu-id="f45f0-107">Kerberos v5 通訊協定是業界標準的安全性套件。</span><span class="sxs-lookup"><span data-stu-id="f45f0-107">Kerberos v5 protocol is an industry-standard security package.</span></span> <span data-ttu-id="f45f0-108">它會使用 fullsic 主體名稱。</span><span class="sxs-lookup"><span data-stu-id="f45f0-108">It uses fullsic principal names.</span></span>
-   <span data-ttu-id="f45f0-109">**SCHANNEL SSP。**</span><span class="sxs-lookup"><span data-stu-id="f45f0-109">**SCHANNEL SSP.**</span></span> <span data-ttu-id="f45f0-110">這個 SSP 會執行 Microsoft 統一通訊協定提供者安全性封裝，以統一 SSL、私用通訊技術 (PCT) ，以及將傳輸層級安全性 (TLS) 成一個安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="f45f0-110">This SSP implements the Microsoft Unified Protocol Provider security package, which unifies SSL, private communication technology (PCT), and transport level security (TLS) into one security package.</span></span> <span data-ttu-id="f45f0-111">它會辨識 msstd 和 fullsic 主體名稱。</span><span class="sxs-lookup"><span data-stu-id="f45f0-111">It recognizes msstd and fullsic principal names.</span></span>
-   <span data-ttu-id="f45f0-112">**NTLM 安全性封裝。**</span><span class="sxs-lookup"><span data-stu-id="f45f0-112">**NTLM Security Package.**</span></span> <span data-ttu-id="f45f0-113">這是 Windows 2000 之前 NTLM 網路的主要安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="f45f0-113">This was the primary security package for NTLM networks prior to Windows 2000.</span></span>

<span data-ttu-id="f45f0-114">此外，Microsoft RPC 提供的 *虛擬 ssp* 可讓應用程式在使用真正的 ssp 之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="f45f0-114">In addition, Microsoft RPC provides a *pseudo-SSP* that enables applications to negotiate between the use of real SSPs.</span></span> <span data-ttu-id="f45f0-115">這個稱為簡單 GSS-API 協商機制 (Snego) SSP 的虛擬 SSP 不提供任何實際的驗證功能。</span><span class="sxs-lookup"><span data-stu-id="f45f0-115">This pseudo-SSP, called the Simple GSS-API Negotiation Mechanism (Snego) SSP, does not provide any actual authentication features.</span></span> <span data-ttu-id="f45f0-116">其唯一用途是協助應用程式選取真實的 SSP。</span><span class="sxs-lookup"><span data-stu-id="f45f0-116">Its only use is to help applications select a real SSP.</span></span> <span data-ttu-id="f45f0-117">目前，用戶端和伺服器程式可以使用 Snego SSP，在使用 NTLM 安全性封裝和 Kerberos 通訊協定安全性封裝之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="f45f0-117">Currently, client and server programs can use the Snego SSP to negotiate between the use of the NTLM security package and Kerberos protocol security package.</span></span> <span data-ttu-id="f45f0-118">如需有關選取 Ssp 的詳細資訊，請參閱 [驗證-服務常數](authentication-service-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f45f0-118">For more information on selecting SSPs, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="f45f0-119">Microsoft 提供的所有 Ssp （SCHANNEL 除外）都是以 [**每秒的 \_ WINNT \_ AUTH \_ IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) 結構所提供的格式來辨識驗證認證。</span><span class="sxs-lookup"><span data-stu-id="f45f0-119">All of the SSPs that Microsoft provides, except SCHANNEL, recognize authentication credentials in the form provided by the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="f45f0-120">如需詳細資訊，請參閱 [用戶端驗證認證](client-authentication-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="f45f0-120">For details, see [Client Authentication Credentials](client-authentication-credentials.md).</span></span> <span data-ttu-id="f45f0-121">如需有關如何使用特定 Ssp 的詳細資訊，請參閱「平臺軟體發展工具組 (SDK) 的安全性檔案中的 [SSPI](/windows/desktop/SecMgmt/management-functions) 函式和 [使用 Schannel 安全性提供者](/windows/desktop/SecAuthN/secure-channel) 。</span><span class="sxs-lookup"><span data-stu-id="f45f0-121">For information on how to use specific SSPs, see [SSPI Functions](/windows/desktop/SecMgmt/management-functions) and [Using the Schannel Security Provider](/windows/desktop/SecAuthN/secure-channel) in the Security documentation of the Platform Software Development Kit (SDK).</span></span>

 

 