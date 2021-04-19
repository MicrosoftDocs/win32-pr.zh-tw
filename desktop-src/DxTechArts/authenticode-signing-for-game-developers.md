---
title: 遊戲開發人員的 Authenticode 簽署
description: 本文討論如何開始驗證您的遊戲，以及如何將驗證整合到每日組建流程。
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f304e6cc8e185264699709987f62dfdca17bf8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967274"
---
# <a name="authenticode-signing-for-game-developers"></a><span data-ttu-id="801d3-103">遊戲開發人員的 Authenticode 簽署</span><span class="sxs-lookup"><span data-stu-id="801d3-103">Authenticode Signing for Game Developers</span></span>

<span data-ttu-id="801d3-104">對遊戲開發人員而言，資料驗證越來越重要。</span><span class="sxs-lookup"><span data-stu-id="801d3-104">Data authentication is increasingly important for game developers.</span></span> <span data-ttu-id="801d3-105">Windows Vista 和 Windows 7 有一些功能（例如家長監護），這些功能都需要適當簽署遊戲，以確保沒有人會篡改資料。</span><span class="sxs-lookup"><span data-stu-id="801d3-105">Windows Vista and Windows 7 have a number of features, such as parental controls, that require games to be properly signed to ensure that no one has tampered with the data.</span></span> <span data-ttu-id="801d3-106">Microsoft Authenticode 可讓終端使用者和作業系統驗證程式代碼來自正當擁有者，而且該程式碼未遭到惡意改變或意外損毀。</span><span class="sxs-lookup"><span data-stu-id="801d3-106">Microsoft Authenticode enables end users and the operating system to verify that program code comes from the rightful owner and that it hasn't been maliciously altered or accidentally corrupted.</span></span> <span data-ttu-id="801d3-107">本文討論如何開始驗證您的遊戲，以及如何將驗證整合到每日組建流程。</span><span class="sxs-lookup"><span data-stu-id="801d3-107">This article discusses how to get started with authenticating your game and how to integrate authentication into a daily build process.</span></span>

