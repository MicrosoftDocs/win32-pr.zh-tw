---
title: '用戶端記錄 (Windows Media Format 11 SDK) '
description: 用戶端記錄
ms.assetid: 3e0d0fea-4370-41f8-b461-73a37de8d8bc
keywords:
- Windows Media Format SDK，用戶端記錄
- Windows Media Format SDK，記錄
- Advanced Systems Format (ASF) 、用戶端記錄
- ASF (Advanced Systems Format) ，用戶端記錄
- Advanced Systems Format (ASF) ，記錄
- ASF (Advanced Systems Format) ，記錄
- 用戶端記錄
- 記錄用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856f2df4c2377b94edc40574c3e2efcced34aa81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093580"
---
# <a name="client-logging-windows-media-format-11-sdk"></a><span data-ttu-id="7a193-111">用戶端記錄 (Windows Media Format 11 SDK) </span><span class="sxs-lookup"><span data-stu-id="7a193-111">Client Logging (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="7a193-112">當讀取器物件從伺服器讀取資料時，它會將記錄資訊傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="7a193-112">When the reader object reads data from a server, it sends logging information to the server.</span></span> <span data-ttu-id="7a193-113">內容提供者通常會使用這項資訊來測量服務品質、產生帳單資訊或追蹤廣告。</span><span class="sxs-lookup"><span data-stu-id="7a193-113">Content providers typically use this information to measure quality of service, generate billing information, or track advertising.</span></span> <span data-ttu-id="7a193-114">記錄資訊不包含任何個人資料。</span><span class="sxs-lookup"><span data-stu-id="7a193-114">The logging information contains no personal data.</span></span>

<span data-ttu-id="7a193-115">應用程式可以在讀取器物件上呼叫 [**IWMReaderAdvanced：： SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) 方法，以指定所記錄的部分資訊。</span><span class="sxs-lookup"><span data-stu-id="7a193-115">The application can specify some of the information that is logged, by calling the [**IWMReaderAdvanced::SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo) method on the reader object.</span></span> <span data-ttu-id="7a193-116">例如，您可以指定使用者代理字串、播放機應用程式的名稱，或裝載播放程式的網頁。</span><span class="sxs-lookup"><span data-stu-id="7a193-116">For example, you can specify the user-agent string, the name of the player application, or the Web page that hosts the player.</span></span>

<span data-ttu-id="7a193-117">記錄資訊包含可識別會話的 GUID。</span><span class="sxs-lookup"><span data-stu-id="7a193-117">The logging information includes a GUID that identifies the session.</span></span> <span data-ttu-id="7a193-118">根據預設，讀取器會產生匿名會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a193-118">By default, the reader generates an anonymous session ID.</span></span> <span data-ttu-id="7a193-119">或者，讀取器可以改為傳送可唯一識別目前使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7a193-119">Optionally, the reader can instead send an ID that uniquely identifies the current user.</span></span> <span data-ttu-id="7a193-120">若要啟用這項功能，請使用值 **TRUE** 來呼叫 [**IWMReaderAdvanced2：： SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)方法。</span><span class="sxs-lookup"><span data-stu-id="7a193-120">To enable this feature, call the [**IWMReaderAdvanced2::SetLogClientID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid) method with the value **TRUE**.</span></span>

<span data-ttu-id="7a193-121">您可以設定 reader 物件，將記錄資訊傳送到另一部伺服器，以及源伺服器。</span><span class="sxs-lookup"><span data-stu-id="7a193-121">You can configure the reader object to send the logging information to another server, in addition to the originating server.</span></span> <span data-ttu-id="7a193-122">若要這樣做，請使用伺服器的 URL 來呼叫 [**IWMReaderNetworkConfig：： AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) 方法。</span><span class="sxs-lookup"><span data-stu-id="7a193-122">To do so, call the [**IWMReaderNetworkConfig::AddLoggingUrl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-addloggingurl) method with the URL of the server.</span></span> <span data-ttu-id="7a193-123">此 URL 應指向可處理 HTTP GET 和 POST 要求的腳本或可執行檔。</span><span class="sxs-lookup"><span data-stu-id="7a193-123">This URL should point to a script or executable that can handle HTTP GET and POST requests.</span></span> <span data-ttu-id="7a193-124">您可以使用多播和記錄通告代理程式 (wmsiislog.dll) ，也可以撰寫自訂 ASP 或 CGI 腳本來接收記錄資料。</span><span class="sxs-lookup"><span data-stu-id="7a193-124">You can use the Multicast and Logging Advertisement Agent (wmsiislog.dll), or you can write a custom ASP or CGI script to receive the log data.</span></span>

