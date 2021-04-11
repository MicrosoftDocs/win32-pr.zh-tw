---
title: 磁帶備份
description: 磁帶磁片區是由錄音媒體和其實體貨運公司所組成。 每個磁帶磁片區都有一或多個磁碟分割。 資料分割通常會依標記或 setmarks 分割成區段。 有三種類型的標記。
ms.assetid: 2057e6e4-b674-4151-b3b6-bde5d87d10c1
keywords:
- 備份備份，磁帶
- 磁帶備份備份
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2820e512646642046059cb151061e3f605d56cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020990"
---
# <a name="tape-backup"></a><span data-ttu-id="3692e-108">磁帶備份</span><span class="sxs-lookup"><span data-stu-id="3692e-108">Tape Backup</span></span>

<span data-ttu-id="3692e-109">*磁帶磁片* 區是由錄音媒體和其實體貨運公司所組成。</span><span class="sxs-lookup"><span data-stu-id="3692e-109">A *tape volume* consists of a recording medium and its physical carrier.</span></span> <span data-ttu-id="3692e-110">磁片區中的整個磁帶長度無法用來記錄資料。</span><span class="sxs-lookup"><span data-stu-id="3692e-110">The entire length of tape in a volume is not available for recording data.</span></span> <span data-ttu-id="3692e-111">在磁帶的開頭和結尾的簡短區段會保留，以將磁帶連接至電訊廠商的中樞。</span><span class="sxs-lookup"><span data-stu-id="3692e-111">Short sections at the beginning and the end of the tape are reserved for attaching the tape to the hubs in the carrier.</span></span> <span data-ttu-id="3692e-112">可以記錄資料之磁帶上的第一個位置，就是所謂的 *開頭標記*，而最後一個位置則稱為「 *中結束記號*」。</span><span class="sxs-lookup"><span data-stu-id="3692e-112">The first position on the tape where data can be recorded is the called the *beginning-of-medium marker*, and the last position is called the *end-of-medium marker*.</span></span>

<span data-ttu-id="3692e-113">每個磁帶磁片區都有一或多個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="3692e-113">Every tape volume has one or more partitions.</span></span> <span data-ttu-id="3692e-114">磁碟分割是磁片區的一部分，其中包含其本身的開始和結束點，而不會與磁片區的任何其他部分重迭。</span><span class="sxs-lookup"><span data-stu-id="3692e-114">A partition is a portion of the volume, containing its own beginning and ending points, that does not overlap with any other portion of the volume.</span></span> <span data-ttu-id="3692e-115">每個分割區都有三個預先定義的位置。</span><span class="sxs-lookup"><span data-stu-id="3692e-115">Each partition has three predefined positions.</span></span> <span data-ttu-id="3692e-116">分割區中您可以記錄資料的第一個位置稱為資料 *分割開頭的標記*，而最後一個位置則稱為「 *分割區結束記號*」。</span><span class="sxs-lookup"><span data-stu-id="3692e-116">The first position in a partition where you can record data is called the *beginning-of-partition marker*, and the last is called *end-of-partition marker*.</span></span> <span data-ttu-id="3692e-117">*早期警告標記* 位於資料分割結束記號的正上方。</span><span class="sxs-lookup"><span data-stu-id="3692e-117">The *early-warning marker* is located immediately before the end-of-partition marker.</span></span> <span data-ttu-id="3692e-118">早期警告位置會通知磁帶應用程式在到達磁碟分割結束記號之前，將緩衝的資料傳輸至磁帶。</span><span class="sxs-lookup"><span data-stu-id="3692e-118">The early-warning position notifies tape applications to transfer buffered data to the tape before reaching the end-of-partition marker.</span></span>

<span data-ttu-id="3692e-119">分割區開始與結束點之間的區域通常 *會依標記* 或 *setmarks* 分割成區段。</span><span class="sxs-lookup"><span data-stu-id="3692e-119">The area between a partition's beginning and ending points is typically divided into sections by *filemarks* or *setmarks*.</span></span> <span data-ttu-id="3692e-120">標記和 setmarks 是不包含使用者資料的特殊記錄元素;它們只是將分割區分成較小的區域，以提供位址配置。</span><span class="sxs-lookup"><span data-stu-id="3692e-120">Filemarks and setmarks are special recorded elements that do not contain user data; they simply divide the partition into smaller areas to provide an address scheme.</span></span> <span data-ttu-id="3692e-121">標記和 setmarks 有類似的用途，但 setmarks 在高容量磁帶機上提供更快速的定位。</span><span class="sxs-lookup"><span data-stu-id="3692e-121">Filemarks and setmarks serve similar purposes, but setmarks provide faster positioning on high-capacity tape drives.</span></span>

