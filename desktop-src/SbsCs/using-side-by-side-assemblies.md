---
description: 使用下列程式開發新的應用程式，或更新現有的應用程式，以使用 Microsoft 或其他並存元件發行者提供的並存元件。
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: 使用並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141711"
---
# <a name="using-side-by-side-assemblies"></a>使用並存元件

使用下列程式開發新的應用程式，或更新現有的應用程式，以使用 Microsoft 或其他並存元件發行者提供的 [並存元件](about-side-by-side-assemblies-.md) 。 如需 Microsoft 目前提供的並存元件清單，請參閱 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。 請注意，應用程式必須至少在 Windows XP 上執行，才能將元件安裝為並存元件。 如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。

**將並存元件新增至應用程式**

1.  識別應用程式所需的並存元件。 從 Windows XP 開始，這些並存元件及其元件資訊清單都會與作業系統一起安裝，但不會進行全域註冊。
2.  使用 XML 編輯器來建立 [應用程式資訊清單](application-manifests.md)。 請參閱下面的範例應用程式資訊清單。 如需詳細資訊，請參閱[資訊清單檔案參考](manifest-files-reference.md)中的[應用程式資訊清單](application-manifests.md)。
3.  在可唯一定義應用程式的應用程式資訊清單的 [*DEF-CoNtext assemblyIdentity*](d-sbscs-gly.md) 子項目中輸入屬性值。 如需有關 DEF 內容 **assemblyIdentity** 的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。
4.  如果元件包含任何相依元件，請在應用程式資訊清單的對應 [*REF 內容 assemblyIdentity*](r-sbscs-gly.md) 子項目中輸入屬性值。 如需參考內容 **assemblyIdentity** 的詳細資訊，請參閱 [應用程式資訊清單](application-manifests.md)。

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  您可以將應用程式資訊清單包含在應用程式的二進位可執行檔標頭檔中。

    在此情況下，也請將下列程式程式碼新增至應用程式標頭檔：

    <dl> CREATEPROCESS \_ 資訊清單 \_ 資源 \_ 識別碼 RT \_ 資訊清單 "YourApp.exe .manifest"  
    </dl>

    或者，您可以將不同的資訊清單檔案放在與應用程式可執行檔相同的目錄中。 作業系統會先從檔案系統載入資訊清單，然後再檢查可執行檔的資源區段。 檔案系統版本優先。

6.  [共用的元件](/windows/desktop/Msi/shared-assemblies)應該使用[Windows Installer](../msi/windows-installer-portal.md)版本2.0 來安裝。 撰寫 Windows Installer 套件，[請參閱如何在 Windows XP 上安裝 Win32 元件以並存共用？](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)。
7.  您可以使用[Windows Installer](../msi/windows-installer-portal.md)版本2.0 來安裝[私用元件](/windows/desktop/Msi/private-assemblies)。 撰寫 Windows Installer 套件，如如何在[Windows XP 上安裝用於應用程式私用的 Win32 元件](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)中所述。 您也可以使用任何其他安裝程式，將私用元件及其資訊清單複製到與應用程式可執行檔相同的資料夾中。
8.  測試您的應用程式以確定結果。 請注意，您的測試電腦不應該註冊並存元件。
9.  將您的應用程式或更新部署為 Windows Installer 套件。

## <a name="example-application-manifest"></a>範例應用程式資訊清單

以下是應用程式資訊清單的範例：

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

 

 
