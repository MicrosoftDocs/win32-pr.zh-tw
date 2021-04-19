---
title: IIS 記錄
description: IIS 記錄是一種可在 URL 群組上啟用的伺服器端記錄類型。
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966816"
---
# <a name="iis-logging"></a><span data-ttu-id="45cce-103">IIS 記錄</span><span class="sxs-lookup"><span data-stu-id="45cce-103">IIS Logging</span></span>

<span data-ttu-id="45cce-104">IIS 記錄是一種可在 URL 群組上啟用的伺服器端記錄類型。</span><span class="sxs-lookup"><span data-stu-id="45cce-104">IIS logging is one type of server side logging that can be enabled on a URL group.</span></span> <span data-ttu-id="45cce-105">IIS 記錄檔格式是固定的 ASCII 文字格式，無法自訂。</span><span class="sxs-lookup"><span data-stu-id="45cce-105">The IIS log file format is a fixed ASCII text-based format that cannot be customized.</span></span> <span data-ttu-id="45cce-106">IIS 記錄檔包含 HTTP 伺服器 API 核心模式快取點擊。</span><span class="sxs-lookup"><span data-stu-id="45cce-106">The IIS log file contains the HTTP Server API kernel-mode cache hits.</span></span> <span data-ttu-id="45cce-107">這種類型的記錄只能在 URL 群組上啟用;它無法用於伺服器會話。</span><span class="sxs-lookup"><span data-stu-id="45cce-107">This type of logging can be enabled on a URL group only; it cannot be used on the server session.</span></span>

<span data-ttu-id="45cce-108">IIS 記錄檔格式會記錄下列資料。</span><span class="sxs-lookup"><span data-stu-id="45cce-108">The IIS log file format records the following data.</span></span> <span data-ttu-id="45cce-109">資料表中的資料會依照記錄檔中的出現順序。</span><span class="sxs-lookup"><span data-stu-id="45cce-109">The data in the table is in the order of occurrence in the log file.</span></span>



| <span data-ttu-id="45cce-110">欄位</span><span class="sxs-lookup"><span data-stu-id="45cce-110">Field</span></span>                | <span data-ttu-id="45cce-111">描述</span><span class="sxs-lookup"><span data-stu-id="45cce-111">Description</span></span>                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cce-112">用戶端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="45cce-112">Client IP address</span></span>    | <span data-ttu-id="45cce-113">發出要求之用戶端的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45cce-113">The IP address of the client that made the request.</span></span>                                                                                                                               |
| <span data-ttu-id="45cce-114">使用者名稱</span><span class="sxs-lookup"><span data-stu-id="45cce-114">User name</span></span>            | <span data-ttu-id="45cce-115">存取伺服器之已驗證使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="45cce-115">The name of the authenticated user that accessed the server.</span></span> <span data-ttu-id="45cce-116">匿名使用者會以連字號表示。</span><span class="sxs-lookup"><span data-stu-id="45cce-116">Anonymous users are indicated by a hyphen.</span></span> <span data-ttu-id="45cce-117">最佳做法是讓應用程式一律提供使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="45cce-117">The best practice is for the application always to provide the user name.</span></span> |
| <span data-ttu-id="45cce-118">Date</span><span class="sxs-lookup"><span data-stu-id="45cce-118">Date</span></span>                 | <span data-ttu-id="45cce-119">活動發生的日期。</span><span class="sxs-lookup"><span data-stu-id="45cce-119">The date on which the activity occurred.</span></span>                                                                                                                                          |
| <span data-ttu-id="45cce-120">Time</span><span class="sxs-lookup"><span data-stu-id="45cce-120">Time</span></span>                 | <span data-ttu-id="45cce-121">活動發生的當地時間。</span><span class="sxs-lookup"><span data-stu-id="45cce-121">The local time at which the activity occurred.</span></span>                                                                                                                                    |
| <span data-ttu-id="45cce-122">服務和實例</span><span class="sxs-lookup"><span data-stu-id="45cce-122">Service and instance</span></span> | <span data-ttu-id="45cce-123">用戶端上執行的網際網路服務名稱和實例編號。</span><span class="sxs-lookup"><span data-stu-id="45cce-123">The Internet service name and instance number that was running on the client.</span></span>                                                                                                     |
| <span data-ttu-id="45cce-124">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="45cce-124">Server name</span></span>          | <span data-ttu-id="45cce-125">產生記錄檔專案的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="45cce-125">The name of the server on which the log file entry was generated.</span></span>                                                                                                                 |
| <span data-ttu-id="45cce-126">伺服器 IP 位址</span><span class="sxs-lookup"><span data-stu-id="45cce-126">Server IP address</span></span>    | <span data-ttu-id="45cce-127">產生記錄檔專案之伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="45cce-127">The IP address of the server on which the log file entry was generated.</span></span>                                                                                                           |
| <span data-ttu-id="45cce-128">花費的時間</span><span class="sxs-lookup"><span data-stu-id="45cce-128">Time taken</span></span>           | <span data-ttu-id="45cce-129">動作所花費的時間長度 (毫秒)。</span><span class="sxs-lookup"><span data-stu-id="45cce-129">The length of time that the action took, in milliseconds.</span></span>                                                                                                                         |
| <span data-ttu-id="45cce-130">傳送的用戶端位元組</span><span class="sxs-lookup"><span data-stu-id="45cce-130">Client bytes sent</span></span>    | <span data-ttu-id="45cce-131">用戶端傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="45cce-131">The number of bytes sent by the client.</span></span>                                                                                                                                           |
| <span data-ttu-id="45cce-132">已傳送的伺服器位元組</span><span class="sxs-lookup"><span data-stu-id="45cce-132">Server bytes sent</span></span>    | <span data-ttu-id="45cce-133">伺服器所傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="45cce-133">The number of bytes sent by the server.</span></span>                                                                                                                                           |
| <span data-ttu-id="45cce-134">服務狀態碼</span><span class="sxs-lookup"><span data-stu-id="45cce-134">Service status code</span></span>  | <span data-ttu-id="45cce-135">值為200表示要求已成功完成。</span><span class="sxs-lookup"><span data-stu-id="45cce-135">A value of 200 indicates that the request was fulfilled successfully.</span></span>                                                                                                             |
| <span data-ttu-id="45cce-136">Windows 狀態碼</span><span class="sxs-lookup"><span data-stu-id="45cce-136">Windows status code</span></span>  | <span data-ttu-id="45cce-137">值為 0 (零) 表示要求已成功完成。</span><span class="sxs-lookup"><span data-stu-id="45cce-137">A value of 0 (zero) indicates that the request was fulfilled successfully.</span></span>                                                                                                        |
| <span data-ttu-id="45cce-138">要求類型</span><span class="sxs-lookup"><span data-stu-id="45cce-138">Request type</span></span>         | <span data-ttu-id="45cce-139">要求動詞。</span><span class="sxs-lookup"><span data-stu-id="45cce-139">The request verb.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="45cce-140">作業的目標</span><span class="sxs-lookup"><span data-stu-id="45cce-140">Target of operation</span></span>  | <span data-ttu-id="45cce-141">動詞的目標，例如 Default.htm。</span><span class="sxs-lookup"><span data-stu-id="45cce-141">The target of the verb, for example, Default.htm.</span></span>                                                                                                                                 |
| <span data-ttu-id="45cce-142">參數</span><span class="sxs-lookup"><span data-stu-id="45cce-142">Parameters</span></span>           | <span data-ttu-id="45cce-143">傳遞至腳本的參數。</span><span class="sxs-lookup"><span data-stu-id="45cce-143">The parameters that are passed to a scrip.</span></span>                                                                                                                                        |



 

