---
description: 發行者設定檔會全域重新導向應用程式和元件相依于並存元件的一個版本，以使用相同元件的另一個版本。
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: 發行者設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194537"
---
# <a name="publisher-configuration"></a>發行者設定

[發行者設定檔](publisher-configuration-files.md)會全域重新導向應用程式和元件相依于並存元件的一個版本，以使用相同元件的另一個版本。 這可讓應用程式和元件使用更新的元件，而不需要重建所有受影響的應用程式。

[發行者設定檔](publisher-configuration-files.md) 可能會在發行具有相容錯誤修正或安全性更新的新版本元件時，由元件發行者提供。 更新後的版本應該完全相容。 除非更新完全相容，否則不應該使用發行者設定檔來新增功能。 發行者設定檔絕不能用來遞增元件的主要或次要版本。 例如，請勿將元件版本6.0.0.0 重新導向至7.0.0.0 或6.1.0.0。

發行者設定檔案只應由元件的發行者發出。 元件開發人員應該簽署共用的並存元件和發行者設定檔案。 使用相同的金鑰來簽署元件和相關聯的發行者設定檔。 發行者設定檔應該使用與元件所用的相同工具來簽署，請參閱 [元件簽署範例](assembly-signing-example.md) 和 [建立簽署的檔案和目錄](creating-signed-files-and-catalogs.md)。

一般來說，元件的新版本和相關聯的發行者設定檔將會安裝在 service pack 更新中。 因為安裝發行者設定檔案會全域重新導向系統上的元件，所以永遠不應該將應用程式提供給發行者設定檔案作為可轉散發套件。 如果要更新的元件是以可轉散發套件的形式提供，發行者應提供下列兩者。

-   Windows Installer 封裝 ( .msi 檔案) ，其中包含具有發行者設定的新元件版本。 這可能會安裝為 service pack 或 QFE，因為在此情況下，客戶已選擇全域更新系統。 應用程式永遠不會安裝此套件版本。
-   Windows Installer merge 模組 ( .msm 檔案) 只包含新版本的元件。 此版本可能包含在應用程式中。

需要最低版本元件的應用程式應該在最低版本上陳述其相依性，如果系統上的最小版本無法使用，則應用程式將無法啟動。 如果是可轉散發套件，則應該包含在應用程式安裝程式中。

例如，安裝下列 [發行者設定檔](publisher-configuration-files.md) 會將系結從 SampleAssembly 的2.0.0.0 版重新導向至版本2.0.1.0。 這會將名為1.1.0.0 的新原則新增至% systemDrive% \\ windows \\ winsxs 原則 \\ x86 \\ SampleAssembly \_ \_ 75e377300ab7b886 \_ x-ww \_ < *hashvalue*>。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

針對相同元件安裝下列發行者設定檔，會將 SampleAssembly 的版本2.0.0.0 的系結重新導向至版本2.0.3.0。 這會將名為2.1.0.0 的另一個原則新增至% systemDrive% \\ windows \\ winsxs 原則 x86 SampleAssembly \\ \\ \_ \_ 75e377300ab7b886 \_ x-x-ww \_ < *hashvalue*>。

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



