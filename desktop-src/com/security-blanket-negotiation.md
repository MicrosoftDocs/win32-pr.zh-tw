---
title: 安全性的總協商
description: 安全性的總協商
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024167"
---
# <a name="security-blanket-negotiation"></a><span data-ttu-id="c4cd7-103">安全性的總協商</span><span class="sxs-lookup"><span data-stu-id="c4cd7-103">Security Blanket Negotiation</span></span>

<span data-ttu-id="c4cd7-104">安全性一般是一組值，這些值會描述套用至進程中所有 proxy 或只套用至特定介面 proxy 的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-104">A security blanket is a group of values that describe the security settings that apply to all proxies in a process or to just a particular interface proxy.</span></span> <span data-ttu-id="c4cd7-105">安全性的總包含下列值：</span><span class="sxs-lookup"><span data-stu-id="c4cd7-105">A security blanket comprises the following values:</span></span>

-   <span data-ttu-id="c4cd7-106">驗證服務</span><span class="sxs-lookup"><span data-stu-id="c4cd7-106">Authentication service</span></span>
-   <span data-ttu-id="c4cd7-107">授權服務</span><span class="sxs-lookup"><span data-stu-id="c4cd7-107">Authorization service</span></span>
-   <span data-ttu-id="c4cd7-108">主要名稱</span><span class="sxs-lookup"><span data-stu-id="c4cd7-108">Principal name</span></span>
-   <span data-ttu-id="c4cd7-109">驗證層級</span><span class="sxs-lookup"><span data-stu-id="c4cd7-109">Authentication level</span></span>
-   <span data-ttu-id="c4cd7-110">模擬等級</span><span class="sxs-lookup"><span data-stu-id="c4cd7-110">Impersonation level</span></span>
-   <span data-ttu-id="c4cd7-111">驗證身分識別</span><span class="sxs-lookup"><span data-stu-id="c4cd7-111">Authentication identity</span></span>
-   <span data-ttu-id="c4cd7-112">功能</span><span class="sxs-lookup"><span data-stu-id="c4cd7-112">Capabilities</span></span>
-   <span data-ttu-id="c4cd7-113">存取控制清單 (ACL) 僅 (伺服器) </span><span class="sxs-lookup"><span data-stu-id="c4cd7-113">An access control list (ACL) (servers only)</span></span>

<span data-ttu-id="c4cd7-114">安全性全面協商是 COM 在建立時，用來選擇 proxy 安全性設定的程式。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-114">Security blanket negotiation is the process that COM uses to choose the security settings for a proxy when it is created.</span></span> <span data-ttu-id="c4cd7-115">此程式牽涉到將伺服器的安全性全面與用戶端的安全性全面進行比較，並使用這些值來建立 proxy 的適當預設安全性。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-115">This process involves comparing the server's security blanket with the client's security blanket and using those values to create an appropriate default security blanket for the proxy.</span></span> <span data-ttu-id="c4cd7-116">下列段落說明用戶端和伺服器安全性毛毯的來源，並說明 COM 如何使用用戶端和伺服器的安全性毛毯，為 proxy 協調安全性的綜合。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-116">The following paragraphs explain where the client's and the server's security blankets come from and describe how COM negotiates the security blanket for the proxy using the client's and server's security blankets.</span></span>

