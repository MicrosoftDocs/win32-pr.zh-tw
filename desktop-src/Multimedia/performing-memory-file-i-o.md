---
title: 執行記憶體檔 i/o
description: 執行記憶體檔 i/o
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- 多媒體檔案 i/o，記憶體
- 檔案 i/o，記憶體
- 輸入和輸出 (i/o) ，記憶體
- I/o (輸入和輸出) ，記憶體
- 記憶體 i/o
- mmioOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462961"
---
# <a name="performing-memory-file-io"></a><span data-ttu-id="7c041-109">執行記憶體檔 i/o</span><span class="sxs-lookup"><span data-stu-id="7c041-109">Performing Memory File I/O</span></span>

<span data-ttu-id="7c041-110">多媒體檔案 i/o 服務可讓您將記憶體區塊視為檔案。</span><span class="sxs-lookup"><span data-stu-id="7c041-110">The multimedia file I/O services let you treat a block of memory as a file.</span></span> <span data-ttu-id="7c041-111">如果您在記憶體中已經有檔案映射，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="7c041-111">This can be useful if you already have a file image in memory.</span></span> <span data-ttu-id="7c041-112">記憶體檔案可讓您減少程式碼中的特殊案例數目，因為基於 i/o 用途，您可以將記憶體檔案視為磁片型檔案。</span><span class="sxs-lookup"><span data-stu-id="7c041-112">Memory files let you reduce the number of special-case conditions in your code because, for I/O purposes, you can treat memory files as if they were disk-based files.</span></span> <span data-ttu-id="7c041-113">您也可以使用記憶體檔案搭配剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="7c041-113">You can also use memory files with the clipboard.</span></span>

<span data-ttu-id="7c041-114">就像 i/o 緩衝區一樣，記憶體檔案也可以使用應用程式所配置的記憶體或檔案 i/o 管理員所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7c041-114">As with I/O buffers, memory files can use memory allocated by the application or by the file I/O manager.</span></span> <span data-ttu-id="7c041-115">此外，記憶體檔案可以是可擴充或 nonexpandable。</span><span class="sxs-lookup"><span data-stu-id="7c041-115">In addition, memory files can be either expandable or nonexpandable.</span></span> <span data-ttu-id="7c041-116">當檔案 i/o 管理員到達可延伸記憶體檔案的結尾時，它會依預先定義的增量展開記憶體檔案。</span><span class="sxs-lookup"><span data-stu-id="7c041-116">When the file I/O manager reaches the end of an expandable memory file, it expands the memory file by a predefined increment.</span></span>

<span data-ttu-id="7c041-117">若要開啟記憶體檔案，請使用 [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) 函數，並將 *szFilename* 參數設定為 **Null** ，並 \_ 在 *dwOpenFlags* 參數中設定 MMIO READWRITE 旗標。</span><span class="sxs-lookup"><span data-stu-id="7c041-117">To open a memory file, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function with the *szFilename* parameter set to **NULL** and the MMIO\_READWRITE flag set in the *dwOpenFlags* parameter.</span></span> <span data-ttu-id="7c041-118">將 *lpmmioinfo* 參數設定為指向已設定的 [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) 結構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7c041-118">Set the *lpmmioinfo* parameter to point to an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure that has been set up as follows:</span></span>

1.  <span data-ttu-id="7c041-119">將 **pIOProc** 成員設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7c041-119">Set the **pIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="7c041-120">將 **fccIOProc** 成員設定為 FOURCC \_ MEM。</span><span class="sxs-lookup"><span data-stu-id="7c041-120">Set the **fccIOProc** member to FOURCC\_MEM.</span></span>
3.  <span data-ttu-id="7c041-121">設定 **pchBuffer** 成員以指向記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="7c041-121">Set the **pchBuffer** member to point to the memory block.</span></span> <span data-ttu-id="7c041-122">若要要求檔案 i/o 管理員配置記憶體區塊，請將 **pchBuffer** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7c041-122">To request that the file I/O manager allocate the memory block, set **pchBuffer** to **NULL**.</span></span>
4.  <span data-ttu-id="7c041-123">將 **cchBuffer** 成員設定為記憶體區塊的初始大小。</span><span class="sxs-lookup"><span data-stu-id="7c041-123">Set the **cchBuffer** member to the initial size of the memory block.</span></span>
5.  <span data-ttu-id="7c041-124">將 **adwInfo** 成員設定為記憶體區塊的最小擴充大小。</span><span class="sxs-lookup"><span data-stu-id="7c041-124">Set the **adwInfo** member to the minimum expansion size of the memory block.</span></span> <span data-ttu-id="7c041-125">若為 nonexpandable 記憶體檔案，請將 **adwInfo** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7c041-125">For a nonexpandable memory file, set **adwInfo** to **NULL**.</span></span>
6.  <span data-ttu-id="7c041-126">將所有其他成員設定為零。</span><span class="sxs-lookup"><span data-stu-id="7c041-126">Set all other members to zero.</span></span>

<span data-ttu-id="7c041-127">配置記憶體以做為 nonexpandable 記憶體檔案沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="7c041-127">There are no restrictions on allocating memory for use as a nonexpandable memory file.</span></span>

 

 