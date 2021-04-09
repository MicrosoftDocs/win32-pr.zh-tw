---
title: NCSA 記錄
description: NCSA 擴充記錄是一種可在 URL 群組上啟用的伺服器端記錄類型。
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04db62d5d561fb227f7a46a33c2aefcacd943b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675503"
---
# <a name="ncsa-logging"></a><span data-ttu-id="840c2-103">NCSA 記錄</span><span class="sxs-lookup"><span data-stu-id="840c2-103">NCSA Logging</span></span>

<span data-ttu-id="840c2-104">NCSA 擴充記錄是一種可在 URL 群組上啟用的伺服器端記錄類型。</span><span class="sxs-lookup"><span data-stu-id="840c2-104">NCSA extended logging is one type of server side logging that can be enabled on a URL group.</span></span> <span data-ttu-id="840c2-105">NCSA 一般記錄檔格式是固定的 ASCII 文字格式，無法自訂。</span><span class="sxs-lookup"><span data-stu-id="840c2-105">The NCSA Common log file format is a fixed ASCII text-based format that cannot be customized.</span></span> <span data-ttu-id="840c2-106">NCSA 記錄檔包含 HTTP 伺服器 API 核心模式快取點擊。</span><span class="sxs-lookup"><span data-stu-id="840c2-106">The NCSA log file contains the HTTP Server API kernel-mode cache hits.</span></span> <span data-ttu-id="840c2-107">這種類型的記錄只能在 URL 群組上啟用;它無法用於伺服器會話。</span><span class="sxs-lookup"><span data-stu-id="840c2-107">This type of logging can be enabled on a URL group only; it cannot be used on the server session.</span></span>

<span data-ttu-id="840c2-108">NCSA 一般記錄檔格式會記錄下列資料。</span><span class="sxs-lookup"><span data-stu-id="840c2-108">The NCSA Common log file format records the following data.</span></span> <span data-ttu-id="840c2-109">資料表中的資料會依照記錄檔中的出現順序。</span><span class="sxs-lookup"><span data-stu-id="840c2-109">The data in the table is in the order of occurrence in the log file.</span></span>



| <span data-ttu-id="840c2-110">欄位</span><span class="sxs-lookup"><span data-stu-id="840c2-110">Field</span></span>                                            | <span data-ttu-id="840c2-111">描述</span><span class="sxs-lookup"><span data-stu-id="840c2-111">Description</span></span>                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="840c2-112">遠端主機位址</span><span class="sxs-lookup"><span data-stu-id="840c2-112">Remote host address</span></span>                              | <span data-ttu-id="840c2-113">發出要求之用戶端的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="840c2-113">The IP address of the client that made the request.</span></span>                                                                                                                               |
| <span data-ttu-id="840c2-114">遠端記錄檔名稱</span><span class="sxs-lookup"><span data-stu-id="840c2-114">Remote log name</span></span>                                  | <span data-ttu-id="840c2-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="840c2-115">Not used.</span></span> <span data-ttu-id="840c2-116">此值一律為連字號。</span><span class="sxs-lookup"><span data-stu-id="840c2-116">This value is always a hyphen.</span></span>                                                                                                                                          |
| <span data-ttu-id="840c2-117">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="840c2-117">User name</span></span>                                        | <span data-ttu-id="840c2-118">存取伺服器之已驗證使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="840c2-118">The name of the authenticated user that accessed the server.</span></span> <span data-ttu-id="840c2-119">匿名使用者會以連字號表示。</span><span class="sxs-lookup"><span data-stu-id="840c2-119">Anonymous users are indicated by a hyphen.</span></span> <span data-ttu-id="840c2-120">最佳做法是讓應用程式一律提供使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="840c2-120">The best practice is for the application always to provide the user name.</span></span> |
| <span data-ttu-id="840c2-121">日期、時間和格林尼治平均時間 (GMT) 位移</span><span class="sxs-lookup"><span data-stu-id="840c2-121">Date, time, and Greenwich mean time (GMT) offset</span></span> | <span data-ttu-id="840c2-122">活動發生的本地日期和時間。</span><span class="sxs-lookup"><span data-stu-id="840c2-122">The local date and time at which the activity occurred.</span></span> <span data-ttu-id="840c2-123">另外也指出格林尼治平均時間的位移。</span><span class="sxs-lookup"><span data-stu-id="840c2-123">The offset from Greenwich mean time is also indicated.</span></span>                                                                    |
| <span data-ttu-id="840c2-124">要求和通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="840c2-124">Request and Protocol version</span></span>                     | <span data-ttu-id="840c2-125">用戶端使用的 HTTP 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="840c2-125">The HTTP protocol version that the client used.</span></span>                                                                                                                                   |
| <span data-ttu-id="840c2-126">服務狀態碼</span><span class="sxs-lookup"><span data-stu-id="840c2-126">Service status code</span></span>                              | <span data-ttu-id="840c2-127">HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="840c2-127">The HTTP status code.</span></span> <span data-ttu-id="840c2-128"> (值200表示要求已順利完成。 ) </span><span class="sxs-lookup"><span data-stu-id="840c2-128">(A value of 200 indicates that the request completed successfully.)</span></span>                                                                                         |
| <span data-ttu-id="840c2-129">傳送的位元組數</span><span class="sxs-lookup"><span data-stu-id="840c2-129">Bytes sent</span></span>                                       | <span data-ttu-id="840c2-130">伺服器所傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="840c2-130">The number of bytes sent by the server.</span></span>                                                                                                                                           |



 

