---
description: 應用程式會使用 ReadFile、ReadFileEx、WriteFile 和 WriteFileEx 函式來讀取和寫入檔案。
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: 讀取和寫入檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979289"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="3b80c-103">讀取和寫入檔案</span><span class="sxs-lookup"><span data-stu-id="3b80c-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="3b80c-104">應用程式會使用 [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)、 [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)、 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)和 [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) 函式來讀取和寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="3b80c-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="3b80c-105">這些函式需要開啟檔案的控制碼，才能分別供讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="3b80c-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="3b80c-106">它們會在檔案指標所指示的位置讀取和寫入指定的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="3b80c-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="3b80c-107">資料的讀取和寫入與指定的完全相同;這些函數不會格式化資料。</span><span class="sxs-lookup"><span data-stu-id="3b80c-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="3b80c-108">當檔案指標到達檔案結尾，而應用程式嘗試從檔案讀取時，不會發生任何錯誤，但不會讀取任何位元組。</span><span class="sxs-lookup"><span data-stu-id="3b80c-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="3b80c-109">因此，讀取零位元組而不發生錯誤，表示應用程式已到達檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="3b80c-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="3b80c-110">寫入零位元組不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="3b80c-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="3b80c-111">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="3b80c-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3b80c-112">本節內容</span><span class="sxs-lookup"><span data-stu-id="3b80c-112">In this section</span></span>



| <span data-ttu-id="3b80c-113">主題</span><span class="sxs-lookup"><span data-stu-id="3b80c-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="3b80c-114">描述</span><span class="sxs-lookup"><span data-stu-id="3b80c-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b80c-115">放置檔案指標</span><span class="sxs-lookup"><span data-stu-id="3b80c-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="3b80c-116">Windows 使用檔案指標來追蹤讀取或寫入的位元組。</span><span class="sxs-lookup"><span data-stu-id="3b80c-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="3b80c-117">使用 Scatter-Gather 配置讀取或寫入檔案</span><span class="sxs-lookup"><span data-stu-id="3b80c-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="3b80c-118">描述在一項作業中用來讀取或寫入非連續資料區塊的散佈集合配置。</span><span class="sxs-lookup"><span data-stu-id="3b80c-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="3b80c-119">將 System-Buffered i/o 資料排清到磁片</span><span class="sxs-lookup"><span data-stu-id="3b80c-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="3b80c-120">Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。</span><span class="sxs-lookup"><span data-stu-id="3b80c-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="3b80c-121">截斷或擴充檔案</span><span class="sxs-lookup"><span data-stu-id="3b80c-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="3b80c-122">應用程式可以藉由呼叫 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)來截斷或擴充檔案。</span><span class="sxs-lookup"><span data-stu-id="3b80c-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




