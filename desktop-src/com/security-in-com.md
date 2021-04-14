---
title: COM 中的安全性
description: COM 中的安全性是根據 Windows 所提供的安全性以及基礎 RPC 安全性機制而穩定的。
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382985"
---
# <a name="security-in-com"></a><span data-ttu-id="d83c7-103">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-103">Security in COM</span></span>

<span data-ttu-id="d83c7-104">COM 中的安全性是根據 Windows 所提供的安全性以及基礎 RPC 安全性機制而穩定的。</span><span class="sxs-lookup"><span data-stu-id="d83c7-104">Security in COM is firmly based on the security provided by Windows and the underlying RPC security mechanisms.</span></span> <span data-ttu-id="d83c7-105">COM 安全性依賴 *驗證* (驗證呼叫者的身分識別) 和 *授權* 的程式 (判斷呼叫端是否已獲授權可進行要求) 的處理常式。</span><span class="sxs-lookup"><span data-stu-id="d83c7-105">COM security relies on *authentication* (the process of verifying a caller's identity) and *authorization* (the process of determining whether a caller is authorized to do what it is asking to do).</span></span> <span data-ttu-id="d83c7-106">COM 中有兩種主要的安全性類型： *啟用安全性* 和 *呼叫安全性*。</span><span class="sxs-lookup"><span data-stu-id="d83c7-106">There are two main types of security in COM: *activation security* and *call security*.</span></span> <span data-ttu-id="d83c7-107">啟用安全性可判斷用戶端是否可以啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="d83c7-107">Activation security determines whether a client can launch a server at all.</span></span> <span data-ttu-id="d83c7-108">啟動伺服器之後，您可以使用 [呼叫安全性] 來控制伺服器物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="d83c7-108">After a server has been launched, you can use call security to control access to a server's objects.</span></span>

<span data-ttu-id="d83c7-109">在此安全性模型中，伺服器會管理和協助保護物件、用戶端透過伺服器取得物件的存取權，而且伺服器可以在模擬用戶端時嘗試存取。</span><span class="sxs-lookup"><span data-stu-id="d83c7-109">In this security model, servers manage and help protect objects, clients get access to objects through servers, and servers can attempt access while impersonating the client.</span></span>

<span data-ttu-id="d83c7-110">系統會執行 Kerberos v5 驗證通訊協定和 Schannel 安全性封裝。</span><span class="sxs-lookup"><span data-stu-id="d83c7-110">The system implements the Kerberos v5 authentication protocol and the Schannel security package.</span></span> <span data-ttu-id="d83c7-111">它也包含委派層級模擬、相互驗證、在登錄中設定 AppID 的驗證層級，以及進行掩蓋等功能。</span><span class="sxs-lookup"><span data-stu-id="d83c7-111">It also includes features such as delegate-level impersonation, mutual authentication, the ability to set authentication levels for an AppID in the registry, and cloaking.</span></span> <span data-ttu-id="d83c7-112">使用 COM 安全性，您可以在不危及安全性的情況下，執行可執行特殊許可權作業的物件。</span><span class="sxs-lookup"><span data-stu-id="d83c7-112">Using COM security, you can implement objects that can perform privileged operations without compromising security.</span></span>

<span data-ttu-id="d83c7-113">因為有各式各樣的 COM 安全性功能，所以一開始就有助於判斷您的應用程式所需的安全性類型。</span><span class="sxs-lookup"><span data-stu-id="d83c7-113">Because there is a wide range of COM security features available, it is helpful to initially determine what kind of security your application needs.</span></span> <span data-ttu-id="d83c7-114">對於大部分的應用程式而言，設定可接受的安全性層級可能是一個簡單的程式，不過您也可以使用 COM 安全性來支援非常複雜的安全性案例。</span><span class="sxs-lookup"><span data-stu-id="d83c7-114">For most applications, setting an acceptable level of security can be a painless process, but you can also use COM security to support very complex security scenarios.</span></span>

<span data-ttu-id="d83c7-115">您可以設定安全性 processwide，方法是使用 Dcomcnfg.exe 設定登錄或呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。</span><span class="sxs-lookup"><span data-stu-id="d83c7-115">You can set security processwide, either by using Dcomcnfg.exe to set the registry or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="d83c7-116">有兩個主要介面、 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 和 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (以及相關聯的 helper 函式) ，可讓您在程式內設定呼叫層級安全性。</span><span class="sxs-lookup"><span data-stu-id="d83c7-116">Two primary interfaces, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (and associated helper functions), allow you to set call-level security within your program.</span></span>

<span data-ttu-id="d83c7-117">若要深入瞭解 COM 安全性，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="d83c7-117">To learn more about COM security, see the following topics:</span></span>

-   [<span data-ttu-id="d83c7-118">判斷您的安全性需求</span><span class="sxs-lookup"><span data-stu-id="d83c7-118">Determining Your Security Needs</span></span>](determining-your-security-needs.md)
-   [<span data-ttu-id="d83c7-119">COM 安全性預設值</span><span class="sxs-lookup"><span data-stu-id="d83c7-119">COM Security Defaults</span></span>](com-security-defaults.md)
-   [<span data-ttu-id="d83c7-120">啟用安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-120">Activation Security</span></span>](activation-security.md)
-   [<span data-ttu-id="d83c7-121">安全性值</span><span class="sxs-lookup"><span data-stu-id="d83c7-121">Security Values</span></span>](security-values.md)
-   [<span data-ttu-id="d83c7-122">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
-   [<span data-ttu-id="d83c7-123">使用 DCOMCNFG 啟用 COM 安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-123">Enabling COM Security Using DCOMCNFG</span></span>](enabling-com-security-using-dcomcnfg.md)
-   [<span data-ttu-id="d83c7-124">關閉安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-124">Turning Off Security</span></span>](turning-off-security.md)
-   [<span data-ttu-id="d83c7-125">伺服器端安全性</span><span class="sxs-lookup"><span data-stu-id="d83c7-125">Server-Side Security</span></span>](server-side-security.md)
-   [<span data-ttu-id="d83c7-126">安全性的總協商</span><span class="sxs-lookup"><span data-stu-id="d83c7-126">Security Blanket Negotiation</span></span>](security-blanket-negotiation.md)
-   [<span data-ttu-id="d83c7-127">COM 和安全性封裝</span><span class="sxs-lookup"><span data-stu-id="d83c7-127">COM and Security Packages</span></span>](com-and-security-packages.md)
-   [<span data-ttu-id="d83c7-128">Windows XP Service Pack 2 和 Windows Server 2003 Service Pack 1 中的 DCOM 安全性增強功能</span><span class="sxs-lookup"><span data-stu-id="d83c7-128">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [<span data-ttu-id="d83c7-129">COM 的存取控制清單</span><span class="sxs-lookup"><span data-stu-id="d83c7-129">Access Control Lists for COM</span></span>](access-control-lists-for-com.md)
-   [<span data-ttu-id="d83c7-130">COM 提高許可權的標記</span><span class="sxs-lookup"><span data-stu-id="d83c7-130">The COM Elevation Moniker</span></span>](the-com-elevation-moniker.md)

 

 