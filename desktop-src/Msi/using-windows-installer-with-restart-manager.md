---
description: 使用 Windows Installer 4.0 進行安裝和服務的應用程式 Windows Vista 會自動使用重新開機管理員來減少系統重新開機。
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: 搭配使用 Windows Installer 與重新開機管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf361cf20d6f56dc25bd43c9077c65a25eeebdae1c6b512dfcde3e756448a7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141148"
---
# <a name="using-windows-installer-with-restart-manager"></a>搭配使用 Windows Installer 與重新開機管理員

使用 Windows Installer 4.0 進行安裝和服務的應用程式 Windows Vista 會自動使用[重新開機管理員](../rstmgr/restart-manager-portal.md)來減少系統重新開機。 Windows Vista 的預設行為是關閉應用程式，而不是盡可能關機並重新啟動作業系統。 在無法避免系統重新開機的情況下，安裝程式可以使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) API 來排程重新開機，以將使用者工作流程的停機時間降到最低。

Windows安裝程式開發人員可以執行下列動作，準備其套件以與[重新開機管理員](../rstmgr/restart-manager-portal.md)一起使用。

-   將 [ [MsiRMFilesInUse](msirmfilesinuse-dialog.md) ] 對話方塊加入至您的封裝。 如果封裝中有 [MsiRMFilesInUse] 對話方塊，則會提供自動關閉並重新啟動應用程式的選項，讓在完整 UI[使用者介面層級](user-interface-levels.md)執行安裝的 Windows Vista 使用者可以選擇。 安裝封裝可以包含 MsiRMFilesInUse 對話方塊和 [ [FilesInUse](filesinuse-dialog.md) ] 對話方塊的資訊。 只有在 Windows Vista 上至少以 Windows Installer 4.0 安裝套件時，才會顯示 [MsiRMFilesInUse] 對話方塊，否則會予以忽略。 沒有 [MsiRMFilesInUse] 對話方塊的現有封裝仍會使用 [FilesInUse] 對話方塊繼續運作。 您可以使用自訂轉換，將 [MsiRMFilesInUse] 對話方塊新增至現有的封裝。

    終端使用者通常會在完整的 UI [使用者介面層級](user-interface-levels.md)執行安裝。 基本 UI 或縮減的 UI 層級安裝可讓使用者選擇使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 來減少系統重新開機，即使 [MsiRMFilesInUse](msirmfilesinuse-dialog.md) 對話方塊不存在也一樣。 無訊息 UI 層級安裝一律會關閉應用程式和服務，而且在 Windows Vista 中，一律使用重新開機管理員。

-   使用 [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) 函式註冊應用程式以重新開機。 重新開機管理員只能重新開機已註冊要重新開機的應用程式。 重新開機管理員會在安裝之後重新開機已註冊的應用程式。 如果安裝需要重新開機系統，重新開機管理員會在系統重新開機後重新開機已註冊的應用程式。
-   \_使用 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)和 [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)函數啟用外部使用者介面處理常式時，請指定 INSTALLLOGMODE RMFILESINUSE。 Windows安裝程式將會 \_ 為支援[重新開機管理員](../rstmgr/restart-manager-portal.md)的外部使用者介面處理常式傳送 INSTALLMESSAGE RMFILESINUSE 訊息。 如果沒有已註冊的或內部使用者介面處理 INSTALLMESSAGE \_ RMFILESINUSE 訊息，安裝程式 \_ 就會針對支援 [FILESINUSE](filesinuse-dialog.md) 對話方塊的使用者介面處理常式傳送 INSTALLMESSAGE FILESINUSE 訊息。 如需詳細資訊，請參閱搭配 [外部 UI 使用重新開機管理員](using-restart-manager-with-an-external-ui-.md)。
-   自訂動作可以加入屬於 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話的資源。 自訂動作應該在 [InstallValidate](installvalidate-action.md) 動作之前排序。 自訂動作可以使用 [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md) 屬性來取得工作階段金鑰，而且應該呼叫重新開機管理員 API 的 [**RmJoinSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) 和 [**RmEndSession**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) 函式。 自訂動作無法移除屬於重新開機管理員會話的資源。 自訂動作不應該嘗試使用 [**RmShutdown**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown)、 [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) 和 [**RmRestart**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart) 函數來關閉或重新開機應用程式。
-   封裝作者可以將 [LaunchCondition 資料表](launchcondition-table.md) 中的條件作為 [**MsiSystemRebootPending**](msisystemrebootpending.md) 屬性的基礎，以防止在系統重新開機暫止時安裝其套件。
-   封裝作者和系統管理員可以使用 [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)、 [**MSIDISABLERMRESTART**](msidisablermrestart.md)、 [**MSIRMSHUTDOWN**](msirmshutdown.md)屬性和 [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)原則來控制 Windows Installer 和重新開機管理員的互動。
-   應用程式和服務應遵循[重新開機管理員](../rstmgr/restart-manager-portal.md)檔的「[使用重新開機管理員](../rstmgr/using-restart-manager.md)」一節所述的指導方針。

 

 
