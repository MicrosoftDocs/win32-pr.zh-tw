---
title: Windows 投射的檔案系統詞彙
description: ProjFS 中使用的特殊字詞。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2020
ms.locfileid: "106990887"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="4f0e4-103">Windows 投射的檔案系統詞彙</span><span class="sxs-lookup"><span data-stu-id="4f0e4-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="4f0e4-104">ProjFS 中使用的特殊字詞。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="4f0e4-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**備份存放區**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-106">提供者維護的階層式資料，會以檔案和目錄的形式投射到檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**中途預留位置**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-108">已在本機修改過的檔案或目錄，在提供者的存放區中不再是其狀態的快取。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="4f0e4-109">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**完整檔案/目錄**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-111">在本機檔案系統中建立的檔案或目錄，或已修改過的檔案，使其不再是備份存放區中其狀態的快取。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="4f0e4-112">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**水合預留位置**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-114">其內容和中繼資料已快取至磁片的檔案。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="4f0e4-115">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**占 位 符**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-117">磁片上未完全存在的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="4f0e4-118">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**墓碑**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-120">表示已從本機檔案系統刪除之專案的特殊隱藏預留位置。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="4f0e4-121">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**虛擬檔案/目錄**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-123">未實際存在於磁片上的檔案或目錄，但投射到列舉結果。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="4f0e4-124">請參閱 [虛擬化根中的](cache-state.md)快取狀態。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**虛擬化實例**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-126">記憶體中的物件，可管理位於特定虛擬根目錄下之檔案和目錄集合的提供者與 ProjFS 之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="4f0e4-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**虛擬化根**</span><span class="sxs-lookup"><span data-stu-id="4f0e4-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="4f0e4-128">檔案系統中用來投射提供者資料的目錄。</span><span class="sxs-lookup"><span data-stu-id="4f0e4-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->