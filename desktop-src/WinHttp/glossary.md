---
description: 詞彙頁面
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 08951f9f-d03d-4720-8f18-1413ba72e93d
title: " (WinHTTP) 的詞彙"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74d707c828a9eeb5f07ebf3ec3c1ca92a9d2b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850112"
---
# <a name="glossary-winhttp"></a><span data-ttu-id="5dcce-103"> (WinHTTP) 的詞彙</span><span class="sxs-lookup"><span data-stu-id="5dcce-103">Glossary (WinHTTP)</span></span>

<dl> <dt>

<span data-ttu-id="5dcce-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**驗證資料**</span><span class="sxs-lookup"><span data-stu-id="5dcce-104"><span id="term_authentication_data"></span><span id="TERM_AUTHENTICATION_DATA"></span>**authentication data**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-105">在驗證期間，在伺服器與用戶端之間交換的配置特定資料區塊。</span><span class="sxs-lookup"><span data-stu-id="5dcce-105">Scheme-specific block of data that is exchanged between the server and client during authentication.</span></span> <span data-ttu-id="5dcce-106">為了證明其身分識別，用戶端會使用使用者名稱和密碼來加密部分或全部資料。</span><span class="sxs-lookup"><span data-stu-id="5dcce-106">To prove its identity, the client encrypts some or all of this data with a user name and password.</span></span> <span data-ttu-id="5dcce-107">用戶端會將加密的資料傳送至伺服器，該伺服器會將資料解密，並將資料與原始資料進行比較。</span><span class="sxs-lookup"><span data-stu-id="5dcce-107">The client sends the encrypted data to the server, which decrypts the data and compares it to the original.</span></span> <span data-ttu-id="5dcce-108">如果解密的資料與原始資料相符，用戶端就會經過驗證。</span><span class="sxs-lookup"><span data-stu-id="5dcce-108">If the decrypted data matches the original data, the client is authenticated.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 編碼**</span><span class="sxs-lookup"><span data-stu-id="5dcce-109"><span id="term_base64_encoding"></span><span id="TERM_BASE64_ENCODING"></span>**base64 encoding**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-110">用來傳輸二進位資料的配置。</span><span class="sxs-lookup"><span data-stu-id="5dcce-110">Scheme used to transmit binary data.</span></span> <span data-ttu-id="5dcce-111">Base64 以24位群組的形式處理資料，將此資料對應到四個編碼的字元。</span><span class="sxs-lookup"><span data-stu-id="5dcce-111">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="5dcce-112">有時也稱為「3對4編碼」。</span><span class="sxs-lookup"><span data-stu-id="5dcce-112">It is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="5dcce-113">24位群組的每6位都是用來做為對應表的索引， (base64 字母) 來取得編碼資料的字元。</span><span class="sxs-lookup"><span data-stu-id="5dcce-113">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="5dcce-114">編碼的資料行長度限制為76個字元。</span><span class="sxs-lookup"><span data-stu-id="5dcce-114">The encoded data has line lengths limited to 76 characters.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**憑證存放區**</span><span class="sxs-lookup"><span data-stu-id="5dcce-115"><span id="term_certificate_store"></span><span id="TERM_CERTIFICATE_STORE"></span>**certificate store**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-116">通常會儲存憑證、憑證撤銷清單 (CRL) 的永久儲存體，以及儲存 (CTL) 的憑證信任清單。</span><span class="sxs-lookup"><span data-stu-id="5dcce-116">Typically, permanent storage where certificates, certificate revocation lists (CRL), and certificate trust lists (CTL) are stored.</span></span> <span data-ttu-id="5dcce-117">使用會話型憑證時，憑證存放區也可以是暫時性的。</span><span class="sxs-lookup"><span data-stu-id="5dcce-117">A certificate store can also be temporary when working with session-based certificates.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span><span class="sxs-lookup"><span data-stu-id="5dcce-118"><span id="term_cobranding"></span><span id="TERM_COBRANDING"></span>**cobranding**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-119">Microsoft Passport 的參與者網站在 Passport network service 頁面上提供自己商標元素和說明的能力。</span><span class="sxs-lookup"><span data-stu-id="5dcce-119">Ability for a Microsoft Passport participant site to provide its own branding elements and explanations on the Passport network service pages.</span></span> <span data-ttu-id="5dcce-120">Cobranding 包括自訂 Passport network 頁面上的外觀與操作、特定文字和特定行為。</span><span class="sxs-lookup"><span data-stu-id="5dcce-120">Cobranding includes customizing the look and feel, specific text, and specific behavior on Passport network pages.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**字碼頁**</span><span class="sxs-lookup"><span data-stu-id="5dcce-121"><span id="term_code_page"></span><span id="TERM_CODE_PAGE"></span>**code page**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-122">將程式所使用的二進位字元碼與鍵盤上的按鍵或監視器上的字元外觀相關聯的資料表。</span><span class="sxs-lookup"><span data-stu-id="5dcce-122">Table that relates the binary character codes used by a program to keys on the keyboard or to the appearance of characters on the monitor.</span></span> <span data-ttu-id="5dcce-123">使用字碼頁可提供不同國家/地區所使用之字元集和鍵盤配置的支援。</span><span class="sxs-lookup"><span data-stu-id="5dcce-123">Using code pages is a way to provide support for character sets and keyboard layouts used in different countries and regions.</span></span> <span data-ttu-id="5dcce-124">您可以設定裝置（例如監視器和鍵盤）來使用特定的字碼頁，並從一個字碼頁 (（例如美國) ）切換至另一個 (，例如使用者要求的葡萄牙) 。</span><span class="sxs-lookup"><span data-stu-id="5dcce-124">You can configure devices such as the monitor and the keyboard to use a specific code page and to switch from one code page (such as United States) to another (such as Portugal) at the user's request.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP 指令動詞**</span><span class="sxs-lookup"><span data-stu-id="5dcce-125"><span id="term_http_verb"></span><span id="TERM_HTTP_VERB"></span>**HTTP verb**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-126">HTTP 動詞命令 (或 HTTP 方法) 是在要求訊息中傳送的指令，會通知 HTTP 伺服器所指定資源上執行的動作。</span><span class="sxs-lookup"><span data-stu-id="5dcce-126">The HTTP verb (or HTTP method) is an instruction sent in a request message that notifies an HTTP server of the action to perform on the specified resource.</span></span> <span data-ttu-id="5dcce-127">例如，"GET" 會指定從伺服器抓取資源。</span><span class="sxs-lookup"><span data-stu-id="5dcce-127">For example, "GET" specifies that a resource is being retrieved from the server.</span></span> <span data-ttu-id="5dcce-128">常見的動詞包括 "GET"、"POST" 和 "HEAD"。</span><span class="sxs-lookup"><span data-stu-id="5dcce-128">Common verbs include "GET", "POST", and "HEAD".</span></span> <span data-ttu-id="5dcce-129">如需詳細資訊和標準 HTTP 動詞命令的完整清單，請參閱 HTTP/1.1 規格。</span><span class="sxs-lookup"><span data-stu-id="5dcce-129">For more information and a complete list of standard HTTP verbs, see the HTTP/1.1 specification.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**票**</span><span class="sxs-lookup"><span data-stu-id="5dcce-130"><span id="term_ticket"></span><span id="TERM_TICKET"></span>**ticket**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-131">包含 Passport 驗證使用者設定檔的 Cookie。</span><span class="sxs-lookup"><span data-stu-id="5dcce-131">Cookie that contains a user profile for Passport authentication.</span></span> <span data-ttu-id="5dcce-132">每個票證都對應至一個 URL。</span><span class="sxs-lookup"><span data-stu-id="5dcce-132">Each ticket corresponds to one URL.</span></span> <span data-ttu-id="5dcce-133">Passport 網域授權單位的登入伺服器會提供用戶端傳送給 Passport 成員進行驗證的票證。</span><span class="sxs-lookup"><span data-stu-id="5dcce-133">The logon server of a Passport Domain Authority provides tickets that the client sends to a Passport member for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="5dcce-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**使用者代理程式**</span><span class="sxs-lookup"><span data-stu-id="5dcce-134"><span id="term_user_agent"></span><span id="TERM_USER_AGENT"></span>**user agent**</span></span>
</dt> <dd>

<span data-ttu-id="5dcce-135">使用者代理程式是從 HTTP 伺服器要求檔的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="5dcce-135">The user agent is the client application that requests a document from an HTTP server.</span></span> <span data-ttu-id="5dcce-136">當用戶端將要求傳送至 HTTP 伺服器時，通常會傳送具有要求標頭的使用者代理程式名稱，讓伺服器能夠判斷用戶端軟體的功能。</span><span class="sxs-lookup"><span data-stu-id="5dcce-136">When the client sends a request to an HTTP server, typically it sends the name of the user agent with the request header so that the server can determine the capabilities of the client software.</span></span>

</dd> </dl>

 

 



