---
description: 您可以透過下列機制來取代受保護的資源。
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: 支援的資源取代機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8f839e65ddd07bbde6bb4e089c3235ee6930dec910c07c1c318e666b034afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999248"
---
# <a name="supported-resource-replacement-mechanisms"></a>支援的資源取代機制

您可以透過下列機制來取代受保護的資源。

在 Windows Vista 和 Windows Server 2008 上修改受 WRP 保護之資源的完整存取權，僅限於使用下列機制搭配 Windows 模組安裝程式服務 TrustedInstaller：

-   WindowsTrustedInstaller 安裝的 Service Pack。
-   TrustedInstaller 安裝的修補程式。
-   TrustedInstaller 安裝的作業系統升級。
-   Windows由 TrustedInstaller 安裝的更新。

如果應用程式和安裝程式嘗試以 WRP 保護的資源取代這些指定方法以外的資源，則會拒絕變更資源並產生拒絕存取錯誤訊息的存取權。

對於嘗試取代受 WRP 保護之資源的知名安裝程式，可能會隱藏拒絕存取錯誤和錯誤訊息。 在此情況下，作業會成功傳回，錯誤和錯誤訊息會隱藏，但不會對受 WRP 保護的資源套用任何變更。 只有在符合下列所有條件時，才可以針對已知的安裝程式隱藏此錯誤：

-   這是繼承應用程式。 應用程式不包含並無 requestedexecutionlevel 的資訊清單，該資訊清單會識別針對 Windows Vista 或 Windows Server 2008 所設計的應用程式。
-   拒絕存取的錯誤是因為嘗試修改受 WRP 保護的資源所造成。
-   系統管理員正在安裝應用程式。

如需搭配 WRP 使用 Windows Installer 的詳細資訊，請參閱在[Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK 中[使用 Windows Installer 和 Windows 資源保護](/windows/desktop/Msi/windows-resource-protection-on-windows-vista)。

**Windows Server 2003 和 Windows XP：** 只有透過下列機制，才支援更換受 WFP 保護的系統檔案：

-   Windows使用 Update.exe 的 Service Pack 安裝
-   使用 Hotfix.exe 安裝的修補程式
-   使用 Winnt32.exe 的作業系統升級
-   Windows Update

以這些指定的方法取代受保護的檔案，會導致 WFP 還原原始檔案。

 

 
