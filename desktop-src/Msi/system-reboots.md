---
description: Windows Installer 可以判斷何時需要重新開機系統，並自動提示使用者在安裝結束時重新開機。
ms.assetid: 10117d2c-c2c8-456f-9fce-a89c2d69d3c1
title: 系統重新開機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b32149bbcd43e284f45d7cabcba94a080be5262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981148"
---
# <a name="system-reboots"></a>系統重新開機

Windows Installer 可以判斷何時需要重新開機系統，並自動提示使用者在安裝結束時重新開機。 例如，安裝程式在安裝期間需要取代任何正在使用的檔案時，會自動提示重新開機。

使用 [Windows Installer](windows-installer-portal.md) 4.0 版或更新版本進行安裝和服務的應用程式會自動使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 來減少系統重新開機。 Windows Installer 4.0 版或更新版本的屬性和原則，可讓封裝作者和系統管理員控制 Windows Installer 與重新開機管理員的互動。 如需詳細資訊，請參閱搭配 [使用 Windows Installer 與重新開機管理員](using-windows-installer-with-restart-manager.md)。

安裝套件作者可以使用順序資料表中的標準動作和設定屬性來排程和隱藏重新開機。 以下是用來處理系統重新開機的動作和屬性。



| 動作、對話方塊或屬性                                                | 簡短描述                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ForceReboot 動作](forcereboot-action.md)                                   | 在安裝期間提示使用者重新開機。                                                                                                        |
| [ScheduleReboot 動作](schedulereboot-action.md)                             | 提示使用者在安裝結束時重新開機。                                                                                                 |
| [**重新開機屬性**](reboot.md)                                              | 強制或抑制系統重新開機的特定自動提示。                                                                                           |
| [**REBOOTPROMPT 屬性**](rebootprompt.md)                                  | 抑制重新開機使用者的提示顯示。 任何需要的重新開機都會自動發生。                                                           |
| [**AFTERREBOOT 屬性**](afterreboot.md)                                    | 常用於 ForceReboot 動作所加諸的條件中。                                                                                               |
| [InstallValidate 動作](installvalidate-action.md)                           | 如有必要，會顯示 [FilesInUse] 對話方塊，讓使用者有機會關閉程式，並避免某些系統重新開機。                              |
| [FilesInUse 對話方塊](filesinuse-dialog.md)                                     | 讓使用者有機會關閉進程，以避免某些系統重新開機。                                                                              |
| [MsiRMFilesInUse 對話方塊](msirmfilesinuse-dialog.md)                           | 提供使用者使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 來關閉和重新開機應用程式的選項。 從 Windows Installer 4.0 版開始提供。 |
| [**ReplacedInUseFiles 屬性**](replacedinusefiles.md)                      | 設定安裝程式是否要在使用中的檔案上安裝。 自訂動作會使用這個屬性來偵測是否需要重新開機。                                |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)                   | 要停用 Windows Installer 與 [重新開機管理員](../rstmgr/restart-manager-portal.md)互動的屬性。 從 Windows Installer 4.0 版開始提供。          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)                             | 指定 [重新開機管理員](../rstmgr/restart-manager-portal.md) 關閉和重新開機應用程式的方式。 從 Windows Installer 4.0 版開始提供。                  |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)                                         | 指定 [重新開機管理員](../rstmgr/restart-manager-portal.md) 關閉和重新開機應用程式的方式。 從 Windows Installer 4.0 版開始提供。                  |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)                       | 如果作業系統重新開機正在擱置中，安裝程式會設定此屬性。 從 Windows Installer 4.0 版開始提供。                         |
| [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) | 停用與 [重新開機管理員](../rstmgr/restart-manager-portal.md)Windows Installer 互動的原則。 從 Windows Installer 4.0 版開始提供。                |



 

「安裝暫止時發生錯誤」 \_ \_ 表示安裝未完成或回復。 安裝必須在完成之前繼續進行。 系統可能需要重新開機後，才能繼續安裝。

\_ \_ 當[ForceReboot 動作](forcereboot-action.md)執行時，WINDOWS INSTALLER 會傳回錯誤碼錯誤安裝暫止。 \_ \_ \_ 如果在執行應用程式之前需要重新開機，它會傳回錯誤成功重新開機， \_ \_ \_ 如果安裝程式真的開始重新開機，則會傳回錯誤成功重新開機。 請注意，因為重新開機是非同步，所以可能會在傳回錯誤碼之前實際重新開機。 如需詳細資訊，請參閱 [錯誤碼](error-codes.md)。

自訂動作可以藉由呼叫 [**MsiSetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode)來強制提示在安裝結束時重新開機。 自訂動作也可以藉由呼叫 [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)來檢查暫止的重新開機提示。

## <a name="filesinuse-dialog"></a>FilesInUse 對話方塊

安裝程式可以判斷何時需要重新開機系統，並提示使用者重新開機要求。 通常需要重新開機系統，因為安裝程式正在嘗試安裝目前正在使用的檔案。 如果 [ [InstallValidate] 動作](installvalidate-action.md) 偵測到檔案的安裝已在使用中，則會顯示 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。

如果您預期安裝程式會顯示 FilesInUseDialog，但卻沒有，這可能是下列其中一個原因所造成：

-   使用中的檔案不是可執行檔。
-   安裝程式不會實際嘗試安裝這些檔案。
-   保存這些檔案的程式是叫用安裝的進程。
-   保存這些檔案的程式是沒有標題與其相關聯之視窗的進程。

如需詳細資訊，請參閱 [重新開機要求的記錄](logging-of-reboot-requests.md)。

 

 