<span data-ttu-id="c4cd7-117">用戶端和伺服器都可以呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來指定各自的安全性毛毯。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-117">The client and the server can each call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to specify their respective security blankets.</span></span> <span data-ttu-id="c4cd7-118">如果應用程式未明確呼叫 **CoInitializeSecurity** ，COM 會使用適當的預設值，針對應用程式隱含呼叫它。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-118">If an application doesn't call **CoInitializeSecurity** explicitly, COM calls it implicitly for the application, using appropriate default values.</span></span> <span data-ttu-id="c4cd7-119">如需這些預設值的詳細資訊，請參閱 [COM 安全性預設](com-security-defaults.md)值。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-119">For more information about these default values, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="c4cd7-120">當應用程式為伺服器時，會套用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的一些參數，而當應用程式是用戶端時，則會套用某些參數。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-120">Some parameters to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) apply when the application is a server, and some apply when the application is a client.</span></span> <span data-ttu-id="c4cd7-121">當應用程式作為伺服器時，這些參數會相關： ACL、驗證服務/授權服務/主體名稱元組的清單，以及驗證層級。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-121">When the application is acting as a server, these parameters are relevant: an ACL, a list of authentication service/authorization service/principal name tuples, and an authentication level.</span></span> <span data-ttu-id="c4cd7-122">伺服器對 **CoInitializeSecurity** 的呼叫（不論是隱含或明確）都會決定伺服器的安全性全面，也就是固定的。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-122">A server's call to **CoInitializeSecurity**, whether implicit or explicit, determines the server's security blanket, which remains fixed.</span></span>

<span data-ttu-id="c4cd7-123">當應用程式做為用戶端時，會將下列傳遞給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的值相關：驗證層級、模擬層級、驗證身分識別和功能。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-123">When the application is acting as a client, the following values passed to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) are relevant: an authentication level, an impersonation level, the authentication identity, and capabilities.</span></span> <span data-ttu-id="c4cd7-124">用戶端對 **CoInitializeSecurity** 的隱含或明確呼叫會指出用戶端想要的安全性階層。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-124">A client's implicit or explicit call to **CoInitializeSecurity** indicates the security blanket that the client wants.</span></span>

<span data-ttu-id="c4cd7-125">建立 proxy 時，COM 會使用伺服器安全性的總和用戶端安全性的總值，來協商適用于 proxy 的預設安全層。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-125">When a proxy is created, COM uses the values specified by the server's security blanket and the client's security blanket to negotiate a default security blanket that is appropriate for the proxy.</span></span> <span data-ttu-id="c4cd7-126">COM 會挑選可同時在用戶端和伺服器上運作的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-126">COM picks an authentication service that works on both the client and server.</span></span> <span data-ttu-id="c4cd7-127">系統會選擇授權服務和主體名稱來使用驗證服務。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-127">The authorization service and principal name are chosen to work with the authentication service.</span></span> <span data-ttu-id="c4cd7-128">針對驗證層級，COM 會選擇用戶端和伺服器所指定的驗證層級較高。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-128">For the authentication level, COM chooses the higher of the authentication levels specified by the client and the server.</span></span> <span data-ttu-id="c4cd7-129">模擬等級和 COM 所選擇的功能是用戶端所指定的功能。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-129">The impersonation level and the capabilities chosen by COM are the ones specified by the client.</span></span> <span data-ttu-id="c4cd7-130">驗證身分識別是用戶端為所選驗證服務指定的身分識別。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-130">The authentication identity is the one specified by the client for the chosen authentication service.</span></span>

<span data-ttu-id="c4cd7-131">一旦計算預設安全性的總值，就會將其值指派給新建立的 proxy。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-131">Once the default security blanket has been computed, its values are assigned to the newly created proxy.</span></span> <span data-ttu-id="c4cd7-132">用戶端可以藉由呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)來覆寫 proxy 的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-132">The client can override the security settings for the proxy by calling [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).</span></span> <span data-ttu-id="c4cd7-133">指定給 **SetBlanket** 的值不會進行協商;它們只會指派給指定的 proxy。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-133">The values specified to **SetBlanket** are not negotiated; they are simply assigned to the specified proxy.</span></span> <span data-ttu-id="c4cd7-134">但是，如果 (預設參數，例如 RPC \_ C \_ IMP \_ 層級 \_ 預設) 會傳遞給 **SetBlanket**，則 COM 會使用先前所述的安全性整體協商演算法來計算預設參數。</span><span class="sxs-lookup"><span data-stu-id="c4cd7-134">However, if default parameters (such as RPC\_C\_IMP\_LEVEL\_DEFAULT) are passed to **SetBlanket**, COM uses the previously described security blanket negotiation algorithm to compute the default parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4cd7-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4cd7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4cd7-136">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="c4cd7-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 