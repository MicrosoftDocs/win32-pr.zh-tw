---
description: 事件記錄會代表系統和在系統上執行的應用程式，儲存重要事件的記錄。
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: 記錄指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115200"
---
# <a name="logging-guidelines"></a><span data-ttu-id="813d4-103">記錄指導方針</span><span class="sxs-lookup"><span data-stu-id="813d4-103">Logging Guidelines</span></span>

<span data-ttu-id="813d4-104">事件記錄會代表系統和在系統上執行的應用程式，儲存重要事件的記錄。</span><span class="sxs-lookup"><span data-stu-id="813d4-104">Event logs store records of significant events on behalf of the system and applications running on the system.</span></span> <span data-ttu-id="813d4-105">由於記錄功能是一般用途，因此您必須決定適當的記錄資訊。</span><span class="sxs-lookup"><span data-stu-id="813d4-105">Because the logging functions are general purpose, you must decide what information is appropriate to log.</span></span> <span data-ttu-id="813d4-106">一般而言，您應該只記錄可能有助於診斷硬體或軟體問題的資訊。</span><span class="sxs-lookup"><span data-stu-id="813d4-106">Generally, you should log only information that could be useful in diagnosing a hardware or software problem.</span></span> <span data-ttu-id="813d4-107">事件記錄並非用來做為追蹤工具。</span><span class="sxs-lookup"><span data-stu-id="813d4-107">Event logging is not intended to be used as a tracing tool.</span></span>

## <a name="choosing-events-to-log"></a><span data-ttu-id="813d4-108">選擇要記錄的事件</span><span class="sxs-lookup"><span data-stu-id="813d4-108">Choosing Events to Log</span></span>

<span data-ttu-id="813d4-109">以下是事件記錄會有説明的案例範例：</span><span class="sxs-lookup"><span data-stu-id="813d4-109">The following are examples of cases in which event logging can be helpful:</span></span>

-   <span data-ttu-id="813d4-110">資源問題。</span><span class="sxs-lookup"><span data-stu-id="813d4-110">Resource problems.</span></span> <span data-ttu-id="813d4-111">當記憶體配置失敗時，記錄警告事件有助於指出記憶體不足狀況的原因。</span><span class="sxs-lookup"><span data-stu-id="813d4-111">Logging a Warning event when memory allocation fails can help indicate the cause of a low-memory situation.</span></span>
-   <span data-ttu-id="813d4-112">硬體問題。</span><span class="sxs-lookup"><span data-stu-id="813d4-112">Hardware problems.</span></span> <span data-ttu-id="813d4-113">如果設備磁碟機發生磁碟控制卡超時、平行埠的電源中斷，或網路或序列卡的資料錯誤，設備磁碟機可以記錄這些事件的相關資訊，以協助系統管理員診斷硬體問題。</span><span class="sxs-lookup"><span data-stu-id="813d4-113">If a device driver encounters a disk controller time-out, a power failure in a parallel port, or a data error from a network or serial card, the device driver can log information about these events to help the system administrator diagnose hardware problems.</span></span>
-   <span data-ttu-id="813d4-114">損毀的磁區。</span><span class="sxs-lookup"><span data-stu-id="813d4-114">Bad sectors.</span></span> <span data-ttu-id="813d4-115">如果磁片驅動程式遇到損壞的磁區，它可能會在重試作業之後讀取或寫入磁區，但最後的磁區將會不良。</span><span class="sxs-lookup"><span data-stu-id="813d4-115">If a disk driver encounters a bad sector, it may be able to read from or write to the sector after retrying the operation, but the sector will go bad eventually.</span></span> <span data-ttu-id="813d4-116">如果磁片驅動程式可以繼續，則應該記錄警告事件;否則，它應該記錄錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="813d4-116">If the disk driver can proceed, it should log a Warning event; otherwise, it should log an Error event.</span></span> <span data-ttu-id="813d4-117">如果檔案系統驅動程式發現大量的損毀的磁區並修正它們，記錄警告事件可能有助於系統管理員判斷磁片可能即將失敗。</span><span class="sxs-lookup"><span data-stu-id="813d4-117">If a file system driver finds a large number of bad sectors and fixes them, logging Warning events might help an administrator determine that the disk may be about to fail.</span></span>
-   <span data-ttu-id="813d4-118">資訊事件。</span><span class="sxs-lookup"><span data-stu-id="813d4-118">Information events.</span></span> <span data-ttu-id="813d4-119">伺服器應用程式 (例如資料庫伺服器) 記錄使用者登入、開啟資料庫或開機檔案傳輸。</span><span class="sxs-lookup"><span data-stu-id="813d4-119">A server application (such as a database server) records a user logging on, opening a database, or starting a file transfer.</span></span> <span data-ttu-id="813d4-120">伺服器也可以記錄其他事件（例如錯誤） (無法存取檔案、主機進程中斷連接等) 、資料庫損毀，或檔案傳輸是否成功。</span><span class="sxs-lookup"><span data-stu-id="813d4-120">The server can also log other events such as errors (cannot access file, host process disconnected, and so on), database corruption, or whether a file transfer was successful.</span></span>

