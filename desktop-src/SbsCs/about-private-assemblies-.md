---
description: 私用元件是與應用程式一起部署的元件，可用於該應用程式的獨佔用途。
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: 關於私用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c785b30ca8654071a9816aaf9a11ecc69a029f605d06f39f44a6a490a2a7aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142611"
---
# <a name="about-private-assemblies"></a>關於私用元件

私用元件是與應用程式一起部署的元件，可用於該應用程式的獨佔用途。 亦即，其他應用程式不會共用私用元件。 私用元件是可以用來建立 [隔離應用程式](isolated-applications.md)的其中一個方法。 如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](about-isolated-applications-and-side-by-side-assemblies.md)。

私用元件必須設計成與系統上的其他元件版本並存運作。 如需詳細資訊，請參閱 [建立並存元件的指導方針](guidelines-for-creating-side-by-side-assemblies.md)。

私用元件必須伴隨著 [組件資訊清單](assembly-manifests.md)。 請注意，封裝 DLL 做為私用元件時，會套用名稱限制，以配合 Windows 搜尋私用元件的方式。 搜尋私用元件時，建議的方法是在 DLL 中包含組件資訊清單做為資源。 在此情況下，資源識別碼必須等於1，而且私用元件的名稱可能與 DLL 的名稱相同。 例如，如果 DLL 的名稱是 MICROSOFT.WINDOWS.MYSAMPLE.DLL，則資訊清單的 **assemblyIdentity** 專案中所使用之 name 屬性的值也可能是 Microsoft。Windows. mysample。 搜尋私用元件的另一種方法是在不同的檔案中提供組件資訊清單。 在此情況下，元件的名稱及其資訊清單必須與 DLL 的名稱不同。 例如，Microsoft。Windows mysampleAsm，Microsoft。Windows mysampleAsm 資訊清單，並 Microsoft.Windows.mysample.dll。 如需如何並存搜尋私用元件的詳細資訊，請參閱 [元件搜尋序列](assembly-searching-sequence.md)。

私用元件會安裝在應用程式目錄結構的資料夾中。 通常，這是包含應用程式可執行檔的資料夾。 私用元件可以部署在與應用程式相同的資料夾中、與元件同名的資料夾中，或是在與元件同名的特定語言子資料夾中。 例如，您可以使用下列其中一個目錄結構來部署私用元件，也就是未指定任何語言的工具。



| 目錄結構                                       | 描述                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| APPDIR \\MICROSOFT.TOOLS.POP.DLL                           | 資訊清單會部署為 DLL 中的資源。                                                     |
| Appdir \\ Microsoft. 資訊清單                      | 資訊清單會部署為個別的檔案。                                                           |
| APPDIR \\ MICROSOFT。工具。POP \\MICROSOFT.TOOLS.POP.DLL      | 資訊清單會部署為 DLL 中的資源，該 DLL 位於具有元件名稱的子資料夾中。 |
| Appdir microsoft 工具。 pop \\ \\ 。 | 資訊清單會在具有元件名稱的子資料夾中部署為個別的檔案。                 |



 

> [!IMPORTANT]
>
> 在 Windows 7 和 Windows Server 2008 R2 之前的 Windows 作業系統版本中，必須將原生私用元件部署在包含應用程式可執行檔的資料夾中。 原生私用元件不支援安裝在特定語言的資料夾或與元件同名的資料夾中。

 

您可以使用下列其中一個目錄結構，以指定的語言部署私用元件。 在下列範例中，Microsoft 所使用的語言是英文 (美國) ，而語言代碼則是 en-us。 您應以正確的 DHTML 語言代碼取代您的元件。

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

可以將元件的檔案複製到這個資料夾中的任何安裝方法（例如 **xcopy** 命令）來安裝私用元件。 如需有關如何使用 Windows Installer 安裝私用元件的詳細資訊，請參閱[Win32 元件的安裝](../msi/installation-of-win32-assemblies.md)。

私用元件也可以安裝在早于 Windows XP 的作業系統上。 在此情況下，必須在這些作業系統上註冊元件，而不會使用資訊清單。 私用元件的複本會安裝到私人資料夾中，以供應用程式專用使用。 另一個版本的元件可以在系統上全域登錄，並且可供任何系結至該元件的應用程式使用。 元件的全域版本可能是隨應用程式安裝的版本，或是較早的版本。 如需詳細資訊，請參閱[Windows 上的 DLL/COM](dll-com-redirection-on-windows.md)重新導向。 元件也可以安裝為共用元件，供多個應用程式使用。 如需詳細資訊，請參閱 [共用的元件](/windows/desktop/Msi/shared-assemblies)。

請注意，建立私用元件的步驟與建立共用元件的步驟相同，但有兩個例外：

-   不需要簽署私用元件，也不需要在組件資訊清單的 **assemblyIdentity** 元素中使用 **publickeyToken** 。
-   您可以使用任何安裝技術，將私用元件安裝到應用程式的資料夾中。 私用元件不需要使用 Windows Installer 安裝。

 

 
