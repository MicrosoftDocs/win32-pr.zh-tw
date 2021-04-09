---
description: 主要升級可以套用至應用程式，方法是從命令列或使用可執行檔來修補應用程式的本機安裝。
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: 藉由修補產品的本機安裝來套用主要升級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848973"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>藉由修補產品的本機安裝來套用主要升級

主要升級可以套用至應用程式，方法是從命令列或使用可執行檔來修補應用程式的本機安裝。

> [!Note]  
> 不建議將主要升級提供為修補程式套件，因為主要升級修補程式套件無法與其他更新一起排序，且修補程式不是 [可卸載修補](uninstallable-patches.md)程式。 [Msimsp.exe](msimsp-exe.md)公用程式無法用來產生套用主要升級的修補程式套件。 相反地，請依照 [安裝產品的主要升級](applying-major-upgrades-by-installing-the-product.md)所述，套用主要升級。

 

**將主要升級修補程式套用至產品的本機安裝**

1.  從命令列或使用可執行檔啟動修補程式的安裝。 若要從命令列啟動，請使用 msiexec/p patch .msp。 若要從可執行檔啟動，請呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或 [**ApplyPatch 方法**](installer-applypatch.md) ，並提供相同的命令列引數。
2.  修補用戶端安裝時，安裝程式會忽略安裝來源，並繼續修補使用者電腦上已安裝的檔案。
3.  安裝程式會將標示為執行來源的任何已修補元件，變更為在本機執行。 只要修補程式保留在電腦上，使用者就無法從來源執行這些元件。
4.  安裝程式會新增任何用來更新 .msi 檔案的轉換，或將修補程式特定的資訊新增至使用者的設定檔。
5.  安裝程式會將 .msi 檔案快取在使用者的電腦上，讓它可以執行隨選安裝、重新安裝及修復應用程式。 將修補程式套用至獨立安裝之後，安裝程式會參考兩個或多個來源清單至外部檔案：一個適用于原始來源，另一個則用於已套用的每個修補程式。

 

 



