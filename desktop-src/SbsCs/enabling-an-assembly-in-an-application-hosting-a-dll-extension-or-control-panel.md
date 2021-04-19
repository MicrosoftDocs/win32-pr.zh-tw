---
description: 如果您的應用程式裝載協力廠商 DLL、延伸模組、外掛程式或控制台，您可能會想要在應用程式中啟用元件&\# 郵件; 您也不需要為裝載的元件啟用此元件。
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: 在裝載 DLL、副檔名或主控台的應用程式中啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974486"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="b723a-103">在裝載 DLL、副檔名或主控台的應用程式中啟用元件</span><span class="sxs-lookup"><span data-stu-id="b723a-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="b723a-104">如果您的應用程式裝載協力廠商 DLL、延伸模組、外掛程式或控制台，您可能會想要在應用程式中啟用元件，而不同時為裝載的元件啟用此元件。</span><span class="sxs-lookup"><span data-stu-id="b723a-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="b723a-105">當裝載的元件需要變更程式碼才能使用元件時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b723a-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="b723a-106">作為應用程式開發人員，您可能無法對這些協力廠商元件進行變更。</span><span class="sxs-lookup"><span data-stu-id="b723a-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="b723a-107">在此情況下，您應該遵循本節所述的程式，讓您的應用程式可以使用元件，而不會影響裝載的元件。</span><span class="sxs-lookup"><span data-stu-id="b723a-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="b723a-108">為了在應用程式中啟用元件，而不會影響任何裝載的 Dll、延伸模組、外掛程式或控制台，描述應用程式相依性的資訊清單應該包含在應用程式中做為資源。</span><span class="sxs-lookup"><span data-stu-id="b723a-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="b723a-109">未使用元件啟用的託管元件不應包含描述此相依性的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="b723a-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="b723a-110">若要啟用應用程式中的元件及其裝載的 Dll、延伸模組、外掛程式或控制台，請將資訊清單納入為應用程式及其裝載元件中的資源。</span><span class="sxs-lookup"><span data-stu-id="b723a-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="b723a-111">應用程式和裝載元件中包含的資訊清單，應該各自描述元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="b723a-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="b723a-112">一般來說，應用程式開發人員會將資訊清單加入至應用程式，而裝載的元件開發人員會將資訊清單新增至 DLL、延伸模組、外掛程式或控制台。</span><span class="sxs-lookup"><span data-stu-id="b723a-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="b723a-113">下列方法可用來將資訊清單加入至應用程式或 DLL、延伸模組、外掛程式或控制台的託管元件。</span><span class="sxs-lookup"><span data-stu-id="b723a-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="b723a-114">**在應用程式或裝載元件中啟用元件。**</span><span class="sxs-lookup"><span data-stu-id="b723a-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="b723a-115">撰寫資訊清單，描述元件上的應用程式或擴充功能的相依性。</span><span class="sxs-lookup"><span data-stu-id="b723a-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="b723a-116">例如，您可以複製下列範例資訊清單來建立 "YourApplication" 的資訊清單，並將正確的值取代為 **assemblyIdentity**、 **processorArchitecture** 和 **description**。</span><span class="sxs-lookup"><span data-stu-id="b723a-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="b723a-117">將 **processorArchitecture** 的值設定為 x86 （如果是在32位平臺上建立），如果是在64位平臺上建立則為 ia64。</span><span class="sxs-lookup"><span data-stu-id="b723a-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="b723a-118">**Description** 元素包含應用程式的選項描述。</span><span class="sxs-lookup"><span data-stu-id="b723a-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="b723a-119">如需資訊清單格式的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。</span><span class="sxs-lookup"><span data-stu-id="b723a-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="b723a-120">在應用程式或類型 RT \_ 資訊清單識別碼2的延伸中建立資源。</span><span class="sxs-lookup"><span data-stu-id="b723a-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="b723a-121">例如，如果應用程式的名稱是 YourApp，則應用程式應該包含下列內容：</span><span class="sxs-lookup"><span data-stu-id="b723a-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="b723a-122">使用-DISOLATION 感知啟用旗標來編譯應用程式 \_ \_ ，或在 \# 包含 "Windows .h" 語句之前插入此語句。</span><span class="sxs-lookup"><span data-stu-id="b723a-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="b723a-123">在具有多個模組的應用程式案例中， \_ \_ 所有模組都需要 DISOLATION 感知啟用旗標。</span><span class="sxs-lookup"><span data-stu-id="b723a-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="b723a-124">測試以確保應用程式所使用的元件在應用程式和裝載的元件中都能正常運作。</span><span class="sxs-lookup"><span data-stu-id="b723a-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="b723a-125">如需將元件新增至不含擴充功能之應用程式的詳細資訊，請參閱 [在不含擴充功能的應用程式中啟用元件](enabling-an-assembly-in-an-application-without-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="b723a-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



