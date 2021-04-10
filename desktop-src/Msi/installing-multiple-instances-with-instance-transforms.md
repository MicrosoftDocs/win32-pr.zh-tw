---
description: 本主題提供安裝或重新安裝使用實例轉換之多個實例安裝的指導方針。
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: 使用實例轉換安裝多個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026379"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>使用實例轉換安裝多個實例

本主題提供安裝或重新安裝使用實例轉換之多個實例安裝的指導方針。

-   當您安裝具有實例轉換的新實例時，請包含 **MSINEWINSTANCE** 屬性，並設定 **MSINEWINSTANCE**= 1。
-   當您安裝具有實例轉換的新實例時，請包含轉換屬性，並將轉換清單中的第一個轉換設定為變更產品代碼的實例轉換。 任何自訂轉換都應遵循此清單開頭的實例轉換。
-   起始維護安裝和重新安裝實例的最簡單方式，就是參考實例的產品代碼。 如果您使用封裝路徑起始維護安裝，您也必須指定實例的產品代碼。 從命令列使用/n {Product Code} 選項。 從程式碼或腳本中，使用 **MSIINSTANCEGUID** 屬性。

下列範例示範如何從命令列安裝新的實例，其中實例轉換的前面會加上冒號，以指定轉換內嵌于封裝中。

**msiexec/I mypackage.msi 轉換 =： instance。 mst MSINEWINSTANCE = 1/qb**

下列範例示範如何使用 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)安裝新的實例。

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

下列範例示範如何從腳本安裝新的實例。

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

下列範例會重新安裝實例，而不需要重新快取套件。 實例是由其產品代碼所參考 {00000001-0002-0000-0000-624474736554} 。

**msiexec/I {00000001-0002-0000-0000-624474736554} 重新安裝 = ALL REINSTALLMODE = omus reinstall/qb**

下列範例會重新安裝實例，並從命令列重新快取套件。 封裝路徑會參考此實例。 如果產品原本是隨著實例轉換而安裝，您只需要包含/n {Product Code} 選項。

**msiexec/I c： \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} 重新安裝 = ALL REINSTALLMODE = vomus reinstall/qb**

下列範例會使用 **MsiInstallProduct** 來重新安裝實例，並快取封裝。 封裝路徑會參考此實例。 您可以使用 **MSIINSTANCEGUID** 屬性來提供實例的產品代碼。

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

下列範例會重新安裝實例，並使用腳本來快取封裝。 您可以使用 **MSIINSTANCEGUID** 屬性來提供實例的產品代碼。

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

下列範例示範如何使用命令列通告實例。

**msiexec/jm mypackage.msi/t： instance. mst/c/qb**

下列範例示範如何使用 **MsiAdvertiseProductEx** 來安裝以公告實例。

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

下列範例顯示如何從命令列將修補程式套用至實例。 如果產品原本是隨著實例轉換而安裝，您只需要包含/n {Product Code} 選項。

**msiexec/p mypatch .msp/n {00000001-0002-0000-0000-624474736554} /qb**

下列範例示範如何使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)將修補程式套用至實例安裝。

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

如需詳細資訊，請參閱 [安裝多個產品的實例和修補程式](installing-multiple-instances-of-products-and-patches.md) ，並 [使用實例轉換來撰寫多個實例](authoring-multiple-instances-with-instance-transforms.md)。

 

 



