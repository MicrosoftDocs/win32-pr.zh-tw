---
title: 剖析例外狀況
description: HTTP 伺服器 API 提供登錄機碼，以支援將例外狀況剖析為 HTTP/1.1 規格，以提供回溯相容性。
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- 剖析例外狀況
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932322"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="a4ad6-104">剖析例外狀況</span><span class="sxs-lookup"><span data-stu-id="a4ad6-104">Parsing Exceptions</span></span>

<span data-ttu-id="a4ad6-105">HTTP 伺服器 API 提供登錄機碼，以支援將例外狀況剖析為 HTTP/1.1 規格，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="a4ad6-106">這些例外狀況預設不會啟用，而且當伺服器遇到與 HTTP 用戶端的相容性問題時，應該只會以個別案例為基礎啟用。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="a4ad6-107">這些值會在下列登錄位置建立：</span><span class="sxs-lookup"><span data-stu-id="a4ad6-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="a4ad6-108">下表列出提供的登錄機碼，可支援所列的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="a4ad6-109">若要啟用例外狀況，請將對應的金鑰值設定為1，然後重新開機 HTTP 服務。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="a4ad6-110">索引鍵名稱</span><span class="sxs-lookup"><span data-stu-id="a4ad6-110">Key name</span></span>                              | <span data-ttu-id="a4ad6-111">Description</span><span class="sxs-lookup"><span data-stu-id="a4ad6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ad6-112">AllowWeakHeaderNameSyntax (DWORD) </span><span class="sxs-lookup"><span data-stu-id="a4ad6-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="a4ad6-113">允許 HTTP 剖析器接受具有分隔符號的標頭名稱，例如 '？ '。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a4ad6-114">AllowWeakHeaderValueSyntax (DWORD) </span><span class="sxs-lookup"><span data-stu-id="a4ad6-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="a4ad6-115">允許 HTTP 剖析器接受含有原始 (非重) 控制字元的標頭值。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a4ad6-116">AllowCaseInsensitiveVerbs (DWORD) </span><span class="sxs-lookup"><span data-stu-id="a4ad6-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="a4ad6-117">允許 HTTP 剖析器接受小寫 HTTP 方法/動詞，例如 "get"。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="a4ad6-118">AllowUnEscapedRestrictedChars (DWORD) </span><span class="sxs-lookup"><span data-stu-id="a4ad6-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="a4ad6-119">允許 HTTP 剖析器接受 abspath 中的控制字元，以及 URL 的查詢字串。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="a4ad6-120">如果是絕對 URL，主機名稱中將不允許控制字元。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="a4ad6-121">所有類別的 Url （即 UTF8、DBCS 和 ANSI）都會允許控制字元。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="a4ad6-122">所有 ASCII 控制字元（NUL (0x00) 、LF (0x0a) 、CR (0x0d) 和水準索引標籤 (0x09) 都將被允許。</span><span class="sxs-lookup"><span data-stu-id="a4ad6-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




