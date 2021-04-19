---
description: 系統管理員可以控制每位使用者可以儲存在 NTFS 檔案系統磁片區的資料量。
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: 管理磁片配額
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000178"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="fa717-103">管理磁片配額</span><span class="sxs-lookup"><span data-stu-id="fa717-103">Managing Disk Quotas</span></span>

<span data-ttu-id="fa717-104">NTFS 檔案系統支援 *磁片配額*，可讓系統管理員控制每位使用者可在 NTFS 檔案系統磁片區上儲存的資料量。</span><span class="sxs-lookup"><span data-stu-id="fa717-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="fa717-105">系統管理員可以選擇性地設定系統在使用者接近其配額時記錄事件，以及拒絕超過其配額的使用者更多磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="fa717-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="fa717-106">系統管理員也可以產生報表，並使用事件監視器來追蹤配額問題。</span><span class="sxs-lookup"><span data-stu-id="fa717-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="fa717-107">您可以藉由呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式並檢查檔案 **磁片區 \_ \_ 配額** 位旗標，判斷檔案系統是否支援磁片配額。</span><span class="sxs-lookup"><span data-stu-id="fa717-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa717-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="fa717-108">In this section</span></span>



| <span data-ttu-id="fa717-109">主題</span><span class="sxs-lookup"><span data-stu-id="fa717-109">Topic</span></span>                                                                                                   | <span data-ttu-id="fa717-110">描述</span><span class="sxs-lookup"><span data-stu-id="fa717-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa717-111">磁片配額的使用者層級管理</span><span class="sxs-lookup"><span data-stu-id="fa717-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="fa717-112">如何在超過配額額度之後取得更多可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="fa717-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="fa717-113">磁片配額的系統層級管理</span><span class="sxs-lookup"><span data-stu-id="fa717-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="fa717-114">系統管理員可以設定磁片區上特定使用者的配額。</span><span class="sxs-lookup"><span data-stu-id="fa717-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="fa717-115">系統管理員也可以設定磁片區的預設配額。</span><span class="sxs-lookup"><span data-stu-id="fa717-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="fa717-116">磁片配額限制</span><span class="sxs-lookup"><span data-stu-id="fa717-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="fa717-117">描述兩種類型的磁片配額限制，以及如何測量磁片配額限制。</span><span class="sxs-lookup"><span data-stu-id="fa717-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="fa717-118">磁片配額介面</span><span class="sxs-lookup"><span data-stu-id="fa717-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="fa717-119">搭配磁片配額使用的介面。</span><span class="sxs-lookup"><span data-stu-id="fa717-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




