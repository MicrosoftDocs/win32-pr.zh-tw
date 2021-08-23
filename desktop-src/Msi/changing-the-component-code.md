---
description: 當您指定安裝的元件時，套件作者應遵循將應用程式組織成元件中所述之元件組織的一般規則。
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: 變更元件程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96217dbcdbdc63d444f95d73dec657cf1a5ddef4ed80128c85b7752e1ec0f0d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520198"
---
# <a name="changing-the-component-code"></a>變更元件程式碼

當您指定安裝的 [元件](windows-installer-components.md) 時，套件作者應遵循將 [應用程式組織成元件](organizing-applications-into-components.md)中所述之元件組織的一般規則。 作者可能需要引進新元件或修改現有的元件。 如果新增、移除或修改資源實際上會建立新的元件，則元件程式碼也必須變更。

## <a name="creating-a-new-component"></a>建立新元件

引進新元件，並在進行下列任何變更時，為它指派唯一的元件程式碼：

-   測試未顯示的任何變更與舊版元件相容。 在此情況下，您也必須變更元件中每個資源的名稱或目標位置。
-   元件中任何檔案、登錄機碼、快捷方式或其他資源之名稱或目標位置的變更。 在此情況下，您也必須變更元件中每個資源的名稱或目標位置。
-   從元件新增或移除任何檔案、登錄機碼、快捷方式或其他資源。 在此情況下，您也必須變更元件中每個資源的名稱或目標位置。
-   將32位元件重新編譯成64位元件。

引進新元件時，作者必須執行下列其中一項動作，以確保元件不會與任何現有的元件衝突：

-   將任何可能安裝的資源名稱或目標位置，變更為其他元件的相同名稱和目標位置。
-   否則，保證新元件永遠不會安裝在與另一個元件相同的資料夾中，而該元件具有一般名稱和位置下的資源。 這包括具有相同檔案名的檔案當地語系化版本。 如需詳細資訊，請參閱 [元件規則中斷時，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)。
-   變更現有元件的元件程式碼時，也請變更元件中每個檔案、登錄機碼、快捷方式和其他資源的名稱或目標位置。

### <a name="creating-a-new-version-of-a-component"></a>建立新版本的元件

新版本的元件會被指派與另一個現有元件相同的元件程式碼。 在下列情況下，修改元件而不變更元件程式碼是選擇性的：

-   對元件所做的變更已經過測試，可與所有舊版元件回溯相容。
-   作者可以保證新版本的元件永遠不會安裝在系統上，因為它會與舊版元件或需要舊版的應用程式發生衝突。 如需詳細資訊，請參閱 [元件規則中斷時，會發生什麼事？](what-happens-if-the-component-rules-are-broken.md)。

當新版本的元件產生兩個元件共用資源時（例如登錄值、檔案或快捷方式），不能變更元件的元件代碼。

 

 



