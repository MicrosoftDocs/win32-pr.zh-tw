---
title: 備份 Active Directory 伺服器
description: Active Directory 伺服器備份需要您備份資料庫和交易記錄。 本主題提供備份應用程式如何備份 Active Directory 目錄服務的逐步解說。
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- 備份 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020749"
---
# <a name="backing-up-an-active-directory-server"></a>備份 Active Directory 伺服器

Active Directory 伺服器備份需要您備份資料庫和交易記錄。 本主題提供備份應用程式如何備份 Active Directory 目錄服務的逐步解說。

這些備份函式的呼叫者必須擁有 **SE \_ 備份 \_ 名稱** 許可權。 您可以使用 [**DsSetAuthIdentity**](dssetauthidentity.md) 函數來設定用來呼叫目錄備份/還原功能的安全性內容。

**若要備份 Active Directory 伺服器，請執行下列步驟：**

1.  呼叫 [**DsIsNTDSOnline**](dsisntdsonline.md) 函數來判斷 Active Directory Domain Services 是否正在執行。
2.  如果 Active Directory Domain Services 正在執行，請呼叫 [**DsBackupPrepare**](dsbackupprepare.md) 函數來初始化備份內容控制碼。 如果 Active Directory Domain Services 未執行，則無法備份，且備份應用程式必須讓備份作業失敗。
3.  呼叫 [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) 函數，以取得要備份的檔案清單。 若要釋放此函式所傳回的記憶體，請呼叫 [**DsBackupFree**](dsbackupfree.md) 函數。
4.  針對傳回的檔案清單中的每個名稱，呼叫 [**DsBackupOpenFile**](dsbackupopenfile.md) 函式，然後重複呼叫 [**DsBackupRead**](dsbackupread.md) 函式，直到讀取整個檔案為止。 當您完成讀取檔案時，請呼叫 [**DsBackupClose**](dsbackupclose.md) 函式來關閉它。
5.  備份所有資料庫檔案之後，請呼叫 [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) 函數來取得交易記錄檔的清單。 此清單的處理方式就和資料庫檔案清單一樣。
6.  當您完成交易記錄的備份時，請呼叫 [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) 函數來刪除已備份的所有已認可交易記錄。
7.  儲存 [**DsBackupPrepare**](dsbackupprepare.md) 函式所提供的到期權杖內容。 這可儲存在檔案或其他的持續性記憶體中。 此權杖必須傳遞至 [**DsRestorePrepare**](dsrestoreprepare.md) 函式，才能起始還原作業。
8.  將權杖指標傳遞至 [**DsBackupFree**](dsbackupfree.md) 函式，以釋放到期權杖的記憶體。
9.  最後，呼叫 [**DsBackupEnd**](dsbackupend.md) 函式，以釋放與備份內容控制碼相關聯的所有資源。

 

 




