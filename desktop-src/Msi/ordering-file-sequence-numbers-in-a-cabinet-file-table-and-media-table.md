---
description: File 資料表包含安裝的所有原始程式檔的完整清單。
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: 排序封包、檔案資料表和媒體資料表中的檔案序號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07f9cd530d90fb0ef4d805b8ff2c96398cd97e55
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106998186"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a><span data-ttu-id="1f76f-103">排序封包、檔案資料表和媒體資料表中的檔案序號</span><span class="sxs-lookup"><span data-stu-id="1f76f-103">Ordering File Sequence Numbers in a Cabinet, File Table and Media Table</span></span>

<span data-ttu-id="1f76f-104">[File 資料表](file-table.md)包含安裝的所有原始程式檔的完整清單。</span><span class="sxs-lookup"><span data-stu-id="1f76f-104">The [File table](file-table.md) contains a complete list of all the source files for the installation.</span></span> <span data-ttu-id="1f76f-105">檔案可以儲存在來源媒體上做為個別檔案，或壓縮在封 [包](cabinet-files.md)檔中。</span><span class="sxs-lookup"><span data-stu-id="1f76f-105">Files can be stored on the source media as individual files or compressed within [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="1f76f-106">File 資料表之 [順序] 資料行中的序號，以及 [媒體資料表](media-table.md)的 [LastSequence] 欄位，指定檔案的安裝順序，以及每個檔案所在的來源媒體。</span><span class="sxs-lookup"><span data-stu-id="1f76f-106">The sequence numbers in the Sequence column of the File table, together with the LastSequence field of the [Media table](media-table.md), specify both the order of installation for files and the source media on which each file is located.</span></span> <span data-ttu-id="1f76f-107">媒體資料表中的每一筆記錄都會識別來源磁片，內含序號小於或等於 LastSequence 資料行中所顯示的值，且大於前一個磁片之 LastSequence 值的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="1f76f-107">Each record in the Media table identifies the source disk containing all the files with sequence numbers less than or equal to the value shown in the LastSequence column and greater than the LastSequence value of the previous disk.</span></span>

<span data-ttu-id="1f76f-108">例如，假設檔案的 [順序] 資料行中輸入了92的序號。</span><span class="sxs-lookup"><span data-stu-id="1f76f-108">For example, suppose a file has a sequence number of 92 entered in the Sequence column of the File table.</span></span> <span data-ttu-id="1f76f-109">為了判斷此檔案所在的來源磁片，安裝程式會檢查媒體資料表的記錄是否有最小 LastSequence 值大於92的專案。</span><span class="sxs-lookup"><span data-stu-id="1f76f-109">To determine on which source disk this file resides, the installer checks the record of the Media table for the entry with the smallest LastSequence value that is larger than 92.</span></span> <span data-ttu-id="1f76f-110">DiskId 資料行是媒體資料表的主要索引鍵，而此欄位可唯一識別資料表中的磁片。</span><span class="sxs-lookup"><span data-stu-id="1f76f-110">The DiskId column is the primary key for the Media table and this field uniquely identifies the disk in the table.</span></span>

<span data-ttu-id="1f76f-111">Windows Installer 封裝的檔案資料表中可列出的檔案數目上限為32767個檔案。</span><span class="sxs-lookup"><span data-stu-id="1f76f-111">The maximum limit on the number of files that can be listed in the File table of a Windows Installer package is 32767 files.</span></span> <span data-ttu-id="1f76f-112">若要建立包含更多檔案的 Windows Installer 套件，請參閱 [撰寫大型封裝](authoring-a-large-package.md)。</span><span class="sxs-lookup"><span data-stu-id="1f76f-112">To create a Windows Installer package containing more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

<span data-ttu-id="1f76f-113">封裝作者可以壓縮原始程式檔並將它們包含在封包檔中，以縮減其安裝套件的大小。</span><span class="sxs-lookup"><span data-stu-id="1f76f-113">Package authors can reduce the size of their installation packages by compressing the source files and including them in cabinet files.</span></span> <span data-ttu-id="1f76f-114">來源檔案映射可以是壓縮、未壓縮或混合兩種類型。</span><span class="sxs-lookup"><span data-stu-id="1f76f-114">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span> <span data-ttu-id="1f76f-115">如需壓縮和未壓縮來源的詳細資訊，請參閱 [壓縮和未](compressed-and-uncompressed-sources.md)壓縮的來源。</span><span class="sxs-lookup"><span data-stu-id="1f76f-115">For more information about compressed and uncompressed sources see [Compressed and Uncompressed Sources](compressed-and-uncompressed-sources.md).</span></span> <span data-ttu-id="1f76f-116">壓縮的來源檔案必須儲存在封包檔中。</span><span class="sxs-lookup"><span data-stu-id="1f76f-116">Compressed source files must be stored inside of a cabinet file.</span></span> <span data-ttu-id="1f76f-117">封包內的壓縮檔案有自己的內部序號。</span><span class="sxs-lookup"><span data-stu-id="1f76f-117">The compressed files inside a cabinet have their own internal sequence numbers.</span></span> <span data-ttu-id="1f76f-118">這些內部序號的值不需要符合 File 資料表內序號的值。</span><span class="sxs-lookup"><span data-stu-id="1f76f-118">The values of these internal sequence numbers do not need to match the value of the sequence numbers within the File table.</span></span> <span data-ttu-id="1f76f-119">但是，檔案資料表中指定的檔案順序必須與封包內的實際檔案順序相同。</span><span class="sxs-lookup"><span data-stu-id="1f76f-119">However, the sequence of the files specified in the File table must be identical to the actual sequence of the files within the cabinets.</span></span> <span data-ttu-id="1f76f-120">未壓縮檔案的序號不需要是唯一的。</span><span class="sxs-lookup"><span data-stu-id="1f76f-120">The sequence numbers of uncompressed files need not be unique.</span></span> <span data-ttu-id="1f76f-121">例如，如果所有檔案都已解壓縮且位於一個磁片上，則檔案資料表中的所有檔案都可以有相同的序號。</span><span class="sxs-lookup"><span data-stu-id="1f76f-121">For example, if all the files are uncompressed and reside on one disk, all the files can have the same sequence number in the File table.</span></span>

<span data-ttu-id="1f76f-122">媒體資料表描述組成安裝來源媒體的磁片集。</span><span class="sxs-lookup"><span data-stu-id="1f76f-122">The Media table describes the set of disks that make up the source media for the installation.</span></span> <span data-ttu-id="1f76f-123">媒體資料表中的第一個專案在 DiskId 欄位中一律必須有1個。</span><span class="sxs-lookup"><span data-stu-id="1f76f-123">The first entry in the Media table must always have a 1 in the DiskId field.</span></span> <span data-ttu-id="1f76f-124">檔案應組織于來源媒體上，讓磁片1上的所有檔案都具有比磁片2上的檔案序號還小的檔案資料表序號，而磁片2上的所有序號都應該小於磁片3的序號，依此類推。</span><span class="sxs-lookup"><span data-stu-id="1f76f-124">Files should be organized on the source media such that all the files on disk 1 have File table sequence numbers that are smaller than the sequence numbers of files on disk 2, and all of the sequence numbers on disk 2 should be smaller than on disk 3, and so on.</span></span> <span data-ttu-id="1f76f-125">這項需求也適用于同時包含壓縮和未壓縮來源的磁片。</span><span class="sxs-lookup"><span data-stu-id="1f76f-125">This requirement also applies to a disk that contains both compressed and uncompressed sources.</span></span> <span data-ttu-id="1f76f-126">例如，如果安裝的媒體來源位於兩個來源磁片上，而且如果磁片1同時包含未壓縮的檔案和封包檔，則這兩個未壓縮的檔案和封包檔中的檔案都必須小於磁片磁碟機上所儲存之任何檔案的最小檔案序號。</span><span class="sxs-lookup"><span data-stu-id="1f76f-126">For example, if the media sources for the installation are located on two source disks, and if disk 1 contains both uncompressed files and a cabinet file, then both of the uncompressed files and the files in the cabinet must have sequence numbers smaller than the smallest file sequence number of any file stored on disk 2.</span></span> <span data-ttu-id="1f76f-127">如果磁片1上的所有檔案都壓縮成封包檔，則可以撰寫如下表所示的媒體資料表。</span><span class="sxs-lookup"><span data-stu-id="1f76f-127">If all files on disk 1 are compressed in a cabinet file, the Media table could be authored as shown in the following table.</span></span>

<span data-ttu-id="1f76f-128">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="1f76f-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="1f76f-129">DiskId</span><span class="sxs-lookup"><span data-stu-id="1f76f-129">DiskId</span></span> | <span data-ttu-id="1f76f-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="1f76f-130">LastSequence</span></span> | <span data-ttu-id="1f76f-131">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="1f76f-131">DiskPrompt</span></span> | <span data-ttu-id="1f76f-132">內閣</span><span class="sxs-lookup"><span data-stu-id="1f76f-132">Cabinet</span></span>   | <span data-ttu-id="1f76f-133">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="1f76f-133">VolumeLabel</span></span> |
|--------|--------------|------------|-----------|-------------|
| <span data-ttu-id="1f76f-134">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-134">1</span></span>      | <span data-ttu-id="1f76f-135">5</span><span class="sxs-lookup"><span data-stu-id="1f76f-135">5</span></span>            | <span data-ttu-id="1f76f-136">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-136">1</span></span>          | <span data-ttu-id="1f76f-137">mycab.cab</span><span class="sxs-lookup"><span data-stu-id="1f76f-137">mycab.cab</span></span> | <span data-ttu-id="1f76f-138">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-138">Disk 1</span></span>      |
| <span data-ttu-id="1f76f-139">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-139">2</span></span>      | <span data-ttu-id="1f76f-140">10</span><span class="sxs-lookup"><span data-stu-id="1f76f-140">10</span></span>           | <span data-ttu-id="1f76f-141">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-141">2</span></span>          |           | <span data-ttu-id="1f76f-142">磁片2</span><span class="sxs-lookup"><span data-stu-id="1f76f-142">Disk 2</span></span>      |



 

<span data-ttu-id="1f76f-143">如果磁片1上的某些檔案壓縮成封包，有些檔案未壓縮，則可以依照下列方式撰寫媒體資料表。</span><span class="sxs-lookup"><span data-stu-id="1f76f-143">If some files on disk 1 are compressed in a cabinet and some are uncompressed, the Media table could be authored as follows.</span></span>

<span data-ttu-id="1f76f-144">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="1f76f-144">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="1f76f-145">DiskId</span><span class="sxs-lookup"><span data-stu-id="1f76f-145">DiskId</span></span> | <span data-ttu-id="1f76f-146">LastSequence</span><span class="sxs-lookup"><span data-stu-id="1f76f-146">LastSequence</span></span> | <span data-ttu-id="1f76f-147">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="1f76f-147">DiskPrompt</span></span> | <span data-ttu-id="1f76f-148">內閣</span><span class="sxs-lookup"><span data-stu-id="1f76f-148">Cabinet</span></span>   | <span data-ttu-id="1f76f-149">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="1f76f-149">VolumeLabel</span></span> |
|--------|--------------|------------|-----------|-------------|
| <span data-ttu-id="1f76f-150">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-150">1</span></span>      | <span data-ttu-id="1f76f-151">5</span><span class="sxs-lookup"><span data-stu-id="1f76f-151">5</span></span>            | <span data-ttu-id="1f76f-152">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-152">1</span></span>          |           | <span data-ttu-id="1f76f-153">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-153">Disk 1</span></span>      |
| <span data-ttu-id="1f76f-154">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-154">2</span></span>      | <span data-ttu-id="1f76f-155">10</span><span class="sxs-lookup"><span data-stu-id="1f76f-155">10</span></span>           | <span data-ttu-id="1f76f-156">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-156">1</span></span>          | <span data-ttu-id="1f76f-157">mycab.cab</span><span class="sxs-lookup"><span data-stu-id="1f76f-157">mycab.cab</span></span> | <span data-ttu-id="1f76f-158">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-158">Disk 1</span></span>      |
| <span data-ttu-id="1f76f-159">3</span><span class="sxs-lookup"><span data-stu-id="1f76f-159">3</span></span>      | <span data-ttu-id="1f76f-160">15</span><span class="sxs-lookup"><span data-stu-id="1f76f-160">15</span></span>           | <span data-ttu-id="1f76f-161">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-161">2</span></span>          |           | <span data-ttu-id="1f76f-162">磁片2</span><span class="sxs-lookup"><span data-stu-id="1f76f-162">Disk 2</span></span>      |



 

<span data-ttu-id="1f76f-163">請注意，下列媒體資料表中的撰寫不正確，因為它指定磁片2上的一些檔案序號，小於磁片1上的封包中的某些檔案。</span><span class="sxs-lookup"><span data-stu-id="1f76f-163">Note that the authoring in the following Media table is incorrect because it specifies some file sequence numbers on disk 2 that are smaller than some files inside the cabinet on disk 1.</span></span>

[<span data-ttu-id="1f76f-164">媒體資料表</span><span class="sxs-lookup"><span data-stu-id="1f76f-164">Media Table</span></span>](media-table.md)



| <span data-ttu-id="1f76f-165">DiskId</span><span class="sxs-lookup"><span data-stu-id="1f76f-165">DiskId</span></span> | <span data-ttu-id="1f76f-166">LastSequence</span><span class="sxs-lookup"><span data-stu-id="1f76f-166">LastSequence</span></span> | <span data-ttu-id="1f76f-167">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="1f76f-167">DiskPrompt</span></span> | <span data-ttu-id="1f76f-168">內閣</span><span class="sxs-lookup"><span data-stu-id="1f76f-168">Cabinet</span></span>   | <span data-ttu-id="1f76f-169">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="1f76f-169">VolumeLabel</span></span> |
|--------|--------------|------------|-----------|-------------|
| <span data-ttu-id="1f76f-170">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-170">1</span></span>      | <span data-ttu-id="1f76f-171">5</span><span class="sxs-lookup"><span data-stu-id="1f76f-171">5</span></span>            | <span data-ttu-id="1f76f-172">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-172">1</span></span>          |           | <span data-ttu-id="1f76f-173">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-173">Disk 1</span></span>      |
| <span data-ttu-id="1f76f-174">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-174">2</span></span>      | <span data-ttu-id="1f76f-175">10</span><span class="sxs-lookup"><span data-stu-id="1f76f-175">10</span></span>           | <span data-ttu-id="1f76f-176">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-176">2</span></span>          |           | <span data-ttu-id="1f76f-177">磁片2</span><span class="sxs-lookup"><span data-stu-id="1f76f-177">Disk 2</span></span>      |
| <span data-ttu-id="1f76f-178">3</span><span class="sxs-lookup"><span data-stu-id="1f76f-178">3</span></span>      | <span data-ttu-id="1f76f-179">15</span><span class="sxs-lookup"><span data-stu-id="1f76f-179">15</span></span>           | <span data-ttu-id="1f76f-180">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-180">1</span></span>          | <span data-ttu-id="1f76f-181">mycab.cab</span><span class="sxs-lookup"><span data-stu-id="1f76f-181">mycab.cab</span></span> | <span data-ttu-id="1f76f-182">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-182">Disk 1</span></span>      |



 

<span data-ttu-id="1f76f-183">大型檔案可以分割成兩個或多個封包檔。</span><span class="sxs-lookup"><span data-stu-id="1f76f-183">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="1f76f-184">在下一個封包檔中，任何一個封包檔中都不能有15個以上的檔案。</span><span class="sxs-lookup"><span data-stu-id="1f76f-184">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="1f76f-185">例如，如果您有三個封包檔，第一個封包可以有15個檔案跨越第二個封包檔，而第二個封包可以有15個檔案跨越第三封封包檔。</span><span class="sxs-lookup"><span data-stu-id="1f76f-185">For example, if you have three cabinet files, the first cabinet can have 15 files that span to the second cabinet file, and the second cabinet can have 15 files that span to the third cabinet file.</span></span> <span data-ttu-id="1f76f-186">當您針對多個封包的檔案將記錄新增至檔案資料表時，請使用檔案的第一個部分來指定您在 [順序] 資料行中輸入的檔案序號。</span><span class="sxs-lookup"><span data-stu-id="1f76f-186">When you add a record to the File table for a file multiple cabinets, use the first part of the file to specify the file sequence number you enter in the Sequence column.</span></span>

<span data-ttu-id="1f76f-187">如果有三個檔案、兩個封包和兩個磁片，則可以撰寫檔案和媒體資料表，如下所示。</span><span class="sxs-lookup"><span data-stu-id="1f76f-187">The File and Media tables could be authored as follows if there are three files, two cabinets, and two disks.</span></span> <span data-ttu-id="1f76f-188">在此範例中，c1.cab 位於 disk1 上，c2.cab 位於 disk2 上。</span><span class="sxs-lookup"><span data-stu-id="1f76f-188">In this example, c1.cab resides on disk1 and c2.cab resides on disk2.</span></span> <span data-ttu-id="1f76f-189">File f2 會跨越兩個封包。</span><span class="sxs-lookup"><span data-stu-id="1f76f-189">The file f2 spans both cabinets.</span></span> <span data-ttu-id="1f76f-190">c1.cab 的封包包含整個 f1 檔案和檔案 f2 的第一個部分。</span><span class="sxs-lookup"><span data-stu-id="1f76f-190">The c1.cab cabinet contains the entire f1 file and the first part of file f2.</span></span> <span data-ttu-id="1f76f-191">c2.cab 的封包包含 f2 和整個 f3 檔案的第二部分。</span><span class="sxs-lookup"><span data-stu-id="1f76f-191">The c2.cab cabinet contains the second part of f2 and the entire f3 file.</span></span>

<span data-ttu-id="1f76f-192">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="1f76f-192">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="1f76f-193">DiskId</span><span class="sxs-lookup"><span data-stu-id="1f76f-193">DiskId</span></span> | <span data-ttu-id="1f76f-194">LastSequence</span><span class="sxs-lookup"><span data-stu-id="1f76f-194">LastSequence</span></span> | <span data-ttu-id="1f76f-195">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="1f76f-195">DiskPrompt</span></span> | <span data-ttu-id="1f76f-196">內閣</span><span class="sxs-lookup"><span data-stu-id="1f76f-196">Cabinet</span></span> | <span data-ttu-id="1f76f-197">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="1f76f-197">VolumeLabel</span></span> |
|--------|--------------|------------|---------|-------------|
| <span data-ttu-id="1f76f-198">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-198">1</span></span>      | <span data-ttu-id="1f76f-199">5</span><span class="sxs-lookup"><span data-stu-id="1f76f-199">5</span></span>            | <span data-ttu-id="1f76f-200">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-200">1</span></span>          | <span data-ttu-id="1f76f-201">c1.cab</span><span class="sxs-lookup"><span data-stu-id="1f76f-201">c1.cab</span></span>  | <span data-ttu-id="1f76f-202">磁片1</span><span class="sxs-lookup"><span data-stu-id="1f76f-202">Disk 1</span></span>      |
| <span data-ttu-id="1f76f-203">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-203">2</span></span>      | <span data-ttu-id="1f76f-204">10</span><span class="sxs-lookup"><span data-stu-id="1f76f-204">10</span></span>           | <span data-ttu-id="1f76f-205">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-205">2</span></span>          | <span data-ttu-id="1f76f-206">c2.cab</span><span class="sxs-lookup"><span data-stu-id="1f76f-206">c2.cab</span></span>  | <span data-ttu-id="1f76f-207">磁片2</span><span class="sxs-lookup"><span data-stu-id="1f76f-207">Disk 2</span></span>      |



 

<span data-ttu-id="1f76f-208">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="1f76f-208">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="1f76f-209">檔案</span><span class="sxs-lookup"><span data-stu-id="1f76f-209">File</span></span> | <span data-ttu-id="1f76f-210">順序</span><span class="sxs-lookup"><span data-stu-id="1f76f-210">Sequence</span></span> |
|------|----------|
| <span data-ttu-id="1f76f-211">按</span><span class="sxs-lookup"><span data-stu-id="1f76f-211">f1</span></span>   | <span data-ttu-id="1f76f-212">1</span><span class="sxs-lookup"><span data-stu-id="1f76f-212">1</span></span>        |
| <span data-ttu-id="1f76f-213">進入</span><span class="sxs-lookup"><span data-stu-id="1f76f-213">f2</span></span>   | <span data-ttu-id="1f76f-214">2</span><span class="sxs-lookup"><span data-stu-id="1f76f-214">2</span></span>        |
| <span data-ttu-id="1f76f-215">f3</span><span class="sxs-lookup"><span data-stu-id="1f76f-215">f3</span></span>   | <span data-ttu-id="1f76f-216">6</span><span class="sxs-lookup"><span data-stu-id="1f76f-216">6</span></span>        |



 

 

 



