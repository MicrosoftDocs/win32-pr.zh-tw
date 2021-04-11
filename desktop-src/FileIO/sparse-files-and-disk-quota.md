---
description: 稀疏檔案會依檔案的名義大小來影響使用者配額，而不是實際配置的磁碟空間量。
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: 稀疏檔案和磁片配額
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113641"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="583ff-103">稀疏檔案和磁片配額</span><span class="sxs-lookup"><span data-stu-id="583ff-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="583ff-104">稀疏檔案會依檔案的名義大小來影響使用者配額，而不是實際配置的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="583ff-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="583ff-105">也就是說，若要建立具有零個位元組的 50 MB 檔案，就會耗用該使用者配額的 50 MB。</span><span class="sxs-lookup"><span data-stu-id="583ff-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="583ff-106">這表示當使用者將資料寫入至稀疏檔案時，他不需要擔心超過其硬性配額限制，因為該空間已收取空間的費用。</span><span class="sxs-lookup"><span data-stu-id="583ff-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="583ff-107">系統管理員不應計算較小的稀疏檔案大小。</span><span class="sxs-lookup"><span data-stu-id="583ff-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="583ff-108">因此，不論使用的是稀疏檔案，它們都不應將超過可用實體空間的硬性配額限制授與使用者。</span><span class="sxs-lookup"><span data-stu-id="583ff-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



