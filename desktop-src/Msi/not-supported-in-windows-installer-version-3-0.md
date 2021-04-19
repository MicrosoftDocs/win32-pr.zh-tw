---
description: 在此頁面上列出的 Windows Installer 函式、資料表和屬性，Windows Installer&160、 \# 3.0 和較早的版本不支援此功能。
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Windows Installer 3.0 中不支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980788"
---
# <a name="not-supported-in-windows-installer-30"></a>Windows Installer 3.0 中不支援

Windows Installer 3.0 及更早版本不支援此頁面上所列的 Windows Installer 函數、資料表和屬性。 這份清單缺少某項功能，並不保證支援此功能。 請參閱主要檔，以判斷特定功能所需的 Windows Installer 版本。 如需其他 Windows Installer 版本的詳細資訊，請參閱 [Windows Installer 中的新功能](what-s-new-in-windows-installer.md)。

Windows Installer 3.0 適用于 Windows Server 2003、Windows XP 或 Windows 2000。 如需所有 Windows Installer 版本和可轉散發套件的清單，請參閱 [Windows Installer 的發行版本](released-versions-of-windows-installer.md)。

Windows Installer 3.0 及更舊版本中不支援下列功能。

[安裝程式函數](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

回呼函數原型

-   [**INSTALLUI \_ 處理常式 \_ 記錄**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[資料庫資料表](database-tables.md)

-   [MsiPatchMetadata 資料表](msipatchmetadata-table.md)的 Value 資料行接受 **OptimizedInstallMode** 和 **MinorUpdateTargetRTM**。

[屬性](properties.md)

-   [**Msix64 屬性**](msix64.md)

[64位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)

-   [**範本摘要屬性**](template-summary.md)接受 x64 值。

[內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
