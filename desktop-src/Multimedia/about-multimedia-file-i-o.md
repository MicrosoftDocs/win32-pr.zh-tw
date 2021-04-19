---
title: 關於多媒體檔案 i/o
description: 關於多媒體檔案 i/o
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows 多媒體，檔案 i/o
- 多媒體，檔案 i/o
- 多媒體輸入，file i/o
- 多媒體檔案 i/o，關於
- 檔案 i/o，關於
- 輸入和輸出 (i/o) ，關於
- I/o (輸入和輸出) ，關於
- 基本 i/o
- " (RIFF) 的資源交換檔案格式"
- 'RIFF (資源交換檔案格式) '
- RIFF I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967621"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="bb483-114">關於多媒體檔案 i/o</span><span class="sxs-lookup"><span data-stu-id="bb483-114">About Multimedia File I/O</span></span>

<span data-ttu-id="bb483-115">大部分的多媒體應用程式都需要檔案輸入和輸出 (i/o) ，也就是建立、讀取和寫入磁片檔案的能力。</span><span class="sxs-lookup"><span data-stu-id="bb483-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="bb483-116">多媒體檔案 i/o 服務提供緩衝和未緩衝處理的檔案 i/o，以及 RIFF 檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="bb483-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="bb483-117">這些服務可使用可在應用程式間共用的自訂 i/o 程式進行擴充。</span><span class="sxs-lookup"><span data-stu-id="bb483-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="bb483-118">大部分的應用程式只需要基本的檔案 i/o 服務和 RIFF 檔案 i/o 服務。</span><span class="sxs-lookup"><span data-stu-id="bb483-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="bb483-119">與檔案 i/o 效能相關的應用程式，例如即時從光碟串流資料的應用程式，可以使用服務直接存取檔案 i/o 緩衝區來將效能優化。</span><span class="sxs-lookup"><span data-stu-id="bb483-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="bb483-120">存取自訂存放裝置系統的應用程式（例如檔案封存和資料庫）可以提供自己的 i/o 程式，以讀取和寫入儲存系統的元素。</span><span class="sxs-lookup"><span data-stu-id="bb483-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




