---
title: 大量多人連線遊戲的安裝最佳做法
description: 本文說明如何為大量多人的線上遊戲建立一環信任設計， (MMOG) 用戶端安裝和自訂遊戲更新系統，以搭配 windows 和 windows Vista 和 Windows 7 的安全性模型運作。
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81003a434b830f046c29d606355104fe618d1f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023710"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a><span data-ttu-id="5388b-103">大量多人連線遊戲的安裝最佳做法</span><span class="sxs-lookup"><span data-stu-id="5388b-103">Installation Best Practices for Massively Multiplayer Online Games</span></span>

<span data-ttu-id="5388b-104">本文說明如何為大量多人的線上遊戲建立一環信任設計， (MMOG) 用戶端安裝和自訂遊戲更新系統，以搭配 windows 和 windows Vista 和 Windows 7 的安全性模型運作。</span><span class="sxs-lookup"><span data-stu-id="5388b-104">This article describes creating a chain of trust design for Massively Multiplayer Online Games (MMOG) client installation and custom game update systems that work well with Windows and the security model of Windows Vista and Windows 7.</span></span> <span data-ttu-id="5388b-105">此方法的設計目的是要在支援標準使用者帳戶（其對硬碟機和系統登錄的存取受到限制）時，啟用 MMOG 標題的修補。</span><span class="sxs-lookup"><span data-stu-id="5388b-105">The approach is designed to enable patching of MMOG titles while supporting standard user accounts, which have restricted access to the hard drive and system registry.</span></span>