> [!Note]  
> <span data-ttu-id="7a193-125">您可以建立具有 **logURL** 屬性的伺服器端播放清單，以取得相同的功能。</span><span class="sxs-lookup"><span data-stu-id="7a193-125">You can get the same functionality by creating a server-side playlist with a **logURL** attribute.</span></span>

 

<span data-ttu-id="7a193-126">當讀取器物件傳送記錄時，它會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="7a193-126">When the reader object sends the log, it does the following:</span></span>

1.  <span data-ttu-id="7a193-127">將空的 GET 要求傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="7a193-127">Sends an empty GET request to the server.</span></span>
2.  <span data-ttu-id="7a193-128">剖析下列其中一個字串的伺服器回應：</span><span class="sxs-lookup"><span data-stu-id="7a193-128">Parses the server response for one of the following strings:</span></span>
    -   `<body><h1>NetShow ISAPI Log Dll</h1>`
    -   <span data-ttu-id="7a193-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` 其中 "0.0.0.0" 是任何有效的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="7a193-129">`<body><h1>WMS ISAPI Log Dll/0.0.0.0</h1>` where "0.0.0.0" is any valid version number.</span></span>
3.  <span data-ttu-id="7a193-130">傳送包含記錄資訊的 POST 要求。</span><span class="sxs-lookup"><span data-stu-id="7a193-130">Sends a POST request with the log information.</span></span>

<span data-ttu-id="7a193-131">下列程式碼顯示的範例 ASP 腳本會接收記錄資訊，並將其寫入檔案：</span><span class="sxs-lookup"><span data-stu-id="7a193-131">The following code shows an example ASP script that receives the logging information and writes it to a file:</span></span>


```
<html>
<body>
<h1>WMS ISAPI Log Dll/9.00.00.00.00</h1>
<%@ Language=VBScript %>
<%
  Dim temp, i, post, file, fso

  ' Convert the binary data to a string.
  For i = 1 To Request.TotalBytes
    temp = Request.BinaryRead(1)
    pose = pose & Chr(AscB(temp))
  Next

  Set fso = createobject("Scripting.FileSystemObject")
  Set file = fso.OpenTextFile("C:\log.txt", 8, TRUE)

  file.writeline Now
  file.writeline post
  file.writeBlankLines 2 
%>
</body>
</html>
```



<span data-ttu-id="7a193-132">您可以指定多部伺服器來接收記錄資訊;只要對每個 URL 呼叫 **AddLoggingUrl** 一次即可。</span><span class="sxs-lookup"><span data-stu-id="7a193-132">You can specify multiple servers to receive logging information; just call **AddLoggingUrl** once with each URL.</span></span> <span data-ttu-id="7a193-133">若要清除接收記錄的伺服器清單，請呼叫 [**IWMReaderNetworkConfig：： ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) 方法。</span><span class="sxs-lookup"><span data-stu-id="7a193-133">To clear the list of servers that receive logs, call the [**IWMReaderNetworkConfig::ResetLoggingUrlList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-resetloggingurllist) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a193-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a193-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a193-135">**執行網路功能**</span><span class="sxs-lookup"><span data-stu-id="7a193-135">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> <dt>

[<span data-ttu-id="7a193-136">**IWMReaderAdvanced 介面**</span><span class="sxs-lookup"><span data-stu-id="7a193-136">**IWMReaderAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)
</dt> <dt>

[<span data-ttu-id="7a193-137">**IWMReaderAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="7a193-137">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




