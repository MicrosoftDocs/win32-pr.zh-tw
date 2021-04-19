---
description: '>ivsscomponent 介面可讓寫入器精確微調以元件為基礎來還原檔案的方式。'
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: 設定 VSS 還原目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001695"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="61967-103">設定 VSS 還原目標</span><span class="sxs-lookup"><span data-stu-id="61967-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="61967-104">[**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)介面可讓寫入器精確微調以元件為基礎來還原檔案的方式。</span><span class="sxs-lookup"><span data-stu-id="61967-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="61967-105">因為還原期間的系統設定可能不是在備份期間所預期的，所以會提供還原目的機制。</span><span class="sxs-lookup"><span data-stu-id="61967-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="61967-106">它可讓寫入器呼叫 [**>ivsscomponent：： SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) 來變更如何還原那些 [*明確包含*](vssgloss-e.md) 在備份元件檔中的元件。</span><span class="sxs-lookup"><span data-stu-id="61967-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="61967-107">這也會變更 [*隱含包含*](vssgloss-i.md)的那些元件所使用的還原機制。</span><span class="sxs-lookup"><span data-stu-id="61967-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="61967-108">在系統重新開機期間發生的檔案還原 (在 [**vss \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉值下，如果無法取代) ，則在重新開機時還原 \_ \_ \_ \_ 和 vss \_ RME 還原， \_ \_ \_ \_ \_ \_ 因為 **MoveFileEx** 將檔案複製到最終位置時沒有執行中的 vss 服務。</span><span class="sxs-lookup"><span data-stu-id="61967-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="61967-109">同樣地，VSS \_ RME \_ 自訂還原可能會受到影響，因為每個自訂還原都是指定的寫入器專屬的，而且可以選擇要考慮或忽略還原目標。</span><span class="sxs-lookup"><span data-stu-id="61967-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="61967-110">要求者和寫入器可以使用 [**>ivsscomponent：： GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) 檢查元件集的還原目標。</span><span class="sxs-lookup"><span data-stu-id="61967-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="61967-111">[**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 支援下列還原目標，可在元件集的元件上設定：</span><span class="sxs-lookup"><span data-stu-id="61967-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="61967-112">VSS \_ RT \_ 原始。</span><span class="sxs-lookup"><span data-stu-id="61967-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="61967-113">將遵守 [**VSS \_ RESTOREMETHOD \_ 列舉**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) 列舉所指定的還原方法。</span><span class="sxs-lookup"><span data-stu-id="61967-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="61967-114">VSS \_ RT \_ 替代。</span><span class="sxs-lookup"><span data-stu-id="61967-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="61967-115">這些檔案會還原至從現有替代位置對應決定的位置。</span><span class="sxs-lookup"><span data-stu-id="61967-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="61967-116">如果存在與元件集子元件中路徑相符的替代位置對應，請盡可能還原至替代位置;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="61967-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



