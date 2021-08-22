---
description: 如果您的應用程式未裝載 DLL、延伸模組、外掛程式或控制台，您可以使用本節所述的方法來啟用應用程式的元件。
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: 在不含擴充功能的應用程式中啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142251"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>在不含擴充功能的應用程式中啟用元件

如果您的應用程式未裝載 DLL、延伸模組、外掛程式或控制台，您可以使用本節所述的方法來啟用應用程式的元件。 如需將元件新增至具有擴充功能之應用程式的詳細資訊，請參閱 [在裝載 DLL、副檔名或主控台的應用程式中啟用元件](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md)。

**若要在應用程式中啟用元件，而不使用任何託管元件**

1.  撰寫資訊清單，描述元件上的應用程式或擴充功能的相依性。

    例如，您可以複製下列範例資訊清單來建立 "YourApplication" 的資訊清單，並將正確的值取代為 **assemblyIdentity**、 **processorArchitecture** 和 **description**。 將 **processorArchitecture** 的值設定為 x86 （如果在32位平臺上建立），並將設定為 ia64 （如果在64位平臺上建立）。 **Description** 元素包含應用程式的選項描述。 如需資訊清單格式的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。

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

2.  將資訊清單新增至應用程式，做為應用程式二進位可執行檔標頭檔中的資源。 不建議您將資訊清單以外部資訊清單檔的形式新增至應用程式。

    若要將資訊清單新增為資源，請在類型 RT \_ 資訊清單識別碼1的應用程式中建立資源。 例如，如果應用程式的名稱是 YourApp，則應用程式的標頭檔應該包含下列內容：

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    如果您改為新增資訊清單做為外部資訊清單檔案，請確定安裝會將資訊清單檔案複製到包含應用程式可執行檔的資料夾中。

3.  測試以確保應用程式所使用的元件在應用程式中正確運作。

 

 



