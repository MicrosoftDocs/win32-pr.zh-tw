---
description: 要求者藉由設定其內容來控制陰影複製的功能。 此內容會指出陰影複製是否會存留在目前的作業中，以及寫入器/提供者協調的程度。
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: 陰影複製內容設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513125"
---
# <a name="shadow-copy-context-configurations"></a>陰影複製內容設定

要求者藉由設定其內容來控制陰影複製的功能。 此內容會指出陰影複製是否會存留在目前的作業中，以及寫入器/提供者協調的程度。

## <a name="persistence-and-shadow-copy-context"></a>持續性和陰影複製內容

陰影複製可能是 [*持續*](vssgloss-p.md)性的，也就是在終止備份作業或釋放 [**>ivssbackupcomponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) 物件後，不會刪除陰影複製。

持續性陰影複製需要 **vss \_ CTX \_ 用戶端 \_ 可存取** 的 vss [**\_ \_ 快照 \_ 內容內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)、 **vss \_ CTX \_ 應用程式 \_ 復原** 或 **vss \_ CTX \_ NAS \_ 復原**。 只有 NTFS 磁片區才能進行永久性陰影複製。

非持續性陰影複製是使用 **vss \_ CTX \_ 備份** 或 **vss CTX 檔案 \_ \_ \_ 共用 \_ 備份** 的內容所建立。 非持續性陰影複製可針對 NTFS 和非 NTFS 磁片區進行。

## <a name="writer-participation-and-shadow-copies"></a>作者參與和陰影複製

陰影複製內容可以分類為涉及寫入器或不涉及寫入器。

在建立時涉及寫入器的陰影複製內容包括：

-   **VSS \_ CTX \_ 應用程式 \_ 復原**
-   **VSS \_ CTX \_ 備份**
-   **VSS \_ CTX \_ 用戶端 \_ 可存取的 \_ 寫入器**

在建立時不牽涉到寫入器的那些套裝程式括：

-   **\_ \_ 可存取 VSS CTX 用戶端 \_**
-   **VSS \_ CTX \_ 檔案 \_ 共用 \_ 備份**
-   **VSS \_ CTX \_ NAS \_ 復原**

其中一個內容可以用於這兩種陰影複製類型，但無法用於建立陰影複製：

-   **VSS \_ CTX \_ 全部**

使用 VSS CTX 建立陰影複製， **\_ \_ 所有** (使用 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 和 [**>ivssbackupcomponents：:D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) 都不受支援。

支援 VSS CTX 內容的作業 **\_ \_ 全都** 是管理作業 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)、 [**>ivssbackupcomponents：:D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots)、 [**>ivssbackupcomponents：： BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)和 [**>ivssbackupcomponents：： ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot)。

## <a name="obtaining-shadow-copy-information"></a>取得陰影複製資訊

如果要求者知道陰影複製 (其 **vss \_ 識別碼**) 的識別 GUID，則可以藉由將呼叫 [**>ivssbackupcomponents：： GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)所傳回的 [**vss \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集內容結構解壓縮，來取得其 **vss \_ 識別碼**) 所識別之特定陰影複製 (內容的相關資訊。

為了取得系統上所有陰影複製的相關內容資訊，要求者會檢查 (的 **Obj 成員。** [**vss \_ \_ 物件**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)樣式的 **\_ lSnapshotAttributes** 成員，這是使用 [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)所取得的 [**vss) \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集的結構，可用來反復查看由呼叫 [**>ivssbackupcomponents：： Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)所傳回的物件清單。

 

 



