---
title: Active Directory Domain Services 備份的考慮
description: 目錄服務資料可以複寫。 還原前必須先建立復原方案。
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory，復原規劃
- Active Directory Domain Services Active Directory，備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023278"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a><span data-ttu-id="f1b56-106">Active Directory Domain Services 備份的考慮</span><span class="sxs-lookup"><span data-stu-id="f1b56-106">Considerations for Active Directory Domain Services Backup</span></span>

<span data-ttu-id="f1b56-107">目錄服務資料可以複寫。</span><span class="sxs-lookup"><span data-stu-id="f1b56-107">Directory service data can be replicated.</span></span> <span data-ttu-id="f1b56-108">還原前必須先建立復原方案。</span><span class="sxs-lookup"><span data-stu-id="f1b56-108">A recovery plan must be created prior to restoration.</span></span> <span data-ttu-id="f1b56-109">其中一個選項是還原目錄的複本，然後傳播從網域中的其他複本備份之後發生的變更。</span><span class="sxs-lookup"><span data-stu-id="f1b56-109">One option is to restore a replica of a directory and then propagate changes that occurred since the backup from other replicas in the domain.</span></span>

<span data-ttu-id="f1b56-110">在某些情況下，您可能會想讓還原的複本優先于網域中的其他複本。</span><span class="sxs-lookup"><span data-stu-id="f1b56-110">In some cases you may want the restored replica to take precedence over the other replicas in the domain.</span></span> <span data-ttu-id="f1b56-111">例如，如果意外刪除物件，並將刪除複寫到所有網域控制站，您就可以從刪除物件之前所做的備份還原一個複本來還原物件。</span><span class="sxs-lookup"><span data-stu-id="f1b56-111">For example, if an object is accidentally deleted and the deletion is replicated to all domain controllers, you could restore the object by restoring one replica from a backup that was made before the object was deleted.</span></span> <span data-ttu-id="f1b56-112">然後您會使用 NTDSUtil 公用程式，將還原的物件標示為已授權還原。</span><span class="sxs-lookup"><span data-stu-id="f1b56-112">Then you would use the NTDSUtil utility to mark the restored object as authoritatively restored.</span></span> <span data-ttu-id="f1b56-113">還原的物件接著會複寫到其他 Dc，而還原的複本將會收到自從進行備份以來發生的所有其他物件的更新。</span><span class="sxs-lookup"><span data-stu-id="f1b56-113">The restored object will then be replicated to the other DCs, and the replica that was restored will receive the updates for all other objects that occurred since the time the backup was made.</span></span> <span data-ttu-id="f1b56-114">所有複本的最終結果與還原前的結果相同，不同之處在于，已不會再刪除授權還原的物件。</span><span class="sxs-lookup"><span data-stu-id="f1b56-114">The end result for all the replicas is the same as that prior to the restore, except that the authoritatively restored object is no longer deleted.</span></span>

<span data-ttu-id="f1b56-115">備份期間發生的所有變更都會儲存在暫存記錄檔中，並在備份完成時新增到備份組的結尾。</span><span class="sxs-lookup"><span data-stu-id="f1b56-115">All changes occurring during backup are stored in a temporary log and added to the end of the backup set when the backup is complete.</span></span>

<span data-ttu-id="f1b56-116">任何復原方案都應該確保備份的存留期不應超過 Active Directory 的標記存留期。</span><span class="sxs-lookup"><span data-stu-id="f1b56-116">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime.</span></span> <span data-ttu-id="f1b56-117">如需標記存留期的詳細資訊，請參閱 TechNet 主題- [管理 Active Directory 備份和](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10))復原的簡介。</span><span class="sxs-lookup"><span data-stu-id="f1b56-117">For more information on Tombstone Lifetime, see the TechNet topic - [Introduction to Administering Active Directory Backup and Recovery](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)).</span></span> <span data-ttu-id="f1b56-118">還原超過標記存留期的備份，可能會導致還原的網域控制站擁有不會在其他 Dc 上複寫的物件。</span><span class="sxs-lookup"><span data-stu-id="f1b56-118">Restoration of a backup older than the tombstone lifetime may cause the restored domain controller to have objects that will not be replicated on other DCs.</span></span> <span data-ttu-id="f1b56-119">如果在進行備份之後刪除物件，並且在永久移除已刪除物件的標記之後進行還原，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f1b56-119">This occurs if an object is deleted after the backup is made and the restore occurs after the tombstone for the deleted object has been permanently removed.</span></span> <span data-ttu-id="f1b56-120">還原的 DC 在刪除之前會有物件存在，而其他 Dc 則沒有該物件曾經存在的記錄。</span><span class="sxs-lookup"><span data-stu-id="f1b56-120">The restored DC would have the object as it existed before the deletion, and the other DCs would have no record that the object ever existed.</span></span> <span data-ttu-id="f1b56-121">在此情況下，系統管理員必須手動刪除已還原之網域控制站上的每個非複寫物件。</span><span class="sxs-lookup"><span data-stu-id="f1b56-121">In this case, an administrator will have to manually delete each non-replicated object on the restored domain controller.</span></span>

<span data-ttu-id="f1b56-122">不支援 Active Directory Domain Services 的增量備份;需要完整備份。</span><span class="sxs-lookup"><span data-stu-id="f1b56-122">Incremental backups of Active Directory Domain Services are not supported; full backups are required.</span></span>

 

 