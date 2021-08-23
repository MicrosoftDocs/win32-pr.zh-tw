---
title: 使用重新開機管理員
description: 下列各節說明如何使用重新開機管理員 API。
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- 重新開機管理員重新開機管理員，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90826091aa4a3cdf39e0a1f063a211255ec4ef9cf84b06214eb172150ac3b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009996"
---
# <a name="using-restart-manager"></a>使用重新開機管理員

下列各節說明如何使用重新開機管理員 API。 您的應用程式和服務也應該遵循 [應用程式和服務的指導方針](guidelines-for-applications-and-services.md)。

## <a name="using-the-microsoft-windows-installer"></a>使用 Microsoft Windows Installer

[Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) 4.0 版是 Windows Vista 或 Windows Server 2008 的應用程式安裝服務。 使用 Windows Installer 4.0 版進行安裝和服務的應用程式會自動使用重新開機管理員來減少系統重新開機。 自訂安裝程式也可以設計來呼叫重新開機管理員 API，以直接關閉和重新開機應用程式和服務，以避免需要重新開機系統。 在無法避免系統重新開機的情況下，安裝程式可以使用 [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) 或 [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) 函式，以將使用者的干擾降至最低的方式進行排程。 互動式 Windows Installer 套件應該執行包含[MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog)對話方塊的使用者介面。 如需詳細資訊，請參閱 Windows Installer SDK 檔中的[使用 Windows Installer 與重新開機管理員](/windows/desktop/Msi/using-windows-installer-with-restart-manager)。

## <a name="using-the-restart-manager-api-with-custom-installers"></a>使用重新開機管理員 API 搭配自訂安裝程式

自訂安裝程式，或包含導致系統重新開機之自訂動作的 Windows Installer 套件，可以使用重新開機管理員 API 來關閉和重新開機應用程式和服務。

-   使用重新開機管理員 API 執行的所有作業都必須與會話相關聯。 每個使用者會話最多可同時在系統上開啟64個重新開機管理員會話。 主要安裝程式會啟動並結束重新開機管理員會話。 如需搭配單一安裝程式使用重新開機管理員的詳細資訊，請參閱搭配 [主要安裝程式使用重新開機管理員](using-restart-manager-with-a-primary-installer.md)。
-   如果安裝有必要，您可以將一或多個次要安裝程式聯結到重新開機管理員會話，並且可以執行同進程或跨進程的主要安裝程式。 次要安裝程式需要主要安裝程式提供工作階段金鑰，才能加入會話。 如需詳細資訊和使用次要安裝程式的範例，請參閱搭配 [次要安裝程式使用重新開機管理員](using-restart-manager-with-a-secondary-installer.md)。
-   互動式安裝程式應該執行包含 [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) 對話方塊的使用者介面，該對話方塊可要求使用者關閉應用程式和服務。 如需詳細資訊，請參閱 Windows Installer SDK 檔中的[使用 Windows Installer 與重新開機管理員](/windows/desktop/Msi/using-windows-installer-with-restart-manager)。
-   安裝程式可以呼叫重新開機管理員 API 來變更、取消和取得目前重新開機管理員操作的狀態。 如需詳細資訊，請參閱下列主題： [取得重新開機管理員作業的狀態](getting-the-status-of-a-restart-manager-operation.md) ，並 [取消目前的重新開機管理員操作](canceling-the-current-restart-manager-operation.md)。
-   在呼叫重新開機管理員 API 之前，安裝程式不應停用檔案系統重新導向。 有些32位的安裝程式在64位 Windows 可能無法在% windir% system32 目錄中註冊檔案 \\ 。

 

 