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
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="de445-103">要求者存取陰影複製的資料</span><span class="sxs-lookup"><span data-stu-id="de445-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="de445-104">陰影複製完成之後，取得所包含之檔案資料存取權最重要的機制，就是透過使用陰影複製的 [*裝置物件*](vssgloss-d.md)。</span><span class="sxs-lookup"><span data-stu-id="de445-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="de445-105">[**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集架構結構的 **m \_ pwszSnapshotDeviceObject** 成員是包含陰影複製之磁片區裝置物件的字串。</span><span class="sxs-lookup"><span data-stu-id="de445-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="de445-106">如果要求者知道磁片區的 **vss \_ 識別碼** (識別 GUID) 並將它傳遞給 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)，就可以取得陰影複製的磁片區的 **vss \_ 快照 \_** 集內容物件。</span><span class="sxs-lookup"><span data-stu-id="de445-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="de445-107">要求者也可以使用 [**vss \_ 物件 \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)屬性結構的 **Obj. Snap** 成員來取得陰影複製屬性資訊 (這是 [**vss \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集屬性結構，) 使用 [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)來反復查看由呼叫 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)所傳回的物件清單。</span><span class="sxs-lookup"><span data-stu-id="de445-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="de445-108">裝置物件應解釋為陰影複製之磁片區的根目錄。</span><span class="sxs-lookup"><span data-stu-id="de445-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="de445-109">基於這個理由，裝置物件不會包含反斜線 ( " \\ " ) 。</span><span class="sxs-lookup"><span data-stu-id="de445-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="de445-110">藉由將原始路徑的根目錄取代為裝置物件，即可取得陰影複製磁片區上的路徑。</span><span class="sxs-lookup"><span data-stu-id="de445-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="de445-111">例如，假設有一個路徑位於 "C： DATABASE .mdb" 的原始磁片區 \\ \\ \* 和 snapProp 的 [**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集，則您會串連 snapPropm \_ pwszShadow copyDeviceObject、" \\ " 和 " \\ DATABASE \\ \* .mdb"，以取得陰影複製磁片區上的路徑。</span><span class="sxs-lookup"><span data-stu-id="de445-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="de445-112">VSS 檔案組的檔案描述項中可能會有萬用字元，因此在元件所管理的陰影複製上取得檔案的完整清單，可能需要使用 **FindFileFirst**、 **FindFileFirstEx** 和 **FindNextFile** 等方法。</span><span class="sxs-lookup"><span data-stu-id="de445-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



