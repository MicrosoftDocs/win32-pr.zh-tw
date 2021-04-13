---
title: COM 安全性預設值
description: 您可以使用應用程式的 COM 安全性預設值，而非指定您自己的安全性設定。
ms.assetid: 6f1f6925-a6ab-4cfa-b0b4-b4b4012979f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cba607044d6e93c9f01243809feae6e5a600851
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300131"
---
# <a name="com-security-defaults"></a><span data-ttu-id="157ea-103">COM 安全性預設值</span><span class="sxs-lookup"><span data-stu-id="157ea-103">COM Security Defaults</span></span>

<span data-ttu-id="157ea-104">您可以使用應用程式的 COM 安全性預設值，而非指定您自己的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="157ea-104">You can use the COM security defaults for your application rather than specifying your own security settings.</span></span> <span data-ttu-id="157ea-105">在這種情況下，COM 會為您初始化及管理安全性。</span><span class="sxs-lookup"><span data-stu-id="157ea-105">In that case, COM will initialize and manage security for you.</span></span> <span data-ttu-id="157ea-106">您不需要設定登錄或呼叫程式中的任何安全性功能。</span><span class="sxs-lookup"><span data-stu-id="157ea-106">You do not need to configure the registry or call any security functions in your program.</span></span>

<span data-ttu-id="157ea-107">但是，如果已設定或修改特定的登錄值，COM 使用的安全性預設值將會受到影響。</span><span class="sxs-lookup"><span data-stu-id="157ea-107">However, if certain registry named values have been set or modified, the security defaults that COM uses will be affected.</span></span> <span data-ttu-id="157ea-108">下列清單說明 COM 安全性的預設值，並說明某些值如何受到登錄設定的影響。</span><span class="sxs-lookup"><span data-stu-id="157ea-108">The list below describes COM security default values and explains how some values are influenced by registry settings.</span></span>

<span data-ttu-id="157ea-109">以下是 COM 使用的預設安全性值：</span><span class="sxs-lookup"><span data-stu-id="157ea-109">Following are the default security values that COM uses:</span></span>

