---
description: 如何使用憑證服務備份功能來備份憑證服務資料庫及其相關聯的檔案。
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: 備份憑證服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773084"
---
# <a name="backing-up-certificate-services"></a>備份憑證服務

下列案例顯示如何使用憑證服務備份功能來備份憑證服務資料庫及其相關聯的檔案。

1.  藉由呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)) ，將 Certadm.dll 程式庫載入記憶體 (。
2.  藉由 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)) ，在 Certadm.dll (中取出每個必要函數的位址。 在其餘步驟中呼叫函式時，請使用這些位址。
3.  呼叫 [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) 來判斷憑證服務是否在線上。 憑證服務必須在線上，備份作業才能成功。
4.  呼叫 [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) 以啟動備份會話。 產生的憑證服務備份內容控制碼將由許多其他備份功能使用。
5.  呼叫 [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) 來判斷還原對應。 還原對應包含還原備份時要使用的路徑。 將 **CertSrvRestoreGetDatabaseLocations** 抓取的資訊儲存至應用程式特定的位置。
6.  呼叫 [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) ，以決定要備份的資料庫檔案名。 針對每個檔案，執行步驟7到9。
7.  呼叫 [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) 以開啟檔案進行備份。
8.  呼叫 [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) 以讀取檔案中的部分位元組，然後呼叫應用程式特定的常式，將位元組儲存在備份媒體上。 重複此步驟，直到備份檔案中的所有位元組為止。
9.  呼叫 [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) 以關閉檔案。
10. 呼叫 [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) ，以決定要備份的記錄檔名稱。 針對每個檔案，執行步驟7到9。
11. 呼叫 [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) ，以截斷在步驟6和10中備份的記錄檔。 此為選擇性步驟;不過，只有在 [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)和 [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)傳回的所有檔案都已 (備份時，才呼叫 **CertSrvBackupTruncateLogs** ，否則還原作業將無法) 。 如需詳細資訊，請參閱 **CertSrvBackupTruncateLogs** 參考頁面。
12. 呼叫 [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) 來決定要備份的非資料庫檔案的名稱。 這些檔案只會由函式識別，且必須透過其他方法來備份。
13. 備份步驟12中所識別的動態檔案，使用與 Certadm.dll 分開的常式。
14. 呼叫 [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) 以結束備份會話。
15. 視需要呼叫 [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) ，以釋放特定憑證服務備份功能所配置的緩衝區。 呼叫 [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)、 [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)和 [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) 將會配置可透過呼叫 **CertSrvBackupFree** 來釋放的緩衝區。
16. 藉由呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)來釋放 Certadm.dll 資源。

如需備份憑證服務資料庫和相關聯的檔案所需之許可權的相關資訊，請參閱 [設定備份和還原許可權](setting-the-backup-and-restore-privileges.md)。

 

 
