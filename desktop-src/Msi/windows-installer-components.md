---
description: 元件是要安裝的應用程式或產品的一部分。
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Installer 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944527"
---
# <a name="windows-installer-components"></a>Windows Installer 元件

元件是要安裝的應用程式或產品的一部分。 元件的範例包括單一檔案、相關檔案的群組、COM 物件、註冊、登錄機碼、快捷方式、資源、群組在目錄中的程式庫，或共用程式碼段（例如 MFC 或 DAO）。

安裝程式服務會以單一一致的部分形式安裝或移除元件。 它會依 [元件資料表](component-table.md)的 [元件識別碼] 資料行中指定的個別元件識別碼 GUID 來追蹤每個元件。

> [!Note]  
> 共用相同元件識別碼的兩個元件會視為相同元件的多個實例，不論其實際內容為何。 只有任何元件的單一實例會安裝在使用者的電腦上。 因此，有幾個功能或應用程式可能會共用某些元件。

 

因為通常會共用元件，所以安裝套件的作者在指定功能或應用程式的元件時，必須遵守嚴格的規則。 這對於 Windows Installer 參考計數機制的正確作業而言是不可或缺的。 如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。

簡單來說，這些規則包括：

-   每個元件都必須儲存在單一資料夾中。
-   不應將任何檔案、登錄專案、快捷方式或其他資源以一個以上的元件的成員形式傳送。 這適用于各產品、產品版本和公司。

如需使用元件的詳細資訊，請參閱。

-   [安裝遺失的元件](installing-a-missing-component.md)
-   [安裝永久元件、檔案、字型、登錄機碼](installing-permanent-components-files-fonts-registry-keys.md)
-   [使用限定元件](using-qualified-components.md)
-   [使用可轉移的元件](using-transitive-components.md)
-   [使用功能和元件](working-with-features-and-components.md)
-   [撰寫大型封裝](authoring-a-large-package.md)
-   [檢查功能、元件、檔案的安裝](checking-the-installation-of-features-components-files.md)
-   [搜尋中斷的功能或元件](searching-for-a-broken-feature-or-component.md)
-   [發佈產品、功能和元件](publishing-products-features-and-components.md)

 

 