<span data-ttu-id="3692e-122">一般而言，磁帶裝置支援的是標記和 setmarks。</span><span class="sxs-lookup"><span data-stu-id="3692e-122">Typically, tape devices support filemarks and setmarks.</span></span> <span data-ttu-id="3692e-123">支援兩者都能將磁帶資料格式化，以便 setmarks 不同磁片區的資料，並將檔案從不同的磁片區上的個別檔案分開。</span><span class="sxs-lookup"><span data-stu-id="3692e-123">Support of both enables tape data to be formatted such that setmarks separate data from different disk volumes and filemarks separate data from individual files on a disk volume.</span></span>

<span data-ttu-id="3692e-124">另一個已錄製的元素，表示磁帶上的位置是 *清除間隙*、清除的磁帶區域或裝置無法辨識為標示或使用者資料的模式。</span><span class="sxs-lookup"><span data-stu-id="3692e-124">Another recorded element that denotes locations on the tape is an *erase gap*, an area of erased tape or a pattern that the device does not recognize as a mark or as user data.</span></span>

<span data-ttu-id="3692e-125">有三種類型的標記。</span><span class="sxs-lookup"><span data-stu-id="3692e-125">There are three types of filemarks.</span></span> <span data-ttu-id="3692e-126">如果寫入作業是從分割區的開頭或較舊的長標記執行，則 *簡短* 的標記包含不能覆寫的簡短清除間距。</span><span class="sxs-lookup"><span data-stu-id="3692e-126">A *short filemark* contains a short erase gap that cannot be overwritten unless the write operation is performed from the beginning of the partition or from an earlier long filemark.</span></span> <span data-ttu-id="3692e-127">*長* 標記包含長清除間距，可讓應用程式將磁帶放置在標記的開頭，以及覆寫標記和清除間距。</span><span class="sxs-lookup"><span data-stu-id="3692e-127">A *long filemark* contains a long erase gap that enables an application to position the tape at the beginning of the filemark and to overwrite the filemark and the erase gap.</span></span> <span data-ttu-id="3692e-128">*一般* 的標記不包含清除間距。</span><span class="sxs-lookup"><span data-stu-id="3692e-128">A *normal filemark* does not contain an erase gap.</span></span> <span data-ttu-id="3692e-129">使用標記的磁帶裝置支援簡短和長的格式標記或一般的標記，但不支援全部三個。</span><span class="sxs-lookup"><span data-stu-id="3692e-129">Tape devices that use filemarks support either short and long filemarks or normal filemarks, but not all three.</span></span>

<span data-ttu-id="3692e-130">Setmarks 或標記之間的分割區可以用來記錄資料。</span><span class="sxs-lookup"><span data-stu-id="3692e-130">The area on a partition between setmarks or filemarks is available for recording data.</span></span> <span data-ttu-id="3692e-131">寫入或讀取磁帶的資料單位稱為區塊。</span><span class="sxs-lookup"><span data-stu-id="3692e-131">A unit of data written to or read from a tape is referred to as a block.</span></span>

<span data-ttu-id="3692e-132">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3692e-132">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3692e-133">磁帶初始化</span><span class="sxs-lookup"><span data-stu-id="3692e-133">Tape Initialization</span></span>](tape-initialization.md)
-   [<span data-ttu-id="3692e-134">磁帶輸入和輸出</span><span class="sxs-lookup"><span data-stu-id="3692e-134">Tape Input and Output</span></span>](tape-input-and-output.md)
-   [<span data-ttu-id="3692e-135">建立備份應用程式</span><span class="sxs-lookup"><span data-stu-id="3692e-135">Creating a Backup Application</span></span>](creating-a-backup-application.md)
-   [<span data-ttu-id="3692e-136">備份和還原永久連結</span><span class="sxs-lookup"><span data-stu-id="3692e-136">Backing Up and Restoring Hard Links</span></span>](backing-up-and-restoring-hard-links.md)

 

 




