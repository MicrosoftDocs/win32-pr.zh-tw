---
description: 這個範例示範如何在安裝元件時，使用自訂動作在本機電腦上建立使用者帳戶。
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: 使用自訂動作在本機電腦上建立使用者帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319607"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>使用自訂動作在本機電腦上建立使用者帳戶

這個範例示範如何在安裝元件時，使用自訂動作在本機電腦上建立使用者帳戶。 移除元件會移除自訂動作所建立的本機使用者帳戶。 示範數個自訂動作，包括 [延後執行自訂動作](deferred-execution-custom-actions.md) 和 [復原自訂動作](rollback-custom-actions.md)。

此範例符合下列規格。

-   安裝只會在執行 Windows 2000 時建立使用者帳戶。
-   只有在安裝元件以在本機執行時，安裝才會建立使用者帳戶。 這無法在元件修復或重新安裝期間建立使用者帳戶。
-   移除元件時，安裝程式會移除這些帳戶。
-   系統會從安裝資料庫中的自訂資料表讀取使用者帳戶資訊，而不是硬式編碼的自訂動作程式碼。
-   由於建立或移除使用者帳戶需要較高的許可權，因此某些自訂動作必須能夠對需要較高許可權的系統進行變更。 這些自訂動作必須是執行腳本時執行的延後自訂動作。
-   每個帳戶都有復原自訂動作，以確保帳戶會在元件安裝復原時移除。 這不包括在移除元件期間復原刪除帳戶。
-   自訂動作會傳送每個建立或移除的帳戶的 ActionData 訊息。 這不包括提供 ProgressBar 的進度訊息。
-   如果無法建立帳戶，自訂動作會報告錯誤。
-   帳戶的密碼是透過使用者與使用者介面互動，或在基本 UI 或無 [消費者介面層級](user-interface-levels.md)進行安裝的情況下取得，作為在命令列上傳遞的屬性。
-   記錄檔中會隱藏敏感性資料。

此範例包含名為 TestAccount 的假想元件。 下列各節中的討論會假設您已建立 TestAccount 所需的資源，並在安裝此元件所需的範例資料庫中撰寫了 [Feature](feature-table.md)、 [Component](component-table.md)、 [File](file-table.md)、 [Directory](directory-table.md)和 [FeatureComponents](featurecomponents-table.md) 資料表。 如需詳細資訊，請參閱 [安裝範例](an-installation-example.md)。

下列主題包含有關如何建立必要的自訂動作，並將其新增至安裝套件的資訊。

-   [撰寫自訂動作](authoring-the-custom-actions.md)
-   [新增自訂 CustomUserAccounts 資料表](adding-a-custom-customuseraccounts-table.md)
-   [撰寫 CustomAction 資料表](authoring-the-customaction-table.md)
-   [撰寫 ActionText 和錯誤資料表](authoring-the-actiontext-and-error-tables.md)
-   [撰寫 InstallExecuteSequence 資料表](authoring-the-installexecutesequence-table.md)
-   [撰寫密碼輸入的消費者介面](authoring-the-user-interface-for-password-input.md)
-   [保護安裝的安全](securing-the-installation.md)

 

 



