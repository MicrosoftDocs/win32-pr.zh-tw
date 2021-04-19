---
description: 加密檔案系統 (EFS) 使用公開金鑰系統，在 NTFS 檔案系統磁片區上提供個別檔案的密碼編譯保護。
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: 檔案加密
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996944"
---
# <a name="file-encryption"></a>檔案加密

加密檔案系統（或 EFS）為檔案和目錄提供額外的安全性層級。 它會使用公開金鑰系統，在 NTFS 檔案系統磁片區上提供個別檔案的密碼編譯保護。

一般而言，Windows 安全性模型提供的檔案和目錄物件存取控制，足以保護機密資訊的未經授權存取。 但是，如果包含敏感性資料的膝上型電腦遺失或遭竊，則該資料的安全性保護可能會受到危害。 加密檔案可提高安全性。

若要判斷檔案系統是否支援檔案和目錄的檔案加密，請呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式，並檢查 **FS 檔案 \_ \_ 加密** 位旗標。 請注意，下列專案無法加密：

-   壓縮檔
-   系統檔案
-   系統目錄
-   根目錄
-   交易

您可以加密稀疏檔案。

TxF 不支援加密檔案系統 (EFS) 檔的大部分作業。 TxF 唯一支援的作業是讀取作業，例如 [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                               | 描述                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [處理加密的檔案和目錄](handling-encrypted-files-and-directories.md)<br/> | 標示為已加密的檔案會使用目前的加密驅動程式，以 NTFS 檔案系統進行加密。<br/>                                                          |
| [加密檔案和使用者金鑰](encrypted-files-and-user-keys.md)<br/>                       | 列出用來建立新金鑰、將金鑰新增至加密檔案、查詢加密檔案的金鑰，以及從加密的檔案中移除金鑰的函式。<br/> |
| [備份與還原加密的檔案](backup-and-restore-of-encrypted-files.md)<br/>       | 原始加密函式會啟用加密檔案的備份。<br/>                                                                                                |



 

如需加密的詳細資訊，請參閱 [將使用者新增至加密的](adding-users-to-an-encrypted-file.md)檔案。

如需密碼編譯的詳細資訊，請參閱 [密碼](/windows/desktop/SecCrypto/cryptography-portal)編譯。

 

