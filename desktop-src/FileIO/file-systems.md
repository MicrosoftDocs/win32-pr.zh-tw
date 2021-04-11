---
description: 管理目錄專案資料表、目錄控制碼、重新分析點的目錄。
title: 本機檔案系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692256"
---
# <a name="local-file-systems"></a>本機檔案系統

*檔案系統* 可讓應用程式儲存和取出儲存裝置上的檔案。 檔案會以階層式結構放置。 檔案系統會指定檔案的命名慣例，並使用格式來指定樹狀結構中檔案的路徑。

每個檔案系統都包含一或多個驅動程式和動態連結程式庫，可定義檔案系統的資料格式和功能。 檔案系統可存在於許多不同類型的存放裝置上，包括硬碟、自動播放程式、卸載式磁片、磁帶備份單元和記憶卡。

Windows 支援的所有檔案系統都有下列儲存元件：

-   卷。 *磁片* 區是目錄和檔案的集合。
-   目錄。 *目錄* 是目錄和檔案的階層式集合。
-   檔案 檔案 *是相關資料的邏輯* 群組。

## <a name="in-this-section"></a>本節內容



| 主題                                                                | 描述                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [目錄管理](directory-management.md)<br/>          | *目錄* 是目錄和檔案的階層式集合。 單一目錄中可包含之檔案數目的唯一條件約束，是目錄所在磁片的實體大小。<br/> |
| [磁碟管理](disk-management.md)<br/>                    | 硬碟是電腦內的 *固定* 磁片，可儲存並提供相對快速的大量資料存取。 這是最常用於 Windows 的儲存體類型。 系統也支援卸載式媒體。<br/>    |
| [檔案管理](file-management.md)<br/>                    | *File 物件* 提供資源的表示 (實體裝置或實體裝置上的資源，可由 i/o 系統管理) 。<br/>                                                            |
| [交易式 NTFS (TxF) ](transactional-ntfs-portal.md)<br/> | 交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。<br/>                                                                                                                 |
| [磁碟區管理](volume-management.md)<br/>                | 檔案系統中的最高層級組織是 *磁片* 區。 檔案系統位於磁片區上。<br/>                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[FAT 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[檔案系統技術](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[NTFS 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