-   [<span data-ttu-id="5388b-106">為什麼 MMOG 用戶端對傳統零售版遊戲有不同的需求</span><span class="sxs-lookup"><span data-stu-id="5388b-106">Why MMOG Clients Have Different Requirements to Traditional Retail Purchased Games</span></span>](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [<span data-ttu-id="5388b-107">一環信任方法的總覽</span><span class="sxs-lookup"><span data-stu-id="5388b-107">Overview of a Chain of Trust Approach</span></span>](#overview-of-a-chain-of-trust-approach)
-   [<span data-ttu-id="5388b-108">所有專案都會在伺服器上進行驗證，如果我的用戶端遭到駭客入侵，為什麼應該擔心？</span><span class="sxs-lookup"><span data-stu-id="5388b-108">Everything is validated on the server, why should I worry if my client gets hacked?</span></span>](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [<span data-ttu-id="5388b-109">Trust-Worthy 載入器應用程式的結構</span><span class="sxs-lookup"><span data-stu-id="5388b-109">Construction of the Trust-Worthy Loader Application</span></span>](#construction-of-the-trust-worthy-loader-application)
    -   [<span data-ttu-id="5388b-110">背景讀取</span><span class="sxs-lookup"><span data-stu-id="5388b-110">Background Reading</span></span>](#background-reading)
    -   [<span data-ttu-id="5388b-111">安裝受信任的載入器和 Patcher</span><span class="sxs-lookup"><span data-stu-id="5388b-111">Installation of the Trusted Loader and Patcher</span></span>](#installation-of-the-trusted-loader-and-patcher)
    -   [<span data-ttu-id="5388b-112">安裝遊戲可執行檔、Dll 和資料</span><span class="sxs-lookup"><span data-stu-id="5388b-112">Installation of the Game Executables, DLLs, and Data</span></span>](#installation-of-the-game-executables-dlls-and-data)
    -   [<span data-ttu-id="5388b-113">存取控制清單修改程式碼</span><span class="sxs-lookup"><span data-stu-id="5388b-113">Access Control List Modification Code</span></span>](#access-control-list-modification-code)
    -   [<span data-ttu-id="5388b-114">Advanced Users 的安裝</span><span class="sxs-lookup"><span data-stu-id="5388b-114">Installations for Advanced Users</span></span>](#installations-for-advanced-users)
    -   [<span data-ttu-id="5388b-115">載入器的信任驗證</span><span class="sxs-lookup"><span data-stu-id="5388b-115">The Loader's Verification of Trust</span></span>](#the-loaders-verification-of-trust)
    -   [<span data-ttu-id="5388b-116">資料驗證</span><span class="sxs-lookup"><span data-stu-id="5388b-116">Data Validation</span></span>](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a><span data-ttu-id="5388b-117">為什麼 MMOG 用戶端對傳統零售版遊戲有不同的需求</span><span class="sxs-lookup"><span data-stu-id="5388b-117">Why MMOG Clients Have Different Requirements to Traditional Retail Purchased Games</span></span>

<span data-ttu-id="5388b-118">Mmog 持續連線和演進的本質，讓它能夠提供用戶端程式代碼和內容的定期更新，以修正安全性弱點並擴充遊戲體驗。</span><span class="sxs-lookup"><span data-stu-id="5388b-118">The constantly connected and evolving nature of MMOGs makes it a fundamental requirement to provide regular updates of client code and content to fix security vulnerabilities and extend the gameplay experience.</span></span> <span data-ttu-id="5388b-119">有了幾乎每日更新的可能性，MMOG 案例需要謹慎的管理，以確保使用者易懂的體驗。</span><span class="sxs-lookup"><span data-stu-id="5388b-119">With the potential for almost daily updates, the MMOG scenario requires careful management to ensure a user friendly experience.</span></span> <span data-ttu-id="5388b-120">這與傳統零售購買模型不同，可能會在產品的零售出貨日期附近提供少量的修補程式。</span><span class="sxs-lookup"><span data-stu-id="5388b-120">This differs from the traditional retail purchase model where a small number of patches may be provided close to the retail ship date of the product.</span></span> <span data-ttu-id="5388b-121">作業系統提供的 Windows Installer 有限使用者修補技術的設計目的，是要處理少量的應用程式修補程式，而不是 Mmog 所需的大量和高頻率。</span><span class="sxs-lookup"><span data-stu-id="5388b-121">The Windows Installer limited user patching technology provided with the operating system is designed to handle small numbers of application patches, and not the large quantity and high frequency needed by MMOGs.</span></span> <span data-ttu-id="5388b-122">因此，通常需要開發自訂修補系統來解決 Mmog 的需求，包括所開發之特定 MMOG 特定的任何特殊需求。</span><span class="sxs-lookup"><span data-stu-id="5388b-122">It is therefore often necessary for custom patching systems to be developed to address the needs of MMOGs, including any special requirements specific to the particular MMOG being developed.</span></span>

<span data-ttu-id="5388b-123">因為許多電腦都連接到網際網路，所以 Windows Vista 和 Windows 7 對使用者有難上加難的安全性限制和保護，這會限制應用程式對硬碟的不同區域所擁有的存取權。</span><span class="sxs-lookup"><span data-stu-id="5388b-123">Because so many computers are connected to the Internet, Windows Vista and Windows 7 have tougher security restrictions and safeguards for users, which limit the access that applications have to various areas of the hard drive.</span></span> <span data-ttu-id="5388b-124">不同于 Windows XP，這些限制會針對使用者帳戶的預設模式啟用。</span><span class="sxs-lookup"><span data-stu-id="5388b-124">Unlike Windows XP, these restrictions are enabled for the default mode for user accounts.</span></span> <span data-ttu-id="5388b-125">設計遊戲的配置、可執行檔和資料，以及其相關聯的修補系統時，必須考慮這些限制。</span><span class="sxs-lookup"><span data-stu-id="5388b-125">These restrictions must be taken into account when designing the layout of a game, executable and data, and its associated patching system.</span></span> <span data-ttu-id="5388b-126">如需作業系統所提供之安全性措施的詳細資訊，請參閱 [遊戲開發人員的使用者帳戶控制](/windows/desktop/DxTechArts/user-account-control-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="5388b-126">For more details about the security measures provided by the operating system, see [User Account Control for Game Developers](/windows/desktop/DxTechArts/user-account-control-for-game-developers).</span></span>

## <a name="overview-of-a-chain-of-trust-approach"></a><span data-ttu-id="5388b-127">一環信任方法的總覽</span><span class="sxs-lookup"><span data-stu-id="5388b-127">Overview of a Chain of Trust Approach</span></span>

<span data-ttu-id="5388b-128">本白皮書中所提供的自訂更新方法，是以可信賴的載入器應用程式安裝到受保護的 Program Files 資料夾，同時將遊戲可執行檔和資料保留在共用的全部使用者存取區域中。</span><span class="sxs-lookup"><span data-stu-id="5388b-128">The custom update approach presented in this whitepaper is based upon having a trustworthy loader application installed to the protected Program Files folder while keeping the games executable files and data in a shared all-user-accessible area.</span></span> <span data-ttu-id="5388b-129">信任鏈從載入器開始，它會在啟動前執行遊戲二進位檔和資料的有效性檢查。</span><span class="sxs-lookup"><span data-stu-id="5388b-129">A chain of trust starts with the loader which performs validity checks on the game binaries and data before launch.</span></span>

![信任鏈從可信任的載入器開始](images/mmo-installation-best-practices-01.gif)

<span data-ttu-id="5388b-131">值得信賴的載入器必須有足夠的邏輯，才能確認遊戲的可執行檔和其他二進位檔在啟動遊戲之前都未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="5388b-131">The trustworthy loader needs to have enough logic to be able to verify that the game's executable and other binaries have not been tampered with before launching the game.</span></span> <span data-ttu-id="5388b-132">載入器也可以視需要驗證遊戲資料，不過，遊戲資料的大小通常太大，因此每次都能在單一行程中進行檢查。</span><span class="sxs-lookup"><span data-stu-id="5388b-132">The loader may also verify game data as often as needed, however, the size of game data is usually too large to allow it be checked every time in a single pass.</span></span> <span data-ttu-id="5388b-133">替代方法是使用取樣模式，以確保整個資料集的驗證會在一段長時間內進行。</span><span class="sxs-lookup"><span data-stu-id="5388b-133">An alternative approach is to use a sampling pattern which ensures that verification of the entire data set occurs over an extended period of time.</span></span> <span data-ttu-id="5388b-134">載入器應用程式可能包含一個遊戲修補引擎，它提供了信任的方法來整合更新與已安裝的遊戲。</span><span class="sxs-lookup"><span data-stu-id="5388b-134">The loader application may contain a game patching engine, which provides a trust worthy method by to integrate updates with the installed game.</span></span>

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a><span data-ttu-id="5388b-135">所有專案都會在伺服器上進行驗證，如果我的用戶端遭到駭客入侵，為什麼應該擔心？</span><span class="sxs-lookup"><span data-stu-id="5388b-135">Everything is validated on the server, why should I worry if my client gets hacked?</span></span>

<span data-ttu-id="5388b-136">不可能信任用戶端未遭到入侵;因此，MMOG 伺服器通常會驗證從用戶端接收的所有資料。</span><span class="sxs-lookup"><span data-stu-id="5388b-136">It is impossible to trust that the client has not been compromised; therefore it is common for MMOG servers to validate all data received from the client.</span></span> <span data-ttu-id="5388b-137">雖然此處理可以識別遊戲 universe 內遭入侵或作弊的遊戲用戶端，但是伺服器無法輕易地識別出遊戲用戶端可以公開的所有問題。</span><span class="sxs-lookup"><span data-stu-id="5388b-137">While this processing can identify compromised or cheating game clients within the game universe, the server cannot easily identify all issues the game client can be exposed to.</span></span> <span data-ttu-id="5388b-138">請務必強化保護，避免駭客想要使用您的用戶端做為您的服務、其他使用者的攻擊平臺，甚至只是做為攻擊用戶端機器本身的向量。</span><span class="sxs-lookup"><span data-stu-id="5388b-138">It's important to strengthen protection from hackers who wish to use your client as a platform for attacks on your service, other users, or even simply as a vector for attacking the client machines themselves.</span></span> <span data-ttu-id="5388b-139">程式碼簽署和資料驗證技術的應用在執行之前，可以協助偵測遭入侵的用戶端。</span><span class="sxs-lookup"><span data-stu-id="5388b-139">The application of code signing and data verification techniques can help detect compromised clients before they get executed.</span></span> <span data-ttu-id="5388b-140">由於修補機制需要公開不受程式檔標準唯讀許可權保護的可執行檔和 DLL 二進位檔，因此在啟動之前先驗證這些檔案，對整體系統安全性很重要。</span><span class="sxs-lookup"><span data-stu-id="5388b-140">Since the patching mechanism requires exposing executable and DLL binaries that are not protected by the standard read-only permissions on Program Files, validating these files before launching them is important for overall system security.</span></span>

<span data-ttu-id="5388b-141">此模型並不會嘗試處理可能會遭到入侵的惡意管理員使用者案例，而是將焦點放在保護標準使用者不小心執行遭篡改的程式碼。</span><span class="sxs-lookup"><span data-stu-id="5388b-141">This model does not attempt to deal with the malicious admin user scenario where the loader itself could become compromised but focuses on protecting standard users from accidentally running tampered code.</span></span> <span data-ttu-id="5388b-142">傳統的伺服器用戶端驗證技術其實是惡意用戶端系統管理員的唯一可能緩和措施。</span><span class="sxs-lookup"><span data-stu-id="5388b-142">Traditional server-client validation techniques are really the only possible mitigation for malicious client system administrators.</span></span>

## <a name="construction-of-the-trust-worthy-loader-application"></a><span data-ttu-id="5388b-143">Trust-Worthy 載入器應用程式的結構</span><span class="sxs-lookup"><span data-stu-id="5388b-143">Construction of the Trust-Worthy Loader Application</span></span>

### <a name="background-reading"></a><span data-ttu-id="5388b-144">背景讀取</span><span class="sxs-lookup"><span data-stu-id="5388b-144">Background Reading</span></span>

<span data-ttu-id="5388b-145">讀者應該熟悉下列檔，其中提供基礎技術的詳細資料，以確保軟體型信任的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="5388b-145">Readers should familiarize themselves with the following documentation, which provides details of the foundation technology for ensuring best practice for software based trust.</span></span>

<dl> <dt>

<span data-ttu-id="5388b-146"><span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>程式碼簽署</span><span class="sxs-lookup"><span data-stu-id="5388b-146"><span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Code Signing</span></span>
</dt> <dd>

[<span data-ttu-id="5388b-147">遊戲開發人員的 Authenticode 簽署</span><span class="sxs-lookup"><span data-stu-id="5388b-147">Authenticode Signing for Game Developers</span></span>](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span data-ttu-id="5388b-148"><span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool</span><span class="sxs-lookup"><span data-stu-id="5388b-148"><span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool</span></span>
</dt> <dd>

<span data-ttu-id="5388b-149">MSDN 上的[SignTool](/windows/desktop/SecCrypto/signtool)</span><span class="sxs-lookup"><span data-stu-id="5388b-149">[SignTool](/windows/desktop/SecCrypto/signtool) on MSDN</span></span>

</dd> </dl>

<span data-ttu-id="5388b-150">下一節將詳細說明用來建立載入器應用程式的 Api，其支援安裝和驗證信任檢查的光碟版面配置。</span><span class="sxs-lookup"><span data-stu-id="5388b-150">The following section details the APIs that should be used to construct the loader application, which support disc layout for install and verification of trust checking.</span></span>

### <a name="installation-of-the-trusted-loader-and-patcher"></a><span data-ttu-id="5388b-151">安裝受信任的載入器和 Patcher</span><span class="sxs-lookup"><span data-stu-id="5388b-151">Installation of the Trusted Loader and Patcher</span></span>

<span data-ttu-id="5388b-152">受信任的載入器和 patcher 公用程式的基底版本應該安裝在 HDD 上的 [受保護的程式檔案] 資料夾底下，就像傳統安裝一樣。</span><span class="sxs-lookup"><span data-stu-id="5388b-152">The trusted loader and base version of the patcher utility should be installed under the protected Program Files folder on the HDD just as in traditional installs.</span></span> <span data-ttu-id="5388b-153">安裝和修補載入器應用程式需要系統管理員許可權，因此請務必將載入器的更新頻率降到最低，以確保使用者不需要經常提高許可權，但 Windows Installer 限制的使用者修補可用來避免提高載入器修補程式的許可權。</span><span class="sxs-lookup"><span data-stu-id="5388b-153">Installation and patching of the loader application requires Admin rights so it is important to minimize the frequency of update for the loader to ensure end users do not need to elevate often, although Windows Installer limited user patching could be used to avoid elevation for loader patches.</span></span>

<span data-ttu-id="5388b-154">請參閱文章修補 Windows XP、Windows Vista 和 Windows 7 中的遊戲軟體。</span><span class="sxs-lookup"><span data-stu-id="5388b-154">See the article Patching Game Software in Windows XP, Windows Vista, and Windows 7.</span></span>

### <a name="installation-of-the-game-executables-dlls-and-data"></a><span data-ttu-id="5388b-155">安裝遊戲可執行檔、Dll 和資料</span><span class="sxs-lookup"><span data-stu-id="5388b-155">Installation of the Game Executables, DLLs, and Data</span></span>

<span data-ttu-id="5388b-156">若要在沒有系統管理許可權的情況下，協助標準使用者更新遊戲，必須將遊戲可執行檔、Dll 和資料安裝到可供所有使用者存取的硬碟區域。</span><span class="sxs-lookup"><span data-stu-id="5388b-156">In order to facilitate Standard User updates of the game without administrative privilege, the games executable, DLLs, and data must be installed to an area of the hard disk that is write accessible for all users.</span></span> <span data-ttu-id="5388b-157">作業系統提供「所有使用者應用程式資料」區域，可用來做為安裝的預設位置。</span><span class="sxs-lookup"><span data-stu-id="5388b-157">The operating system provides an "All Users Application Data" area which can be used as the default location for installation.</span></span> <span data-ttu-id="5388b-158">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 應該搭配 CSIDL \_ 一般 \_ APPDATA 索引鍵使用，以決定此區域的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5388b-158">[**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) should be used with the CSIDL\_COMMON\_APPDATA key to determine the file path for this area.</span></span> <span data-ttu-id="5388b-159">請勿對此金鑰傳回的路徑進行任何假設，因為它可能是使用者可設定的。</span><span class="sxs-lookup"><span data-stu-id="5388b-159">It is important that no assumptions be made about the path to which this key returns as it may be user configurable.</span></span>

<span data-ttu-id="5388b-160">安裝必須改變或管理資料夾許可權，才能達到更新標題所需的所有使用者共用寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="5388b-160">The installation needs to alter or manage the folder permissions in order to achieve the all-user-shared-write access needed for updating the title.</span></span> <span data-ttu-id="5388b-161">使用正確的許可權，載入器程式的遊戲更新程式功能可以輕鬆地修補遊戲，而不需要任何使用者帳戶的特殊許可權，包括標準使用者啟動時的時間。</span><span class="sxs-lookup"><span data-stu-id="5388b-161">With the correct permissions, the game updater functionality of the loader program can easily patch the game without the need for special privilege from any users account including times when launched by standard users.</span></span>

### <a name="access-control-list-modification-code"></a><span data-ttu-id="5388b-162">存取控制清單修改程式碼</span><span class="sxs-lookup"><span data-stu-id="5388b-162">Access Control List Modification Code</span></span>

<span data-ttu-id="5388b-163">若為 Windows XP，您將需要執行程式碼，以手動方式變更 (ACL) 的存取控制清單，以下是示範如何執行這項作業的範例函式：</span><span class="sxs-lookup"><span data-stu-id="5388b-163">For Windows XP, you will need to execute code to change the access control list (ACL) manually, here is an example function that demonstrates how to do this:</span></span>

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

<span data-ttu-id="5388b-164">這個程式碼範例也適用于 Windows Vista 和 Windows 7;不過，它們也會提供命令列公用程式 icacls，以編輯您可以選擇改用的檔案 ACL。</span><span class="sxs-lookup"><span data-stu-id="5388b-164">This code example will also work for Windows Vista and Windows 7; however, they also provide the command line utility icacls to edit file ACLS which you may choose to use instead.</span></span>

<span data-ttu-id="5388b-165">不過，此工具會在執行時提供詳細的說明，此工具的其中一個範例使用方式為：</span><span class="sxs-lookup"><span data-stu-id="5388b-165">The tool provides a detailed help when executed however, one example usage for the tool is:</span></span>

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

<span data-ttu-id="5388b-166">此使用方式會授與使用者 >rex 刪除和寫入 DAC 許可權至硬碟的所有使用者區域中所儲存的遊戲資料夾。</span><span class="sxs-lookup"><span data-stu-id="5388b-166">This usage will grant the user Rex Delete and Write DAC permissions to game folder stored in the All Users areas of the hard drive.</span></span>

### <a name="installations-for-advanced-users"></a><span data-ttu-id="5388b-167">Advanced Users 的安裝</span><span class="sxs-lookup"><span data-stu-id="5388b-167">Installations for Advanced Users</span></span>

<span data-ttu-id="5388b-168">針對先進的使用者安裝案例，使用者可能會想要手動指定遊戲安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="5388b-168">For advanced user installation scenarios, a user may want to specify the games installation path manually.</span></span> <span data-ttu-id="5388b-169">目錄選取範圍應限制為程式檔之外的一個，以確保該資料夾位於硬碟的真正可共用區域中。</span><span class="sxs-lookup"><span data-stu-id="5388b-169">The directory selection should be restricted to one outside of program files to ensure the folder is in a truly sharable area of the hard drive.</span></span> <span data-ttu-id="5388b-170">使用者選取的路徑應僅用於遊戲 exe 和資料，因為遊戲載入器和 Patcher exe 應該一律安裝在 [安全程式檔案] 資料夾下，以提升安全性。</span><span class="sxs-lookup"><span data-stu-id="5388b-170">The user selected path should only be used for the games exes and data as the game Loader and Patcher exes should always be installed under the secure Program Files folder for better security.</span></span>

### <a name="the-loaders-verification-of-trust"></a><span data-ttu-id="5388b-171">載入器的信任驗證</span><span class="sxs-lookup"><span data-stu-id="5388b-171">The Loader's Verification of Trust</span></span>

<span data-ttu-id="5388b-172">Windows 提供 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) 功能來檢查已簽署程式碼的有效性，並以作業系統中的密碼編譯服務為基礎。</span><span class="sxs-lookup"><span data-stu-id="5388b-172">Windows provides the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function for checking the validity of signed code and is based on the cryptographic services in the operating system.</span></span> <span data-ttu-id="5388b-173">此函式完整記載于 MSDN： **WinVerifyTrust** 函數。</span><span class="sxs-lookup"><span data-stu-id="5388b-173">The function is fully documented on MSDN: **WinVerifyTrust** Function.</span></span>

<span data-ttu-id="5388b-174">下列 MSDN 上的範例程式詳細說明如何使用函式來判斷程式可執行檔是否使用有效的憑證簽署： [範例 C 程式：驗證 PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)檔案的簽章。</span><span class="sxs-lookup"><span data-stu-id="5388b-174">The following example program on MSDN details the use of the function to determine whether a program executable is signed with a valid certificate: [Example C Program: Verifying the Signature of a PE File](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).</span></span>

<span data-ttu-id="5388b-175">為了確認已簽署的遊戲可執行檔可在載入器內執行，一般驗證動作將足夠：</span><span class="sxs-lookup"><span data-stu-id="5388b-175">For the purposes of verifying that the signed game executable is trustworthy to be executed from within the loader, the Generic Verify action will suffice:</span></span>

<dl> <dt>

<span data-ttu-id="5388b-176"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值</span><span class="sxs-lookup"><span data-stu-id="5388b-176"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="5388b-177">WINTRUST \_ 動作 \_ 一般 \_ 驗證 \_ V2</span><span class="sxs-lookup"><span data-stu-id="5388b-177">WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2</span></span>

</dd> <dt>

<span data-ttu-id="5388b-178"><span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>意義</span><span class="sxs-lookup"><span data-stu-id="5388b-178"><span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Meaning</span></span>
</dt> <dd>

<span data-ttu-id="5388b-179">使用 Authenticode 原則提供者驗證檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="5388b-179">Verify a file or object using the Authenticode policy provider.</span></span>

</dd> </dl>

<span data-ttu-id="5388b-180">函數會採用輸入結構引數，其中包含信任提供者處理指定動作所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="5388b-180">The function takes an input structure argument which contains information that the trust provider needs to process the specified action.</span></span> <span data-ttu-id="5388b-181">一般來說，如上述範例所示，結構所包含的資訊會識別信任提供者必須評估的物件。</span><span class="sxs-lookup"><span data-stu-id="5388b-181">Typically, as in the preceding example case, the structure includes information that identifies the object that the trust provider must evaluate.</span></span>

<span data-ttu-id="5388b-182">結構的格式是特定于動作識別碼。</span><span class="sxs-lookup"><span data-stu-id="5388b-182">The format of the structure is specific to the action identifier.</span></span> <span data-ttu-id="5388b-183">MSDN 上的下列主題詳細說明 WinTrust 提供者的範例結構： [**WinTrust \_ 資料**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) 結構。</span><span class="sxs-lookup"><span data-stu-id="5388b-183">The following topic on MSDN details the example structure for the WinTrust provider: [**WINTRUST\_DATA**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) Structure.</span></span>

<span data-ttu-id="5388b-184">如果信任提供者確認主體受限於指定的動作，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="5388b-184">If the trust provider verifies that the subject is trusted for the specified action, the return value is zero.</span></span> <span data-ttu-id="5388b-185">除了零以外的其他值都不應視為成功的傳回值。</span><span class="sxs-lookup"><span data-stu-id="5388b-185">No other value besides zero should be considered a successful return.</span></span>

### <a name="data-validation"></a><span data-ttu-id="5388b-186">資料驗證</span><span class="sxs-lookup"><span data-stu-id="5388b-186">Data Validation</span></span>

<span data-ttu-id="5388b-187">Codesigning 機制只支援簽署一些特定類型的檔案，包括可執行檔、Dll、Windows Installer 套件 ( .msi 檔案) 以及封包 ( .cab) 檔。</span><span class="sxs-lookup"><span data-stu-id="5388b-187">The codesigning mechanism only supports signing a few specific types of files, including executables, DLLs, Windows Installer packages (.msi files), and cabinet (.cab) files.</span></span> <span data-ttu-id="5388b-188">[**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) API 不應用來確認大型資料檔案 ( .cab 檔（例如) 尚未遭篡改），因為在驗證非常大型的檔案時，有一些效能和穩定性問題。</span><span class="sxs-lookup"><span data-stu-id="5388b-188">The [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) API should not be used to verify that large data files (.cab files for example) have not been tampered with, as there are some issues with performance and stability when validating very large files.</span></span> <span data-ttu-id="5388b-189">程式可執行檔通常很小，可使用 WinTrust 提供者進行完全信任檢查，但是遊戲的資料檔案通常是大小的 gb 範圍。</span><span class="sxs-lookup"><span data-stu-id="5388b-189">Program executables tend be small enough for a full trust check to occur using the WinTrust provider but data files for games are often of the realm of many gigabytes in size.</span></span> <span data-ttu-id="5388b-190">載入器用來驗證遊戲資料的方法，應該是在遊戲的執行時間測試資料集的小型樣本。</span><span class="sxs-lookup"><span data-stu-id="5388b-190">The approach taken by the loader for verification of game data should be one where a small sample of the dataset is tested over the run time of the game.</span></span> <span data-ttu-id="5388b-191">這種方法可將驗證測試的成本散佈在遊戲播放體驗的存留期內，並可提供順暢的使用者體驗，而不需要長時間等候。</span><span class="sxs-lookup"><span data-stu-id="5388b-191">This approach spreads the cost of verification tests over the life of the game play experience and can provide a seamless user experience without long wait times.</span></span> <span data-ttu-id="5388b-192">為了達成此目的，您可能需要謹慎地組織資料。</span><span class="sxs-lookup"><span data-stu-id="5388b-192">To achieve this, careful organization of the data may be required.</span></span> <span data-ttu-id="5388b-193">有些 Mmog 採用資料庫方法來協助管理、維護及驗證一段時間的遊戲資產是否正確。</span><span class="sxs-lookup"><span data-stu-id="5388b-193">Some MMOGs employ a database approach to help manage, maintain and verify correctness of game assets over time.</span></span>

<span data-ttu-id="5388b-194">從安全性的觀點來看，用戶端程式代碼應該設計為不信任資料檔案，即使使用某種類型的基本資料驗證與受信任的載入器也一樣。</span><span class="sxs-lookup"><span data-stu-id="5388b-194">From a security standpoint, the client code should be designed to not trust data files even if using some kind of basic data validation with the trusted loader.</span></span> <span data-ttu-id="5388b-195">應該採用標頭檢查、雜湊和其他傳統的完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="5388b-195">Header checks, hashes, and other traditional integrity checking should be employed.</span></span> <span data-ttu-id="5388b-196">強化用戶端 i/o 程式碼的工作也應該使用模糊測試之類的技術來完成，以及利用自動靜態程式碼分析工具（例如 Visual Studio 2005 中的 **/analyze** 參數），以及 Windows SDK) 隨附的免費編譯器中的 Visual Studio 2008 Visual Studio (。</span><span class="sxs-lookup"><span data-stu-id="5388b-196">Work to hardened the client's I/O code should also be done using techniques such as fuzz testing as well as taking advantage of automatic static code analysis tools such as the **/analyze** switch in Visual Studio 2005 and Visual Studio 2008 (available in Visual Studio Team System and the free compiler that ships with the Windows SDK).</span></span>

<span data-ttu-id="5388b-197">如需軟體安全性的詳細資訊，請參閱 [遊戲開發的最佳安全性作法](/windows/desktop/DxTechArts/best-security-practices-in-game-development)。</span><span class="sxs-lookup"><span data-stu-id="5388b-197">For more information about software security, see [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).</span></span>

 

 