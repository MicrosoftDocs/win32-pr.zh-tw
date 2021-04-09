---
title: ADSI 與 ASP 的驗證問題
description: 根據內部網路的設定，從 ASP 頁面執行 ADSI 程式碼時可能會發生驗證問題。
ms.assetid: 287e2e19-7da9-497b-bf46-595ff4755261
ms.tgt_platform: multiple
keywords:
- ADSI、ASP pages、驗證問題
- ADSI、驗證、ASP 問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423d1aa39006f89ca366423da9d135e00af45693
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683083"
---
# <a name="authentication-issues-for-adsi-with-asp"></a><span data-ttu-id="3e531-105">ADSI 與 ASP 的驗證問題</span><span class="sxs-lookup"><span data-stu-id="3e531-105">Authentication Issues for ADSI with ASP</span></span>

<span data-ttu-id="3e531-106">根據內部網路的設定，從 ASP 頁面執行 ADSI 程式碼時可能會發生驗證問題。</span><span class="sxs-lookup"><span data-stu-id="3e531-106">Depending on the configuration of your intranet, authentication issues may occur when ADSI code is run from an ASP page.</span></span>

<span data-ttu-id="3e531-107">您可以使用委派來指定存取網域控制站的驗證。</span><span class="sxs-lookup"><span data-stu-id="3e531-107">Authentication to access the domain controller can be given using delegation.</span></span> <span data-ttu-id="3e531-108">委派允許服務以使用者身分運作，因此可以使用該使用者認證來存取網路資源。</span><span class="sxs-lookup"><span data-stu-id="3e531-108">Delegation permits a service to act as the user, so it can access a network resource using that user credentials.</span></span> <span data-ttu-id="3e531-109">如果您的內部網路採用此設定，您必須將 IIS 設定為使用委派。</span><span class="sxs-lookup"><span data-stu-id="3e531-109">If your intranet follows this configuration, you must set up IIS to use delegation.</span></span> <span data-ttu-id="3e531-110">將 IIS 驗證機制設定為 [匿名] 或 [NTLM]。</span><span class="sxs-lookup"><span data-stu-id="3e531-110">Set the IIS Authentication mechanism as Anonymous or NTLM.</span></span> <span data-ttu-id="3e531-111">如果您選擇 [匿名]，安全性內容將會對應到 [IUSR \_ 電腦帳戶]。</span><span class="sxs-lookup"><span data-stu-id="3e531-111">If you choose anonymous, your security context will be mapped to IUSR\_MACHINE account.</span></span> <span data-ttu-id="3e531-112">如果您選取 [NTLM]，安全性內容將會變更，視使用者登入您的網站而定。</span><span class="sxs-lookup"><span data-stu-id="3e531-112">If you select NTLM, the security context will change, depending on which user logs on to your website.</span></span> <span data-ttu-id="3e531-113">如需有關設定 IIS 伺服器以進行委派的詳細資訊和指示，請參閱 [Windows 2000 資源套件](https://support.microsoft.com/kb/927229)。</span><span class="sxs-lookup"><span data-stu-id="3e531-113">For more information and instructions for setting up the IIS server for delegation, see [Windows 2000 Resource Kit](https://support.microsoft.com/kb/927229).</span></span>

<span data-ttu-id="3e531-114">如果您使用的 IIS 伺服器使用 NT 挑戰/回應，或不支援 Kerberos 的瀏覽器用戶端，則不支援雙躍點驗證。</span><span class="sxs-lookup"><span data-stu-id="3e531-114">If you are using a an IIS server that uses the NT challenge/response, or a browser client that does not support Kerberos, then double-hop authentication is not supported.</span></span> <span data-ttu-id="3e531-115">雙躍點驗證表示使用者認證會從瀏覽器用戶端傳遞至 IIS 伺服器，然後 IIS 伺服器會將認證傳遞給後端伺服器。</span><span class="sxs-lookup"><span data-stu-id="3e531-115">Double-hop authentication means that the user credentials are passed from the browser client to the IIS server, and then the IIS server passes the credentials to the backend server.</span></span> <span data-ttu-id="3e531-116">在這種情況下，您可以使用下列其中一個解決方案，允許從 ASP 頁面存取目錄：</span><span class="sxs-lookup"><span data-stu-id="3e531-116">In this situation, you can use one of the following solutions to allow access to the directory from the ASP page:</span></span>

-   <span data-ttu-id="3e531-117">使用 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) 或 [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) 將認證傳遞至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="3e531-117">Use [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) or [**ADsOpenObject**](binding-with-adsopenobject-and-iadsopendsobject-opendsobject.md) to pass credentials to Active Directory.</span></span> <span data-ttu-id="3e531-118">網頁會向 IIS 伺服器驗證已連接的使用者。</span><span class="sxs-lookup"><span data-stu-id="3e531-118">The webpage authenticates the connected user against the IIS server.</span></span> <span data-ttu-id="3e531-119">當使用者經過驗證後，網頁可以使用 Objdso.opendsobject 或 ADsOpenObject 將使用者名稱和密碼傳遞至目錄服務，以取得後端伺服器的驗證。</span><span class="sxs-lookup"><span data-stu-id="3e531-119">When the user has been authenticated, the webpage can use OpenDSObject or ADsOpenObject to pass a user name and password to the directory service to obtain authentication to the backend server.</span></span> <span data-ttu-id="3e531-120">然後，網頁可以存取目錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="3e531-120">The webpage can then access data from the directory.</span></span>
-   <span data-ttu-id="3e531-121">將您的程式碼新增至 COM 物件，並將此物件放入 [Com + 應用程式](../cossdk/com--application-overview.md) 中， (先前稱為 MTS 封裝) 。</span><span class="sxs-lookup"><span data-stu-id="3e531-121">Add your code to a COM object and put this object into a [COM+ application](../cossdk/com--application-overview.md) (previously called an MTS package).</span></span> <span data-ttu-id="3e531-122">然後，COM + 應用程式可以做為 [網域使用者帳戶](/windows/desktop/AD/domain-user-accounts)來執行。</span><span class="sxs-lookup"><span data-stu-id="3e531-122">The COM+ application can then be run as a [domain user account](/windows/desktop/AD/domain-user-accounts).</span></span>
-   <span data-ttu-id="3e531-123">使用多個 ASP 頁面，其中一個頁面會驗證用戶端，而另一個頁面會在網域使用者帳戶上使用匿名驗證，將認證傳遞至目錄。</span><span class="sxs-lookup"><span data-stu-id="3e531-123">Use multiple ASP pages, where one page authenticates the client and another page passes credentials to the directory using anonymous authentication on a domain user account.</span></span>

<span data-ttu-id="3e531-124">這些方法牽涉到驗證網頁用戶端，然後在聯繫目錄時變更認證，因為使用相同認證的雙躍點驗證是不可能的。</span><span class="sxs-lookup"><span data-stu-id="3e531-124">These methods involve authenticating the web client and then changing the credentials when contacting the directory because double-hop authentication, with the same credentials, is not possible.</span></span>

 

 