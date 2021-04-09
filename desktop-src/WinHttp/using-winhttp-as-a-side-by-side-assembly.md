---
description: 在 Windows Server 2003 上，WinHTTP 會實作為並存元件，而且必須連結到。 請注意，這並不適用于 Windows Vista 和更新版本。
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: 使用 WinHTTP 作為並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690432"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>使用 WinHTTP 作為並存元件

在 Windows Server 2003 上，WinHTTP 會實作為並存元件，而且必須連結到。 請注意，這並不適用于 Windows Vista 和更新版本。

## <a name="side-by-side-assemblies"></a>並存元件

從 Microsoft Windows XP 開始，提供並存元件機制來控制執行時間連結，以避免動態連結程式庫 (DLL) 版本控制衝突。 如需並存元件的詳細資訊，請參閱 [關於隔離應用程式和並存元件](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)。

若要使用此機制連結至 Windows Server 2003 上的 WinHTTP 5.1 版，應用程式必須併入指定 WinHTTP 作為相依元件的資訊清單。 如需如何進行這項操作的詳細資訊，請參閱 [使用並存元件](/windows/desktop/SbsCs/using-side-by-side-assemblies) 。

## <a name="a-sample-winhttp-application-manifest"></a>範例 WinHTTP 應用程式資訊清單

以下範例資訊清單說明可用來連結至 WinHTTP 的應用程式資訊清單。

"" 的 "type" 以外的所有屬性都 <assembly> <assemblyIdentity> 必須適當地針對您的特定應用程式加以修改。 " &lt; Description" 元素的內容也是相同的 &gt; 。

此外，請確定 "" 的 "processorArchitecture" 屬性 <dependentAssembly> <assemblyIdentity> 符合 "" 的 "processorArchitecture" 屬性 <assembly> <assemblyIdentity> 。 例如，在下列兩者都設定為 "x86"。

所有不是您應用程式特有的值都應該採用如下所示的表單。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
