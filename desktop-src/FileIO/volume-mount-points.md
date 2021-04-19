---
description: 您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: 裝載的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995844"
---
# <a name="mounted-folders"></a>裝載的資料夾

NTFS 檔案系統支援裝載的資料夾。 *裝載的資料夾* 是磁片區與另一個磁片區上的目錄之間的關聯。 建立掛接的資料夾時，使用者和應用程式可以使用掛接的資料夾路徑，或使用磁片區的磁碟機號，來存取目標磁片區。 例如，使用者可以建立已掛接的資料夾，將磁片磁碟機 D：與 \\ \\ 磁片磁碟機 c 上的 C： Mnt DDrive 資料夾產生關聯。建立掛接的資料夾之後，使用者可以使用 "C： \\ Mnt \\ DDrive" 路徑來存取磁片磁碟機 D：如同磁片磁碟機 c：的資料夾一樣：

您可以使用掛接的資料夾，將不同的檔案系統（例如 NTFS 檔案系統、16位 FAT 檔案系統，以及在 CD-ROM 光碟機上的 ISO-9660 檔案系統）統一成單一 NTFS 磁片區上的一個邏輯檔案系統。 使用者或應用程式都不需要特定檔案所在目標磁片區的相關資訊。 尋找指定檔案所需的所有資訊都是使用 NTFS 磁片區上掛接之資料夾的完整路徑。 磁片區可以重新排列、替代或細分為許多磁片區，而不需要變更設定的使用者或應用程式。

如需有關已掛接資料夾的詳細資訊，請參閱下列主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                         | 描述                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [建立載入的資料夾](mounting-and-dismounting-a-volume.md)<br/>                                                  | 建立裝載的資料夾是兩個步驟的程式。<br/>                                                                                                                                                                 |
| [列舉裝載的資料夾](enumerating-volume-mount-points.md)<br/>                                                 | 用來列舉磁片區上所裝載之資料夾的函式。<br/>                                                                                                                                                       |
| [判斷目錄是否為裝載的資料夾](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | 如何判斷指定的目錄是否為裝載的資料夾。<br/>                                                                                                                                              |
| [指派磁碟機號給磁片區](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | 如果沒有 \) 已指派給該磁碟機號的磁片區，您可以使用 [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) 函式，將磁碟機號 (例如 X：指派給本機磁片區。<br/> |
| [裝載的資料夾函式](volume-mount-point-functions.md)<br/>                                                       | 用來管理裝載資料夾的函式。<br/>                                                                                                                                                                        |



 

如需範例，請參閱 [裝載的資料夾範例](volume-mount-point-examples.md)。

 

 




