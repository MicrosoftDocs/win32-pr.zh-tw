---
description: 原始加密函式會啟用加密檔案的備份。
ms.assetid: 00f9b00e-305d-4554-8b43-7061228c92c3
title: 備份與還原加密的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbc5d1babbbbb92cef9e78f9a0dade702fd63d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026383"
---
# <a name="backup-and-restore-of-encrypted-files"></a>備份與還原加密的檔案

加密檔案系統 (EFS) 篩選開啟加密檔案的方式，讓開啟檔案的應用程式取得未加密資訊的存取權，當然它具有適當的認證可存取檔案，並取得解密檔案所需的金鑰。 後續的讀取作業將會產生未加密的文字。 這對加密檔案的一般存取非常有其期望，並讓檔案的加密和解密保持透明。 但是，它會妨礙加密檔案的備份，因為如果嘗試使用標準檔案 i/o 呼叫（例如 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)、 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)和 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)）進行備份，則備份的檔案將會是純文字版本。

提供未經處理的加密功能來解決此問題。 備份應用程式是適用于這些功能的主要使用者。 原始加密函式與其他檔案系統函式不同之處在于，開啟、讀取和寫入函式允許存取原始加密的資料流程，也允許讀取/寫入 $EFS 資料流程。 因此，原始加密函式的呼叫端不需要存取解密檔案的密碼編譯金鑰。 下列原始加密 Api 可用於備份和還原應用程式： 

| 原始加密 API                                     | Description                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OpenEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)   | 開啟加密的檔案，並存取加密格式的資料。 如果呼叫端無法存取檔案的金鑰，則呼叫端需要 [SeBackupPrivilege](/windows/desktop/SecAuthZ/authorization-constants) 來匯出加密的檔案或 SeRestorePrivilege，以匯入加密的檔案。 |
| [**CloseEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-closeencryptedfileraw) | 關閉以 OpenEncryptedFileRaw 開啟的加密[ 檔案](/windows/desktop/api/WinBase/nf-winbase-openencryptedfilerawa)                                                                                                                                                                                      |
| [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)   | 讀取加密的檔案，以加密格式保留其資料                                                                                                                                                                                                                   |
| [**WriteEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw) | 撰寫加密的檔案，以加密格式保留其資料                                                                                                                                                                                                                  |
| [**ImportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_import_func)               | 應用程式定義的回呼，可與 [ **WriteEncryptedFileRaw** 搭配使用](/windows/desktop/api/WinBase/nf-winbase-writeencryptedfileraw)                                                                                                                                                                              |
| [**ExportCallback**](/windows/desktop/api/WinBase/nc-winbase-pfe_export_func)               | 應用程式定義的回呼，可與 [ **ReadEncryptedFileRaw** 搭配使用](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)                                                                                                                                                                                |



 

 

 
