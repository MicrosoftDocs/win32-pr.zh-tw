---
description: WinHTTP 記錄可以用來協助針對 WSDAPI 應用程式進行疑難排解。 當中繼資料交換失敗或 SSL/TLS 協商失敗時，這會很有説明。
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: 正在捕獲 WinHTTP 記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115028"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="b56e2-104">正在捕獲 WinHTTP 記錄檔</span><span class="sxs-lookup"><span data-stu-id="b56e2-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="b56e2-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) 記錄可以用來協助針對 WSDAPI 應用程式進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="b56e2-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="b56e2-106">當中繼資料交換失敗或 SSL/TLS 協商失敗時，這會很有説明。</span><span class="sxs-lookup"><span data-stu-id="b56e2-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="b56e2-107">此程式說明如何在用戶端電腦上捕獲 WinHTTP 記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b56e2-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="b56e2-108">啟用記錄時，不能執行以 WSDAPI 為基礎的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b56e2-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="b56e2-109">如果用戶端應用程式在啟用記錄功能時執行，則必須先重新開機用戶端和/或電腦，才能 WS-Discovery 和中繼資料交換流量將會出現在 WinHTTP 記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="b56e2-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="b56e2-110">**若要捕獲 WinHTTP 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="b56e2-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="b56e2-111">在用戶端電腦上開啟提高許可權的命令提示字元視窗。</span><span class="sxs-lookup"><span data-stu-id="b56e2-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="b56e2-112">執行下列命令： **netsh winHTTP set 追蹤 trace-file-prefix = "C： \\ Temp \\ dpws" level = verbose format = ansi state = enabled max-trace-file-size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="b56e2-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="b56e2-113">此命令會啟用 WinHTTP 記錄。</span><span class="sxs-lookup"><span data-stu-id="b56e2-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="b56e2-114">所有記錄檔都會儲存在 C： \\ Temp 目錄中，而且檔案名會以 dpws 前置詞開頭。</span><span class="sxs-lookup"><span data-stu-id="b56e2-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="b56e2-115">最多會儲存 1 GB 的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b56e2-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="b56e2-116">如果在用戶端上使用 WinHTTP 的進程已在執行中，請重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="b56e2-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="b56e2-117">例如，如果使用的是 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) api，則必須重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="b56e2-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="b56e2-118">函式探索 Api 會從服務主機內部呼叫 WinHTTP，在啟用追蹤時可能已經啟動。</span><span class="sxs-lookup"><span data-stu-id="b56e2-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="b56e2-119">啟動以 WSDAPI 為基礎的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b56e2-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="b56e2-120">您可以使用正在進行調試的應用程式或 WSD Debug 用戶端。</span><span class="sxs-lookup"><span data-stu-id="b56e2-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="b56e2-121">重現應用程式失敗。</span><span class="sxs-lookup"><span data-stu-id="b56e2-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="b56e2-122">終止以 WSDAPI 為基礎的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b56e2-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="b56e2-123">如果使用 WinHTTP 的進程未與用戶端應用程式一起終止，請重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="b56e2-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="b56e2-124">例如，如果使用的是 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) api，則必須重新開機電腦。</span><span class="sxs-lookup"><span data-stu-id="b56e2-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="b56e2-125">執行下列命令： **netsh winHTTP set 追蹤 state = disabled**</span><span class="sxs-lookup"><span data-stu-id="b56e2-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="b56e2-126">此命令會停用 WinHTTP 記錄。</span><span class="sxs-lookup"><span data-stu-id="b56e2-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="b56e2-127">檢查 C： Temp 中的 DPWS 記錄 \\ ，並確認已傳送所需的要求和訊息。</span><span class="sxs-lookup"><span data-stu-id="b56e2-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="b56e2-128">如果正在使用安全通道 (HTTPS) 通訊，請檢查 SSL/TLS 是否失敗。</span><span class="sxs-lookup"><span data-stu-id="b56e2-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="b56e2-129">一旦捕捉到 WinHTTP 記錄檔，就可以檢查記錄以尋找 WSDAPI 應用程式失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="b56e2-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="b56e2-130">請注意，用來查看這些記錄的文字編輯器必須以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="b56e2-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="b56e2-131">如需詳細資訊，請參閱 [使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="b56e2-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b56e2-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="b56e2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56e2-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b56e2-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="b56e2-134">使用 WinHTTP 記錄來確認取得流量</span><span class="sxs-lookup"><span data-stu-id="b56e2-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
