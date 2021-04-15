---
title: Active Directory Domain Services 中的備份錯誤
description: 本主題列出 Active Directory Domain Services 中函數的備份錯誤傳回值。
ms.assetid: d042f189-1b86-42ca-bdb4-a8aaa96c9c65
ms.tgt_platform: multiple
keywords:
- Active Directory 備份錯誤
- Active Directory 網域服務備份錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9b38ba9f28e47fd95e69a923e953d59fdd4d37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461972"
---
# <a name="backup-errors-in-active-directory-domain-services"></a>Active Directory Domain Services 中的備份錯誤

本主題列出 Active Directory Domain Services 中函數的備份錯誤傳回值。



| 值                                      | 描述                                                                                                                                                                                  |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hrNyi**<br/>                       | 函式不會實作為。<br/>                                                                                                                                                  |
| **hrInvalidParam**<br/>              | 參數無效。<br/>                                                                                                                                                       |
| **hrError**<br/>                     | 發生內部錯誤。<br/>                                                                                                                                                       |
| **hrInvalidHandle**<br/>             | 控制碼無效。<br/>                                                                                                                                                          |
| **hrRestoreInProgress**<br/>         | 還原進程正在進行中。<br/>                                                                                                                                               |
| **hrAlreadyOpen**<br/>               | 指定的檔案已開啟。<br/>                                                                                                                                                       |
| **hrInvalidRecips**<br/>             | 收件者無效。 <br/>                                                                                                                                                    |
| **hrCouldNotConnect**<br/>           | 無法備份。 偵測到指定的備份伺服器無法連線，或您嘗試備份的服務未執行。<br/>                                       |
| **hrRestoreMapExists**<br/>          | 指定之元件的還原對應存在。 執行完整還原時，可以指定還原對應。<br/>                                                                  |
| **hrIncrementalBackupDisabled**<br/> | 另一個應用程式已修改指定的 Windows NT/Windows 2000 目錄服務資料庫，讓任何後續備份都將失敗。 若要修正此問題，請執行完整備份。<br/> |
| **hrLogFileNotFound**<br/>           | 因為找不到必要的 Windows NT/Windows 2000 目錄服務資料庫記錄檔，所以無法執行增量備份。<br/>                                        |
| **hrCircularLogging**<br/>           | 指定的 Windows NT/Windows 2000 目錄服務元件已設定為使用迴圈資料庫記錄。 它無法以累加方式進行備份。 執行完整備份。<br/>       |
| **hrNoFullRestore**<br/>             | 資料庫尚未還原至此電腦。 在還原完整備份之前，您無法還原增量備份。<br/>                                            |
| **hrCommunicationError**<br/>        | 嘗試執行本機備份時發生通訊錯誤。<br/>                                                                                                       |
| **hrFullBackupNotTaken**<br/>        | 您必須執行完整備份，才能執行增量備份。<br/>                                                                                                      |
| **hrMissingExpiryToken**<br/>        | 遺漏到期權杖。 沒有到期資料即無法還原。<br/>                                                                                                                  |
| **hrUnknownExpiryTokenFormat**<br/>  | 到期權杖的格式為無法辨識。<br/>                                                                                                                                      |
| **hrContentsExpired**<br/>           | 備份中的 DS 內容已過期。 以最新的複本還原。<br/>                                                                                                            |



 

## <a name="see-also"></a>另請參閱

[成功](success.md)、 [Active Directory Domain Services 中的系統錯誤](system-errors-in-active-directory-domain-services.md)、[目錄管理員錯誤](directory-manager-errors.md)、Active Directory Domain Services 中函式的[記錄和復原錯誤](logging-and-recovery-errors-in-functions-in-active-directory-domain-services.md)、 [Active Directory Domain Services 中](return-values-for-functions-in-active-directory-domain-services.md)函式的傳回值


 

 





