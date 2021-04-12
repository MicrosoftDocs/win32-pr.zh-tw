---
description: 您可以將小型更新套用至 MNP2000 的本機安裝，並使用在產生 Patch 套件中建立的 patch MNPpatch 範例。
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: 將修補程式套件套用至本機安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192465"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>將修補程式套件套用至本機安裝

您可以將小型更新套用至 MNP2000 的本機安裝，並使用在 [產生 Patch 套件](generating-a-patch-package.md)中建立的 patch MNPpatch 範例。 藉 [由修補產品的本機安裝](applying-small-updates-by-patching-the-local-installation-of-the-product.md)，在套用 Small update 一節中討論一般程式。

將原始 MNP2000 產品安裝在本機電腦上。 請確認此錯誤 Concert.txt 小型更新要修正的錯誤。 接著輸入下列命令列來啟動安裝。

**msiexec/p MNP2000 .msp 重新安裝 = ALL REINSTALLMODE = omus reinstall**

重新檢查屬於 MNP2000 的 Concert.txt，以確認安裝程式已套用 small update 來修正此檔案。

若要將小更新套用至系統管理映射，請參閱將 [修補套件套用至系統管理安裝](applying-a-patch-package-to-an-administrative-installation.md)。

[繼續](applying-a-patch-package-to-an-administrative-installation.md)

 

 



