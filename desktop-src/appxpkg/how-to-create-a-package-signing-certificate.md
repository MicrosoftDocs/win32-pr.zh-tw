---
title: 如何建立應用程式套件簽署憑證
description: 瞭解如何使用 MakeCert.exe 和 Pvk2Pfx.exe 來建立測試程式碼簽署憑證，讓您可以簽署 Windows 應用程式套件。
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023300"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="c6eb0-103">如何建立應用程式套件簽署憑證</span><span class="sxs-lookup"><span data-stu-id="c6eb0-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6eb0-104">MakeCert.exe 已被取代。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="c6eb0-105">如需建立憑證的目前指導方針，請參閱 [建立封裝簽署的憑證](/windows/msix/package/create-certificate-package-signing)。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="c6eb0-106">瞭解如何使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) 來建立測試程式碼簽署憑證，讓您可以簽署 Windows 應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="c6eb0-107">您必須在部署封裝的 Windows 應用程式之前，先對其進行數位簽署。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="c6eb0-108">如果您未使用 Microsoft Visual Studio 2012 來建立和簽署應用程式套件，則需要建立及管理您自己的程式碼簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="c6eb0-109">您可以使用 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) 建立憑證，並 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Windows 驅動程式套件 (WDK) 。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="c6eb0-110">然後，您可以使用憑證來簽署應用程式套件，以便在本機部署以進行測試。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c6eb0-111">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="c6eb0-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c6eb0-112">技術</span><span class="sxs-lookup"><span data-stu-id="c6eb0-112">Technologies</span></span>

