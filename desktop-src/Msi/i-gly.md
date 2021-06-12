---
description: 瞭解以字母 I 開頭的 Windows Installer 概念，例如匯入位址表格和安裝層級。
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: '我 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010651"
---
# <a name="i-windows-installer"></a>我 (Windows Installer) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**idt 檔案**
</dt> <dd>

匯出的安裝程式資料庫資料表。 如需詳細資訊，請參閱匯 [入和匯出](importing-and-exporting.md) 和 [Windows Installer 副檔名](windows-installer-file-extensions.md)。

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**匯入位址表 (IAT)**
</dt> <dd>

從所有 Dll 匯入的每個函式都會儲存計算的虛擬位址。

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**內部使用者介面**
</dt> <dd>

安裝程式的內建功能，可以用來撰寫圖形化 UI 以進行安裝。 作者可以選擇 [*外部使用者介面*](e-gly.md)。 如需詳細資訊，請參閱 [關於消費者介面](about-the-user-interface.md)。

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**安裝層級**
</dt> <dd>

指定的安裝值。 只有當應用程式的層級小於或等於安裝層級時，才會安裝應用程式。 因此，您可以藉由改變安裝層級來變更安裝所選擇的應用程式集。 如需詳細資訊，請參閱 [功能表](feature-table.md)。

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**隨選安裝**
</dt> <dd>

依使用者或其他應用程式的要求安裝應用程式或功能的服務。 [*廣告*](a-gly.md) 讓功能或應用程式可用於隨選安裝。 如需詳細資訊，請參閱： [隨選安裝](installation-on-demand.md)。

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**安裝內容**
</dt> <dd>

安裝許可權與安裝類型的組合會產生三個不同的安裝內容：每位使用者的非受控、每位使用者管理，以及每部電腦管理的內容。 每一部電腦都沒有這類的非受控功能。

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**安裝**
</dt> <dd>

[*Windows Installer*](m-gly.md)。

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**安裝程式資料庫**
</dt> <dd>

關係資料庫，其中包含安裝的安裝指示。 安裝程式資料庫會儲存在 [*.msi*](m-gly.md)檔案中。 如需詳細資訊，請參閱 [安裝程式資料庫](installer-database.md)。

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**安裝程式函數**
</dt> <dd>

由使用者或應用程式呼叫，以取得安裝程式服務和功能。 這是安裝程式的應用程式開發介面。 如需詳細資訊，請參閱 [安裝程式函數參考](installer-function-reference.md)。

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**安裝程式套件 authoring tool**
</dt> <dd>

可讓開發人員建立和編輯 [*.msi*](m-gly.md)檔案的軟體。 這與任何 [*外部來源*](e-gly.md) 檔案都包含一個 [*套件*](p-gly.md) ，其中包含安裝所需的所有資訊。

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**內部來源檔案**
</dt> <dd>

儲存在 [*.msi*](m-gly.md)檔案中。 您可以將多個內部來源檔案壓縮並儲存在儲存在 .msi 檔案中的封 [*包*](c-gly.md) 檔中。

</dd> </dl>

 

 



