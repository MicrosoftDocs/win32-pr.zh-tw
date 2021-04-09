---
title: 還原 Active Directory 伺服器
description: Active Directory 伺服器必須離線還原。
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- 還原 Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273d02fd50d6b3bd68a055a6a783566e4ebddcf7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842027"
---
# <a name="restoring-an-active-directory-server"></a>還原 Active Directory 伺服器

Active Directory 伺服器必須離線還原。 系統必須以目錄服務還原模式重新開機。 在此模式中，作業系統會在沒有 Active Directory Domain Services 的情況下執行，而且所有使用者驗證都會透過登錄中的安全性帳戶管理員 (SAM) 進行。 若要還原 Active Directory Domain Services，請在還原的網域控制站上使用本機系統管理員的認證。

Restore 函數的呼叫端必須具有 **SE \_ 還原 \_ 名稱** 存取權限。 您可以使用 [**DsSetAuthIdentity**](dssetauthidentity.md) 函數來設定用來呼叫目錄備份和還原功能的安全性內容。

請注意，當您還原 Active Directory Domain Services 時，您也必須還原其他的系統狀態元件。

**若要還原 Active Directory Domain Services**

1.  呼叫 [**DsIsNTDSOnline**](dsisntdsonline.md) 函數來判斷 Active Directory Domain Services 是否正在執行。
2.  如果 Active Directory Domain Services 未執行，則會呼叫 [**DsRestorePrepare**](dsrestoreprepare.md) 函式來初始化還原作業，並取得備份內容控制碼。 如果 Active Directory Domain Services 正在執行，則無法還原，而且還原應用程式必須讓還原作業失敗。 **DsRestorePrepare** 函式需要在備份作業期間從 [**DsBackupPrepare**](dsbackupprepare.md)函數取得到期權杖。
3.  呼叫 [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) 函數，以判斷要還原檔案的目錄。 如果此函式失敗，請將資料還原回原始的備份來原始目錄;這是備份資料的來原始目錄。
4.  呼叫 [**DsRestoreRegister**](dsrestoreregister.md) 函式來準備 Active Directory server 以進行還原作業，並鎖定還原目錄。
5.  使用標準 Win32 函數來還原檔案。 首先，刪除目的地目錄中的所有檔案;然後，將備份檔案複製到目的地目錄。
6.  呼叫 [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) 函數，指出還原已完成。
7.  呼叫 [**DsRestoreEnd**](dsrestoreend.md) 函式，以釋放與內容相關聯的任何資源。

在目錄服務還原模式的還原之後，網域控制站應該以正常模式重新開機。 當目錄服務啟動時，網域控制站會執行正常的一致性檢查，而還原的目錄則會上線。

請注意，還原 Active Directory 伺服器一律是兩部分的作業。 首先，將資料庫還原到取得備份的時間。 其次，複寫目錄，其中新還原的 DSA 會從網域和企業樹系中的其他 Dsa 複寫備份後更新。

在 Windows 2000 或 Windows Server 2003 上執行的電腦（其中包含目錄服務的複本）是網域控制站。

[**DsRestoreRegister**](dsrestoreregister.md)函式會將資料新增到登錄中，該登錄必須存留登錄還原程式，才能讓還原正常運作。 為了確保保留此登錄資料，在呼叫 [**RegReplaceKey**](/windows/desktop/api/winreg/nf-winreg-regreplacekeya)函式之後，請先使用 **DsRestore \*** 函式還原 Active Directory Domain Services，然後再重新開機電腦。 此程式的運作方式是因為 **RegReplaceKey** 不會實際取代登錄區，直到重新開機電腦，並且明確地排除 **DsRestoreRegister** 函式新增的登錄資料，而不是在登錄還原作業期間遭到取代。

 

 