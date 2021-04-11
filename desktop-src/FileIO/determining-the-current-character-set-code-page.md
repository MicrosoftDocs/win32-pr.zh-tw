---
description: AreFileApisANSI 函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: 判斷目前的字元集字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849504"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="e8808-103">判斷目前的字元集字碼頁</span><span class="sxs-lookup"><span data-stu-id="e8808-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="e8808-104">[**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi)函式會判斷檔案 i/o 函數是否使用 ANSI 或 OEM 字元集字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e8808-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="e8808-105">[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)函式會讓函數使用 ANSI 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e8808-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="e8808-106">[**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)函式會讓函數使用 OEM 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e8808-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="e8808-107">依預設，檔案 i/o 函數會使用 ANSI 檔案名。</span><span class="sxs-lookup"><span data-stu-id="e8808-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="e8808-108">接受或傳回檔案名的 Kernel32.dll 所匯出的函式會受到檔案字碼頁設定的影響。</span><span class="sxs-lookup"><span data-stu-id="e8808-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="e8808-109">[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi)和 [**可透過 setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem)都會設定每個進程的字碼頁，而不是每個執行緒或每部電腦的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="e8808-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



