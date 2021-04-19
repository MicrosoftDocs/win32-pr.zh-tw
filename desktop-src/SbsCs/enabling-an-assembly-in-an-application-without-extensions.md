---
description: 如果您的應用程式未裝載 DLL、延伸模組、外掛程式或控制台，您可以使用本節所述的方法來啟用應用程式的元件。
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: 在不含擴充功能的應用程式中啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996986"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="2e7b1-103">在不含擴充功能的應用程式中啟用元件</span><span class="sxs-lookup"><span data-stu-id="2e7b1-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="2e7b1-104">如果您的應用程式未裝載 DLL、延伸模組、外掛程式或控制台，您可以使用本節所述的方法來啟用應用程式的元件。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="2e7b1-105">如需將元件新增至具有擴充功能之應用程式的詳細資訊，請參閱 [在裝載 DLL、副檔名或主控台的應用程式中啟用元件](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md)。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="2e7b1-106">**若要在應用程式中啟用元件，而不使用任何託管元件**</span><span class="sxs-lookup"><span data-stu-id="2e7b1-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="2e7b1-107">撰寫資訊清單，描述元件上的應用程式或擴充功能的相依性。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="2e7b1-108">例如，您可以複製下列範例資訊清單來建立 "YourApplication" 的資訊清單，並將正確的值取代為 **assemblyIdentity**、 **processorArchitecture** 和 **description**。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="2e7b1-109">將 **processorArchitecture** 的值設定為 x86 （如果在32位平臺上建立），並將設定為 ia64 （如果在64位平臺上建立）。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="2e7b1-110">**Description** 元素包含應用程式的選項描述。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="2e7b1-111">如需資訊清單格式的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="2e7b1-112">將資訊清單新增至應用程式，做為應用程式二進位可執行檔標頭檔中的資源。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="2e7b1-113">不建議您將資訊清單以外部資訊清單檔的形式新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="2e7b1-114">若要將資訊清單新增為資源，請在類型 RT \_ 資訊清單識別碼1的應用程式中建立資源。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="2e7b1-115">例如，如果應用程式的名稱是 YourApp，則應用程式的標頭檔應該包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="2e7b1-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="2e7b1-116">如果您改為新增資訊清單做為外部資訊清單檔案，請確定安裝會將資訊清單檔案複製到包含應用程式可執行檔的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="2e7b1-117">測試以確保應用程式所使用的元件在應用程式中正確運作。</span><span class="sxs-lookup"><span data-stu-id="2e7b1-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



