---
description: 產生 patch 封裝的建議方法是使用修補程式建立工具，例如 Msimsp.exe 在 Patchwiz.dll 中呼叫 UiCreatePatchPackage。 Windows Installer SDK 中提供 Msimsp.exe 和 PatchWiz.dll。
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: 產生 Patch 封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581428"
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

 

 



