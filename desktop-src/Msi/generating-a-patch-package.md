---
description: 產生 patch 封裝的建議方法是使用修補程式建立工具，例如 Msimsp.exe 在 Patchwiz.dll 中呼叫 UiCreatePatchPackage。 Windows Installer SDK 中提供 Msimsp.exe 和 PatchWiz.dll。
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: 產生 Patch 封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944545"
---
# <a name="generating-a-patch-package"></a>產生 Patch 封裝

產生 patch 封裝的建議方法是使用修補程式建立工具，例如[Msimsp.exe](msimsp-exe.md)在[Patchwiz.dll](patchwiz-dll.md)中呼叫[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 。 Windows Installer SDK 中提供 Msimsp.exe 和 PatchWiz.dll。

下列命令列範例會使用 Msimsp.exe，以及在 [建立修補程式建立屬性](creating-a-patch-creation-properties-file.md) 檔案時所建立的 pcp 檔案，以產生範例修補套件 MNP2000 .msp。

**Msimsp.exe-s C： \\ note \_ installer \\ patch \\ MNP2000. pcp-p C： \\ Note \_ installer \\ patch \\ MNP2000 .msp**

撰寫的修補程式建立工具可能會藉由呼叫 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 來產生 patch 封裝，如下所示。

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[繼續](applying-a-patch-package-to-a-local-installation.md)

 

 



