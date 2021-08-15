---
description: Master file 資料表 (MFT) 儲存從 NTFS 磁碟分割取出檔案所需的資訊。
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: '主要檔案資料表 (開發人員注意事項) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28a9655c6d3cbba21449b15bd70cf5a24b17e3864dc1b525cb5f6e4e32fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955747"
---
# <a name="master-file-table"></a>主檔案資料表

\[本檔僅適用于 NTFS 磁片區的第3版。\]

Master file 資料表 (MFT) 儲存從 NTFS 磁碟分割取出檔案所需的資訊。

檔案可以有一或多個 MFT 記錄，而且可以包含一或多個屬性。 在 NTFS 中，檔案參考是基底檔案記錄的 MFT 區段參考。 如需詳細資訊，請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。

此 MFT 包含檔案記錄區段;上述的前16個會保留給特殊檔案，如下所示：

-   0： MFT ($Mft) 
-   5：根目錄 (\\) 
-   6：磁片區叢集設定檔 ($Bitmap) 
-   8：叢集檔案 ($BadClus 不正確) 

每個檔案記錄區段的開頭都是檔案記錄區段標頭。 如需詳細資訊，請參閱檔案 [**\_ 記錄 \_ 區段 \_ 標頭**](file-record-segment-header.md)。 每個檔案記錄區段後面都有一或多個屬性。 每個屬性的開頭都是屬性記錄標頭。 如需詳細資訊，請參閱 [**屬性 \_ 記錄 \_ 標頭**](attribute-record-header.md)。 屬性記錄包含屬性類型 (例如 $DATA 或 $BITMAP) 、選擇性名稱和屬性值。 「使用者資料流程」（attribute）是一種屬性，也就是所有的資料流程。 屬性清單會以 0xFFFFFFFF ($END) 終止。

以下是一些範例屬性。

-   $Mft 檔案包含未命名的 $DATA 屬性，也就是依序排列的 MFT 記錄區段順序。
-   $Mft 檔案包含未命名的 $BITMAP 屬性，指出正在使用的 MFT 記錄。
-   $Bitmap 檔案包含未命名的 $DATA 屬性，指出使用中的叢集。
-   $BadClus 檔案包含名為 $BAD 的 $DATA 屬性，其中包含對應至每個錯誤叢集的專案。

當檔案記錄區段中沒有空間可供儲存屬性時，會配置額外的檔案記錄區段，並將其插入至第一個 (或基底) 檔案記錄區段（位於稱為屬性清單的屬性中）。 [屬性] 清單指出可以找到與檔案相關聯的每個屬性。 這包括基底檔案記錄中的所有屬性（attribute 清單本身除外）。 如需詳細資訊，請參閱 [**屬性 \_ 清單 \_ 專案**](attribute-list-entry.md)。

與此 MFT 相關的結構包括下列各項：

-   [**屬性 \_ 清單 \_ 專案**](attribute-list-entry.md)
-   [**屬性 \_ 記錄 \_ 標頭**](attribute-record-header.md)
-   [**檔案名 \_**](file-name.md)
-   [**檔案 \_ 記錄 \_ 區段 \_ 標題**](file-record-segment-header.md)
-   [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)
-   [**多 \_ 磁區 \_ 標頭**](multi-sector-header.md)
-   [**標準 \_ 資訊**](standard-information.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[NTFS 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
