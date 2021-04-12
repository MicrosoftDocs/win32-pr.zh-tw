---
description: Windows Installer 開發人員可以遵循搭配使用 Windows Installer 與重新開機管理員中所述的指導方針，來準備安裝套件以使用重新開機管理員。
ms.assetid: 777f8864-b3d2-43c7-9296-1118f3595d7b
title: 搭配外部 UI 使用重新開機管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f112884669b173b40f3806c48cf8e05308c5b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191372"
---
# <a name="using-restart-manager-with-an-external-ui"></a>搭配外部 UI 使用重新開機管理員

Windows Installer 開發人員可以遵循搭配[使用 Windows Installer 與重新開機管理員](using-windows-installer-with-restart-manager.md)中所述的指導方針，來準備安裝套件以使用[重新開機管理員](../rstmgr/restart-manager-portal.md)。

\_呼叫 [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)或 [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)函式來啟用外部使用者介面處理常式時，請指定 INSTALLLOGMODE RMFILESINUSE 訊息類型。 Windows Installer 然後傳送 INSTALLMESSAGE \_ RMFILESINUSE 訊息，以供支援 [重新開機管理員](../rstmgr/restart-manager-portal.md)的外部使用者介面處理常式使用。

您的外部使用者介面處理常式應處理 INSTALLMESSAGE RMFILESINUSE 訊息中包含的資訊 \_ 。 如果沒有已註冊的或內部使用者介面處理 INSTALLMESSAGE \_ RMFILESINUSE 訊息，Windows Installer 傳送 INSTALLMESSAGE \_ FILESINUSE 訊息，供支援 INSTALLMESSAGE \_ FILESINUSE 訊息和 [FILESINUSE](filesinuse-dialog.md) 對話方塊的現有外部處理常式使用。

外部使用者介面可以傳回下表所列的值。



| 外部 UI 傳回值 | Windows Installer 採取的動作                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IDOK                     | 使用者已按下 [ **確定]** 按鈕。 Windows Installer 將要求 [重新開機管理員](../rstmgr/restart-manager-portal.md) 關閉，然後重新開機包含目前使用中之檔案的應用程式。                                                                                                                                               |
| IDCANCEL                 | 已按下 [ **取消** ] 按鈕。 取消安裝。                                                                                                                                                                                                                                                                                    |
| IDIGNORE                 | 已按下 [ **忽略** ] 按鈕。 略過並繼續安裝。 安裝結束時將需要重新開機。                                                                                                                                                                                                            |
| IDNO                     | 未按下 [ **否** ] 按鈕。 如果封裝有 [MsiRMFilesInUse](msirmfilesinuse-dialog.md) 對話方塊，請傳送1610訊息。 如需詳細資訊，請參閱 [Windows Installer 錯誤訊息](windows-installer-error-messages.md)。 如果封裝沒有 MsiRMFilesInUse 對話方塊，請傳送 INSTALLMESSAGE \_ FILESINUSE 訊息。 |
| IDRETRY                  | 已按下 [ **重試** ] 按鈕。 傳送 INSTALLMESSAGE \_ FILESINUSE 訊息。                                                                                                                                                                                                                                                                 |
| -1                       | 錯誤。 結束安裝。                                                                                                                                                                                                                                                                                                                |



 

 

 
