---
description: 要求者會在執行備份的開始時建立備份元件檔。
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: 使用備份元件檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973850"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="ca6f2-103">使用備份元件檔</span><span class="sxs-lookup"><span data-stu-id="ca6f2-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="ca6f2-104">要求者會在執行備份的開始時建立備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="ca6f2-105">檔一開始只包含備份操作狀態的描述。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="ca6f2-106">在還原期間，檔應該提供有關要求者如何繼續將檔案複製回磁片的指示。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="ca6f2-107">在還原作業的過程中，會修改備份元件檔，並且包含該作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="ca6f2-108">不同于寫入器元資料檔案（唯讀），有一個視窗可讓要求者和寫入器修改備份元件檔。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="ca6f2-109">您可以更新檔，直到在備份作業期間產生 [*BackupComplete*](vssgloss-b.md) 或 [*BackupShutdown*](vssgloss-b.md) 事件，到還原期間的 [*PostRestore*](vssgloss-p.md) 事件為止。</span><span class="sxs-lookup"><span data-stu-id="ca6f2-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="ca6f2-110">若要使用要求者的備份元件檔，必須瞭解下列主題：</span><span class="sxs-lookup"><span data-stu-id="ca6f2-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="ca6f2-111">備份元件檔生命週期</span><span class="sxs-lookup"><span data-stu-id="ca6f2-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="ca6f2-112">備份元件檔內容</span><span class="sxs-lookup"><span data-stu-id="ca6f2-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



