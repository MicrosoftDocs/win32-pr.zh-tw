---
title: 光碟格式
description: IMAPI.EXE 支援三種檔案系統格式： ISO 9660、Joliet 和 UDF。
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300923"
---
# <a name="disc-formats"></a><span data-ttu-id="9f5f4-103">光碟格式</span><span class="sxs-lookup"><span data-stu-id="9f5f4-103">Disc Formats</span></span>

<span data-ttu-id="9f5f4-104">IMAPI.EXE 支援三種檔案系統格式： [ISO 9660](#iso-9660)、 [Joliet](#joliet)和 [UDF](#universal-disk-format-udf)。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="9f5f4-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="9f5f4-105">ISO 9660</span></span>

<span data-ttu-id="9f5f4-106">ISO 9660 格式是 CD 資料光碟的原始標準檔案系統。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="9f5f4-107">此格式可在數個作業系統上辨識，包括 MSDOS.SYS、Mac OS、UNIX 和 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="9f5f4-108">ISO 9660 格式是由國際標準組織 (ISO) 所發行。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="9f5f4-109">格式從第16磁區開始，磁片區標頭為 CD0001;標頭的其餘部分如下。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="9f5f4-110">其他衍生格式也會從第16磁區開始，但會使用另一個字串作為磁片區標頭。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="9f5f4-111">例如，高塞拉里昂光碟使用字串 CD ROM0001 和光碟互動格式使用 CD I0001。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="9f5f4-112">標頭會指向以 ISO 9660 格式儲存檔案名的光碟區域。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="9f5f4-113">檔案和目錄命名慣例是由8個字元、一個句點和3個字元所組成。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="9f5f4-114">這是由 MSDOS.SYS 作業系統所使用的相同命名慣例。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="9f5f4-115">針對 Joliet 和 UDF 等格式的其他檔案系統標頭可以並存存在於光碟，而不會影響 ISO 9660 格式的可讀性。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="9f5f4-116">在索引之後，一組資料檔案會佔用光碟。每個檔案系統的索引會獨立參考光碟上的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="9f5f4-117">ISO 9660 規格定義了下列三種層級的格式：</span><span class="sxs-lookup"><span data-stu-id="9f5f4-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="9f5f4-118">層級1定義使用8.3 字元格式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="9f5f4-119">層級2允許較長的檔案名，如 DOS 6. xx、MacIntosh 和 UNIX 平臺上所找到的名稱。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="9f5f4-120">層級3允許交錯的資料和音訊檔案，以改善) 效能的抓取 (播放。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="9f5f4-121">此層級也會移除2GB 的檔案限制。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="9f5f4-122">映射主控 API **不** 支援此層級。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="9f5f4-123">DVD 光碟也可以使用 ISO 9660;不過，UDF 檔案系統是與 DVD 媒體搭配使用的最常見檔案系統。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="9f5f4-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="9f5f4-124">Joliet</span></span>

<span data-ttu-id="9f5f4-125">Joliet 格式是 ISO 9660 的衍生。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="9f5f4-126">此格式除了 ISO 9660 檔案系統索引之外，還會將 Joliet 檔案系統索引寫入光碟映射。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="9f5f4-127">Joliet 索引會針對檔案系統索引提供下列改善：</span><span class="sxs-lookup"><span data-stu-id="9f5f4-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="9f5f4-128">辨識長度最多為32個字元的長檔名。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="9f5f4-129">區分檔案名中的大寫和小寫字母。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="9f5f4-130">支援檔案名中的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="9f5f4-131">Joliet 格式標頭開始于光碟的第17磁區。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="9f5f4-132">由於 Joliet 格式會保留光碟上的 ISO 9660 檔案系統，因此會保留與符合 ISO 9660 規範之裝置的相容性。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="9f5f4-133">國際磁碟格式 (UDF)</span><span class="sxs-lookup"><span data-stu-id="9f5f4-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="9f5f4-134"> (UDF) 的國際磁碟格式是以光學儲存體技術關聯 (OSTA) 為光學媒體所開發的較新檔案系統。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="9f5f4-135">UDF 是數個作業系統所能辨識的可移植格式。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="9f5f4-136">UDF 會將 ISO 9660 取代為新的標準，尤其是在讀取/寫入媒體中。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="9f5f4-137">UDF 的功能包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="9f5f4-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="9f5f4-138">最多可支援2TB 大小的媒體。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="9f5f4-139">支援 flash 媒體、Iomega REV 光碟以及 CD MRW 光碟。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="9f5f4-140">將小於 2 KB 的檔案儲存在檔案專案區塊中。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="9f5f4-141">最多可支援 2 TB 的檔案，且長度為255個字元。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="9f5f4-142">支援一組符合各種作業系統的豐富檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="9f5f4-143">支援橋接器格式，其中的 ISO 9660、Joliet 和 UDF 格式都位於相同的光碟片上。這是在影片應用程式中使用，例如 DVD 影片、DVD + VR 和 DVD VR。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="9f5f4-144">支援命名資料流程和「即時」檔案。</span><span class="sxs-lookup"><span data-stu-id="9f5f4-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




