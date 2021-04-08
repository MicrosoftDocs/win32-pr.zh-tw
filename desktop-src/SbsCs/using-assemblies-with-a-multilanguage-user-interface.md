---
description: 如果您希望應用程式的使用者或核心 DLL 能夠變更使用者介面的語言，您應該考慮將語言資源放在不同的附屬資源 Dll 中。
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: 使用具有多語系消費者介面的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690151"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>使用具有多語系消費者介面的元件

如果您希望應用程式的使用者或核心 DLL 能夠變更使用者介面的語言，您應該考慮將語言資源放在不同的附屬資源 Dll 中。 如需使用附屬資源 Dll 的詳細資訊，請參閱 [ (MUI) 的多語言消費者介面 ](/windows/desktop/Intl/multilingual-user-interface)。

每個附屬 DLL 都包含不同語言的資源。 核心 DLL 可作為元件提供，而且每個附屬 Dll 都可以提供為個別的附屬元件。 在此情況下，每個附屬元件都應該有自己的自我描述組件資訊清單。 附屬元件的資訊清單不應描述其他元件的任何相依性。 其他元件上附屬元件的任何相依性，應該改為在核心元件的資訊清單中描述。

[多語系消費者介面 (MUI) ](/windows/desktop/Intl/multilingual-user-interface)版本的 Windows，可讓使用者根據其喜好設定指定使用者介面語言，前提是已在系統中新增必要的語言。 核心元件可使用多個 MUI 元件來支援多種語言。 在此情況下，每個 MUI 元件都應該有自己的資訊清單，而其他元件的任何相依性應該只在核心元件的資訊清單中描述。

例如，Proseware 可能是相依于 Proseware. SampleAssembly 元件的核心並存元件，而此元件則會發生。 如果 Proseware 使用 MUI 來支援多種語言，則可以為每種語言提供個別的 MUI 元件。 每個 MUI 元件都應該有自己的資訊清單，描述這個特定的附屬資源 DLL。 MUI 元件資訊清單不應包含其他元件之相依性的任何參考。 描述核心元件 Proseware 的資訊清單應該描述 Proseware 的相依性。 Proseware. SampleAssembly 元件上的 Pop。

附屬元件之 **assemblyIdentity** 元素的屬性與基底元件資訊清單中的屬性類似。 **Name** 屬性應該與基底元件相同，並加入「資源」。 例如，如果基底元件中的名稱是 "Proseware. 拼字檢查"，則資源元件中的名稱會是 "Proseware. 拼字檢查. 資源"。 **Language** 屬性應該識別資源元件的語言。 **檔** 屬性應該包含屬於資源 dll 的檔案清單。

下列是 Proseware 資訊清單的範例，例如拼字檢查。執行時間程式庫資源元件的資訊清單。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

基底元件描述資源元件的選擇性相依性。 在此範例中，如果使用者執行的 Windows 具有指定為德文的地區設定，則使用 Proseware 拼字檢查元件的應用程式會顯示德文中的文字。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
