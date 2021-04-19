---
description: 所有驗證設定都是透過網際網路服務管理員進行。
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: 針對 WMI ASP 腳本設定 IIS 5.0 和更新版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992023"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="63e29-103">針對 WMI ASP 腳本設定 IIS 5.0 和更新版本</span><span class="sxs-lookup"><span data-stu-id="63e29-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="63e29-104">所有驗證設定都是透過網際網路服務管理員進行。</span><span class="sxs-lookup"><span data-stu-id="63e29-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="63e29-105">設定 Internet Information Server 時 (IIS) 5.0 和 IIS 6.0 security （適用于 WMI ASP 腳本），請考慮下列問題：</span><span class="sxs-lookup"><span data-stu-id="63e29-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="63e29-106">驗證等級</span><span class="sxs-lookup"><span data-stu-id="63e29-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="63e29-107">您可以在伺服器、目錄或檔案層級進行設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="63e29-108">驗證設定</span><span class="sxs-lookup"><span data-stu-id="63e29-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="63e29-109">您可以將驗證設定為匿名、整合式 Windows 或兩者。</span><span class="sxs-lookup"><span data-stu-id="63e29-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="63e29-110">保護</span><span class="sxs-lookup"><span data-stu-id="63e29-110">Protection</span></span>](#protection)

    <span data-ttu-id="63e29-111">您可以將 ASP 設定為以同進程方式執行 (低保護) ，或使用 Dllhost.exe (中或高保護) 來執行跨進程。</span><span class="sxs-lookup"><span data-stu-id="63e29-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="63e29-112">驗證等級</span><span class="sxs-lookup"><span data-stu-id="63e29-112">Authentication Level</span></span>

<span data-ttu-id="63e29-113">為了增加安全性，您可以在目錄或檔案層級設定驗證。</span><span class="sxs-lookup"><span data-stu-id="63e29-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="63e29-114">如果驗證是在伺服器層級設定，除非在目錄或檔案層級明確改變，否則所有後續的目錄和檔案都會遵守伺服器驗證。</span><span class="sxs-lookup"><span data-stu-id="63e29-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="63e29-115">您可以建立一個目錄結構，以包含 wmi ASP 腳本，其中 WMI 專用的 HTML 網頁和 Asp 可以與伺服器的其餘部分分開設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="63e29-116">執行下列程式，以變更伺服器、目錄或檔案的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="63e29-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="63e29-117">**設定任何層級的驗證**</span><span class="sxs-lookup"><span data-stu-id="63e29-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="63e29-118">在主控台中，按兩下 [系統 **管理工具**]，然後按兩下 [IIS] 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="63e29-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="63e29-119">找出 ASP 頁面圖示，然後開啟要設定之層級的屬性，可以是 [伺服器]、[目錄] 或 [檔案]。</span><span class="sxs-lookup"><span data-stu-id="63e29-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="63e29-120">驗證設定 **位於 [內容] 工作表的**[**目錄安全性**] 或 [檔案 **安全性**] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="63e29-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="63e29-121">驗證設定</span><span class="sxs-lookup"><span data-stu-id="63e29-121">Authentication Setting</span></span>

