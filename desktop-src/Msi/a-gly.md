---
description: 瞭解以字母 A 開始的 Windows Installer 概念，例如協助工具和取得階段。
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: " (Windows Installer) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011121"
---
# <a name="a-windows-installer"></a> (Windows Installer) 

[B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [](u-gly.md) [W X](v-gly.md) Y Z

<dl> <dt>

<span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**工具**
</dt> <dd>

讓所有使用者都能存取安裝程式之使用者介面的設計實行。 如需協助工具的詳細資訊，請參閱總覽主題： [協助工具](accessibility.md)。

</dd> <dt>

<span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**取得階段**
</dt> <dd>

安裝程式用來決定程式的安裝階段。 取得階段會在應用程式或使用者指示 [*Windows Installer*](m-gly.md) 安裝應用程式或功能時開始。 然後，安裝程式會在資料庫產生安裝的 [*執行腳本*](e-gly.md)時，查詢 [*資料庫*](i-gly.md)中的資訊。 如需有關安裝階段的詳細資訊，請參閱 [安裝機制](installation-mechanism.md)。

</dd> <dt>

<span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**行動**
</dt> <dd>

Windows Installer 所執行的許多函數都會封裝至動作中。 每個動作都會指定特定函式的執行，而安裝程式的總程式流程則是依 [*順序資料表*](s-gly.md)中的動作順序來指定。 Windows Installer 中內建 [*標準動作*](s-gly.md)。 [*自訂動作*](c-gly.md) 是由安裝 [*套件*](p-gly.md)的作者所撰寫。

</dd> <dt>

<span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**管理核准模式**
</dt> <dd>

使用者帳戶保護所啟用的核准狀態 (UAC) ，以最小許可權（包括系統管理員）執行所有使用者。 使用者必須提供同意，才能提升需要系統管理員許可權的安裝。

</dd> <dt>

<span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**廣告**
</dt> <dd>

能夠讓載入所需的介面，並讓應用程式可供使用，而不需要安裝應用程式。 當使用者或應用程式啟動已公告的介面時，安裝程式就會繼續安裝必要的元件。 這兩種類型的廣告是 [*指派*](/windows) 和 [*發佈*](p-gly.md)的。 如需詳細資訊，請參閱 [*隨選安裝*](i-gly.md)。 如需安裝程式如何通告應用程式的詳細資訊，請參閱 [公告](advertisement.md)。

</dd> <dt>

<span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**應用程式資訊服務 (AIS)**
</dt> <dd>

Windows Vista 的系統服務，可協助您開始執行需要提高許可權才能執行的安裝。 提供使用者帳戶控制用來提示使用者提供系統管理員授權的同意 UI。

</dd> <dt>

<span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**分配**
</dt> <dd>

讓應用程式可供使用，並讓它看起來好像已安裝給使用者，而不需要實際安裝。 指派會在 [ **開始** ] 功能表中加入快捷方式和圖示、關聯適當的檔案，以及寫入應用程式的登錄專案。 當使用者嘗試開啟指派的應用程式時，安裝程式會安裝應用程式。 指派和 [*發佈*](p-gly.md) 是兩種 [*廣告*](/windows)方法。 如需詳細資訊，請參閱 [公告](advertisement.md)。

</dd> <dt>

<span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**非同步執行**
</dt> <dd>

[*自訂動作*](c-gly.md) ，在此期間，安裝程式會同時執行自訂動作的個別執行緒和目前的安裝。 如需詳細資訊，請參閱 [同步和非同步自訂動作](synchronous-and-asynchronous-custom-actions.md)。

</dd> </dl>

 

 
