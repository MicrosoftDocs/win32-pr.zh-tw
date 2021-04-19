---
description: 記錄和錯誤報表
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: 記錄和錯誤報表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970739"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="430fc-103">記錄和錯誤報表</span><span class="sxs-lookup"><span data-stu-id="430fc-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="430fc-104">記錄檔</span><span class="sxs-lookup"><span data-stu-id="430fc-104">Log file</span></span>

<span data-ttu-id="430fc-105">COMREPL 會產生包含狀態和錯誤訊息的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="430fc-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="430fc-106">此檔案會儲存在 COMREPL 于% systemdir% \\ com replication COMREPL 中啟動的電腦上 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="430fc-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="430fc-107">當複製階段開始時，會清除此記錄檔。</span><span class="sxs-lookup"><span data-stu-id="430fc-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="430fc-108">後續的目標安裝將會附加至檔案。</span><span class="sxs-lookup"><span data-stu-id="430fc-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="430fc-109">錯誤處理</span><span class="sxs-lookup"><span data-stu-id="430fc-109">Error handling</span></span>

<span data-ttu-id="430fc-110">錯誤會記錄在上述的記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="430fc-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="430fc-111">您也可以在來源或目的電腦的事件記錄檔中找到詳細的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="430fc-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="430fc-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="430fc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="430fc-113">檔案管理</span><span class="sxs-lookup"><span data-stu-id="430fc-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="430fc-114">複寫階段</span><span class="sxs-lookup"><span data-stu-id="430fc-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="430fc-115">使用 COMREPL</span><span class="sxs-lookup"><span data-stu-id="430fc-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="430fc-116">複寫的內容</span><span class="sxs-lookup"><span data-stu-id="430fc-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



