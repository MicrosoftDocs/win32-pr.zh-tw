---
description: 您可以撰寫 [MsiRMFilesInUse] 對話方塊，以顯示目前執行的檔案必須由安裝覆寫或刪除的進程清單。
ms.assetid: e8d93310-388e-4a08-9bce-04c31c33a665
title: MsiRMFilesInUse 對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04aa3167609693135e2d3196fef0495d5244fe44f1a6e7d95d11f999efe51a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012886"
---
# <a name="msirmfilesinuse-dialog"></a>MsiRMFilesInUse 對話方塊

您可以撰寫 [MsiRMFilesInUse] 對話方塊，以顯示目前執行的檔案必須由安裝覆寫或刪除的進程清單。 使用者可以選取 [自動關閉應用程式並重新啟動應用程式] 或 [不要關閉應用程式] 選項。  (將需要重新開機。 ) 」如果使用者選取 [自動關閉應用程式並重新啟動應用程式] 選項，就可以撰寫此對話方塊上的 [推送] 按鈕控制項來發佈 RMShutdownAndRestart 控制項事件，然後 [重新開機管理員](../rstmgr/restart-manager-portal.md) 可以關閉應用程式，並在安裝結束時重新開機應用程式。 這可以消除或減少重新開機電腦的需求。 如需詳細資訊，請參閱 [系統重新開機](system-reboots.md)。

只有在下列所有條件都成立時，才會在安裝期間顯示 [ **MsiRMFilesInUse** ] 對話方塊。 當這些是 false 時，Windows Installer 會忽略 [ **MsiRMFilesInUse** ] 對話方塊。

-   不早于4.0 版的 Windows Installer 版本，以及早于 Windows Vista 或 Windows Server 2008 的作業系統正在執行安裝。
-   使用完整的 UI [使用者介面層級](user-interface-levels.md) 。
-   [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)屬性或 [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)原則尚未停用與 [重新開機管理員](../rstmgr/restart-manager-portal.md)的互動。
-   [ **MsiRMFilesInUse** ] 對話方塊存在於安裝套件中。
-   從 Windows Installer 到[重新開機管理員](../rstmgr/restart-manager-portal.md)的所有呼叫都會成功。

此對話方塊將會依 [InstallValidate 動作](installvalidate-action.md)的要求建立。

 

 
