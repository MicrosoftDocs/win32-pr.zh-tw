---
description: 您可以藉由修補應用程式的本機安裝，將小型更新套用至應用程式。
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: 藉由修補產品的本機安裝來套用小型更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944029"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>藉由修補產品的本機安裝來套用小型更新

您可以藉由修補應用程式的本機安裝，將小型更新套用至應用程式。

**將小型更新修補程式套用至產品的本機安裝**

1.  從命令列或使用可執行檔啟動修補程式的安裝。 若要從命令列啟動，請使用 **msiexec/p patch。 msp 重新 \[ 安裝 =**_Feature list_ *_\] REINSTALLMODE = omus reinstall_*。 若要從可執行檔啟動，請呼叫 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或 [**ApplyPatch 方法**](installer-applypatch.md) ，並提供相同的命令列引數。
2.  修補用戶端安裝時，安裝程式會忽略安裝來源，並繼續修補使用者電腦上已安裝的檔案。
3.  安裝程式會將標示為執行來源的任何已修補元件，變更為在本機執行。 只要修補程式保留在電腦上，使用者就無法從來源執行這些元件。
4.  安裝程式會新增任何用來更新 .msi 檔案的轉換，或將修補程式特定的資訊新增至使用者的設定檔。
5.  安裝程式會將 .msi 檔案快取在使用者的電腦上，讓它可以執行隨選安裝、重新安裝及修復應用程式。 將修補程式套用至獨立安裝之後，安裝程式會參考兩個或多個來源清單至外部檔案：一個適用于原始來源，另一個則用於已套用的每個修補程式。

 

 



