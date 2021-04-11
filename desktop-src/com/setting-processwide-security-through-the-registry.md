---
title: 透過登錄設定 Process-Wide 安全性
description: 如果您想要設定整個進程的安全性，有一個解決方案是在登錄中設定您想要的安全性層級。
ms.assetid: 87f0a64f-f3ec-4ee2-8d65-4f82e8971f0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d303f184229cb20aef1cbf71733956a3b6ce6618
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933648"
---
# <a name="setting-process-wide-security-through-the-registry"></a><span data-ttu-id="39284-103">透過登錄設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="39284-103">Setting Process-Wide Security Through the Registry</span></span>

<span data-ttu-id="39284-104">如果您想要設定整個進程的安全性，有一個解決方案是在登錄中設定您想要的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="39284-104">If you want to set security for an entire process, one solution is to set the security levels you want in the registry.</span></span> <span data-ttu-id="39284-105">如果您的應用程式無法呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ，或如果您不想使用程式設計安全性，這可能是個不錯的選項。</span><span class="sxs-lookup"><span data-stu-id="39284-105">If your application cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or if you prefer not to use programmatic security, this might be a good option.</span></span> <span data-ttu-id="39284-106">如果您決定使用登錄設定整個進程的安全性，請注意，如果您在程式中呼叫 **CoInitializeSecurity** ，就會使用 **CoInitializeSecurity** 中的值並忽略登錄值。</span><span class="sxs-lookup"><span data-stu-id="39284-106">If you decide to set process-wide security using the registry, you should be aware that if you call **CoInitializeSecurity** within your program COM will use the values in **CoInitializeSecurity** and ignore the registry values.</span></span>

<span data-ttu-id="39284-107">有兩種方式可以為您的應用程式設定登錄中的安全性：</span><span class="sxs-lookup"><span data-stu-id="39284-107">There are two ways to set security in the registry for your application:</span></span>

-   <span data-ttu-id="39284-108">您可以使用 Dcomcnfg.exe，這會提供簡單的使用者介面來修改安全性值。</span><span class="sxs-lookup"><span data-stu-id="39284-108">You can use Dcomcnfg.exe, which provides a simple user interface for modifying security values.</span></span> <span data-ttu-id="39284-109">您可以使用 Dcomcnfg.exe 設定所有的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="39284-109">All COM servers can be configured using Dcomcnfg.exe.</span></span> <span data-ttu-id="39284-110">如需詳細資訊，請參閱 [使用 DCOMCNFG 設定 Process-Wide 安全性](setting-processwide-security-using-dcomcnfg.md)。</span><span class="sxs-lookup"><span data-stu-id="39284-110">For more information, see [Setting Process-Wide Security Using DCOMCNFG](setting-processwide-security-using-dcomcnfg.md).</span></span> <span data-ttu-id="39284-111">不過，用戶端應用程式通常不會出現在 Dcomcnfg.exe 中，除非用戶端建立 GUID 並將它輸入到登錄中。</span><span class="sxs-lookup"><span data-stu-id="39284-111">However, client applications do not normally appear in Dcomcnfg.exe unless the client creates a GUID and enters it in the registry.</span></span>
-   <span data-ttu-id="39284-112">您可以在應用程式的 [AppID](appid-key.md) 金鑰下設定安全性值。</span><span class="sxs-lookup"><span data-stu-id="39284-112">You can set security values under the [AppID](appid-key.md) key for the application.</span></span> <span data-ttu-id="39284-113">本主題的其餘部分將說明如何使用 **AppID** 金鑰在登錄中設定安全性。</span><span class="sxs-lookup"><span data-stu-id="39284-113">The rest of this topic explains how to set security in the registry using the **AppID** key.</span></span>

<span data-ttu-id="39284-114">AppID 是 GUID，代表一或多個類別的伺服器進程。</span><span class="sxs-lookup"><span data-stu-id="39284-114">An AppID is a GUID that represents a server process for one or more classes.</span></span> <span data-ttu-id="39284-115">每個類別都只會與一個 AppID 相關聯，而 Appid 只能指派給 Exe。</span><span class="sxs-lookup"><span data-stu-id="39284-115">Each class is associated with exactly one AppID, and AppIDs can be assigned only to EXEs.</span></span> <span data-ttu-id="39284-116">除非 Dll 是在代理程式中執行，否則 Dll 不會取得 Appid，而是具有 AppID 的代理程式。</span><span class="sxs-lookup"><span data-stu-id="39284-116">DLLs do not get AppIDs unless they are running in a surrogate, and then it is the surrogate process that has the AppID.</span></span> <span data-ttu-id="39284-117">如果將多個 Dll 載入至代理，每個代理程式只會有一個 AppID。</span><span class="sxs-lookup"><span data-stu-id="39284-117">If multiple DLLs are loaded into a surrogate, each surrogate has only one AppID.</span></span>

