---
description: 如何在超過配額額度之後取得更多可用磁碟空間。
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: 磁片配額的使用者層級管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978094"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="ee77c-103">磁片配額的使用者層級管理</span><span class="sxs-lookup"><span data-stu-id="ee77c-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="ee77c-104">磁片配額對使用者而言是透明的。</span><span class="sxs-lookup"><span data-stu-id="ee77c-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="ee77c-105">當使用者詢問磁片上有多少可用空間時，系統只會報告使用者可用的配額額度。</span><span class="sxs-lookup"><span data-stu-id="ee77c-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="ee77c-106">如果使用者超過此額度，系統會傳回 **錯誤磁片的 \_ \_ 完整** 錯誤，就如同指出磁片已滿一樣。</span><span class="sxs-lookup"><span data-stu-id="ee77c-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="ee77c-107">若要在超過配額額度之後取得更多可用磁碟空間，使用者必須執行下列其中一項動作：</span><span class="sxs-lookup"><span data-stu-id="ee77c-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="ee77c-108">刪除部分檔案。</span><span class="sxs-lookup"><span data-stu-id="ee77c-108">Delete some files.</span></span>
-   <span data-ttu-id="ee77c-109">讓其他使用者宣告某些檔案的擁有權。</span><span class="sxs-lookup"><span data-stu-id="ee77c-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="ee77c-110">讓系統管理員增加配額額度。</span><span class="sxs-lookup"><span data-stu-id="ee77c-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="ee77c-111">需要取出實際可用磁碟空間量的程式可以呼叫 [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) 函式，並查看 *TotalNumberOfFreeBytes* 參數。</span><span class="sxs-lookup"><span data-stu-id="ee77c-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



