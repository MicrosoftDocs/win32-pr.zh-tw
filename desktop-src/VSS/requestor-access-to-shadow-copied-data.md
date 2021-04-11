---
description: 陰影複製完成之後，取得所包含之檔案資料存取權最重要的機制，就是透過使用陰影複製的裝置物件。
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: 要求者存取陰影複製的資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115149"
---
# <a name="requester-access-to-shadow-copied-data"></a>要求者存取陰影複製的資料

陰影複製完成之後，取得所包含之檔案資料存取權最重要的機制，就是透過使用陰影複製的 [*裝置物件*](vssgloss-d.md)。

[**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集架構結構的 **m \_ pwszSnapshotDeviceObject** 成員是包含陰影複製之磁片區裝置物件的字串。 如果要求者知道磁片區的 **vss \_ 識別碼** (識別 GUID) 並將它傳遞給 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)，就可以取得陰影複製的磁片區的 **vss \_ 快照 \_** 集內容物件。

要求者也可以使用 [**vss \_ 物件 \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)屬性結構的 **Obj. Snap** 成員來取得陰影複製屬性資訊 (這是 [**vss \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集屬性結構，) 使用 [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)來反復查看由呼叫 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)所傳回的物件清單。

裝置物件應解釋為陰影複製之磁片區的根目錄。 基於這個理由，裝置物件不會包含反斜線 ( " \\ " ) 。

藉由將原始路徑的根目錄取代為裝置物件，即可取得陰影複製磁片區上的路徑。 例如，假設有一個路徑位於 "C： DATABASE .mdb" 的原始磁片區 \\ \\ \* 和 snapProp 的 [**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集，則您會串連 snapPropm \_ pwszShadow copyDeviceObject、" \\ " 和 " \\ DATABASE \\ \* .mdb"，以取得陰影複製磁片區上的路徑。

VSS 檔案組的檔案描述項中可能會有萬用字元，因此在元件所管理的陰影複製上取得檔案的完整清單，可能需要使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile** 等方法。

 

 



