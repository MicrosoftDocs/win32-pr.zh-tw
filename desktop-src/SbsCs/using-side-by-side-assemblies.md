---
description: 使用下列程式開發新的應用程式，或更新現有的應用程式，以使用 Microsoft 或其他並存元件發行者提供的並存元件。
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: 使用並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847897"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="88694-103">使用並存元件</span><span class="sxs-lookup"><span data-stu-id="88694-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="88694-104">使用下列程式開發新的應用程式，或更新現有的應用程式，以使用 Microsoft 或其他並存元件發行者提供的 [並存元件](about-side-by-side-assemblies-.md) 。</span><span class="sxs-lookup"><span data-stu-id="88694-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="88694-105">如需 Microsoft 目前提供的並存元件清單，請參閱 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="88694-106">請注意，應用程式必須至少在 Windows XP 上執行，才能將元件安裝為並存元件。</span><span class="sxs-lookup"><span data-stu-id="88694-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="88694-107">如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="88694-108">**將並存元件新增至應用程式**</span><span class="sxs-lookup"><span data-stu-id="88694-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="88694-109">識別應用程式所需的並存元件。</span><span class="sxs-lookup"><span data-stu-id="88694-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="88694-110">從 Windows XP 開始，這些並存元件及其元件資訊清單會與作業系統一起安裝，但不會進行全域登錄。</span><span class="sxs-lookup"><span data-stu-id="88694-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="88694-111">使用 XML 編輯器來建立 [應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="88694-112">請參閱下面的範例應用程式資訊清單。</span><span class="sxs-lookup"><span data-stu-id="88694-112">See the example application manifest below.</span></span> <span data-ttu-id="88694-113">如需詳細資訊，請參閱[資訊清單檔案參考](manifest-files-reference.md)中的[應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="88694-114">在可唯一定義應用程式的應用程式資訊清單的 [*DEF-CoNtext assemblyIdentity*](d-sbscs-gly.md) 子項目中輸入屬性值。</span><span class="sxs-lookup"><span data-stu-id="88694-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="88694-115">如需有關 DEF 內容 **assemblyIdentity** 的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="88694-116">如果元件包含任何相依元件，請在應用程式資訊清單的對應 [*REF 內容 assemblyIdentity*](r-sbscs-gly.md) 子項目中輸入屬性值。</span><span class="sxs-lookup"><span data-stu-id="88694-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="88694-117">如需參考內容 **assemblyIdentity** 的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="88694-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="88694-118">您可以將應用程式資訊清單包含在應用程式的二進位可執行檔標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="88694-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="88694-119">在此情況下，也請將下列程式程式碼新增至應用程式標頭檔：</span><span class="sxs-lookup"><span data-stu-id="88694-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="88694-120">CREATEPROCESS \_ 資訊清單 \_ 資源 \_ 識別碼 RT \_ 資訊清單 "YourApp.exe .manifest"</span><span class="sxs-lookup"><span data-stu-id="88694-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="88694-121">或者，您可以將不同的資訊清單檔案放在與應用程式可執行檔相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="88694-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="88694-122">作業系統會先從檔案系統載入資訊清單，然後再檢查可執行檔的資源區段。</span><span class="sxs-lookup"><span data-stu-id="88694-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="88694-123">檔案系統版本優先。</span><span class="sxs-lookup"><span data-stu-id="88694-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="88694-124">[共用的元件](/windows/desktop/Msi/shared-assemblies) 應該使用 [Windows Installer](../msi/windows-installer-portal.md) 版本2.0 來安裝。</span><span class="sxs-lookup"><span data-stu-id="88694-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="88694-125">撰寫 Windows Installer 套件，如 [如何在 WINDOWS XP 上安裝並行共用的 Win32 元件](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)中所述？。</span><span class="sxs-lookup"><span data-stu-id="88694-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="88694-126">您可以使用[Windows Installer](../msi/windows-installer-portal.md)版本2.0 來安裝[私用元件](/windows/desktop/Msi/private-assemblies)。</span><span class="sxs-lookup"><span data-stu-id="88694-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="88694-127">撰寫 Windows Installer 套件，如如何在 [WINDOWS XP 上安裝用於應用程式私用的 Win32 元件](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="88694-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="88694-128">您也可以使用任何其他安裝程式，將私用元件及其資訊清單複製到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="88694-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="88694-129">測試您的應用程式以確定結果。</span><span class="sxs-lookup"><span data-stu-id="88694-129">Test your application to ensure the results.</span></span> <span data-ttu-id="88694-130">請注意，您的測試電腦不應該註冊並存元件。</span><span class="sxs-lookup"><span data-stu-id="88694-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="88694-131">將您的應用程式或更新部署為 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="88694-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="88694-132">範例應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="88694-132">Example Application Manifest</span></span>

<span data-ttu-id="88694-133">以下是應用程式資訊清單的範例：</span><span class="sxs-lookup"><span data-stu-id="88694-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
