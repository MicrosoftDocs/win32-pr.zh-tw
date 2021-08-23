---
description: 檔案的所有相關資訊，包括其大小、時間和日期戳記、許可權和資料內容，都會儲存在主要檔案資料表中 (MFT) 專案，或儲存在 mft 專案所描述之 MFT 以外的空間中。
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: 'Master File Table (本機檔案系統) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fefec19906e6e2e2c67bbcabf8bd891ccc032b7e8d0882a3622011c324d11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525638"
---
# <a name="master-file-table-local-file-systems"></a>Master File Table (本機檔案系統) 

NTFS 檔案系統包含稱為 *主要檔案資料表* 或 MFT 的檔案。 針對 NTFS 檔案系統磁片區上的每個檔案，在 MFT 中至少有一個專案（包括 MFT 本身）。 檔案的所有相關資訊，包括其大小、時間和日期戳記、許可權和資料內容，都會儲存在 MFT 專案中，或儲存在 mft 專案所描述之 MFT 以外的空間中。

當檔案新增至 NTFS 檔案系統磁片區時，會將多個專案新增至 MFT，而 MFT 的大小會增加。 從 NTFS 檔案系統磁片區刪除檔案時，它們的 MFT 專案會標示為可用，而且可能會重複使用。 不過，已配置給這些專案的磁碟空間不會重新配置，且不會減少 MFT 的大小。

NTFS 檔案系統會保留此 MFT 的空間，以便在該 MFT 成長時盡可能保持連續。 每個磁片區中的 MFT NTFS 檔案系統所保留的空間稱為「MFT 區域」。 檔案和目錄的空間也會從此空間配置，但只有在已配置了 MFT 區域以外的所有磁片區空間之後。

根據平均檔案大小和其他變數，磁片上的保留的 MFT 區域或未保留的空間可能會先配置，因為磁片會填滿容量。 具有少量相對較大檔案的磁片區會先配置未保留的空間，而具有大量較小檔案的磁片區則會先配置 MFT 區域。 無論是哪一種情況，當一個區域或另一個區域都已完全配置時，MFT 的片段都會開始發生。 如果未配置的空間已完全配置，則會從 MFT 區域配置使用者檔案和目錄的空間。 如果已完全配置 MFT 區域，則會從未保留的空間配置新的 MFT 專案的空間。

MFT 本身可以進行磁碟重組。 若要減少在重組程式完成之前，將 MFT 區域完全配置的機率，請在將磁片區重組之前，盡可能在該 MFT 區域開頭保留更多空間。 如果在磁碟重組完成之前，已完全配置了 MFT 區域，則在 MFT 區域以外必須有未配置的空間。

預設的 MFT 區域會在掛接磁片區時計算並保留，且是以磁片區大小為基礎。 您可以透過 [Microsoft 知識庫文章 174619](https://support.microsoft.com/kb/174619)中詳細說明的登錄專案來增加 MFT 區域，但您無法讓預設的 MFT 區域小於計算的專案。 增加 MFT 區域不會減少使用者可用於資料檔案的磁碟空間。

若要判斷目前的 MFT 大小，請使用「磁碟重組工具」來分析 NTFS 檔案系統磁片磁碟機，然後按一下 [ **視圖報告** ] 按鈕。 將會顯示磁片磁碟機統計資料，包括目前的 MFT 大小和片段數目。 您也可以使用 [**FSCTL \_ 取得 \_ NTFS \_ 磁片區 \_ 資料**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) 控制程式代碼來取得 MFT 的大小。

 

 
