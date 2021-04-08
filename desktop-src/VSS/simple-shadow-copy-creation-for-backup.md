---
description: 要求者可以建立許多不同類型的陰影複製。
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: 備份的簡易陰影複製建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690192"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>備份的簡易陰影複製建立

要求者可以建立許多不同類型的陰影複製。 不過，對於大部分的備份應用程式，您可以執行下列動作：

1.  使用 VSS CTX 備份的內容來呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) \_ \_ 。
2.  呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 來初始化與寫入器的通訊。
3.  呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ，將檔案和資料庫元件新增至備份。
4.  呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 來初始化陰影複製機制。
5.  呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) ，以將磁片區包含在陰影複製中。
6.  呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ，以通知寫入器的備份作業。

 

 



