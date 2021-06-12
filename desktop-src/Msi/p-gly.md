---
description: 瞭解以字母 P 開頭的 Windows Installer 概念，例如封裝程式碼和修補。
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: 'P (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011100"
---
# <a name="p-windows-installer"></a>P (Windows Installer) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**包**
</dt> <dd>

[*.msi*](m-gly.md) 檔案，以及此檔案可能指向的任何 [*外部原始*](e-gly.md) 程式檔。 因此，套件包含 Windows Installer 執行 UI 以及安裝或卸載應用程式所需的所有資訊。 如需詳細資訊，請參閱 [*安裝程式資料庫*](i-gly.md)。

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**封裝程式碼**
</dt> <dd>

識別特定封裝的 GUID。 需要唯一的封裝程式碼，因為某些轉換或修補套件可以套用至多個應用程式，或者可以將應用程式升級到另一個應用程式或版本。 如需詳細資訊，請參閱 [封裝程式碼](package-codes.md)。

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**修補**
</dt> <dd>

更新檔案的方法，該檔案只會取代變更的位，而不是整個檔案。 這表示使用者可以下載產品的升級修補程式，而此產品遠小於整個產品。 如需詳細資訊，請參閱 [修補套件](patch-packages.md)。

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**修補檔案**
</dt> <dd>

用於修補的 P [atch 套件](patch-packages.md) 。 如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**預覽模式**
</dt> <dd>

用來查看 UI 設計的模式。 如需詳細資訊，請參閱 [預覽消費者介面](previewing-the-user-interface.md)。

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**進度列**
</dt> <dd>

控制安裝程式可以在腳本執行時間顯示，以代表安裝進度。 如需詳細資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)。

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**財產**
</dt> <dd>

在安裝期間使用的全域變數。  (查看 [屬性](about-properties.md)。 ) 

「屬性」一詞也指的是 automation 物件的屬性。  (請參閱 [Automation 介面](automation-interface.md)。 ) 

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**出版**
</dt> <dd>

[*廣告*](a-gly.md)功能或應用程式的方法。 發佈不會填入 UI。 但是，如果另一個應用程式嘗試開啟已發佈的應用程式，則安裝程式會有足夠的資訊來指派已發行的應用程式。 如需詳細資訊，請參閱 [*指派*](a-gly.md) 和 [元件和功能](components-and-features.md)。

</dd> </dl>

 

 



