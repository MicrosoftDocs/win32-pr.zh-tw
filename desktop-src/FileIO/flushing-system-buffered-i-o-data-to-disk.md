---
description: Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: 將 System-Buffered i/o 資料排清到磁片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513993"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a><span data-ttu-id="36dde-103">將 System-Buffered i/o 資料排清到磁片</span><span class="sxs-lookup"><span data-stu-id="36dde-103">Flushing System-Buffered I/O Data to Disk</span></span>

<span data-ttu-id="36dde-104">Windows 會將資料儲存在系統維護的資料緩衝區中的檔案讀取和寫入作業，以將磁片效能優化。</span><span class="sxs-lookup"><span data-stu-id="36dde-104">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span> <span data-ttu-id="36dde-105">當應用程式寫入檔案時，系統通常會緩衝資料，並定期將資料寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="36dde-105">When an application writes to a file, the system usually buffers the data and writes the data to the disk on a regular basis.</span></span> <span data-ttu-id="36dde-106">應用程式可以使用 [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) 函數，強制作業系統將這些資料緩衝區的內容寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="36dde-106">An application can force the operating system to write the contents of these data buffers to the disk by using the [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) function.</span></span> <span data-ttu-id="36dde-107">或者，應用程式可以指定當使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式建立或開啟檔案時，將檔案旗標設定為 **\_ \_ 無 \_ 緩衝** 旗標，以略過資料緩衝區並直接寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="36dde-107">Alternatively, an application can specify that write operations are to bypass the data buffer and write directly to the disk by setting the **FILE\_FLAG\_NO\_BUFFERING** flag when the file is created or opened using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span>

<span data-ttu-id="36dde-108">如果在檔案關閉時，內部緩衝區中有資料，作業系統不會在關閉檔案之前自動將緩衝區的內容寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="36dde-108">If there is data in the internal buffer when the file is closed, the operating system does not automatically write the contents of the buffer to the disk before closing the file.</span></span> <span data-ttu-id="36dde-109">如果應用程式不會在關閉檔案之前強制作業系統將緩衝區寫入磁片，快取演算法會決定寫入緩衝區的時間。</span><span class="sxs-lookup"><span data-stu-id="36dde-109">If the application does not force the operating system to write the buffer to disk before closing the file, the caching algorithm determines when the buffer is written.</span></span>

> [!Note]  
> <span data-ttu-id="36dde-110">在讀取或寫入作業使用時存取資料緩衝區可能會損毀緩衝區。</span><span class="sxs-lookup"><span data-stu-id="36dde-110">Accessing a data buffer while a read or write operation is using it may corrupt the buffer.</span></span> <span data-ttu-id="36dde-111">在作業完成之前，應用程式不得讀取、寫入、重新配置或釋放讀取或寫入作業正在使用的資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="36dde-111">Applications must not read from, write to, reallocate, or free the data buffer that a read or write operation is using until the operation completes.</span></span>

 

 

 



