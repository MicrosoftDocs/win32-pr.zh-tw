---
description: 描述兩種類型的磁片配額限制，以及如何測量磁片配額限制。
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: 磁片配額限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990303"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="ef436-103">磁片配額限制</span><span class="sxs-lookup"><span data-stu-id="ef436-103">Disk Quota Limits</span></span>

<span data-ttu-id="ef436-104">每個檔案使用的磁碟空間會直接向擁有檔案的使用者收取費用。</span><span class="sxs-lookup"><span data-stu-id="ef436-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="ef436-105">檔案的擁有者是以檔案安全性資訊中的安全識別碼 (SID) 來識別。</span><span class="sxs-lookup"><span data-stu-id="ef436-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="ef436-106">對使用者收費的總磁碟空間是所有資料流程長度的總和。</span><span class="sxs-lookup"><span data-stu-id="ef436-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="ef436-107">換句話說，屬性集資料流程和常駐使用者資料流程會影響使用者的配額。</span><span class="sxs-lookup"><span data-stu-id="ef436-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="ef436-108">重新剖析點、安全描述項或其他與檔案相關聯的中繼資料，不需支付配額。</span><span class="sxs-lookup"><span data-stu-id="ef436-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="ef436-109">壓縮或解壓縮檔案不會影響針對檔案所報告的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="ef436-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="ef436-110">因此，一個磁片區上的配額設定可以與另一個磁片區上的設定進行比較。</span><span class="sxs-lookup"><span data-stu-id="ef436-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="ef436-111">磁片配額限制有兩種類型，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ef436-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="ef436-112">限制</span><span class="sxs-lookup"><span data-stu-id="ef436-112">Limit</span></span>                        | <span data-ttu-id="ef436-113">描述</span><span class="sxs-lookup"><span data-stu-id="ef436-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef436-114">警告臨界值</span><span class="sxs-lookup"><span data-stu-id="ef436-114">Warning threshold</span></span><br/> | <span data-ttu-id="ef436-115">您可以設定系統在向使用者收取的磁碟空間超過此值時產生系統記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="ef436-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="ef436-116">固定配額</span><span class="sxs-lookup"><span data-stu-id="ef436-116">Hard quota</span></span><br/>        | <span data-ttu-id="ef436-117">您可以設定系統在向使用者收取的磁碟空間超過此值時產生系統記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="ef436-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="ef436-118">您也可以設定系統在使用者向使用者收取的磁碟空間超過此值時，拒絕額外的磁碟空間給使用者。</span><span class="sxs-lookup"><span data-stu-id="ef436-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="ef436-119">當使用者第一次寫入磁片區時，NTFS 檔案系統會自動建立使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="ef436-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="ef436-120">系統會將自動建立的專案指派給磁片區的預設警告臨界值和固定配額限制值。</span><span class="sxs-lookup"><span data-stu-id="ef436-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




