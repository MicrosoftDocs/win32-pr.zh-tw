---
description: 「掩蓋」是模擬的延伸模組，可讓您更有效地控制 COM 如何透過 proxy 模擬用戶端。 如同許多形式的 WMI 安全性，您可以透過 CoSetProxyBlanket 和 CoInitializeSecurity 介面設定掩蓋。
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: 實施掩蓋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193869"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="0edee-104">實施掩蓋</span><span class="sxs-lookup"><span data-stu-id="0edee-104">Implementing Cloaking</span></span>

<span data-ttu-id="0edee-105">「掩蓋」是模擬的延伸模組，可讓您更有效地控制 COM 如何透過 proxy 模擬用戶端。</span><span class="sxs-lookup"><span data-stu-id="0edee-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="0edee-106">如同許多形式的 WMI 安全性，您可以透過 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 介面設定掩蓋。</span><span class="sxs-lookup"><span data-stu-id="0edee-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="0edee-107">COM 提供下列形式的掩蓋：</span><span class="sxs-lookup"><span data-stu-id="0edee-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="0edee-108">Static</span><span class="sxs-lookup"><span data-stu-id="0edee-108">Static</span></span>

    <span data-ttu-id="0edee-109">在第一次呼叫 proxy 時，COM 會依據執行緒或進程 token 來建立權杖識別。</span><span class="sxs-lookup"><span data-stu-id="0edee-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="0edee-110">如果您對 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)使用靜態掩蓋，請在 proxy 的存留期間設定 proxy 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="0edee-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="0edee-111">動態</span><span class="sxs-lookup"><span data-stu-id="0edee-111">Dynamic</span></span>

    <span data-ttu-id="0edee-112">COM 會在每次呼叫 proxy 時，重新建立執行緒或進程 token 中的權杖身分識別。</span><span class="sxs-lookup"><span data-stu-id="0edee-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="0edee-113">由於 COM 會在每次呼叫時檢查身分識別，因此動態擬呼可讓您更精確地控制用戶端身分識別。</span><span class="sxs-lookup"><span data-stu-id="0edee-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="0edee-114">不過，動態掩蓋的效率不如靜態的掩蓋。</span><span class="sxs-lookup"><span data-stu-id="0edee-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="0edee-115">當您設定與模擬委派層級的掩蓋時，伺服器可以跨伺服器傳播用戶端的身分識別，即使是在遠端伺服器也一樣。</span><span class="sxs-lookup"><span data-stu-id="0edee-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="0edee-116">如果您未啟用掩蓋，COM 會在實際的伺服器進程的環境下，從本機伺服器到遠端伺服器的任何呼叫。</span><span class="sxs-lookup"><span data-stu-id="0edee-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="0edee-117">「掩蓋」可讓 WMI 模擬用戶端跨多個電腦界限存取本機和遠端網路資源。</span><span class="sxs-lookup"><span data-stu-id="0edee-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="0edee-118">WMI 可以將用戶端的身分識別傳遞給本機和遠端伺服器，例如 WMI 的其他遠端實例。</span><span class="sxs-lookup"><span data-stu-id="0edee-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="0edee-119">然後，這些遠端伺服器就可以在初始用戶端內容下執行作業。</span><span class="sxs-lookup"><span data-stu-id="0edee-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="0edee-120">下列程式說明如何搭配使用掩蓋和委派。</span><span class="sxs-lookup"><span data-stu-id="0edee-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="0edee-121">**搭配使用掩蓋和委派**</span><span class="sxs-lookup"><span data-stu-id="0edee-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="0edee-122">將驗證服務設定為 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="0edee-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="0edee-123">Kerberos 是唯一支援遠端掩蓋和委派的驗證服務。</span><span class="sxs-lookup"><span data-stu-id="0edee-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="0edee-124">這表示只有在遠端伺服器上才能使用「掩蔽」和「委派」。</span><span class="sxs-lookup"><span data-stu-id="0edee-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="0edee-125">在 Active Directory 服務中，將伺服器登入帳戶標示為「受信任的委派」。</span><span class="sxs-lookup"><span data-stu-id="0edee-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="0edee-126">在 Active Directory 服務中，將用戶端登入帳戶標示為「帳戶是機密的，無法委派」。</span><span class="sxs-lookup"><span data-stu-id="0edee-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="0edee-127">例如，呼叫 View 提供者可能會從多部電腦上的多個 WMI 實例傳回物件，可受益于委派和掩蓋。</span><span class="sxs-lookup"><span data-stu-id="0edee-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