-   <span data-ttu-id="c6eb0-113">[程式碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6eb0-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="c6eb0-114">[應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="c6eb0-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="c6eb0-115">簽署驅動程式的工具</span><span class="sxs-lookup"><span data-stu-id="c6eb0-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="c6eb0-116">必要條件</span><span class="sxs-lookup"><span data-stu-id="c6eb0-116">Prerequisites</span></span>

-   <span data-ttu-id="c6eb0-117">從 WDK [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert)和 [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)工具</span><span class="sxs-lookup"><span data-stu-id="c6eb0-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="c6eb0-118">指示</span><span class="sxs-lookup"><span data-stu-id="c6eb0-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="c6eb0-119">步驟1：決定封裝的發行者名稱</span><span class="sxs-lookup"><span data-stu-id="c6eb0-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="c6eb0-120">若要讓您建立的簽署憑證可與您要簽署的應用程式套件搭配使用，簽署憑證的主體名稱必須符合該應用程式之 AppxManifest.xml 中 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)元素的 **發行者** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="c6eb0-121">例如，假設 AppxManifest.xml 包含：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="c6eb0-122">針對您在下一個步驟中使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert)公用程式指定的 *publisherName* 參數，請使用 "CN = contoso Software，O = contoso CORPORATION，C = US"。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="c6eb0-123">此參數字串以引號指定，且區分大小寫和空白字元。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="c6eb0-124">針對 AppxManifest.xml 中的 [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity)專案定義的發行者屬性字串，必須與您使用 [憑證主體名稱 **]** 的 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n 參數指定的字串相同。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="c6eb0-125">盡可能複製並貼上字串。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="c6eb0-126">步驟2：使用 MakeCert.exe 建立私密金鑰</span><span class="sxs-lookup"><span data-stu-id="c6eb0-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="c6eb0-127">使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 公用程式來建立自我簽署的測試憑證和私密金鑰：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="c6eb0-128">此命令會提示您提供 pvk 檔案的密碼。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="c6eb0-129">建議您選擇 [強式密碼](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) ，並將您的私密金鑰放在安全的位置。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="c6eb0-130">基於下列原因，我們建議您在上述範例中使用建議的參數：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="c6eb0-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="c6eb0-132">建立自我簽署的根憑證。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="c6eb0-133">這可簡化您的測試憑證管理。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="c6eb0-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="c6eb0-135">將憑證的基本條件約束標示為終端實體。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="c6eb0-136">這可防止憑證用來作為憑證授權單位單位， (可發出其他憑證的 CA) 。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="c6eb0-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="c6eb0-138">設定憑證 (EKU) 值的增強金鑰使用方法。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="c6eb0-139">請勿在兩個逗號分隔值之間加上空格。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="c6eb0-140">1.3.6.1.5.5.7.3.3 表示憑證對程式碼簽署有效。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="c6eb0-141">一律指定此值以限制憑證的預期用途。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="c6eb0-142">1.3.6.1.4.1.311.10.3.13 指出憑證遵循存留期簽署。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="c6eb0-143">一般來說，如果簽章是時間戳記，只要憑證在時間戳記的時間點有效，簽章仍會保持有效，即使憑證過期也一樣。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="c6eb0-144">無論簽章是否已加上時間戳記，這個 EKU 都會強制簽章過期。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="c6eb0-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="c6eb0-146">設定憑證的到期日。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="c6eb0-147">以 mm/dd/yyyy 格式提供 *expirationDate* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="c6eb0-148">建議您只針對測試用途（通常不到一年），選擇只需一段時間的到期日。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="c6eb0-149">此到期日與存留期簽署 EKU 結合，有助於限制憑證可能遭到入侵和誤用的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="c6eb0-150">如需其他選項的詳細資訊，請參閱 [**MakeCert**](/windows-hardware/drivers/devtest/makecert)。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="c6eb0-151">步驟3：使用 Pvk2Pfx.exe 建立個人資訊交換 ( .pfx) 檔案</span><span class="sxs-lookup"><span data-stu-id="c6eb0-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="c6eb0-152">使用 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) 公用程式，將 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 建立的 pvk 和 .cer 檔案轉換成可搭配 [SignTool](/windows/desktop/SecCrypto/signtool) 使用的 .pfx 檔案來簽署應用程式套件：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="c6eb0-153">*MyKey. pvk* 和 *MyKey .cer* 檔案是在上一個步驟中建立的 [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert)相同檔案。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="c6eb0-154">您可以使用選擇性的/po 參數，為產生的 .pfx 指定不同的密碼;否則，.pfx 的密碼會與 *MyKey. pvk* 相同。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="c6eb0-155">如需其他選項的詳細資訊，請參閱 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx)。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6eb0-156">備註</span><span class="sxs-lookup"><span data-stu-id="c6eb0-156">Remarks</span></span>

<span data-ttu-id="c6eb0-157">建立 .pfx 檔案之後，您可以使用 [SignTool](/windows/desktop/SecCrypto/signtool) 檔案來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="c6eb0-158">如需詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="c6eb0-159">但是，除非您將憑證安裝到本機電腦的信任憑證存放區，否則本機電腦仍不會信任憑證來部署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="c6eb0-160">您可以使用 Windows 隨附的 [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="c6eb0-161">**使用 WindowsCertutil.exe安裝憑證**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="c6eb0-162">以系統管理員身分執行 **Cmd.exe** 。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="c6eb0-163">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="c6eb0-164">如果不再使用憑證，建議您移除這些憑證。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="c6eb0-165">在相同的系統管理員命令提示字元中，執行此命令：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="c6eb0-166">**CertID** 是憑證的序號。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="c6eb0-167">執行此命令以判斷憑證序號：</span><span class="sxs-lookup"><span data-stu-id="c6eb0-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="c6eb0-168">安全性考量</span><span class="sxs-lookup"><span data-stu-id="c6eb0-168">Security Considerations</span></span>

<span data-ttu-id="c6eb0-169">藉由將認證新增至[本機電腦憑證存放區](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores) (英文)，您會對電腦上所有使用者的憑證信任造成影響。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="c6eb0-170">建議您將任何要用於測試應用程式套件的程式碼簽署憑證，安裝到 [受信任的人] 憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="c6eb0-171">當不再需要時，請立即移除這些憑證，以防止它們被用來危害系統信任。</span><span class="sxs-lookup"><span data-stu-id="c6eb0-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6eb0-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="c6eb0-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c6eb0-173">**範例**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="c6eb0-174">建立應用程式套件範例</span><span class="sxs-lookup"><span data-stu-id="c6eb0-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="c6eb0-175">**概念**</span><span class="sxs-lookup"><span data-stu-id="c6eb0-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="c6eb0-176">[程式碼簽署最佳作法](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6eb0-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c6eb0-177">[如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="c6eb0-177">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
</dt> <dt>

<span data-ttu-id="c6eb0-178">[簽署應用程式套件](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="c6eb0-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 