<span data-ttu-id="840c2-131">並非所有欄位都包含資訊。</span><span class="sxs-lookup"><span data-stu-id="840c2-131">Not all fields will contain information.</span></span> <span data-ttu-id="840c2-132">針對沒有資訊的欄位， ( ) 的連字號會顯示為預留位置。</span><span class="sxs-lookup"><span data-stu-id="840c2-132">For fields for which there is no information, a hyphen (-) appears as a placeholder.</span></span> <span data-ttu-id="840c2-133">如果欄位包含非列印字元，HTTP 伺服器 API 會將它取代為加號 (+) ，以保留記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="840c2-133">If a field contains a nonprintable character, the HTTP Server API replaces it with a plus sign (+) to preserve the log file format.</span></span> <span data-ttu-id="840c2-134">這通常發生在病毒攻擊的情況下，例如，惡意使用者傳送換行字元和換行字元（如果不是以加號 (+) 取代），就會破壞記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="840c2-134">This typically occurs with virus attacks, when, for example, a malicious user sends carriage returns and line feeds that, if not replaced with the plus sign (+), would break the log file format.</span></span> <span data-ttu-id="840c2-135">欄位會以空格分隔，而時間會記錄為當地時間與 GMT 位移。</span><span class="sxs-lookup"><span data-stu-id="840c2-135">Fields are separated by spaces, and the time is recorded as local time with the GMT offset.</span></span>

<span data-ttu-id="840c2-136">下列範例顯示在文字編輯器中看到的 NCSA 一般記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="840c2-136">The following example shows an NCSA Common log file entry, as viewed in a text editor.</span></span>

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

<span data-ttu-id="840c2-137">用戶端的 IP 位址是172.21.13.45，而使用者名稱是 Microsoft \\ JohnDoe。</span><span class="sxs-lookup"><span data-stu-id="840c2-137">The IP address of the client is 172.21.13.45, and the user name is Microsoft\\JohnDoe.</span></span> <span data-ttu-id="840c2-138">記錄檔記錄于2005年4月7日，17:39:04 在年4月7日，格林威治時差為8小時。</span><span class="sxs-lookup"><span data-stu-id="840c2-138">The log was recorded on April 7, 2005 at 17:39:04 local time with a Greenwich offset of 8 hours.</span></span> <span data-ttu-id="840c2-139">要求動詞和通訊協定版本為 "GET/scripts/iisadmin/ism.dll？ HTTP/serv HTTP/1.0"。</span><span class="sxs-lookup"><span data-stu-id="840c2-139">The request verb and protocol version were "GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0".</span></span> <span data-ttu-id="840c2-140">狀態碼是 200 OK，而用戶端傳送的位元組數目是3401。</span><span class="sxs-lookup"><span data-stu-id="840c2-140">The status codes was 200 OK, and the number of bytes sent by the client was 3401.</span></span>

 

 




