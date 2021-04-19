---
description: 在還原作業之後，服務可能需要先停止再重新開機。
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: 停止服務以供要求者還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548af25a4b4550d35a8e6fa4d4c0e791897b6e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000118"
---
# <a name="stopping-services-for-restore-by-requesters"></a><span data-ttu-id="16de4-103">停止服務以供要求者還原</span><span class="sxs-lookup"><span data-stu-id="16de4-103">Stopping Services for Restore by Requesters</span></span>

<span data-ttu-id="16de4-104">在還原作業之後，服務可能需要先停止再重新開機。</span><span class="sxs-lookup"><span data-stu-id="16de4-104">It may be necessary for a service to be stopped prior to and restarted following a restore operation.</span></span>

<span data-ttu-id="16de4-105">一般而言，處理 [*PreRestore*](vssgloss-p.md) 事件 (時，寫入器會將服務停止並啟動以支援還原，而 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) 和 [*PostRestore*](vssgloss-p.md) 事件 (與 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)) 。</span><span class="sxs-lookup"><span data-stu-id="16de4-105">Typically, stopping and starting a service to support a restore would be performed by a writer when handling the [*PreRestore*](vssgloss-p.md) event (with [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) and the [*PostRestore*](vssgloss-p.md) event (with [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).</span></span>

<span data-ttu-id="16de4-106">不過，在某些情況下，要求者必須明確地停止執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="16de4-106">However, there may be cases when it is necessary for a requester to explicitly stop a running service.</span></span> <span data-ttu-id="16de4-107">寫入器會藉由將 \_ \_ \_ vss RESTOREMETHOD 列舉列舉的 vss RME 停止還原 \_ 啟動或 vss \_ RME \_ 還原 \_ \_ 開始值設定為 [**\_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) 方法呼叫的 restore method 引數，並指定要停止的服務名稱，來指出是否為這種情況。</span><span class="sxs-lookup"><span data-stu-id="16de4-107">Writers indicate if this is the case by setting the VSS\_RME\_STOP\_RESTORE\_START or VSS\_RME\_RESTORE\_STOP\_START value of the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration as the restore method argument of a call to the [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) method and specifying the name of the service to be stopped.</span></span>

<span data-ttu-id="16de4-108">當使用 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) 方法時，要求者會取得還原方法的相關資訊，以及使用寫入器中繼資料時要停止的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="16de4-108">A requester obtains information about the restore method and the name of the service to be stopped when working with writer metadata by using the [**IVssExamineWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) method.</span></span>

<span data-ttu-id="16de4-109">寫入器指定要停止的服務名稱時，請務必使用該服務的正確公開已知名稱。</span><span class="sxs-lookup"><span data-stu-id="16de4-109">It is important that the writer, when specifying the name of a service to be stopped, uses the correct publicly known name of that service.</span></span> <span data-ttu-id="16de4-110">不明確或不正確的名稱可能會導致要求者停止錯誤的服務，或無法判斷要停止的服務。</span><span class="sxs-lookup"><span data-stu-id="16de4-110">An ambiguous or inaccurate name may result in requesters stopping the wrong service or being unable to determine which service to stop.</span></span>

<span data-ttu-id="16de4-111">完成還原作業之後，要求者必須重新開機服務。</span><span class="sxs-lookup"><span data-stu-id="16de4-111">After the completion of the restore operation, requesters must restart the service.</span></span>

<span data-ttu-id="16de4-112">您必須謹慎設計和執行支援要求者必須停止並重新啟動的寫入器。</span><span class="sxs-lookup"><span data-stu-id="16de4-112">You must be careful in designing and implementing writers that support services that requesters must stop and restart.</span></span> <span data-ttu-id="16de4-113">具體而言，這類寫入器實際上不應該是服務的一部分，也就是，寫入器本身應該不需要停止，然後在還原作業期間重新開機。</span><span class="sxs-lookup"><span data-stu-id="16de4-113">Specifically, such writers should not actually be part of the service—that is, the writer itself should not need to be stopped and then restarted in the course of the restore operation.</span></span>

<span data-ttu-id="16de4-114">在重新開機時，其進程已停止的寫入器會有不同的寫入器實例。</span><span class="sxs-lookup"><span data-stu-id="16de4-114">A writer whose process is stopped will have a different writer instance upon restart.</span></span> <span data-ttu-id="16de4-115">寫入器的新實例將不會收到適用于寫入器原始實例的 VSS 事件。</span><span class="sxs-lookup"><span data-stu-id="16de4-115">The new instance of the writer will not receive VSS events intended for the original instance of the writer.</span></span> <span data-ttu-id="16de4-116">具體而言，如果在處理 PreRestore 事件之後停止寫入器實例的進程，新的實例將不會收到 PostRestore 事件。</span><span class="sxs-lookup"><span data-stu-id="16de4-116">Specifically, if the process of a writer instance is stopped after handling a PreRestore event, the new instance will not receive the PostRestore event.</span></span> <span data-ttu-id="16de4-117">此外，VSS 將會產生錯誤，指出在還原作業中遺失參與的寫入器，而 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 可能會傳回失敗。</span><span class="sxs-lookup"><span data-stu-id="16de4-117">Further, VSS will generate an error indicating the loss of a participating writer in the restore operation, and [**IVssBackupComponents::PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) may return a failure.</span></span>

 

 