-   [<span data-ttu-id="801d3-108">背景</span><span class="sxs-lookup"><span data-stu-id="801d3-108">Background</span></span>](#background)
-   [<span data-ttu-id="801d3-109">快速入門</span><span class="sxs-lookup"><span data-stu-id="801d3-109">Getting Started</span></span>](#getting-started)
-   [<span data-ttu-id="801d3-110">使用受信任的憑證授權單位單位</span><span class="sxs-lookup"><span data-stu-id="801d3-110">Using a Trusted Certificate Authority</span></span>](#using-a-trusted-certificate-authority)
-   [<span data-ttu-id="801d3-111">使用測試憑證的範例</span><span class="sxs-lookup"><span data-stu-id="801d3-111">Example Using a Test Certificate</span></span>](#example-using-a-test-certificate)
-   [<span data-ttu-id="801d3-112">將程式碼登入整合到每日組建系統</span><span class="sxs-lookup"><span data-stu-id="801d3-112">Integrating Code Signing into the Daily Build System</span></span>](#integrating-code-signing-into-the-daily-build-system)
-   [<span data-ttu-id="801d3-113">撤銷</span><span class="sxs-lookup"><span data-stu-id="801d3-113">Revocation</span></span>](#revocation)
-   [<span data-ttu-id="801d3-114">程式碼簽署驅動程式</span><span class="sxs-lookup"><span data-stu-id="801d3-114">Code-Signing Drivers</span></span>](#code-signing-drivers)
-   [<span data-ttu-id="801d3-115">總結</span><span class="sxs-lookup"><span data-stu-id="801d3-115">Summary</span></span>](#summary)
-   [<span data-ttu-id="801d3-116">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="801d3-116">More information</span></span>](#more-information)

> [!Note]  
> <span data-ttu-id="801d3-117">自2016年1月1日起，Windows 7 和更新版本不再信任到期日為2016或更新版本的任何 SHA-1 程式碼簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-117">As of January 1, 2016, Windows 7 and later no longer trust any SHA-1 code signing certificate with an expiration date of January 1, 2016 or later.</span></span> <span data-ttu-id="801d3-118">如需詳細資訊，請參閱 [Windows 強制執行 Authenticode 程式碼簽署和時間戳記](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="801d3-118">See [Windows Enforcement of Authenticode Code Signing and Timestamping](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) for more information.</span></span>

 

## <a name="background"></a><span data-ttu-id="801d3-119">背景</span><span class="sxs-lookup"><span data-stu-id="801d3-119">Background</span></span>

<span data-ttu-id="801d3-120">數位憑證是用來建立作者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="801d3-120">Digital certificates are used to establish the identity of the author.</span></span> <span data-ttu-id="801d3-121">數位憑證是由信任的協力廠商（稱為憑證授權單位單位 (CA) ，例如 VeriSign 或 Thawte）發行。</span><span class="sxs-lookup"><span data-stu-id="801d3-121">Digital certificates are issued by a trusted third party known as a Certificate Authority (CA) such as VeriSign or Thawte.</span></span> <span data-ttu-id="801d3-122">CA 負責確認擁有者不會宣告錯誤識別。</span><span class="sxs-lookup"><span data-stu-id="801d3-122">The CA is responsible for verifying that owner is not claiming a false identify.</span></span> <span data-ttu-id="801d3-123">將憑證套用至憑證的 CA 之後，商業開發人員在兩周內都能預期對其應用程式的回應。</span><span class="sxs-lookup"><span data-stu-id="801d3-123">After applying to a CA for a certificate, commercial developers can expect a response to their application in less than two weeks.</span></span>

<span data-ttu-id="801d3-124">在 CA 決定符合其原則準則之後，它會產生符合 x.509 的程式碼簽署憑證，該憑證格式符合國際電信聯集所建立的產業標準憑證格式（含第3版延伸模組）。</span><span class="sxs-lookup"><span data-stu-id="801d3-124">After the CA decides that you meet its policy criteria, it generates a code-signing certificate that conforms to X.509, the industry-standard certificate format created by the International Telecommunications Union, with Version 3 extensions.</span></span> <span data-ttu-id="801d3-125">此憑證會識別您的公開金鑰並包含公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="801d3-125">This certificate identifies you and contains your public key.</span></span> <span data-ttu-id="801d3-126">它是由 CA 儲存以供參考，並以電子方式提供複本給您。</span><span class="sxs-lookup"><span data-stu-id="801d3-126">It is stored by the CA for reference, and a copy is given to you electronically.</span></span> <span data-ttu-id="801d3-127">同時，您也可以建立私用金鑰，而您必須保持安全，且不能與任何人共用，即使是 CA 也一樣。</span><span class="sxs-lookup"><span data-stu-id="801d3-127">At the same time, you also create a private, key which you must keep safe and which you must not share with anyone, even the CA.</span></span>

<span data-ttu-id="801d3-128">擁有公開和私密金鑰之後，您就可以開始散發已簽署的軟體。</span><span class="sxs-lookup"><span data-stu-id="801d3-128">After you have a public and private key, you can then begin distributing signed software.</span></span> <span data-ttu-id="801d3-129">Microsoft 提供在 Windows SDK 中進行這項作業的工具。</span><span class="sxs-lookup"><span data-stu-id="801d3-129">Microsoft provides tools to do this in the Windows SDK.</span></span> <span data-ttu-id="801d3-130">這些工具會使用單向雜湊、產生固定長度的摘要，並使用私密金鑰產生加密簽章。</span><span class="sxs-lookup"><span data-stu-id="801d3-130">The tools utilize a one-way hash, produce a fixed-length digest, and generate an encrypted signature with a private key.</span></span> <span data-ttu-id="801d3-131">然後，他們會將該加密簽章與您的憑證和認證合併成一個稱為簽章區塊的結構，並將它內嵌到可執行檔的檔案格式中。</span><span class="sxs-lookup"><span data-stu-id="801d3-131">They then combine that encrypted signature with your certificate and credentials into a structure known as a signature block and embed it into the file format of the executable.</span></span> <span data-ttu-id="801d3-132">可以簽署任何類型的可執行二進位檔案，包括 Dll、可執行檔和封包檔。</span><span class="sxs-lookup"><span data-stu-id="801d3-132">Any type of executable binary file can be signed, including DLLs, executable files, and cabinet files.</span></span>

<span data-ttu-id="801d3-133">您可以透過多種方式來驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="801d3-133">The signature can be verified in multiple ways.</span></span> <span data-ttu-id="801d3-134">程式可以呼叫 CertVerifyCertificateChainPolicy 函式，而 SignTool (signtool.exe) 可以用來從命令提示字元驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="801d3-134">Programs can call the CertVerifyCertificateChainPolicy function, and SignTool (signtool.exe) can be used to verify a signature from the command-line prompt.</span></span> <span data-ttu-id="801d3-135">Windows 檔案總管在 [檔案屬性] 中也有 [數位簽章] 索引標籤，可顯示已簽署之二進位檔案的每個憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-135">Windows Explorer also has a Digital Signatures tab in File Properties that displays each certificate of a signed binary file.</span></span> <span data-ttu-id="801d3-136"> (數位簽章] 索引標籤只會出現在已簽署檔案的檔案屬性中 ) 。此外，您也可以使用 [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy)，自行驗證應用程式。</span><span class="sxs-lookup"><span data-stu-id="801d3-136">(The Digital Signatures tab only appears in File Properties for signed files.) Also, an application can be self-verifying by use of [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).</span></span>

<span data-ttu-id="801d3-137">Authenticode 簽章不僅適用于使用者所進行的資料驗證，也需要用於修補受限的使用者帳戶，以及 Windows Vista 和 Windows 7 中的家長監護。</span><span class="sxs-lookup"><span data-stu-id="801d3-137">Authenticode signing is not only useful for data authentication by end users, but is also needed for patching of Limited User Accounts and by parental controls in Windows Vista and Windows 7.</span></span> <span data-ttu-id="801d3-138">此外，Windows 作業系統中的未來技術也可能需要簽署程式碼，因此強烈建議所有 professional 和總是業餘開發人員從 CA 取得程式碼簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-138">In addition, future technologies in Windows operating systems may also require that code is signed, so it is strongly advised that all professional and amateur developers acquire a code-signing certificate from a CA.</span></span> <span data-ttu-id="801d3-139">如需如何完成此操作的詳細資訊，請參閱本文稍後 [使用受信任的憑證授權單位](#using-a-trusted-certificate-authority)單位。</span><span class="sxs-lookup"><span data-stu-id="801d3-139">More information on how this is done can be found later in this article in [Using a Trusted Certificate Authority](#using-a-trusted-certificate-authority).</span></span>

<span data-ttu-id="801d3-140">遊戲程式碼、patchers 和安裝程式可透過在程式碼中驗證檔案是否為真，來進一步利用 Authenicode 簽署。</span><span class="sxs-lookup"><span data-stu-id="801d3-140">Game code, patchers, and installers can further leverage Authenicode signing by verifying files are authentic in code.</span></span> <span data-ttu-id="801d3-141">這可用於反相關和一般網路安全性。</span><span class="sxs-lookup"><span data-stu-id="801d3-141">This can be used for anti-cheat and general network security.</span></span> <span data-ttu-id="801d3-142">檢查檔案是否已簽署的範例程式碼，可以在這裡找到： [範例 C 程式：驗證 PE 檔案的](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)簽章，以及在已簽署檔案上檢查簽署憑證擁有權的範例程式碼： [如何從 Authenticode 簽署的可執行檔取得資訊](https://support.microsoft.com/kb/323809)。</span><span class="sxs-lookup"><span data-stu-id="801d3-142">Example code for checking if a file is signed can be found here: [Example C Program: Verifying the Signature of a PE File](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file), and example code for checking ownership of a signing certificate on a signed file can be found here: [How To Get Information from Authenticode Signed Executables](https://support.microsoft.com/kb/323809).</span></span>

## <a name="getting-started"></a><span data-ttu-id="801d3-143">開始使用</span><span class="sxs-lookup"><span data-stu-id="801d3-143">Getting Started</span></span>

<span data-ttu-id="801d3-144">為了開始使用，Microsoft 提供了 Visual Studio 2005 和 Visual Studio 2008，以及 [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)中的工具，可協助您執行及驗證程式代碼簽署程式。</span><span class="sxs-lookup"><span data-stu-id="801d3-144">To get started, Microsoft provides tools with Visual Studio 2005 and Visual Studio 2008, and in the [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx), to help perform and verify the code-signing process.</span></span> <span data-ttu-id="801d3-145">安裝 Visual Studio 或 Windows SDK 之後，此技術檔中所述的工具位於安裝的子目錄中，其中可能包含下列一或多個專案：</span><span class="sxs-lookup"><span data-stu-id="801d3-145">After installing Visual Studio or the Windows SDK, the tools described in this technical article are located in a subdirectory of the installation, which may include one or more of the following:</span></span>

-   <span data-ttu-id="801d3-146">% SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ SDK v2.0 \\ \\ Bin</span><span class="sxs-lookup"><span data-stu-id="801d3-146">%SystemDrive%\\Program Files\\Microsoft Visual Studio 8\\SDK\\v2.0\\Bin</span></span>
-   <span data-ttu-id="801d3-147">% SystemDrive% \\ Program Files \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ Bin</span><span class="sxs-lookup"><span data-stu-id="801d3-147">%SystemDrive%\\Program Files\\Microsoft Visual Studio 8\\VC\\PlatformSDK\\Bin</span></span>
-   <span data-ttu-id="801d3-148">% SystemDrive% \\ Program Files \\ Microsoft Visual Studio 9.0 \\ SmartDevices \\ SDK \\ SDKTools</span><span class="sxs-lookup"><span data-stu-id="801d3-148">%SystemDrive%\\Program Files\\Microsoft Visual Studio 9.0\\SmartDevices\\SDK\\SDKTools</span></span>\\
-   <span data-ttu-id="801d3-149">% SystemDrive% \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 a \\ bin</span><span class="sxs-lookup"><span data-stu-id="801d3-149">%SystemDrive%\\Program Files\\Microsoft SDKs\\Windows\\v6.0A\\bin</span></span>\\

<span data-ttu-id="801d3-150">下列工具最適合用於簽署程式碼：</span><span class="sxs-lookup"><span data-stu-id="801d3-150">The following tools are the most useful for signing code:</span></span>

<dl> <dt>

<span data-ttu-id="801d3-151"><span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>憑證建立工具 (MakeCert.exe) </span><span class="sxs-lookup"><span data-stu-id="801d3-151"><span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Certificate Creation Tool (MakeCert.exe)</span></span>
</dt> <dd>

<span data-ttu-id="801d3-152">將 x.509 憑證以 .cer 檔案的形式產生，該檔案包含您的公開金鑰和私密金鑰（pvk 檔案）。</span><span class="sxs-lookup"><span data-stu-id="801d3-152">Generates a test X.509 certificate, as a .cer file, that contains your public key and a private key, as a .pvk file.</span></span> <span data-ttu-id="801d3-153">此憑證僅供內部測試之用，無法公開使用。</span><span class="sxs-lookup"><span data-stu-id="801d3-153">This certificate is only for internal testing purposes and can't be used publicly.</span></span>

</dd> <dt>

<span data-ttu-id="801d3-154"><span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe</span><span class="sxs-lookup"><span data-stu-id="801d3-154"><span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe</span></span>
</dt> <dd>

<span data-ttu-id="801d3-155">從一對 .cer 和 pvk 檔案建立個人資訊交換 ( .pfx) 檔案。</span><span class="sxs-lookup"><span data-stu-id="801d3-155">Creates a Personal Information Exchange (.pfx) file from a pair of .cer and .pvk files.</span></span> <span data-ttu-id="801d3-156">.Pfx 檔案包含您的公開和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="801d3-156">The .pfx file contains both your public and private key.</span></span>

</dd> <dt>

<span data-ttu-id="801d3-157"><span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe) </span><span class="sxs-lookup"><span data-stu-id="801d3-157"><span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)</span></span>
</dt> <dd>

<span data-ttu-id="801d3-158">使用 .pfx 檔案來簽署檔案。</span><span class="sxs-lookup"><span data-stu-id="801d3-158">Signs file by using the .pfx file.</span></span> <span data-ttu-id="801d3-159">SignTool 支援簽署 DLL 檔案、可執行檔、Windows Installer ( .msi) 檔案，以及封包 ( .cab) 檔。</span><span class="sxs-lookup"><span data-stu-id="801d3-159">SignTool supports the signing of DLL files, executable files, Windows Installer (.msi) files, and cabinet (.cab) files.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="801d3-160">閱讀其他檔時，您可能會找到 Signcode.exe (SignCode.exe) 的參考，但這項工具已淘汰且不再支援，請改用 SignTool。</span><span class="sxs-lookup"><span data-stu-id="801d3-160">While reading other documentation, you might find references to SignCode (SignCode.exe), but this tool is deprecated and is no longer supported—use SignTool instead.</span></span>

 

## <a name="using-a-trusted-certificate-authority"></a><span data-ttu-id="801d3-161">使用受信任的憑證授權單位單位</span><span class="sxs-lookup"><span data-stu-id="801d3-161">Using a Trusted Certificate Authority</span></span>

<span data-ttu-id="801d3-162">若要取得受信任的憑證，您必須將 (CA) 的憑證授權單位單位（例如 VeriSign 或 Thawte）套用至憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="801d3-162">To obtain a trusted certificate, you must apply to a Certificate Authority (CA), such as VeriSign or Thawte.</span></span> <span data-ttu-id="801d3-163">Microsoft 不建議使用任何 CA，但如果您想要整合至 Windows 錯誤報告 (WER) 服務，您應該考慮使用 VeriSign 來發出憑證，因為存取 WER 資料庫需要 WinQual 帳戶，需要 VeriSign 識別碼。</span><span class="sxs-lookup"><span data-stu-id="801d3-163">Microsoft doesn't recommend any CA over another, but if you want to integrate into the Windows Error Reporting (WER) service, you should consider using VeriSign to issue the certificate, because accessing the WER database requires a WinQual account which requires a VeriSign ID.</span></span> <span data-ttu-id="801d3-164">如需信任的協力廠商憑證授權單位單位的完整清單，請參閱 [Microsoft 根憑證計畫成員](/previous-versions/ms995347(v=msdn.10))。</span><span class="sxs-lookup"><span data-stu-id="801d3-164">For a complete list of trusted third-party certificate authorities, see [Microsoft Root Certificate Program Members](/previous-versions/ms995347(v=msdn.10)).</span></span> <span data-ttu-id="801d3-165">如需使用 WER 註冊的詳細資訊，請參閱[ISV 區域](https://msdn.microsoft.com/)中的「[簡介 Windows 錯誤報告](https://msdn.microsoft.com/)」。</span><span class="sxs-lookup"><span data-stu-id="801d3-165">For more information about registering with WER, see "[Introducing Windows Error Reporting](https://msdn.microsoft.com/)" in [ISV Zone](https://msdn.microsoft.com/).</span></span>

<span data-ttu-id="801d3-166">當您收到來自 CA 的憑證之後，您可以使用 SignTool 簽署您的程式，並將您的程式發行至公用。</span><span class="sxs-lookup"><span data-stu-id="801d3-166">After you receive your certificate from the CA, you can sign your program by using SignTool and release your program to the public.</span></span> <span data-ttu-id="801d3-167">不過，您必須小心保護您的私密金鑰，這是包含在 .pfx 和 pvk 檔案中的金鑰。</span><span class="sxs-lookup"><span data-stu-id="801d3-167">However, you must be careful to protect your private key, which is contained in your .pfx and .pvk files.</span></span> <span data-ttu-id="801d3-168">請務必將這些檔案保存在安全的位置。</span><span class="sxs-lookup"><span data-stu-id="801d3-168">Be sure to keep these files in a secure location.</span></span>

## <a name="example-using-a-test-certificate"></a><span data-ttu-id="801d3-169">使用測試憑證的範例</span><span class="sxs-lookup"><span data-stu-id="801d3-169">Example Using a Test Certificate</span></span>

<span data-ttu-id="801d3-170">下列步驟將示範如何建立程式碼簽署憑證以供測試之用，然後使用此測試憑證來簽署 Direct3D 範例程式 (呼叫 BasicHLSL.exe) 。</span><span class="sxs-lookup"><span data-stu-id="801d3-170">The following steps demonstrate the creation of a code-signing certificate for testing purposes, followed by the signing of a Direct3D sample program (called BasicHLSL.exe) with this test certificate.</span></span> <span data-ttu-id="801d3-171">此程式會建立 .cer 和 pvk 檔案（分別是您的公開和私密金鑰），這些檔案不能用於公開認證。</span><span class="sxs-lookup"><span data-stu-id="801d3-171">This procedure creates .cer and .pvk files—your public and private keys, respectively — which cannot be used for public certification.</span></span>

<span data-ttu-id="801d3-172">在此範例中，也會將時間戳記加入簽章。</span><span class="sxs-lookup"><span data-stu-id="801d3-172">In this example, a time stamp is also added to the signature.</span></span> <span data-ttu-id="801d3-173">時間戳記會在憑證過期時防止簽章變成無效。</span><span class="sxs-lookup"><span data-stu-id="801d3-173">A time stamp prevents the signature from becoming invalid when the certificate expires.</span></span> <span data-ttu-id="801d3-174">簽署但缺少時間戳記的程式碼將不會在憑證到期後進行驗證。</span><span class="sxs-lookup"><span data-stu-id="801d3-174">Code that is signed but lacking a time stamp will not validate after the certificate expires.</span></span> <span data-ttu-id="801d3-175">因此，所有公開發行的程式碼都應該有時間戳記。</span><span class="sxs-lookup"><span data-stu-id="801d3-175">Therefore, all publicly released code should have a time stamp.</span></span>

<span data-ttu-id="801d3-176">**建立憑證並簽署程式**</span><span class="sxs-lookup"><span data-stu-id="801d3-176">**To create a certificate and sign a program**</span></span>

1.  <span data-ttu-id="801d3-177">使用 (MakeCert.exe) 的憑證建立工具建立測試憑證和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="801d3-177">Create a test certificate and private key by using the Certificate Creation Tool (MakeCert.exe).</span></span>

    <span data-ttu-id="801d3-178">下列命令列範例會將 MyPrivateKey 指定為私密金鑰的檔案名 (. pvk) file、MyPublicKey 作為憑證的檔案名 ( .cer) 檔和 MySoftwareCompany 作為憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="801d3-178">The following command-line example specifies MyPrivateKey as the file name for the private key (.pvk) file, MyPublicKey as the file name for the certificate (.cer) file, and MySoftwareCompany as the name of the certificate.</span></span> <span data-ttu-id="801d3-179">它也會讓憑證自我簽署，使其不受信任的根授權單位。</span><span class="sxs-lookup"><span data-stu-id="801d3-179">It also makes the certificate self-signed, so that it does not have an untrusted root authority.</span></span>

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  <span data-ttu-id="801d3-180">從您的私密金鑰建立個人資訊交換 ( .pfx) 檔案 (. 使用 ( pvk) 檔案和憑證) .cer pvk2pfx.exe 檔案。</span><span class="sxs-lookup"><span data-stu-id="801d3-180">Create a Personal Information Exchange (.pfx) file from your private key (.pvk) file and certificate (.cer) file by using pvk2pfx.exe.</span></span>

    <span data-ttu-id="801d3-181">.Pfx 檔案會將您的公開金鑰和私密金鑰合併成單一檔案。</span><span class="sxs-lookup"><span data-stu-id="801d3-181">The .pfx file combines your public and private keys into a single file.</span></span> <span data-ttu-id="801d3-182">下列命令列範例會使用來自上一個步驟的 pvk 和 .cer 檔案，以密碼來建立名為 MyPFX 的 .pfx 檔案 \_ ：</span><span class="sxs-lookup"><span data-stu-id="801d3-182">The following command-line example uses the .pvk and .cer files from the previous step to create the .pfx file named MyPFX with the password your\_password:</span></span>

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  <span data-ttu-id="801d3-183">使用 SignTool，以您的個人資訊交換簽署您的程式 ( .pfx) 檔。</span><span class="sxs-lookup"><span data-stu-id="801d3-183">Sign your program with your Personal Information Exchange (.pfx) file by using SignTool.</span></span>

    <span data-ttu-id="801d3-184">您可以在命令列上指定數個選項。</span><span class="sxs-lookup"><span data-stu-id="801d3-184">You can specify several options on the command line.</span></span> <span data-ttu-id="801d3-185">下列命令列範例會使用來自上一個步驟的 .pfx 檔案、將您 \_ 的密碼指定為密碼、將 BasicHLSL 指定為要簽署的檔案，以及從指定的伺服器抓取時間戳記：</span><span class="sxs-lookup"><span data-stu-id="801d3-185">The following command-line example uses the .pfx file from the previous step, gives your\_password as the password, specifies BasicHLSL as the file to be signed, and retrieves a time stamp from a specified server:</span></span>

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > <span data-ttu-id="801d3-186">時間戳記服務的 URL 是由 CA 提供，而且是選擇性的，可供測試。</span><span class="sxs-lookup"><span data-stu-id="801d3-186">The URL to the time stamp service is provided by the CA, and is optional for testing.</span></span> <span data-ttu-id="801d3-187">生產簽章必須包含有效的時間戳記授權單位，否則簽章將無法在憑證到期時進行驗證。</span><span class="sxs-lookup"><span data-stu-id="801d3-187">It is important for production signing to include a valid time stamp authority, or the signature will fail to validate when the certificate expires.</span></span>

     

4.  <span data-ttu-id="801d3-188">確認程式是使用 SignTool 簽署的。</span><span class="sxs-lookup"><span data-stu-id="801d3-188">Verify that the program is signed by using SignTool.</span></span>

    <span data-ttu-id="801d3-189">下列命令列範例指定 SignTool 應該嘗試使用所有可用的方法來驗證 BasicHLSL.exe 上的簽章，同時提供詳細資訊輸出：</span><span class="sxs-lookup"><span data-stu-id="801d3-189">The following command-line example specifies that SignTool should attempt to verify the signature on BasicHLSL.exe by using all available methods while providing verbose output:</span></span>

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    <span data-ttu-id="801d3-190">在此範例中，SignTool 應該指出憑證已附加，同時也指出它不受信任，因為它不是由 CA 所發行。</span><span class="sxs-lookup"><span data-stu-id="801d3-190">In this example, SignTool should indicate that the certificate is attached, while also stating that it is not trusted, since it is not issued by a CA.</span></span>

5.  <span data-ttu-id="801d3-191">信任測試憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-191">Trust the test certificate.</span></span>

    <span data-ttu-id="801d3-192">針對測試憑證，您需要信任該憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-192">For test certificates you need to trust the certificate.</span></span> <span data-ttu-id="801d3-193">您應略過 CA 提供的憑證的這個步驟，因為這些憑證會預設為受信任。</span><span class="sxs-lookup"><span data-stu-id="801d3-193">This step should be skipped for certificates provided by a CA since those will trusted by default.</span></span>

    <span data-ttu-id="801d3-194">在您想要信任測試憑證的電腦上，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="801d3-194">On only the computers where you want to trust the test certificate, run the following:</span></span>

    ```
    certmgr.msc
    ```

    

    <span data-ttu-id="801d3-195">然後以滑鼠右鍵按一下 [信任的根憑證授權單位]，然後選擇 [所有工作匯 \| 入]</span><span class="sxs-lookup"><span data-stu-id="801d3-195">Then right click on Trusted Root Certification Authorities and choose All Tasks \| Import.</span></span> <span data-ttu-id="801d3-196">然後，流覽至您建立的 .pfx 檔案，然後依照嚮導步驟，將憑證放在受信任的根憑證授權單位中。</span><span class="sxs-lookup"><span data-stu-id="801d3-196">Then browse to the .pfx file you created and follow the wizard steps, placing the certificate in the Trusted Root Certification Authorities.</span></span>

    <span data-ttu-id="801d3-197">當嚮導完成時，您可以使用該電腦上的受信任憑證來開始測試。</span><span class="sxs-lookup"><span data-stu-id="801d3-197">When the wizard completes, you can start testing with the trusted certificate on that computer.</span></span>

## <a name="integrating-code-signing-into-the-daily-build-system"></a><span data-ttu-id="801d3-198">將程式碼登入整合到每日組建系統</span><span class="sxs-lookup"><span data-stu-id="801d3-198">Integrating Code Signing into the Daily Build System</span></span>

<span data-ttu-id="801d3-199">若要將程式碼登入至專案，您可以建立批次檔或腳本來執行命令列工具。</span><span class="sxs-lookup"><span data-stu-id="801d3-199">To integrate code signing into a project, you can create a batch file or script to run the command line tools.</span></span> <span data-ttu-id="801d3-200">建立專案之後，請使用適當的設定執行 SignTool， (如範例) 的步驟3所示。</span><span class="sxs-lookup"><span data-stu-id="801d3-200">After the project is built, run SignTool with the proper settings (as shown in step 3 of our example).</span></span>

<span data-ttu-id="801d3-201">在您的組建程式中特別謹慎，以確保 .pfx 和 pvk 檔案的存取限制為最少的電腦和使用者。</span><span class="sxs-lookup"><span data-stu-id="801d3-201">Be especially cautious in your build process to insure that access to the .pfx and .pvk files is restricted to as few computers and users as possible.</span></span> <span data-ttu-id="801d3-202">最佳做法是，開發人員只應使用測試憑證來簽署程式碼，直到準備好寄送。</span><span class="sxs-lookup"><span data-stu-id="801d3-202">As a best practice, developers should only sign code by using the test certificate until they are ready to ship.</span></span> <span data-ttu-id="801d3-203">同樣地，私密金鑰 ( pvk) 應該保留在安全的位置，例如安全或鎖定的空間，而且在理想的情況下，像是智慧卡。</span><span class="sxs-lookup"><span data-stu-id="801d3-203">Again, the private key (.pvk) should be kept in a secured location, like a safe or locked room, and ideally on a cryptographic device, like a smart card.</span></span>

<span data-ttu-id="801d3-204">使用 Microsoft Authenticode 來簽署 Windows Installer (MSI) 封裝本身，以提供另一層保護。</span><span class="sxs-lookup"><span data-stu-id="801d3-204">Another layer of protection is provided by using Microsoft Authenticode to sign the Windows Installer (MSI) package itself.</span></span> <span data-ttu-id="801d3-205">這有助於防止 MSI 套件遭受篡改和意外損毀。</span><span class="sxs-lookup"><span data-stu-id="801d3-205">This helps protect the MSI package against tampering and accidental corruption.</span></span> <span data-ttu-id="801d3-206">如需如何使用 Authenticode 簽署套件的詳細資訊，請參閱 MSI 建立工具的檔。</span><span class="sxs-lookup"><span data-stu-id="801d3-206">Refer to the documentation for your MSI creation tool for more information about how to sign packages with Authenticode.</span></span>

## <a name="revocation"></a><span data-ttu-id="801d3-207">撤銷</span><span class="sxs-lookup"><span data-stu-id="801d3-207">Revocation</span></span>

<span data-ttu-id="801d3-208">如果私密金鑰的安全性遭到入侵，或某些安全性相關事件呈現 Code-Signing 憑證無效，則開發人員必須撤銷憑證。</span><span class="sxs-lookup"><span data-stu-id="801d3-208">In the event that the security of the private key is compromised or some security-related event renders a Code-Signing certificate invalid, the developer must revoke the certificate.</span></span> <span data-ttu-id="801d3-209">這樣做會降低開發人員的完整性和簽署程式碼的效率。</span><span class="sxs-lookup"><span data-stu-id="801d3-209">Not doing so would weaken the integrity of the developer and the effectiveness of signing code.</span></span> <span data-ttu-id="801d3-210">CA 也可以發出特定時間的撤銷;在撤銷時間之前使用時間戳簽署的程式碼仍會被視為有效，但是具有後續時間戳記的程式碼將會無效。</span><span class="sxs-lookup"><span data-stu-id="801d3-210">A CA can also issue a revocation with specific time; code signed with a time stamp prior to the revocation time will still be considered valid, but code with a subsequent time stamp will be invalid.</span></span> <span data-ttu-id="801d3-211">憑證撤銷會影響任何以已撤銷的憑證簽署之應用程式中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="801d3-211">Certificate revocation affects code in any applications that is signed with the revoked certificate.</span></span>

## <a name="code-signing-drivers"></a><span data-ttu-id="801d3-212">Code-Signing 驅動程式</span><span class="sxs-lookup"><span data-stu-id="801d3-212">Code-Signing Drivers</span></span>

<span data-ttu-id="801d3-213">驅動程式可以而且應該是 Authenticode 簽署的。</span><span class="sxs-lookup"><span data-stu-id="801d3-213">Drivers can and should be Authenticode-signed.</span></span> <span data-ttu-id="801d3-214">核心模式驅動程式有其他需求：64位版本的 Windows Vista 和 Windows 7 會防止安裝所有未簽署的核心模式驅動程式，而當使用者嘗試安裝未簽署的驅動程式時，所有版本的 Windows 都會出現警告提示。</span><span class="sxs-lookup"><span data-stu-id="801d3-214">Kernel-mode drivers have additional requirements: 64-bit editions of Windows Vista and Windows 7 will prevent installation of all unsigned kernel-mode drivers, and all versions of Windows will present a warning prompt when a user attempts to install an unsigned driver.</span></span> <span data-ttu-id="801d3-215">此外，系統管理員可以設定群組原則，以防止未簽署的驅動程式安裝在 Microsoft Windows Server 2003、Windows XP Professional x64 Edition 和32位版本的 Windows Vista 和 Windows 7 上。</span><span class="sxs-lookup"><span data-stu-id="801d3-215">In addition, administrators can set Group Policy to prevent unsigned drivers from being installed on Microsoft Windows Server 2003, Windows XP Professional x64 Edition, and 32-bit editions of Windows Vista and Windows 7.</span></span>

<span data-ttu-id="801d3-216">您可以使用 Microsoft 受信任的簽章簽署許多類型的驅動程式，也就是 [Windows 硬體品質實驗室](https://www.microsoft.com/whdc/whql/) (WHQL) 的 Windows 認證計畫，或非分類的簽章 [程式](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (先前稱為驅動程式可靠性簽章) 中，這可讓系統完全信任這些驅動程式，並在沒有系統管理認證的情況下安裝它們。</span><span class="sxs-lookup"><span data-stu-id="801d3-216">Many types of drivers can be signed with a Microsoft-trusted signature — as part of the Windows Certification Program of [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) or the [Unclassified Signature Program](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (formerly named Driver Reliability Signature) — which allows the system to fully trust these drivers and install them even without administrative credentials.</span></span>

<span data-ttu-id="801d3-217">驅動程式至少必須經過 Authenticode 簽署，因為未簽署或自我簽署 (的驅動程式（使用測試憑證) 簽署）將無法安裝在許多 Windows 平臺上。</span><span class="sxs-lookup"><span data-stu-id="801d3-217">At a minimum, drivers should be Authenticode-signed, because drivers that are unsigned or self-signed (that is, signed with a test certificate) will fail to install on many Windows-based platforms.</span></span> <span data-ttu-id="801d3-218">如需有關簽署驅動程式和程式碼和相關功能的詳細資訊，請參閱[Windows 硬體開發人員中心](https://www.microsoft.com/whdc/)上[Windows 的驅動程式簽署需求](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx)。</span><span class="sxs-lookup"><span data-stu-id="801d3-218">For more information about signing drivers and code and related feature, see [Driver Signing Requirements for Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="summary"></a><span data-ttu-id="801d3-219">總結</span><span class="sxs-lookup"><span data-stu-id="801d3-219">Summary</span></span>

<span data-ttu-id="801d3-220">使用 Microsoft Authenticode 是相當簡單的流程。</span><span class="sxs-lookup"><span data-stu-id="801d3-220">Using Microsoft Authenticode is a straightforward process.</span></span> <span data-ttu-id="801d3-221">一旦取得 CER 並建立私密金鑰之後，就可以使用 Microsoft 所提供的工具，簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="801d3-221">Once you have obtained a CER and created a private key, it is a simple matter of using the tools provided by Microsoft.</span></span> <span data-ttu-id="801d3-222">然後，您可以在 Windows Vista 和 Windows 7 （例如家長監護）中啟用重要功能，並讓客戶知道您的產品直接來自其正當擁有者。</span><span class="sxs-lookup"><span data-stu-id="801d3-222">You can then enable important features in Windows Vista and Windows 7, such as parental controls, and let customers know that your product comes directly from its rightful owner.</span></span>

## <a name="more-information"></a><span data-ttu-id="801d3-223">詳細資訊</span><span class="sxs-lookup"><span data-stu-id="801d3-223">More information</span></span>

<span data-ttu-id="801d3-224">如需有關與簽署程式碼相關之工具和程式的詳細資訊，請參閱下列連結：</span><span class="sxs-lookup"><span data-stu-id="801d3-224">More information about tools and processes related to signing code, see the following links:</span></span>

-   [<span data-ttu-id="801d3-225">密碼編譯工具</span><span class="sxs-lookup"><span data-stu-id="801d3-225">Cryptography Tools</span></span>](/windows/desktop/SecCrypto/cryptography-tools)
-   [<span data-ttu-id="801d3-226">加密 API 工具參考</span><span class="sxs-lookup"><span data-stu-id="801d3-226">Crypto API Tools Reference</span></span>](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   <span data-ttu-id="801d3-227">[Authenticode 總覽和 Turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="801d3-227">[Authenticode Overview and Turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))</span></span>
-   [<span data-ttu-id="801d3-228">數位憑證</span><span class="sxs-lookup"><span data-stu-id="801d3-228">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
-   [<span data-ttu-id="801d3-229">部署 Authenticode</span><span class="sxs-lookup"><span data-stu-id="801d3-229">Deploying Authenticode</span></span>](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [<span data-ttu-id="801d3-230">如何：建立要在開發期間使用的暫時憑證</span><span class="sxs-lookup"><span data-stu-id="801d3-230">How To: Create Temporary Certificates for Use During Development</span></span>](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 