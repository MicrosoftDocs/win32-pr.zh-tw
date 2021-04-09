---
description: 當您第一次使用 PATCH 屬性安裝應用程式時，可以套用 Windows Installer Patch (MSP) 。
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: 修補初始安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945325"
---
# <a name="patching-initial-installations"></a>修補初始安裝

當您第一次使用 [**patch**](patch.md) 屬性安裝應用程式時，可以套用 Windows Installer PATCH (MSP) 。

若要在第一次安裝應用程式時套用修補程式，則必須在命令列上設定 [**patch**](patch.md) 屬性。 在命令列上，將修補程式的完整路徑指定為 "PATCH = {*patch to patch*}" 屬性-值配對。

請注意，在命令列上指定 [**patch**](patch.md) 屬性會覆寫使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或/p [命令列選項](command-line-options.md)時所執行的修補程式適用性檢查。

如果使用 [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) 或/P [命令列選項](command-line-options.md)來套用修補程式，安裝程式會將目前安裝在電腦上的應用程式，與符合在 [**範本摘要**](template-summary.md) 屬性中接收修補程式的產品代碼清單進行比較。

當您在命令列上設定 [**PATCH**](patch.md) 屬性以在第一次安裝時安裝時，有資格接收修補程式的應用程式是由修補程式套件中內嵌之轉換的驗證條件所決定。 產生修補程式套件的建議方法是使用修補程式建立工具，例如 [Msimsp.exe](msimsp-exe.md) 和 [PATCHWIZ.DLL](patchwiz-dll.md)。 修補程式中轉換的驗證條件源自于 Patch 建立屬性 (. pcp) 檔案的 [TargetImages](targetimages-table-patchwiz-dll-.md) 資料表中的 ProductValidateFlags 資料行。

第一次使用命令列、另一個應用程式或腳本安裝應用程式時，可以套用修補程式。

以下顯示從命令列進行的第一次修補。

**msiexec/i** *package.msi* **PATCH =**_"c： \\ directory \\ PATCH .msp"_

以下顯示來自另一個應用程式的第一次修補。

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

以下顯示腳本的第一次修補。


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3.0 和更新版本： * *

從 Windows Installer 版本3.0 開始，在第一次安裝應用程式時，可以套用多個修補程式。 將 [**PATCH**](patch.md) 屬性設定為以分號分隔的修補程式完整路徑清單。 以下顯示從命令列的多個修補程式的第一次修補。

**msiexec/i** *package.msi* **PATCH =**_"c： \\ directory \\ PATCH .msp; c： \\ directory \\ patch2 .msp; c： \\ directory \\ patch3 .msp"_

 

 



