---
description: 如果在沒有寫入器介入的情況下進行 VSS 備份作業，仍可能會建立陰影複製。
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: 不含寫入器參與的備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983916"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="6ca12-103">不含寫入器參與的備份</span><span class="sxs-lookup"><span data-stu-id="6ca12-103">Backups without Writer Participation</span></span>

<span data-ttu-id="6ca12-104">如果在沒有寫入器介入的情況下進行 VSS 備份作業，仍可能會建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="6ca12-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="6ca12-105">如先前所述 (查看 [預設陰影複製狀態](shadow-copies-and-shadow-copy-sets.md)) ，這種陰影複製類型的結果是磁片區，可反映陰影複製時磁片的狀態：陰影複製的磁片區上的資料可能會反映不完整或部分 i/o 作業，而且會描述為處於損 [*毀一致狀態*](vssgloss-c.md)。</span><span class="sxs-lookup"><span data-stu-id="6ca12-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="6ca12-106">有幾種情況需要備份應用程式處理損毀一致的陰影複製資料：</span><span class="sxs-lookup"><span data-stu-id="6ca12-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="6ca12-107">**資料是由 VSS 感知的應用程式所管理**</span><span class="sxs-lookup"><span data-stu-id="6ca12-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="6ca12-108">幾乎每個系統都有一些應用程式（文字編輯器、郵件讀取器、文字處理器等等）不是 VSS 感知，所以陰影複製上的部分資料一律會被視為處於損毀一致狀態。</span><span class="sxs-lookup"><span data-stu-id="6ca12-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="6ca12-109">這類資料通常不是系統或服務關鍵，因此備份它應該不會有問題，或至少在傳統備份期間沒有任何問題。</span><span class="sxs-lookup"><span data-stu-id="6ca12-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="6ca12-110">如同傳統備份的準備工作，在可能的情況下，備份操作員應該在啟動 VSS 備份作業之前，先嘗試暫停或終止這類應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ca12-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="6ca12-111">**系統，沒有與 VSS 相容的寫入器**</span><span class="sxs-lookup"><span data-stu-id="6ca12-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="6ca12-112">這種情況可能相當罕見，因為 VSS 備份應用程式可以備份的大部分系統都會有啟用 VSS 的 Windows 版本，其應包含寫入器。</span><span class="sxs-lookup"><span data-stu-id="6ca12-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="6ca12-113">不過，在某些情況下可能會發生此問題，例如，如果您是在不使用 VSS 支援的情況下備份系統，但系統使用具備 VSS 功能的網路設備來儲存它。</span><span class="sxs-lookup"><span data-stu-id="6ca12-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="6ca12-114">雖然從損毀一致映射備份系統的狀態並不是最佳的，但讓電腦重新開機操作狀態可能就已足夠。</span><span class="sxs-lookup"><span data-stu-id="6ca12-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="6ca12-115">在許多情況下，電腦會從任何未完成的 i/o 作業復原到檔案系統，而且會正常運作。</span><span class="sxs-lookup"><span data-stu-id="6ca12-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="6ca12-116">**要求者選擇不使用系統寫入器**</span><span class="sxs-lookup"><span data-stu-id="6ca12-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="6ca12-117">如果要求者選擇不新增寫入器元件，或停用所有寫入器，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="6ca12-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="6ca12-118">通常不建議以這種方式執行備份。</span><span class="sxs-lookup"><span data-stu-id="6ca12-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="6ca12-119">雖然陰影複製的磁片區可能足以將系統還原為執行中，但並不是理想的做法。</span><span class="sxs-lookup"><span data-stu-id="6ca12-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="6ca12-120">事實上，假設在系統上執行的寫入器是以可與 VSS 和陰影複製合作的功能來設計的，因此以這種方式備份資料可能會造成不穩定的情形。</span><span class="sxs-lookup"><span data-stu-id="6ca12-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