<span data-ttu-id="45cce-144">並非所有欄位都包含資訊。</span><span class="sxs-lookup"><span data-stu-id="45cce-144">Not all fields will contain information.</span></span> <span data-ttu-id="45cce-145">針對沒有資訊的欄位， ( ) 的連字號會顯示為預留位置。</span><span class="sxs-lookup"><span data-stu-id="45cce-145">For fields for which there is no information, a hyphen (-) appears as a placeholder.</span></span> <span data-ttu-id="45cce-146">如果欄位包含非列印字元，HTTP 伺服器 API 會將它取代為加號 (+) ，以保留記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="45cce-146">If a field contains a nonprintable character, the HTTP Server API replaces it with a plus sign (+) to preserve the log file format.</span></span> <span data-ttu-id="45cce-147">這通常發生在病毒攻擊的情況下，例如，惡意使用者傳送換行字元和換行字元（如果不是以加號 (+) 取代），就會破壞記錄檔格式。</span><span class="sxs-lookup"><span data-stu-id="45cce-147">This typically occurs with virus attacks, when, for example, a malicious user sends carriage returns and line feeds that, if not replaced with the plus sign (+), would break the log file format.</span></span> <span data-ttu-id="45cce-148">欄位會以逗號分隔，使格式比其他 ASCII 格式更容易閱讀，而這些格式會使用空格做為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="45cce-148">Fields are separated by commas, making the format easier to read than the other ASCII formats, which use spaces for separators.</span></span> <span data-ttu-id="45cce-149">時間會記錄為當地時間。</span><span class="sxs-lookup"><span data-stu-id="45cce-149">The time is recorded as local time.</span></span> <span data-ttu-id="45cce-150">花費的時間是以毫秒為單位來記錄。</span><span class="sxs-lookup"><span data-stu-id="45cce-150">The time taken is recorded in milliseconds.</span></span> <span data-ttu-id="45cce-151">如需 [花費時間] 欄位的詳細資訊，請參閱 [W3C 記錄](w3c-logging.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="45cce-151">For more information about the time taken field, see the [W3C Logging](w3c-logging.md) topic.</span></span>

<span data-ttu-id="45cce-152">下列範例顯示 NCSA 一般記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="45cce-152">The following example shows an NCSA Common log file entry.</span></span>

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




