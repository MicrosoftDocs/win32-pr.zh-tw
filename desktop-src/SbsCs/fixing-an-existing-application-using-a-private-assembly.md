---
description: 從 Windows XP 開始，您可以建立私用元件，並將它提供給特定的應用程式使用。
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: 使用私用元件來修正現有的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026160"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>使用私用元件來修正現有的應用程式

從 Windows XP 開始，您可以建立私用元件，並將它提供給特定的應用程式使用。 這項功能可以用來修正與更新不相容的應用程式。 例如，在升級作業系統之後，應用程式會變成與最新版 MSVCRT.DLL 不相容的應用程式。 在此情況下，您沒有取代系統版本的選項，因為 MSVCRT.DLL 是 Windows 受保護的檔案。 您可以建立 MSVCRT.LIB 的私用元件，並將其安裝在您的應用程式資料夾中，而不需要重寫應用程式來使用新版 MSVCRT.LIB。 請注意，並非每個共用元件都是私用並存元件的適當候選元件，而某些元件具有可安裝其元件之位置的授許可權制。 此元件必須符合並存元件的準則。 如果可提供適當的元件，請詢問元件的發行者。

私用元件的資訊清單和應用程式資訊清單都應該安裝在與應用程式可執行檔相同的資料夾中。 當應用程式執行時，它會查閱應用程式資訊清單，並載入應用程式私用的 MSVCRT.LIB 版本。

在此範例中，私用元件會同時包含 MSVCRT.DLL 和 MSVCIRT.DLL，如下列組件資訊清單所示：

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

以下是可能的應用程式資訊清單範例。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



