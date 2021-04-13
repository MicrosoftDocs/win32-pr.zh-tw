---
title: Capture 檔案的磁碟空間預先配置
description: Capture 檔案的磁碟空間預先配置
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE 訊息
- capFileAlloc 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300692"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="56c15-105">Capture 檔案的磁碟空間預先配置</span><span class="sxs-lookup"><span data-stu-id="56c15-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="56c15-106">預先配置磁碟空間可供 capture 檔案在開始進行捕獲作業之前，先在磁片上建立指定大小的檔案。</span><span class="sxs-lookup"><span data-stu-id="56c15-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="56c15-107">預先配置 capture 檔案可減少在進行 capture 時所需的處理，並導致減少捨棄的畫面格。</span><span class="sxs-lookup"><span data-stu-id="56c15-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="56c15-108">您可以使用 [ [**WM \_ CAP 檔案 \_ \_ 配置**](wm-cap-file-allocate.md) 訊息 (] 或 [ [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏) 來預先配置 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="56c15-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="56c15-109">一般而言，您的應用程式應預先配置足夠的磁碟空間，以包含預期的最大 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="56c15-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="56c15-110">預先配置磁碟空間不會限制所捕獲檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="56c15-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="56c15-111">如果捕捉的資料超過配置的空間，則會自動放大檔案大小。</span><span class="sxs-lookup"><span data-stu-id="56c15-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="56c15-112">對 capture 檔案進行的後續寫入作業會重複使用配置給檔案的磁碟空間部分，以保留檔案的大小和片段。</span><span class="sxs-lookup"><span data-stu-id="56c15-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="56c15-113">您也可以藉由重組捕獲檔案來改善「捕獲效能」。</span><span class="sxs-lookup"><span data-stu-id="56c15-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="56c15-114">若要重組檔案，請使用磁碟重組工具，例如磁片磁碟重組工具。</span><span class="sxs-lookup"><span data-stu-id="56c15-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="56c15-115">如果您使用已重組的捕獲檔案，並于稍後將它放大，則應該重組放大的檔案。</span><span class="sxs-lookup"><span data-stu-id="56c15-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="56c15-116">擴大重組的捕獲檔案可將檔案的展開部分片段化，並降低捕捉作業的效能。</span><span class="sxs-lookup"><span data-stu-id="56c15-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="56c15-117">您也可以使用未壓縮的磁片來取得影片捕獲，以改善效能。</span><span class="sxs-lookup"><span data-stu-id="56c15-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="56c15-118">在 capture 期間壓縮資料可以限制磁片的捕獲輸送量。</span><span class="sxs-lookup"><span data-stu-id="56c15-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="56c15-119">應用程式可以保留永久的捕獲檔案，以避免每次啟動時預先配置和重組檔案所需的時間。</span><span class="sxs-lookup"><span data-stu-id="56c15-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="56c15-120">因為 capture 檔案可能需要相當大的磁碟空間，而且預先配置 capture 檔案會移除現有 capture 檔案中的所有資料，所以應用程式應該讓使用者決定檔案是永久或暫時性的。</span><span class="sxs-lookup"><span data-stu-id="56c15-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




