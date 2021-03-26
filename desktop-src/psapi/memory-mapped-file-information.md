---
title: Memory-Mapped 檔案資訊
description: 記憶體對應檔 (或檔案對應) 是將檔案的內容與進程的部分虛擬位址空間產生關聯的結果。 可以用來在兩個或多個進程之間共用檔案或記憶體。
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093120"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="daa14-104">Memory-Mapped 檔案資訊</span><span class="sxs-lookup"><span data-stu-id="daa14-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="daa14-105">*記憶體對應* 檔 (或檔案 *對應*) 是將檔案的內容與進程的部分虛擬位址空間產生關聯的結果。</span><span class="sxs-lookup"><span data-stu-id="daa14-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="daa14-106">可以用來在兩個或多個進程之間共用檔案或記憶體。</span><span class="sxs-lookup"><span data-stu-id="daa14-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="daa14-107">[**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea)函式會接收進程控制碼和位址的指標做為輸入。</span><span class="sxs-lookup"><span data-stu-id="daa14-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="daa14-108">如果位址是在進程的虛擬位址空間中的記憶體對應檔案內，則函式會傳回記憶體對應檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="daa14-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="daa14-109">**GetMappedFileName** 所傳回的檔案名會使用裝置表單，而不是磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="daa14-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="daa14-110">例如，檔案名 c： \\ winnt \\ system32 \\ ctype. nls 在裝置形式中看起來會像這樣：</span><span class="sxs-lookup"><span data-stu-id="daa14-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="daa14-111">\\裝置 \\ Harddisk0 \\ Partition1 \\ WINNT \\ System32 \\ ctype. nls</span><span class="sxs-lookup"><span data-stu-id="daa14-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="daa14-112">如需記憶體對應檔案的詳細資訊，請參閱檔案 [對應](/windows/desktop/Memory/file-mapping)。</span><span class="sxs-lookup"><span data-stu-id="daa14-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="daa14-113">如需將裝置形式的檔案名轉換成磁碟機號的範例，請參閱 [從檔案控制代碼取得檔案名](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle)。</span><span class="sxs-lookup"><span data-stu-id="daa14-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 