-   <span data-ttu-id="157ea-110">預設的安全性服務提供者是由 COM 決定最符合環境的安全性服務提供者。</span><span class="sxs-lookup"><span data-stu-id="157ea-110">The default security service provider is the one that is determined by COM to be the most compatible with the environment.</span></span> <span data-ttu-id="157ea-111">COM 會選擇 Kerberos v5 通訊協定或 NTLMSSP，其中的 Kerberos 通訊協定是預設選項。</span><span class="sxs-lookup"><span data-stu-id="157ea-111">COM chooses either the Kerberos v5 protocol or NTLMSSP, with the Kerberos protocol being the default choice.</span></span> <span data-ttu-id="157ea-112">Schannel 提供的通訊協定都未被選擇為預設值。</span><span class="sxs-lookup"><span data-stu-id="157ea-112">None of the protocols provided by Schannel are ever chosen as the default.</span></span>
-   <span data-ttu-id="157ea-113">系統會透過使用者名稱和密碼來識別呼叫者，並自動建立安全性系統所使用的識別權杖。</span><span class="sxs-lookup"><span data-stu-id="157ea-113">The system identifies a caller through user name and password and automatically creates an identification token used by the security system.</span></span>
-   <span data-ttu-id="157ea-114">如果 [LegacyAuthenticationLevel](legacyauthenticationlevel.md) 名稱值存在，而且已設定其值，則會使用該值。</span><span class="sxs-lookup"><span data-stu-id="157ea-114">If the [LegacyAuthenticationLevel](legacyauthenticationlevel.md) named value exists and if its value has been set, that value is used.</span></span> <span data-ttu-id="157ea-115">否則，驗證層級會設定為 connect (RPC \_ C \_ 驗證 \_ level \_ connect) 。</span><span class="sxs-lookup"><span data-stu-id="157ea-115">Otherwise, the authentication level is set at connect (RPC\_C\_AUTHN\_LEVEL\_CONNECT).</span></span> <span data-ttu-id="157ea-116">這個層級表示，在用戶端對伺服器進行的第一次呼叫時，COM 會進行驗證檢查。</span><span class="sxs-lookup"><span data-stu-id="157ea-116">This level means that at the first call a client makes to the server, COM does an authentication check.</span></span> <span data-ttu-id="157ea-117">如果用戶端通過檢查，就不會再進行進一步的驗證。</span><span class="sxs-lookup"><span data-stu-id="157ea-117">If the client passes the check, no further authentication is done.</span></span> <span data-ttu-id="157ea-118">AuthenticationLevel 值也可以在 [AppID](appid-key.md) 索引鍵下設定。</span><span class="sxs-lookup"><span data-stu-id="157ea-118">The AuthenticationLevel value can also be set under the [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="157ea-119">如果 [LegacyImpersonationLevel](legacyimpersonationlevel.md) 名稱值存在，而且已設定其值，則會使用該值。</span><span class="sxs-lookup"><span data-stu-id="157ea-119">If the [LegacyImpersonationLevel](legacyimpersonationlevel.md) named value exists and if its value has been set, that value is used.</span></span> <span data-ttu-id="157ea-120">否則，會將模擬層級設定為識別)  (RPC \_ C \_ IMP \_ 等級 \_ 。</span><span class="sxs-lookup"><span data-stu-id="157ea-120">Otherwise, the impersonation level is set to identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span> <span data-ttu-id="157ea-121">用戶端會將模擬許可權授與伺服器。</span><span class="sxs-lookup"><span data-stu-id="157ea-121">Impersonation rights are granted by the client to the server.</span></span> <span data-ttu-id="157ea-122">識別層級表示伺服器可以取得用戶端的身分識別。</span><span class="sxs-lookup"><span data-stu-id="157ea-122">Identify level means that the server can obtain the client's identity.</span></span> <span data-ttu-id="157ea-123">伺服器可以模擬用戶端的存取控制清單 (ACL) 檢查，但是無法存取系統物件做為用戶端。</span><span class="sxs-lookup"><span data-stu-id="157ea-123">The server can impersonate the client for access control list (ACL) checking but cannot access system objects as the client.</span></span> <span data-ttu-id="157ea-124">如需詳細資訊，請參閱模擬 [層級](impersonation-levels.md) 和 [掩蓋](cloaking.md)。</span><span class="sxs-lookup"><span data-stu-id="157ea-124">For more information, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>
-   <span data-ttu-id="157ea-125">如果 **AppID** 下的 [AccessPermission](accesspermission.md)命名值存在且已設定，則會使用該值。</span><span class="sxs-lookup"><span data-stu-id="157ea-125">If the [AccessPermission](accesspermission.md) named value under **AppID** exists and has been set, that value is used.</span></span> <span data-ttu-id="157ea-126">否則，COM 會檢查是否有 [DefaultAccessPermission](defaultaccesspermission.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="157ea-126">Otherwise, COM checks for a [DefaultAccessPermission](defaultaccesspermission.md) entry.</span></span> <span data-ttu-id="157ea-127">如果存在，則會使用該值。</span><span class="sxs-lookup"><span data-stu-id="157ea-127">If present, that value is used.</span></span> <span data-ttu-id="157ea-128">如果此值不存在，COM 會將授與許可權給伺服器身分識別和本機系統的 ACL 進行結構。</span><span class="sxs-lookup"><span data-stu-id="157ea-128">If this value is not present, COM constructs an ACL that grants permissions to the server identity and the local system.</span></span>
-   <span data-ttu-id="157ea-129">如果 **AppID** 下的 [SRPTrustLevel](srptrustlevel.md)命名值存在且已設定，則會使用該值。</span><span class="sxs-lookup"><span data-stu-id="157ea-129">If the [SRPTrustLevel](srptrustlevel.md) named value under **AppID** exists and has been set, that value is used.</span></span> <span data-ttu-id="157ea-130">否則，軟體限制原則 (SRP) 信任層級設定為 [不允許]， (更安全的 \_ LEVELID \_) ，這表示應用程式會在受限的環境中執行，而且不允許存取使用者的任何安全性敏感性使用者權限。</span><span class="sxs-lookup"><span data-stu-id="157ea-130">Otherwise, the Software Restriction Policy (SRP) trust level is set to Disallowed (SAFER\_LEVELID\_DISALLOWED), which indicates that the application is run in a constrained environment and is disallowed from accessing any security-sensitive user privileges of the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="157ea-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="157ea-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157ea-132">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="157ea-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




