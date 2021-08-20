---
description: 如果您的應用程式裝載協力廠商 DLL、延伸模組、外掛程式或控制台，您可能會想要在應用程式中啟用元件&\# 郵件; 您也不需要為裝載的元件啟用此元件。
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: 在裝載 DLL、副檔名或主控台的應用程式中啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ac528c10d7ca0de903c6b132e0349c16061d63f121c390483458b4ef422d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885538"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>在裝載 DLL、副檔名或主控台的應用程式中啟用元件

如果您的應用程式裝載協力廠商 DLL、延伸模組、外掛程式或控制台，您可能會想要在應用程式中啟用元件，而不同時為裝載的元件啟用此元件。 當裝載的元件需要變更程式碼才能使用元件時，就會發生這種情況。 作為應用程式開發人員，您可能無法對這些協力廠商元件進行變更。 在此情況下，您應該遵循本節所述的程式，讓您的應用程式可以使用元件，而不會影響裝載的元件。

-   為了在應用程式中啟用元件，而不會影響任何裝載的 Dll、延伸模組、外掛程式或控制台，描述應用程式相依性的資訊清單應該包含在應用程式中做為資源。 未使用元件啟用的託管元件不應包含描述此相依性的資訊清單。
-   若要啟用應用程式中的元件及其裝載的 Dll、延伸模組、外掛程式或控制台，請將資訊清單納入為應用程式及其裝載元件中的資源。 應用程式和裝載元件中包含的資訊清單，應該各自描述元件的相依性。 一般來說，應用程式開發人員會將資訊清單加入至應用程式，而裝載的元件開發人員會將資訊清單新增至 DLL、延伸模組、外掛程式或控制台。

下列方法可用來將資訊清單加入至應用程式或 DLL、延伸模組、外掛程式或控制台的託管元件。

**在應用程式或裝載元件中啟用元件。**

1.  撰寫資訊清單，描述元件上的應用程式或擴充功能的相依性。

    例如，您可以複製下列範例資訊清單來建立 "YourApplication" 的資訊清單，並將正確的值取代為 **assemblyIdentity**、 **processorArchitecture** 和 **description**。 將 **processorArchitecture** 的值設定為 x86 （如果是在32位平臺上建立），如果是在64位平臺上建立則為 ia64。 **Description** 元素包含應用程式的選項描述。 如需資訊清單格式的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。

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

2.  在應用程式或類型 RT \_ 資訊清單識別碼2的延伸中建立資源。

    例如，如果應用程式的名稱是 YourApp，則應用程式應該包含下列內容：

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  使用-DISOLATION 感知啟用旗標來編譯應用程式 \_ \_ ，或在 \# 包含 "Windows .h" 語句之前插入此語句。 在具有多個模組的應用程式案例中， \_ \_ 所有模組都需要 DISOLATION 感知啟用旗標。

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  測試以確保應用程式所使用的元件在應用程式和裝載的元件中都能正常運作。

如需將元件新增至不含擴充功能之應用程式的詳細資訊，請參閱 [在不含擴充功能的應用程式中啟用元件](enabling-an-assembly-in-an-application-without-extensions.md)。

 

 



