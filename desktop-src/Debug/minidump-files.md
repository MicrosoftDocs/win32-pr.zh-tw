---
description: 應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: 小型傾印檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110208"
---
# <a name="minidump-files"></a><span data-ttu-id="37ea0-103">小型傾印檔案</span><span class="sxs-lookup"><span data-stu-id="37ea0-103">Minidump Files</span></span>

<span data-ttu-id="37ea0-104">應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。</span><span class="sxs-lookup"><span data-stu-id="37ea0-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="37ea0-105">應用程式可以非常快速且有效率地建立小型傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="37ea0-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="37ea0-106">因為小型傾印檔案很小，所以可以輕鬆地透過網際網路傳送給應用程式的技術支援。</span><span class="sxs-lookup"><span data-stu-id="37ea0-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="37ea0-107">小型傾印檔案未包含完整損毀傾印檔案的資訊，但它包含足夠的資訊來執行基本的調試作業。</span><span class="sxs-lookup"><span data-stu-id="37ea0-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="37ea0-108">若要讀取小型傾印檔案，您必須有可供偵錯工具使用的二進位檔和符號檔。</span><span class="sxs-lookup"><span data-stu-id="37ea0-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="37ea0-109">目前版本的 Microsoft Office 和 Microsoft Windows 會建立小型傾印檔案，以在客戶的電腦上分析失敗的目的。</span><span class="sxs-lookup"><span data-stu-id="37ea0-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="37ea0-110">下列 DbgHelp 函式可用於小型傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="37ea0-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="37ea0-111">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="37ea0-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="37ea0-112">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="37ea0-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="37ea0-113">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="37ea0-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



