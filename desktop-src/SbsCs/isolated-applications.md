---
description: 隔離的應用程式是與資訊清單一起安裝的自我描述應用程式。 隔離的應用程式可以同時使用私用元件和共用元件。
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: 隔離的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468904"
---
# <a name="isolated-applications"></a>隔離的應用程式

隔離的應用程式是與 [資訊清單](manifests.md)一起安裝的自我描述應用程式。 隔離的應用程式可以同時使用 [私用元件](/windows/desktop/Msi/private-assemblies) 和 [共用元件](/windows/desktop/Msi/shared-assemblies)。

如果應用程式的所有元件都是共用 [並存元件](about-side-by-side-assemblies-.md) 或私用元件，則會被視為完全隔離的應用程式。 如果它使用不是並存元件的部分元件，它就稱為部分隔離。 請注意，如果應用程式使用的部分元件並非並存元件，或使用私用元件，則應用程式可能會受到系統上其他應用程式的安裝或移除所影響。 如需詳細資訊，請參閱 [並存元件共用](side-by-side-assembly-sharing.md)。

開發人員建議您設計隔離的應用程式，並將現有的應用程式更新為隔離的應用程式，原因如下：

-   隔離的應用程式更穩定且可靠地更新，因為它們不會受到系統上其他應用程式的安裝、移除或升級所影響。
-   您可以設計隔離的應用程式，使其一律使用建立和測試時所用的相同元件版本來執行。
-   隔離的應用程式可以使用由 Microsoft 提供的並存元件所提供的功能。 如需詳細資訊，請參閱 [支援的 Microsoft 並存元件](supported-microsoft-side-by-side-assemblies.md)。
-   隔離的應用程式不會系結至其並存元件的出貨排程，因為應用程式和系統管理員可以在部署後更新設定，而不需要重新安裝應用程式。 在只有一個版本的元件可供使用的情況下，這並不適用。
-   您可以使用 **xcopy** 命令來安裝完全隔離的應用程式。 [Windows Installer](../msi/windows-installer-portal.md) 也可以用來安裝隔離的應用程式，而不會影響登錄。 如需詳細資訊，請參閱 [Win32 元件的安裝](../msi/installation-of-win32-assemblies.md)。

在某些情況下，現有的應用程式可以更新為隔離的應用程式，而不需要重寫應用程式程式碼。 您可以建立 [應用程式資訊清單](application-manifests.md) ，以描述應用程式對 [並存元件](about-side-by-side-assemblies-.md)的相依性。 如果應用程式使用非並存元件的元件，這些元件可能會部署為 [私](/windows/desktop/Msi/private-assemblies)用元件。 請注意，使用協力廠商元件來執行此操作的可能性可能取決於授權，因為元件必須撰寫為元件。 例如，藉由建立應用程式資訊清單，並指定對並存通用控制項的相依性 (COMCTL32.DLL) ，在 Windows XP 上執行的應用程式可以利用 Windows *主題*。 您應一律測試您的應用程式，以確保它與新版本的 COMCTL32.DLL 元件相容。

可能無法將每個現有的應用程式更新為完全隔離的應用程式。 例如，某些 [Windows 檔案保護 (WFP) ](/windows/desktop/Wfp/windows-resource-protection-portal) 系統元件無法以並存元件的方式提供，而且無法與應用程式一起安裝為私用元件。 您可以針對應用程式資訊清單中的部分應用程式元件指定並存元件相依性，以部分隔離這類應用程式。

 

 
