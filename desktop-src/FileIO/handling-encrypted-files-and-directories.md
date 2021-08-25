---
description: 標示為已加密的檔案會使用目前的加密驅動程式，以 NTFS 檔案系統進行加密。
ms.assetid: 166bfb8c-b97d-4cc7-bf6b-399837cb8ad0
title: 處理加密的檔案和目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a3a7b4a2d38aa2f4e012ccb96d01712f280879ff578afdb5c69392ab826a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927788"
---
# <a name="handling-encrypted-files-and-directories"></a>處理加密的檔案和目錄

程式設計師或使用者可能會將目錄或檔案標示為已加密。 標示為已加密的檔案會使用目前的加密驅動程式，以 NTFS 檔案系統進行加密。 如果您在稍後的日期將檔案標示為未加密，則會將它解密，並將其保留為純文字 (不安全的) 狀態。

目錄本身不會加密。 依預設，在「加密」目錄中，目錄中的所有新檔案都會在建立時加密。 如果使用者不想要加密檔案，使用者必須特別將新檔案的狀態變更為 [解密]。 可以看到加密的目錄。 若要讓其他使用者無法存取目錄，請使用存取控制的標準方法。

加密函式不能與 [備份 API](/windows/desktop/Backup/backup)搭配使用。

若要加密新的檔案，請使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式搭配 **檔 \_ 屬性 \_ 加密** 旗標。 若要加密現有的檔案，請使用 [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) 函數。 檔案中的所有資料流程都會加密。 如果檔案已加密， **EncryptFile** 就不會執行任何動作，但會傳回非零值，表示成功。 如果檔案已壓縮， **EncryptFile** 會在將檔案加密之前解壓縮檔案。

若要解密加密的檔案，請使用 [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) 函數。 如果檔案未加密， **DecryptFile** 就不會執行任何動作，但會傳回非零值以表示成功。

[**EncryptionDisable**](/windows/desktop/api/WinEfs/nf-winefs-encryptiondisable)函式會停用或啟用指定的目錄和檔案中的檔案加密。 它不會影響所指定目錄下的子目錄加密。

若要取出檔案的加密狀態，請使用 [**FileEncryptionStatus**](/windows/desktop/api/WinBase/nf-winbase-fileencryptionstatusa) 函數。 或者，呼叫 [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) 函數，並檢查傳回值中的 **檔 \_ 屬性 \_ 加密** 旗標。

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) 和 [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) 會嘗試使用加密原始程式檔時所用的金鑰來加密目的地檔案。 如果無法這麼做，這兩個函式都會嘗試以預設金鑰來加密目的地檔案。 如果這兩種方法都無法完成， **CopyFile** 和 **CopyFileEx** 將會失敗，並出現 **錯誤 \_ 加密 \_ 失敗** 錯誤。 如果您想要讓 **CopyFileEx** 完成複製作業，即使目的地檔案無法加密，請在您對 **CopyFileEx** 的呼叫中，于 *dwCopyFlags* 參數的值中加入 [**複製檔案 \_ \_ 允許解密的 \_ \_ 目的地**] 旗標。

 

 