<span data-ttu-id="39284-118">針對某些 COM 伺服器，註冊程式碼會產生 AppID，並將專案放在登錄中，以將 AppID 對應到可執行檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="39284-118">For some COM servers, the registration code generates an AppID and places entries in the registry that map the AppID to the name of the executable.</span></span> <span data-ttu-id="39284-119">但某些 COM 伺服器並不提供此功能。</span><span class="sxs-lookup"><span data-stu-id="39284-119">But some COM servers do not provide this functionality.</span></span> <span data-ttu-id="39284-120">但是，如果在執行 dcomcnfg.exe 時，伺服器的註冊程式碼新增 HKCR \\ CLSID {ServerCLSID} \\ [LocalServer32](localserver32.md)的專案，則會自動新增 CLSID 的 AppID。</span><span class="sxs-lookup"><span data-stu-id="39284-120">However, if the server's registration code adds an entry for HKCR\\CLSID{ServerCLSID}\\[LocalServer32](localserver32.md) when dcomcnfg.exe is run, it will automatically add an AppID for the CLSID.</span></span>

<span data-ttu-id="39284-121">若為非伺服器的 COM 用戶端，則不會建立此對應，因為用戶端從未註冊。</span><span class="sxs-lookup"><span data-stu-id="39284-121">For a COM client that is not a server, this mapping is not created because the client is never registered.</span></span> <span data-ttu-id="39284-122">因此，若要使用 **AppID** 金鑰設定安全性，用戶端必須使用登錄 [功能](/windows/desktop/SysInfo/registry-functions) 或使用 regedit 以程式設計的方式建立必要的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="39284-122">Therefore, to set security using the **AppID** key, the client must create the necessary registry entries, either programmatically by using the [registry functions](/windows/desktop/SysInfo/registry-functions) or by using regedit.</span></span>

<span data-ttu-id="39284-123">如果您決定以 **appid** 金鑰在登錄中設定整個進程的安全性，請注意，您可以在不具有系統管理員許可權的情況下設定的 **appid** 金鑰底下有兩個名為的值：</span><span class="sxs-lookup"><span data-stu-id="39284-123">If you decide to set process-wide security in the registry under the **AppID** key, be aware that there are two named values under the **AppID** key that you can set without having administrator permissions:</span></span>

-   [<span data-ttu-id="39284-124">AccessPermission</span><span class="sxs-lookup"><span data-stu-id="39284-124">AccessPermission</span></span>](accesspermission.md)
-   [<span data-ttu-id="39284-125">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="39284-125">AuthenticationLevel</span></span>](authenticationlevel.md)

<span data-ttu-id="39284-126">**AuthenticationLevel** 和 **AccessPermission** 值是獨立設定的，而且具有個別的預設值。</span><span class="sxs-lookup"><span data-stu-id="39284-126">The **AuthenticationLevel** and **AccessPermission** values are set independently and have separate default values.</span></span> <span data-ttu-id="39284-127">如果 **AuthenticationLevel** 值不存在，就會使用 [LegacyAuthenticationLevel](legacyauthenticationlevel.md) 值作為預設值。</span><span class="sxs-lookup"><span data-stu-id="39284-127">If the **AuthenticationLevel** value is not present, the [LegacyAuthenticationLevel](legacyauthenticationlevel.md) value is used as the default.</span></span> <span data-ttu-id="39284-128">同樣地，如果 **AccessPermission** 值不存在，就會使用 [DefaultAccessPermission](defaultaccesspermission.md) 值作為預設值。</span><span class="sxs-lookup"><span data-stu-id="39284-128">Similarly, if the **AccessPermission** value is not present, the [DefaultAccessPermission](defaultaccesspermission.md) value is used as the default.</span></span> <span data-ttu-id="39284-129">不過， **AuthenticationLevel** 和 **AccessPermission** 值會以下列方式相互關聯：</span><span class="sxs-lookup"><span data-stu-id="39284-129">However, the **AuthenticationLevel** and the **AccessPermission** values are interrelated in the following ways:</span></span>

-   <span data-ttu-id="39284-130">如果 **AuthenticationLevel** 為 none，則會忽略該應用程式的 **AccessPermission** 和 **DefaultAccessPermission** 值。</span><span class="sxs-lookup"><span data-stu-id="39284-130">If the **AuthenticationLevel** is none, the **AccessPermission** and **DefaultAccessPermission** values are ignored for that application.</span></span>
-   <span data-ttu-id="39284-131">如果 **AuthenticationLevel** 不存在，而且 **LegacyAuthenticationLevel** 為 none，則該應用程式的 **AccessPermission** 和 **DefaultAccessPermission** 值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="39284-131">If the **AuthenticationLevel** is not present and the **LegacyAuthenticationLevel** is none, the **AccessPermission** and **DefaultAccessPermission** values are ignored for that application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39284-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="39284-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39284-133">設定 Process-Wide 安全性</span><span class="sxs-lookup"><span data-stu-id="39284-133">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 