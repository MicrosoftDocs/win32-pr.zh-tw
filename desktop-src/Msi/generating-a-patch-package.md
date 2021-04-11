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
# <a name="generating-a-patch-package"></a><span data-ttu-id="b5537-104">產生 Patch 封裝</span><span class="sxs-lookup"><span data-stu-id="b5537-104">Generating a Patch Package</span></span>

<span data-ttu-id="b5537-105">產生 patch 封裝的建議方法是使用修補程式建立工具，例如[Msimsp.exe](msimsp-exe.md)在[Patchwiz.dll](patchwiz-dll.md)中呼叫[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5537-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="b5537-106">Windows Installer SDK 中提供 Msimsp.exe 和 PatchWiz.dll。</span><span class="sxs-lookup"><span data-stu-id="b5537-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="b5537-107">下列命令列範例會使用 Msimsp.exe，以及在 [建立修補程式建立屬性](creating-a-patch-creation-properties-file.md) 檔案時所建立的 pcp 檔案，以產生範例修補套件 MNP2000 .msp。</span><span class="sxs-lookup"><span data-stu-id="b5537-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="b5537-108">**Msimsp.exe-s C： \\ note \_ installer \\ patch \\ MNP2000. pcp-p C： \\ Note \_ installer \\ patch \\ MNP2000 .msp**</span><span class="sxs-lookup"><span data-stu-id="b5537-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="b5537-109">撰寫的修補程式建立工具可能會藉由呼叫 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 來產生 patch 封裝，如下所示。</span><span class="sxs-lookup"><span data-stu-id="b5537-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="b5537-110">繼續</span><span class="sxs-lookup"><span data-stu-id="b5537-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



