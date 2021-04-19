---
title: 如何使用 SignTool 簽署應用程式套件
description: 瞭解如何使用 SignTool 來簽署您的 Windows 應用程式套件，以便部署。
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969736"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="7762a-103">如何使用 SignTool 簽署應用程式套件</span><span class="sxs-lookup"><span data-stu-id="7762a-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="7762a-104">如需簽署 Windows 應用程式套件，請參閱 [使用 SignTool 簽署應用程式套件](/windows/msix/package/sign-app-package-using-signtool)。</span><span class="sxs-lookup"><span data-stu-id="7762a-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="7762a-105">瞭解如何使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署您的 Windows 應用程式套件，以便部署。</span><span class="sxs-lookup"><span data-stu-id="7762a-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="7762a-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) 是 WINDOWS 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7762a-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="7762a-107">所有 Windows 應用程式套件都必須經過數位簽署，才能進行部署。</span><span class="sxs-lookup"><span data-stu-id="7762a-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="7762a-108">雖然 Microsoft Visual Studio 2012 和更新版本可以在建立應用程式套件時進行簽署，但您使用應用程式封裝工具建立的封裝 [ (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md) Windows SDK 工具不會簽署。</span><span class="sxs-lookup"><span data-stu-id="7762a-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="7762a-109">您只能使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署 Windows 8 和更新版本或 windows Server 2012 及更新版本上的 Windows 應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="7762a-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="7762a-110">您無法使用 **SignTool** 來簽署舊版作業系統（例如 Windows 7 或 windows Server 2008 R2）上的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="7762a-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="7762a-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7762a-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7762a-112">技術</span><span class="sxs-lookup"><span data-stu-id="7762a-112">Technologies</span></span>

-   <span data-ttu-id="7762a-113">[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7762a-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="7762a-114">[應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="7762a-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="7762a-115">用來簽署檔案和檢查簽章的工具</span><span class="sxs-lookup"><span data-stu-id="7762a-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="7762a-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="7762a-116">Prerequisites</span></span>

-   <span data-ttu-id="7762a-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool)，這是 Windows SDK 的一部分</span><span class="sxs-lookup"><span data-stu-id="7762a-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="7762a-118">有效的程式碼簽署憑證，例如，使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) 工具建立的個人資訊交換 ( .pfx) 檔案</span><span class="sxs-lookup"><span data-stu-id="7762a-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="7762a-119">如需建立有效程式碼簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="7762a-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="7762a-120">封裝的 Windows 應用程式，例如，使用應用程式封裝工具建立的 .appx 檔案 [ (MakeAppx.exe) ](make-appx-package--makeappx-exe-.md) 工具</span><span class="sxs-lookup"><span data-stu-id="7762a-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="7762a-121">**其他考量**</span><span class="sxs-lookup"><span data-stu-id="7762a-121">**Additional considerations**</span></span>

<span data-ttu-id="7762a-122">您用來簽署應用程式套件的憑證必須符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="7762a-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="7762a-123">憑證的主體名稱必須符合封裝中儲存之 AppxManifest.xml 檔案的 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)元素所包含的 **發行者** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7762a-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="7762a-124">發行者名稱是已封裝之 Windows 應用程式身分識別的一部分，因此您必須讓憑證的主體名稱符合應用程式的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="7762a-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="7762a-125">這可讓您根據數位簽章檢查已簽署套件的身分識別。</span><span class="sxs-lookup"><span data-stu-id="7762a-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="7762a-126">如需使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool)簽署應用程式套件時可能產生之簽署錯誤的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)的備註一節。</span><span class="sxs-lookup"><span data-stu-id="7762a-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="7762a-127">憑證必須有效，才能進行程式碼簽署。</span><span class="sxs-lookup"><span data-stu-id="7762a-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="7762a-128">這表示這兩個專案都必須為 true：</span><span class="sxs-lookup"><span data-stu-id="7762a-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="7762a-129">憑證的 [擴充金鑰使用方法] (EKU) 欄位必須設定為 [未設定]，或包含 [程式碼簽署 (1.3.6.1.5.5.7.3.3) 的 EKU 值。</span><span class="sxs-lookup"><span data-stu-id="7762a-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="7762a-130">憑證的金鑰使用方法 (KU) 欄位必須取消設定或包含數位簽章 (0x80) 的使用位。</span><span class="sxs-lookup"><span data-stu-id="7762a-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="7762a-131">憑證包含私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="7762a-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="7762a-132">憑證有效。</span><span class="sxs-lookup"><span data-stu-id="7762a-132">The certificate is valid.</span></span> <span data-ttu-id="7762a-133">它是作用中、尚未過期，而且尚未撤銷。</span><span class="sxs-lookup"><span data-stu-id="7762a-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="7762a-134">指示</span><span class="sxs-lookup"><span data-stu-id="7762a-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="7762a-135">步驟1：決定要使用的雜湊演算法</span><span class="sxs-lookup"><span data-stu-id="7762a-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="7762a-136">當您簽署應用程式套件時，您必須使用建立應用程式封裝時所使用的相同雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7762a-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="7762a-137">如果您使用預設設定來建立應用程式套件，則使用的雜湊演算法是 SHA256。</span><span class="sxs-lookup"><span data-stu-id="7762a-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="7762a-138">如果您使用具有特定雜湊演算法的應用程式封裝程式來建立應用程式套件，請使用相同的演算法來簽署套件。</span><span class="sxs-lookup"><span data-stu-id="7762a-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="7762a-139">若要判斷用於簽署封裝的雜湊演算法，您可以解壓縮封裝內容，並檢查 AppxBlockMap.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="7762a-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="7762a-140">[**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap)專案的 **HashMethod** 屬性工作表示建立應用程式封裝時所使用的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="7762a-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="7762a-141">例如：</span><span class="sxs-lookup"><span data-stu-id="7762a-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="7762a-142">上述 [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) 元素指出使用 SHA256 演算法。</span><span class="sxs-lookup"><span data-stu-id="7762a-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="7762a-143">下表列出目前可用演算法的對應：</span><span class="sxs-lookup"><span data-stu-id="7762a-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="7762a-144">**HashMethod** 值</span><span class="sxs-lookup"><span data-stu-id="7762a-144">**HashMethod** value</span></span>                            | <span data-ttu-id="7762a-145">要使用的 *hashAlgorithm*</span><span class="sxs-lookup"><span data-stu-id="7762a-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="7762a-146">SHA256 ( .appx 預設) </span><span class="sxs-lookup"><span data-stu-id="7762a-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="7762a-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="7762a-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="7762a-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="7762a-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="7762a-149">步驟2：執行 SignTool.exe 來簽署套件</span><span class="sxs-lookup"><span data-stu-id="7762a-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="7762a-150">**使用 .pfx 檔案中的簽署憑證簽署套件**</span><span class="sxs-lookup"><span data-stu-id="7762a-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="7762a-151">如果未指定，則 [**SignTool**](/windows-hardware/drivers/devtest/signtool)會將/fd *hashAlgorithm* 參數預設為 sha1，而 sha1 對簽署應用程式封裝而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="7762a-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="7762a-152">因此，當您簽署應用程式封裝時，必須指定此參數。</span><span class="sxs-lookup"><span data-stu-id="7762a-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="7762a-153">若要簽署使用預設 SHA256 雜湊所建立的應用程式套件，您可以將/fd *hashAlgorithm* 參數指定為 SHA256：</span><span class="sxs-lookup"><span data-stu-id="7762a-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="7762a-154">如果您使用未受密碼保護的 .pfx 檔案，您可以省略/p *password* 參數。</span><span class="sxs-lookup"><span data-stu-id="7762a-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="7762a-155">您也可以使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 所支援的其他憑證選取選項來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="7762a-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="7762a-156">如需這些選項的詳細資訊，請參閱 [SignTool](/windows/desktop/SecCrypto/signtool)。</span><span class="sxs-lookup"><span data-stu-id="7762a-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="7762a-157">您無法在已簽署的應用程式套件上使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 時間戳記操作;不支援此操作。</span><span class="sxs-lookup"><span data-stu-id="7762a-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="7762a-158">如果您想要為應用程式套件進行時間戳記，您必須在簽署作業期間執行此動作。</span><span class="sxs-lookup"><span data-stu-id="7762a-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="7762a-159">例如：</span><span class="sxs-lookup"><span data-stu-id="7762a-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="7762a-160">讓/tr *timestampServerUrl* 參數等於 RFC 3161 時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="7762a-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="7762a-161">備註</span><span class="sxs-lookup"><span data-stu-id="7762a-161">Remarks</span></span>

<span data-ttu-id="7762a-162">本節討論應用程式套件簽署錯誤的疑難排解。</span><span class="sxs-lookup"><span data-stu-id="7762a-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="7762a-163">針對應用程式套件簽署錯誤進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7762a-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="7762a-164">除了 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 可以傳回的簽署錯誤之外， **SignTool** 也會傳回簽署應用程式套件的特定錯誤。</span><span class="sxs-lookup"><span data-stu-id="7762a-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="7762a-165">這些錯誤通常會顯示為內部錯誤：</span><span class="sxs-lookup"><span data-stu-id="7762a-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="7762a-166">如果錯誤碼以0x8008 開頭，例如 0x80080206 APPX 電子損毀 \_ 的 \_ \_ 內容) ，則表示簽署的套件無效。</span><span class="sxs-lookup"><span data-stu-id="7762a-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="7762a-167">在此情況下，您必須先重建套件，才能簽署封裝。</span><span class="sxs-lookup"><span data-stu-id="7762a-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="7762a-168">如需0x8008 錯誤的完整清單 \* ，請參閱 [**COM 錯誤碼 (安全性和設定)**](/windows/desktop/com/com-error-codes-4)。</span><span class="sxs-lookup"><span data-stu-id="7762a-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="7762a-169">更常見的情況是，錯誤的 0x8007000b (錯誤 \_ \_ 格式) 。</span><span class="sxs-lookup"><span data-stu-id="7762a-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="7762a-170">在此情況下，您可以在事件記錄檔中找到更明確的錯誤資訊：</span><span class="sxs-lookup"><span data-stu-id="7762a-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="7762a-171">**若要搜尋事件記錄檔**</span><span class="sxs-lookup"><span data-stu-id="7762a-171">**To search the event log**</span></span>

1.  <span data-ttu-id="7762a-172">執行 Eventvwr.msc services.msc。</span><span class="sxs-lookup"><span data-stu-id="7762a-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="7762a-173">開啟事件記錄檔：事件檢視器 (本機) > 應用程式和服務記錄 > Microsoft > Windows > AppxPackagingOM > Microsoft Windows-AppxPackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="7762a-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="7762a-174">尋找最新的錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="7762a-174">Look for the most recent error event.</span></span>

<span data-ttu-id="7762a-175">內部錯誤通常會對應到下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="7762a-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7762a-176">事件識別碼</span><span class="sxs-lookup"><span data-stu-id="7762a-176">Event ID</span></span></th>
<th><span data-ttu-id="7762a-177">範例事件字串</span><span class="sxs-lookup"><span data-stu-id="7762a-177">Example event string</span></span></th>
<th><span data-ttu-id="7762a-178">建議</span><span class="sxs-lookup"><span data-stu-id="7762a-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7762a-179">150</span><span class="sxs-lookup"><span data-stu-id="7762a-179">150</span></span></td>
<td><span data-ttu-id="7762a-180">錯誤 0x8007000B: 應用程式資訊清單發行者名稱 (CN=Contoso) 必須符合簽署憑證 (CN=Contoso, C=US) 的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7762a-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="7762a-181">應用程式資訊清單發行者名稱必須完全符合簽署的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7762a-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7762a-182">這些名稱會以引號指定，且區分大小寫和空白字元。</span><span class="sxs-lookup"><span data-stu-id="7762a-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="7762a-183">您可以更新為 AppxManifest.xml 檔中的<a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a>專案定義的<strong>發行者</strong>屬性字串，以符合所需簽署憑證的主體名稱。</span><span class="sxs-lookup"><span data-stu-id="7762a-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="7762a-184">或者，選取具有與應用程式資訊清單發行者名稱相符之主體名稱的不同簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="7762a-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="7762a-185">資訊清單發行者名稱和憑證主體名稱都會列在事件訊息中。</span><span class="sxs-lookup"><span data-stu-id="7762a-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7762a-186">151</span><span class="sxs-lookup"><span data-stu-id="7762a-186">151</span></span></td>
<td><span data-ttu-id="7762a-187">錯誤 0x8007000B: 指定的簽章雜湊方法 (SHA512) 必須符合應用程式套件區塊對應中使用的雜湊方法 (SHA256)。</span><span class="sxs-lookup"><span data-stu-id="7762a-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="7762a-188">在/fd 參數中指定的 hashAlgorithm 不正確 (請參閱步驟1：判斷要使用的雜湊演算法) 。</span><span class="sxs-lookup"><span data-stu-id="7762a-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="7762a-189">使用符合應用程式套件區塊對應的 hashAlgorithm 重新執行 <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="7762a-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7762a-190">152</span><span class="sxs-lookup"><span data-stu-id="7762a-190">152</span></span></td>
<td><span data-ttu-id="7762a-191">錯誤 0x8007000B: 應用程式套件內容必須通過區塊對應的驗證。</span><span class="sxs-lookup"><span data-stu-id="7762a-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="7762a-192">應用程式套件損壞，需要重建產生新區塊對應。</span><span class="sxs-lookup"><span data-stu-id="7762a-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="7762a-193">如需建立應用程式套件的詳細資訊，請參閱使用 <a href="make-appx-package--makeappx-exe-.md">應用程式封裝程式</a> 建立應用程式套件或 <a href="/previous-versions/hh975357(v=vs.110)">使用 Visual Studio 2012 建立應用程式套件</a>。</span><span class="sxs-lookup"><span data-stu-id="7762a-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="7762a-194">安全性考量</span><span class="sxs-lookup"><span data-stu-id="7762a-194">Security Considerations</span></span>

<span data-ttu-id="7762a-195">簽署封裝之後，您用來簽署套件的憑證仍然必須由要部署封裝的電腦所信任。</span><span class="sxs-lookup"><span data-stu-id="7762a-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="7762a-196">藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。</span><span class="sxs-lookup"><span data-stu-id="7762a-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="7762a-197">建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區，並在不再需要時立即移除這些憑證。</span><span class="sxs-lookup"><span data-stu-id="7762a-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="7762a-198">如果您建立自己的測試憑證來簽署應用程式套件，我們也建議您限制與測試憑證相關聯的許可權。</span><span class="sxs-lookup"><span data-stu-id="7762a-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="7762a-199">如需建立測試憑證以簽署應用程式套件的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="7762a-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7762a-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="7762a-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7762a-201">**範例**</span><span class="sxs-lookup"><span data-stu-id="7762a-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="7762a-202">建立應用程式套件範例</span><span class="sxs-lookup"><span data-stu-id="7762a-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="7762a-203">**概念**</span><span class="sxs-lookup"><span data-stu-id="7762a-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="7762a-204">[程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7762a-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7762a-205">[在 Visual Studio 2012 中簽署套件](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="7762a-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="7762a-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="7762a-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="7762a-207">應用程式封裝工具 (MakeAppx.exe) </span><span class="sxs-lookup"><span data-stu-id="7762a-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="7762a-208">如何建立應用程式套件簽署憑證</span><span class="sxs-lookup"><span data-stu-id="7762a-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

