---
description: 說明如何使用憑證服務備份功能來還原和復原憑證服務資料庫及其相關聯的檔案。
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: 從備份還原憑證服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665a1aed873cdf25f24dc5a7bc8b8466a5c3ae7a6c1aaf6bec07d2e8be336e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900521"
---
# <a name="restoring-certificate-services-from-backup"></a>從備份還原憑證服務

下列案例顯示如何使用憑證服務備份功能來還原和復原憑證服務資料庫及其相關聯的檔案。 還原程式牽涉到將備份組內包含的檔案寫入磁片中。 您可以將多個備份組還原 (一個完整備份，再加上零個或多個增量備份) ，但是所有還原都必須在開始復原程式之前完成。 復原程式牽涉到憑證服務重新執行記錄檔，以確保資料庫和記錄檔的一致性，進而確保資料庫的完整性。 此案例說明用來還原備份組的函式呼叫，並通知修復參數的憑證服務。

在執行此案例之前，必須先有憑證服務資料庫的完整備份。

1.  藉由呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)) ，將 Certadm.dll 程式庫載入記憶體 (。
2.  藉由 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)) ，在 Certadm.dll (中取出每個必要函數的位址。 在其餘步驟中呼叫函式時，請使用這些位址。
3.  呼叫 [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) 來判斷憑證服務是否在線上。 如果憑證服務正在執行，請將它關閉後再繼續。 憑證服務不得上線，還原作業才會成功。
4.  呼叫 [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) 來開始還原會話。 產生的憑證服務備份內容控制碼將會由數個其他功能使用。
5.  判斷資料庫位置的路徑。 在備份案例中，可以透過呼叫 [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw)來使用此值;此值應儲存為備份的一部分。
6.  建立還原對應，指定已還原之資料庫的名稱。 憑證服務資料庫還原對應結構 (CSEDB \_ RSTMAPW) 用來指定還原對應。 將 CSEDB \_ RSTMAPW 的 **pwszDatabaseName** 成員和 CSEDB \_ RSTMAPW 的 **pwszNewDatabaseName** 成員設定為在步驟5中決定的資料庫位置。 （選擇性）如果還原的資料庫與備份資料庫的名稱不同，請將 CSEDB \_ RSTMAPW 的 **pwszNewDatabaseName** 成員設定為新的資料庫名稱。
7.  如果您想要確保在執行備份後對資料庫所做的修改不會在資料庫還原完成後重新套用 (在下一次執行憑證服務時執行的資料庫復原) ，請從目標伺服器的作用中資料庫和記錄檔目錄中刪除檔案。
8.  將完整備份中包含的檔案複製到目標伺服器的作用中資料庫和記錄檔目錄。
9.  呼叫 [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) 以註冊完整備份的還原作業。 **CertSrvRestoreRegister** 會使用步驟6中指定的還原對應。 **CertSrvRestoreRegister** 也會指定備份資料庫和記錄檔的位置。 呼叫 **CertSrvRestoreRegister** 會強制憑證服務在下次啟動時嘗試還原作業。 它也會防止憑證服務處理憑證要求，直到還原完成為止。
10. 呼叫 [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)，藉此完成步驟8中啟動的註冊活動。 請注意，還原作業的註冊是啟動憑證服務時要遵循的指示;實際的復原只會在憑證服務啟動後進行。
11. 針對要還原的每個增量備份，將增量備份中包含的檔案複製到目標伺服器的 active log 目錄，然後呼叫 [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)，然後呼叫 [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)。 進行還原的增量備份註冊可能會以任何順序發生，但在每次呼叫 **CertSrvRestoreRegister** 之前，只能將一組增量備份的檔案複製到伺服器。
12. 將憑證服務動態檔案複製到目標伺服器。 呼叫 [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) 時，會在備份期間識別動態檔案。 可能必須停止 World Wide Web 發行服務，以允許覆寫動態檔案。
13. 呼叫 [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) 以結束還原會話。
14. 手動啟動憑證服務應用程式 (或等候下一次重新開機後，自動啟動) 。 當憑證服務啟動時，它會判斷是否已註冊還原作業;如果已註冊還原作業，憑證服務將會開始復原。 在復原作業完成之前，憑證服務將不會處理任何憑證要求。

> [!Note]  
> 復原完成時，請務必對憑證服務資料庫進行新的完整備份。 這是截斷已還原記錄檔以及建立基礎備份組以供日後還原的必要動作。 還原之後所執行的備份，在還原之前無法與備份 (完整或增量) ：也就是說，在還原憑證服務資料庫並進入後續狀態之後，您就無法使用還原前的備份，將資料庫還原至後續的狀態。

 

 

 