## <a name="writing-messages"></a><span data-ttu-id="813d4-121">寫入訊息</span><span class="sxs-lookup"><span data-stu-id="813d4-121">Writing Messages</span></span>

<span data-ttu-id="813d4-122">對於嘗試針對問題進行疑難排解的系統管理員和使用者而言，訊息應該是合理的。</span><span class="sxs-lookup"><span data-stu-id="813d4-122">Messages should make sense to administrators and users who are trying to troubleshoot a problem.</span></span> <span data-ttu-id="813d4-123">訊息應該包含所有必要資訊，以瞭解造成問題的原因，以及如何修正問題。</span><span class="sxs-lookup"><span data-stu-id="813d4-123">A message should contain all the information needed to understand what caused the problem and how to correct it.</span></span>

<span data-ttu-id="813d4-124">避免寫入一則模糊的訊息，例如「從 i/o 子系統接收的驅動程式封包無效。</span><span class="sxs-lookup"><span data-stu-id="813d4-124">Avoid writing a cryptic message such as "A driver packet received from the I/O subsystem was invalid.</span></span> <span data-ttu-id="813d4-125">資料為封包。」更好的訊息會指出有問題的驅動程式正常運作，但會記錄格式不正確的封包。</span><span class="sxs-lookup"><span data-stu-id="813d4-125">The data is the packet."A better message would indicate that the driver in question is functioning properly, but is logging incorrectly formatted packets.</span></span> <span data-ttu-id="813d4-126">您可以繼續說，需要有 Unicode 版本的驅動程式才能更正問題。</span><span class="sxs-lookup"><span data-stu-id="813d4-126">It could go on to say that a Unicode version of the driver is needed to correct the problem.</span></span> <span data-ttu-id="813d4-127">如需有關撰寫良好錯誤訊息的詳細資訊，請參閱 [錯誤訊息指導方針](/windows/desktop/Debug/error-message-guidelines)。</span><span class="sxs-lookup"><span data-stu-id="813d4-127">For more information about writing good error messages, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

<span data-ttu-id="813d4-128">請勿在郵件內文中使用 tab 或逗點，因為事件記錄檔可以儲存為逗號或 tab 分隔的文字檔。</span><span class="sxs-lookup"><span data-stu-id="813d4-128">Do not use tabs or commas in the message text, because event logs can be saved as comma or tab-separated text files.</span></span> <span data-ttu-id="813d4-129">許多組織會將這些檔案匯入資料庫中，而額外的格式化字元需要手動操作。</span><span class="sxs-lookup"><span data-stu-id="813d4-129">Many organizations import these files into databases, and the extra formatting characters will require manual manipulation.</span></span>

