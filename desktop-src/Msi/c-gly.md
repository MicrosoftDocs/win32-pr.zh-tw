---
description: 瞭解以字母 C 為開頭的 Windows Installer 概念，例如封包檔和總和檢查碼。
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: 'C (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010921"
---
# <a name="c-windows-installer"></a>C (Windows Installer) 

[](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**封包檔**
</dt> <dd>

單一檔案，通常會有 .cab 副檔名，可將壓縮檔案儲存在檔案庫中。 封包格式是封裝多個檔案的有效方式，因為壓縮會跨檔案界限執行，大幅改善壓縮率。 如需建立封包的相關資訊，請參閱封 [包](cabinet-files.md)檔。

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**校驗**
</dt> <dd>

相依于檔案內容的計算值。 它會與資料一起儲存，以偵測檔案損毀。 系統會檢查此值，以確保資料不會被損壞。

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**元件**
</dt> <dd>

安裝程式所處理的最小部分安裝，也是來自程式設計人員觀點的應用程式或功能的組建區塊。 元件的範例包括一組相關的檔案、COM 物件或程式庫。 如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**認可資料庫**
</dt> <dd>

在資料庫中進行的累積變更。 在資料庫認可之前，這些變更不會反映在實際的資料庫中。 如需詳細資訊，請參閱認可 [資料庫](committing-databases.md)。

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**
</dt> <dd>

安裝程式使用者介面的功能層面。 一般的 ControlEvent 會在啟動對話方塊控制項或其他事件時，觸發安裝程式的一些動作。 如需詳細資訊，請參閱 [ControlEvent 總覽](controlevent-overview.md)。

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**成本**
</dt> <dd>

安裝程式用來判斷安裝磁碟空間需求的方法。 成本考慮會考慮是否需要覆寫現有的檔案。 如需詳細資訊，請參閱檔案 [成本](file-costing.md)。

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub 檔案**
</dt> <dd>

儲存和提供 ICE 自訂動作存取權的驗證模組。 如需詳細資訊，請參閱 [範例 .cub](sample--cub-file.md)檔。 如需詳細資訊，請參閱也 [Windows Installer 的副檔名](windows-installer-file-extensions.md)。

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**自訂動作**
</dt> <dd>

由 [*封裝*](p-gly.md) 的作者所撰寫，但不是以標準動作的形式內建在安裝程式中。 如需詳細資訊，請參閱 [自訂動作](custom-actions.md)。

</dd> </dl>

 

 



