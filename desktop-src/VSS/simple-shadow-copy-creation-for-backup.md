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
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="773f1-103">備份的簡易陰影複製建立</span><span class="sxs-lookup"><span data-stu-id="773f1-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="773f1-104">要求者可以建立許多不同類型的陰影複製。</span><span class="sxs-lookup"><span data-stu-id="773f1-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="773f1-105">不過，對於大部分的備份應用程式，您可以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="773f1-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="773f1-106">使用 VSS CTX 備份的內容來呼叫 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="773f1-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="773f1-107">呼叫 [**>ivssbackupcomponents：： GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) 來初始化與寫入器的通訊。</span><span class="sxs-lookup"><span data-stu-id="773f1-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="773f1-108">呼叫 [**>ivssbackupcomponents：： AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) ，將檔案和資料庫元件新增至備份。</span><span class="sxs-lookup"><span data-stu-id="773f1-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="773f1-109">呼叫 [**>ivssbackupcomponents：： StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) 來初始化陰影複製機制。</span><span class="sxs-lookup"><span data-stu-id="773f1-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="773f1-110">呼叫 [**>ivssbackupcomponents：： AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) ，以將磁片區包含在陰影複製中。</span><span class="sxs-lookup"><span data-stu-id="773f1-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="773f1-111">呼叫 [**>ivssbackupcomponents：:P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) ，以通知寫入器的備份作業。</span><span class="sxs-lookup"><span data-stu-id="773f1-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