<span data-ttu-id="813d4-130">使用 UNC 名稱或其他包含空格的連結時，請將名稱括在角括弧中。</span><span class="sxs-lookup"><span data-stu-id="813d4-130">When using UNC names, or other links that contain spaces, enclose the name in angle brackets.</span></span> <span data-ttu-id="813d4-131">例如，<\\ \\ *共用* \\ *名 servername*>。</span><span class="sxs-lookup"><span data-stu-id="813d4-131">For example, <\\\\*sharename*\\*servername*>.</span></span> <span data-ttu-id="813d4-132">您可以將 URL 寫入至訊息結尾，以將使用者指向相關的說明內容。</span><span class="sxs-lookup"><span data-stu-id="813d4-132">You can write a URL to the end of the message that points the user to related help material.</span></span> <span data-ttu-id="813d4-133">URL 必須是完整的 DNS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="813d4-133">The URL must be a fully qualified DNS host name.</span></span> <span data-ttu-id="813d4-134">例如，您可以將下列文字附加至訊息：「如需有關此訊息的詳細資訊，請造訪我們的支援網站」 https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp 。</span><span class="sxs-lookup"><span data-stu-id="813d4-134">For example, you could append the following text to your messages: "For additional information on this message, please visit our support site at https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp."</span></span> <span data-ttu-id="813d4-135">連結會導致 ASP 頁面將使用者重新導向至與錯誤訊息相關的內容。</span><span class="sxs-lookup"><span data-stu-id="813d4-135">The link would lead to an ASP page that redirects the user to content relating to the error message.</span></span> <span data-ttu-id="813d4-136">它會剖析 (在) URL 時傳遞的額外參數，以判斷要將使用者重新導向至何處。</span><span class="sxs-lookup"><span data-stu-id="813d4-136">It would parse additional parameters (passed when the URL is clicked) to determine where to redirect the user.</span></span>

<span data-ttu-id="813d4-137">傳遞至 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) 函數的引數會附加至 URL，如下所示：</span><span class="sxs-lookup"><span data-stu-id="813d4-137">The arguments passed to the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function are appended to the URL as follows:</span></span>

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

<span data-ttu-id="813d4-138">如果事件來源的郵件 DLL 標頭中的公司名稱、產品名稱、產品版本、檔案名和檔案版本是有效的，則它們也會附加至 URL：</span><span class="sxs-lookup"><span data-stu-id="813d4-138">If the company name, product name, product version, file name, and file version from the message DLL header for the event source are valid, they are also appended to the URL:</span></span>

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a><span data-ttu-id="813d4-139">減少額外負荷</span><span class="sxs-lookup"><span data-stu-id="813d4-139">Reducing Overhead</span></span>

<span data-ttu-id="813d4-140">事件記錄會耗用磁碟空間和處理器時間等資源。</span><span class="sxs-lookup"><span data-stu-id="813d4-140">Event logging consumes resources such as disk space and processor time.</span></span> <span data-ttu-id="813d4-141">事件記錄檔所需的磁碟空間量，以及記錄事件的應用程式所產生的額外負荷，取決於您選擇要記錄多少資訊。</span><span class="sxs-lookup"><span data-stu-id="813d4-141">The amount of disk space that an event log requires and the overhead for an application that logs events depend on how much information you choose to log.</span></span> <span data-ttu-id="813d4-142">這就是為什麼只記錄基本資訊很重要的原因。</span><span class="sxs-lookup"><span data-stu-id="813d4-142">This is why it is important to log only essential information.</span></span> <span data-ttu-id="813d4-143">也可以將事件記錄呼叫放入程式碼中的錯誤路徑，而不是在主要程式碼路徑中，這樣會降低效能。</span><span class="sxs-lookup"><span data-stu-id="813d4-143">It is also good to place event logging calls in an error path in the code rather than in the main code path, which would reduce performance.</span></span>

<span data-ttu-id="813d4-144">每個事件記錄檔記錄所需的磁碟空間量包括 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="813d4-144">The amount of disk space required for each event log record includes the members of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span> <span data-ttu-id="813d4-145">這是可變長度的結構;字串和二進位資料會儲存在結構後面。</span><span class="sxs-lookup"><span data-stu-id="813d4-145">This is a variable length structure; strings and binary data are stored following the structure.</span></span>

 

 