<span data-ttu-id="63e29-122">若為 WMI ASP 腳本，則會關閉 [匿名驗證] 的組合 (未核取的) ，並開啟 (檢查) 的整合 Windows 驗證，可提供更高的安全性設定機會。</span><span class="sxs-lookup"><span data-stu-id="63e29-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="63e29-123">若要使用 NT LAN Manager (NTLM) 、Passport 或 Digest IIS 驗證設定，您必須開啟遠端啟用許可權，因為系統會將使用者視為網路身分識別，並從遠端登入。</span><span class="sxs-lookup"><span data-stu-id="63e29-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="63e29-124">匿名和基本驗證不需要遠端啟用設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="63e29-125">但是，當您使用匿名和基本驗證時，系統會比較不安全。</span><span class="sxs-lookup"><span data-stu-id="63e29-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="63e29-126">如果匿名驗證搭配使用或未整合 Windows 驗證，最安全的方法是使用需要使用者輸入使用者名稱和密碼的登入。</span><span class="sxs-lookup"><span data-stu-id="63e29-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="63e29-127">預設登入是 IIS 身分識別，但您可以使用適用于 WMI ASP 腳本的特定許可權來建立登入，這些腳本可作為匿名或來賓連接的帳戶使用。</span><span class="sxs-lookup"><span data-stu-id="63e29-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="63e29-128">如果您選擇不是 IIS 身分識別的登入識別碼，請清除 [ **允許 IIS 控制密碼** ] 核取方塊，然後輸入正確的密碼。</span><span class="sxs-lookup"><span data-stu-id="63e29-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="63e29-129">這會強制所有匿名或來賓連接使用登入識別碼。</span><span class="sxs-lookup"><span data-stu-id="63e29-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="63e29-130">藉由建立與 IIS 身分識別分開的登入，就可以控制存取 WMI 的帳戶許可權，而不會影響 IIS 伺服器上的其他目錄或檔案，除非驗證是在伺服器層級設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="63e29-131">執行下列程式，使用主控台中的 IIS 嵌入式管理單元來設定 ASP 頁面的驗證需求。</span><span class="sxs-lookup"><span data-stu-id="63e29-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="63e29-132">**若要取得帳戶設定**</span><span class="sxs-lookup"><span data-stu-id="63e29-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="63e29-133">在主控台中，按兩下 [系統 **管理工具** ] 圖示、開啟 IIS 嵌入式管理單元、找出 ASP 頁面，然後開啟要設定之層級的屬性，可以是 [伺服器]、[目錄] 或 [檔案]。</span><span class="sxs-lookup"><span data-stu-id="63e29-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="63e29-134">您可以在 [內容]**工作表的**[**目錄安全性**] 或 [檔案 **安全性**] 索引標籤上找到驗證設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="63e29-135">在 [匿名驗證] 區域中，按一下 [ **編輯**]。</span><span class="sxs-lookup"><span data-stu-id="63e29-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="63e29-136">如果已選取 [IIS 身分識別] 以外的登入識別碼，請清除 [ **允許 IIS 控制密碼**] 核取方塊，然後輸入正確的密碼。</span><span class="sxs-lookup"><span data-stu-id="63e29-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="63e29-137">這會強制所有匿名或來賓連接使用登入識別碼。</span><span class="sxs-lookup"><span data-stu-id="63e29-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="63e29-138">使用與 IIS 身分識別不同的登入，就可以控制存取 WMI 的帳戶許可權，而不會影響 IIS 伺服器上的其他目錄或檔案，除非驗證是在伺服器層級設定。</span><span class="sxs-lookup"><span data-stu-id="63e29-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="63e29-139">先前的設定可讓 IIS 伺服器在某些區域中使用匿名驗證，以及在其他區域中使用整合式 Windows 或混合式驗證。</span><span class="sxs-lookup"><span data-stu-id="63e29-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="63e29-140">保護</span><span class="sxs-lookup"><span data-stu-id="63e29-140">Protection</span></span>

<span data-ttu-id="63e29-141">設定 IIS 伺服器時的最後一個考慮是執行 ASP 時要使用的保護。</span><span class="sxs-lookup"><span data-stu-id="63e29-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="63e29-142">您可以設定 ASP 來執行下列程式：</span><span class="sxs-lookup"><span data-stu-id="63e29-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="63e29-143">IIS 的同進程 (低保護) 。</span><span class="sxs-lookup"><span data-stu-id="63e29-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="63e29-144">以 Dllhost.exe 為集區或跨進程的 IIS 外部， (集區中保護) 。</span><span class="sxs-lookup"><span data-stu-id="63e29-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="63e29-145">跨進程自我裝載 (高保護) 。</span><span class="sxs-lookup"><span data-stu-id="63e29-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="63e29-146">為了獲得最佳的安全性和效能平衡，請使用集區主機。</span><span class="sxs-lookup"><span data-stu-id="63e29-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



