---
description: 您可以藉由安裝在產生 Patch 套件中建立的範例 patch MNP2000，將小更新套用至 MNP2000.msi 的系統管理來源映射。
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: 將修補套件套用至系統管理安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c29cbec604ae18745348a62f147d13d2ccbf06c0620b3a5dcca7c6c009045b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105438"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>將修補套件套用至系統管理安裝

您可以藉由安裝在 [產生 Patch 套件](generating-a-patch-package.md)中建立的範例 patch MNP2000，將小更新套用至 MNP2000.msi 的系統管理來源映射。 然後，您可以要求使用者從新的系統管理來源映射重新安裝應用程式，以將更新傳播給使用者。

系統管理員可以使用下列命令列，將位於//server/MNP2000.msi 的系統管理來源映射更新為新的來源映射，此映射與系統管理安裝從完整更新的 CD-ROM 產生的不同。

**msiexec/a//server/MNP2000.msi/p MNP2000 .msp**

使用 MNP2000 的工作組成員必須從新的系統管理來源映射重新安裝應用程式，才能接收更新。

若要完全重新安裝應用程式，並在使用者的電腦上快取更新的 .msi 檔案，使用者可以輸入下列其中一個命令。

**msiexec/fvomus//server/MNP2000.msi**

**msiexec/I//server/MNP2000.msi 重新安裝 = ALL REINSTALLMODE = vomus reinstall**

若只要重新安裝已更新的協同功能，並快取使用者電腦上更新的 .msi 檔案，則使用者可以輸入下列命令。

**msiexec/I//server/MNP2000.msi 重新安裝 = 協同 REINSTALLMODE = vomus reinstall**

## <a name="next-example"></a>下一個範例

[當地語系化範例](a-localization-example.md)

 

 



