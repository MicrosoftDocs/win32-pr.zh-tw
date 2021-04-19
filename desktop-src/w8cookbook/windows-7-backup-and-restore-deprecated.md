---
title: Windows 7 備份及還原已淘汰
description: Windows 7 備份及還原已淘汰
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106984521"
---
# <a name="windows-7-backup-and-restore-deprecated"></a><span data-ttu-id="23ac0-103">Windows 7 備份及還原已淘汰</span><span class="sxs-lookup"><span data-stu-id="23ac0-103">Windows 7 Backup and Restore deprecated</span></span>

## <a name="platform"></a><span data-ttu-id="23ac0-104">平台</span><span class="sxs-lookup"><span data-stu-id="23ac0-104">Platform</span></span>

<span data-ttu-id="23ac0-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="23ac0-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="23ac0-106">Description</span><span class="sxs-lookup"><span data-stu-id="23ac0-106">Description</span></span>

<span data-ttu-id="23ac0-107">雖然備份和還原沒有任何行為變更，但這項功能已被取代，而且將不會更新。</span><span class="sxs-lookup"><span data-stu-id="23ac0-107">While there is no behavioral change to Backup and Restore, this function is being deprecated and will not be updated.</span></span> <span data-ttu-id="23ac0-108">它很少使用，且其功能已由新的檔案歷程記錄功能取代。</span><span class="sxs-lookup"><span data-stu-id="23ac0-108">It was rarely used and its functionality has been replaced by the new File History feature.</span></span> <span data-ttu-id="23ac0-109">它會隨附于從 Windows 7 升級至 Windows 8 或相依于備份與還原或磁片映射備份的 Windows 8 與愛好者，仍能使用它。</span><span class="sxs-lookup"><span data-stu-id="23ac0-109">It will ship in Windows 8 and enthusiasts who upgraded from Windows 7 to Windows 8 or depend on Backup and Restore or disk image backup will be still able to use it.</span></span> <span data-ttu-id="23ac0-110">不過，除了主控台之外，所有備份和還原的存取點都已移除。</span><span class="sxs-lookup"><span data-stu-id="23ac0-110">However, all access points to Backup and Restore, with the exception of the Control Panel, have been removed.</span></span> <span data-ttu-id="23ac0-111">備份和還原所使用的主控台小程式已重新命名為 Windows 7 檔復原。</span><span class="sxs-lookup"><span data-stu-id="23ac0-111">The Control Panel applet used by Backup and Restore was renamed to Windows 7 File Recovery.</span></span>

<span data-ttu-id="23ac0-112">設定登錄機碼以停用其映射中的備份通知的 Oem 將不再需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="23ac0-112">OEMs that were setting the registry key to disable backup notification in their images will no longer need to do that.</span></span>

<span data-ttu-id="23ac0-113">我們不建議同時使用這兩項功能。</span><span class="sxs-lookup"><span data-stu-id="23ac0-113">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="23ac0-114">檔案歷程記錄會檢查備份排程是否存在且是否為作用中，如果找到的話，就不會讓使用者開啟它。</span><span class="sxs-lookup"><span data-stu-id="23ac0-114">File History checks if Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="23ac0-115">在此情況下，想要使用檔案歷程記錄的使用者將必須刪除 Windows 備份排程。</span><span class="sxs-lookup"><span data-stu-id="23ac0-115">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="23ac0-116">表現</span><span class="sxs-lookup"><span data-stu-id="23ac0-116">Manifestation</span></span>

<span data-ttu-id="23ac0-117">工作流程可能會中斷，而參考先前存取 Windows 備份和還原功能的檔則需要更新，以反映這些變更。</span><span class="sxs-lookup"><span data-stu-id="23ac0-117">Workflows may be interrupted and documentation that refers to the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="mitigation"></a><span data-ttu-id="23ac0-118">降低</span><span class="sxs-lookup"><span data-stu-id="23ac0-118">Mitigation</span></span>

<span data-ttu-id="23ac0-119">應重新撰寫可能觸發備份和還原的應用程式，以檢查檔案歷程記錄是否開啟，並讓使用者選擇其慣用的方法。</span><span class="sxs-lookup"><span data-stu-id="23ac0-119">Apps that might trigger Backup and Restore should be rewritten to check if File History is on and let users choose their preferred method.</span></span>

 

 




