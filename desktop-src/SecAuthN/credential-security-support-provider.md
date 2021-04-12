---
description: " (CredSSP) 的認證安全性支援提供者通訊協定是安全性支援提供者，它是使用安全性支援提供者介面 (SSPI) 所執行。"
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: 認證安全性支援提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191735"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="05f1d-103">認證安全性支援提供者</span><span class="sxs-lookup"><span data-stu-id="05f1d-103">Credential Security Support Provider</span></span>

<span data-ttu-id="05f1d-104"> (CredSSP) 的認證安全性支援提供者通訊協定是安全性支援提供者，它是使用安全性支援提供者介面 ([SSPI](sspi.md)) 所執行。</span><span class="sxs-lookup"><span data-stu-id="05f1d-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="05f1d-105">CredSSP 可讓應用程式將使用者的認證從用戶端委派給目標伺服器，以進行遠端驗證。</span><span class="sxs-lookup"><span data-stu-id="05f1d-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="05f1d-106">CredSSP 提供加密的 [傳輸層安全性通訊協定](transport-layer-security-protocol.md) 通道。</span><span class="sxs-lookup"><span data-stu-id="05f1d-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="05f1d-107">用戶端會使用簡單且受保護的協商 (SPNEGO) 通訊協定（使用 [Microsoft Kerberos](microsoft-kerberos.md) 或 [microsoft NTLM](microsoft-ntlm.md)），透過加密通道進行驗證。</span><span class="sxs-lookup"><span data-stu-id="05f1d-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="05f1d-108">這不是限制委派。</span><span class="sxs-lookup"><span data-stu-id="05f1d-108">This is not constrained delegation.</span></span> <span data-ttu-id="05f1d-109">CredSSP 會將使用者的完整認證傳遞給沒有任何條件約束的伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f1d-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="05f1d-110">如需 SPNEGO 的詳細資訊，請參閱 [Microsoft Negotiate](microsoft-negotiate.md)。</span><span class="sxs-lookup"><span data-stu-id="05f1d-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="05f1d-111">用戶端和伺服器經過驗證之後，用戶端就會將使用者的認證傳遞給伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f1d-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="05f1d-112">認證會在 SPNEGO 和 TLS 工作階段金鑰下雙向加密。</span><span class="sxs-lookup"><span data-stu-id="05f1d-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="05f1d-113">CredSSP 支援以密碼為基礎的登入，以及根據 [*x.509*](/windows/desktop/SecGloss/x-gly) 和 PKINIT 的智慧卡登入。</span><span class="sxs-lookup"><span data-stu-id="05f1d-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05f1d-114">CredSSP 不支援 Wow64 用戶端。</span><span class="sxs-lookup"><span data-stu-id="05f1d-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="05f1d-115">如需 CredSSP 的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="05f1d-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="05f1d-116">主題</span><span class="sxs-lookup"><span data-stu-id="05f1d-116">Topic</span></span>                                                                         | <span data-ttu-id="05f1d-117">描述</span><span class="sxs-lookup"><span data-stu-id="05f1d-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05f1d-118">CredSSP 群組原則設定</span><span class="sxs-lookup"><span data-stu-id="05f1d-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="05f1d-119">您可以使用群組原則設定來控制 CredSSP 的認證委派。</span><span class="sxs-lookup"><span data-stu-id="05f1d-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

