---
description: 下列範例會討論如何產生由組件資訊清單、驗證目錄和元件檔案組成的帶正負號並存元件。
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: 組件簽署範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106986718"
---
# <a name="assembly-signing-example"></a><span data-ttu-id="012ab-103">組件簽署範例</span><span class="sxs-lookup"><span data-stu-id="012ab-103">Assembly Signing Example</span></span>

<span data-ttu-id="012ab-104">下列範例會討論如何產生由組件資訊清單、驗證目錄和元件檔案組成的帶正負號並存元件。</span><span class="sxs-lookup"><span data-stu-id="012ab-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="012ab-105">共用並存元件應該經過簽署。</span><span class="sxs-lookup"><span data-stu-id="012ab-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="012ab-106">作業系統會先驗證元件簽章，然後再將共用的元件安裝到全域並存存放區 (WinSxS) 。</span><span class="sxs-lookup"><span data-stu-id="012ab-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="012ab-107">這會讓您難以偽造並存元件的發行者。</span><span class="sxs-lookup"><span data-stu-id="012ab-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="012ab-108">請注意，在產生元件類別目錄之後變更元件檔或資訊清單內容會使目錄和元件失效。</span><span class="sxs-lookup"><span data-stu-id="012ab-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="012ab-109">如果您必須在建立和簽署類別目錄之後更新元件檔或資訊清單，您必須再次簽署該元件，並產生新的目錄。</span><span class="sxs-lookup"><span data-stu-id="012ab-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="012ab-110">從元件檔、組件資訊清單和您將用來簽署元件的憑證檔案開始。</span><span class="sxs-lookup"><span data-stu-id="012ab-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="012ab-111">憑證檔案必須是2048位或更大。</span><span class="sxs-lookup"><span data-stu-id="012ab-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="012ab-112">您不需要使用受信任的憑證。</span><span class="sxs-lookup"><span data-stu-id="012ab-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="012ab-113">憑證只能用來驗證元件是否已損毀。</span><span class="sxs-lookup"><span data-stu-id="012ab-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="012ab-114">執行 Microsoft Windows 軟體開發套件 (SDK) 所提供的 [Pktextract.exe](pktextract-exe.md) 公用程式，從憑證檔案中解壓縮公開金鑰 token。</span><span class="sxs-lookup"><span data-stu-id="012ab-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="012ab-115">若要讓 Pktextract 正常運作，憑證檔案必須存在於與公用程式相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="012ab-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="012ab-116">使用已解壓縮的公開金鑰 token 值，更新資訊清單檔案中 **assemblyIdentity** 元素的 **publicKeyToken** 屬性。</span><span class="sxs-lookup"><span data-stu-id="012ab-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="012ab-117">以下是名為 MySampleAssembly 的資訊清單檔案範例。</span><span class="sxs-lookup"><span data-stu-id="012ab-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="012ab-118">MySampleAssembly 元件僅包含一個檔案，MYFILE.DLL。</span><span class="sxs-lookup"><span data-stu-id="012ab-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="012ab-119">請注意， **assemblyIdentity** 元素的 **publicKeyToken** 屬性值已更新為公開金鑰 token 的值。</span><span class="sxs-lookup"><span data-stu-id="012ab-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

<span data-ttu-id="012ab-120">接下來，執行 Windows SDK 所提供的 [Mt.exe](mt-exe.md) 公用程式。</span><span class="sxs-lookup"><span data-stu-id="012ab-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="012ab-121">元件檔必須位於與資訊清單相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="012ab-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="012ab-122">在此範例中，這是 MySampleAssembly 目錄。</span><span class="sxs-lookup"><span data-stu-id="012ab-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="012ab-123">呼叫範例的 Mt.exe，如下所示：</span><span class="sxs-lookup"><span data-stu-id="012ab-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="012ab-124">**c： \\ MySampleAssembly>mt.exe-資訊清單 MySampleAssembly. hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="012ab-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="012ab-125">以下是執行 Mt.exe 後，範例資訊清單的外觀。</span><span class="sxs-lookup"><span data-stu-id="012ab-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="012ab-126">請注意，使用 hashupdate 選項執行 Mt.exe 會新增檔案的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="012ab-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="012ab-127">請勿變更此值。</span><span class="sxs-lookup"><span data-stu-id="012ab-127">Do not change this value.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

<span data-ttu-id="012ab-128">使用-makecdfs 選項執行 Mt.exe 會產生名為 MySampleAssembly 的檔案，其中描述將用來驗證資訊清單的安全性目錄內容。</span><span class="sxs-lookup"><span data-stu-id="012ab-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="012ab-129">下一步是在這個的 Makecat.exe 上執行，以建立元件的安全性目錄。</span><span class="sxs-lookup"><span data-stu-id="012ab-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="012ab-130">此範例的 Makecat.exe 呼叫會如下所示：</span><span class="sxs-lookup"><span data-stu-id="012ab-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="012ab-131">**c： \\ MySampleAssembly>Makecat MySampleAssembly .manifest**</span><span class="sxs-lookup"><span data-stu-id="012ab-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="012ab-132">最後一個步驟是執行 SignTool.exe，以使用憑證簽署類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="012ab-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="012ab-133">這應該是先前用來產生公開金鑰 token 的相同憑證。</span><span class="sxs-lookup"><span data-stu-id="012ab-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="012ab-134">如需 SignTool.exe 的詳細資訊，請參閱 [**SignTool**](../seccrypto/signtool.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="012ab-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="012ab-135">範例的 **SignTool** 呼叫會如下所示：</span><span class="sxs-lookup"><span data-stu-id="012ab-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="012ab-136">**c： \\ MySampleAssembly>signtool sign/f \<fullpath> mycompany .pfx/du HTTPs： \/ /www.mycompany.com/MySampleAssembly/t HTTPs： \/ /timestamp.digicert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="012ab-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="012ab-137">如果您有經過驗證的數位憑證，而您的憑證授權單位單位使用 PVK 檔案格式來儲存私密金鑰，您可以使用 PVK 數位憑證檔案匯入工具 (pvkimprt.exe) 將金鑰匯入 (CSP) 的密碼編譯服務提供者中。</span><span class="sxs-lookup"><span data-stu-id="012ab-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="012ab-138">此公用程式可讓您匯出至「PFX/P12」的產業標準格式。</span><span class="sxs-lookup"><span data-stu-id="012ab-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="012ab-139">如需 PVK 的數位憑證檔案匯入工具的詳細資訊，請參閱 MSDN library 的「部署資源」一節，或洽詢您的憑證授權單位單位。</span><span class="sxs-lookup"><span data-stu-id="012ab-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="012ab-140">您可能可以從取得 pvkimprt.exe https://office.microsoft.com/downloads/2000/pvkimprt.aspx 。</span><span class="sxs-lookup"><span data-stu-id="012ab-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="012ab-141">另請參閱 [建立已簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。</span><span class="sxs-lookup"><span data-stu-id="012ab-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
