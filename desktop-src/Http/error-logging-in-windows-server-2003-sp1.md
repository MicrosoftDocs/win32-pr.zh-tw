---
title: Windows Server 2003 SP1 中的錯誤記錄
description: Windows Server 2003 SP1 中的錯誤記錄
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- Windows Server 2003 Service Pack 1 (SP1) 中的錯誤記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b82c816dab39877f700973de3c0c7798034d124
ms.sourcegitcommit: 7bdca1558c21be976be950a213c5a072c449f111
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/14/2019
ms.locfileid: "103679092"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a><span data-ttu-id="2a845-104">Windows Server 2003 SP1 中的錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="2a845-104">Error Logging in Windows Server 2003 SP1</span></span>

## <a name="addition-of-w3c-style-headers"></a><span data-ttu-id="2a845-105">加入 W3C 樣式標頭</span><span class="sxs-lookup"><span data-stu-id="2a845-105">Addition of W3C Style Headers</span></span>

<span data-ttu-id="2a845-106">從 Windows Server 2003 Service Pack 1 (SP1) 開始，HTTP 伺服器 API 錯誤記錄檔包含的 W3C 樣式標頭，可讓您使用標準記錄剖析器剖析記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a845-106">Starting with Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API error log includes W3C style headers allowing log files to be parsed using standard log parsers.</span></span> <span data-ttu-id="2a845-107">下方顯示的範本會列出可記錄在 HTTP 錯誤記錄檔中的所有欄位。</span><span class="sxs-lookup"><span data-stu-id="2a845-107">The template shown below lists all the fields that can be logged in the http error log file.</span></span>

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a><span data-ttu-id="2a845-108">記錄其他欄位</span><span class="sxs-lookup"><span data-stu-id="2a845-108">Logging Additional Fields</span></span>

<span data-ttu-id="2a845-109">HTTP 錯誤記錄檔已擴充為包含九個以上的欄位，可記錄有關發生之失敗的資料。</span><span class="sxs-lookup"><span data-stu-id="2a845-109">The HTTP error log has been extended to include nine more fields to log data about failures that occur.</span></span> <span data-ttu-id="2a845-110">新的錯誤欄位如下所示：</span><span class="sxs-lookup"><span data-stu-id="2a845-110">The new error fields are listed below:</span></span>

-   <span data-ttu-id="2a845-111">伺服器電腦名稱稱 \[ S-COMPUTERNAME\]</span><span class="sxs-lookup"><span data-stu-id="2a845-111">Server Computer Name \[S-COMPUTERNAME\]</span></span>
-   <span data-ttu-id="2a845-112">使用者代理程式 \[ CS (使用者 \_ 代理程式) \]</span><span class="sxs-lookup"><span data-stu-id="2a845-112">User Agent \[CS(USER\_AGENT)\]</span></span>
-   <span data-ttu-id="2a845-113">Cookie \[ CS (cookie) \]</span><span class="sxs-lookup"><span data-stu-id="2a845-113">Cookie \[CS(COOKIE)\]</span></span>
-   <span data-ttu-id="2a845-114">訪客 (訪客) 的推薦者 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a845-114">referrer \[CS(referrer)\]</span></span>
-   <span data-ttu-id="2a845-115">主機名稱 \[ CS-主機\]</span><span class="sxs-lookup"><span data-stu-id="2a845-115">Host Name \[CS-HOST\]</span></span>
-   <span data-ttu-id="2a845-116">伺服器 SC 所接收的位元組 \[ -位元組\]</span><span class="sxs-lookup"><span data-stu-id="2a845-116">Bytes received by the server \[SC-BYTES\]</span></span>
-   <span data-ttu-id="2a845-117">伺服器 CS 接收和處理的位元組 \[ -位元組\]</span><span class="sxs-lookup"><span data-stu-id="2a845-117">Bytes received and processed by the server \[CS-BYTES\]</span></span>
-   <span data-ttu-id="2a845-118">處理要求時間所花費的時間 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a845-118">Time Taken to process the request \[TIME-TAKEN\]</span></span>
-   <span data-ttu-id="2a845-119">Queue-Name (保留給 IIS) \[ S-QUEUENAME\]</span><span class="sxs-lookup"><span data-stu-id="2a845-119">Queue-Name (Reserved for IIS) \[S-QUEUENAME\]</span></span>

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a><span data-ttu-id="2a845-120">選取 Fileds 以登入 HTTP 錯誤記錄檔</span><span class="sxs-lookup"><span data-stu-id="2a845-120">Selecting Fileds to Log in the HTTP Error Log File</span></span>

<span data-ttu-id="2a845-121">已新增 **ErrorLoggingFields** 登錄機碼，以控制登入 HTTP 錯誤記錄檔中的欄位。</span><span class="sxs-lookup"><span data-stu-id="2a845-121">The **ErrorLoggingFields** registry key has been added to control the fields logged into the HTTP error log.</span></span> <span data-ttu-id="2a845-122">此登錄值位於下列位置的 HTTP \\ 參數機碼：</span><span class="sxs-lookup"><span data-stu-id="2a845-122">This registry values is located under an HTTP\\Parameters key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

<span data-ttu-id="2a845-123">**ErrorLoggingFields** 登錄值是 DWORD 值，其中包含每個可記錄欄位的位值。</span><span class="sxs-lookup"><span data-stu-id="2a845-123">The **ErrorLoggingFields** registry value is a DWORD value that contains bit values for each of the fields that can be logged.</span></span> <span data-ttu-id="2a845-124">若要啟用特定欄位的記錄功能，請將其對應的位值設定為1，然後重新開機 HTTP 服務。</span><span class="sxs-lookup"><span data-stu-id="2a845-124">To enable logging of a specific field, set its corresponding bit value to 1 and restart the HTTP service.</span></span> <span data-ttu-id="2a845-125">若要停用記錄，請將位值設定為0。</span><span class="sxs-lookup"><span data-stu-id="2a845-125">To disable logging, set the bit value to 0.</span></span> <span data-ttu-id="2a845-126">若要設定多個欄位，請使用個別值的位 OR。</span><span class="sxs-lookup"><span data-stu-id="2a845-126">To configure multiple fields, use a bitwise OR of the individual values.</span></span> <span data-ttu-id="2a845-127">例如，若要開啟 Cookie 和查閱者記錄欄位，此值應為 0x00020000 \| 0x00040000 = 0x00060000。</span><span class="sxs-lookup"><span data-stu-id="2a845-127">For example, to turn on the Cookie and Referrer logging fields, the value should be 0x00020000 \| 0x00040000 = 0x00060000.</span></span> <span data-ttu-id="2a845-128">如果 **ErrorLoggingFields** 登錄機碼不存在，則會記錄預設欄位。</span><span class="sxs-lookup"><span data-stu-id="2a845-128">If the **ErrorLoggingFields** registry key is absent, the default fields are logged.</span></span> <span data-ttu-id="2a845-129">要記錄預設欄位的 **ErrorLoggingFields** 值是0x7c884c7。</span><span class="sxs-lookup"><span data-stu-id="2a845-129">The **ErrorLoggingFields** value to log the default fields is 0x7c884c7.</span></span> <span data-ttu-id="2a845-130">若要針對下表所顯示的所有欄位啟用記錄，請將值設定為0x7dff4e7。</span><span class="sxs-lookup"><span data-stu-id="2a845-130">To enable logging for all the fields shown in the table below, set the value to 0x7dff4e7.</span></span>

<span data-ttu-id="2a845-131">錯誤記錄欄位會列在下表中：</span><span class="sxs-lookup"><span data-stu-id="2a845-131">The error logging fields are listed in the following table:</span></span>



| <span data-ttu-id="2a845-132">記錄欄位</span><span class="sxs-lookup"><span data-stu-id="2a845-132">Log field</span></span>            | <span data-ttu-id="2a845-133">預設記錄</span><span class="sxs-lookup"><span data-stu-id="2a845-133">Logged by default</span></span> | <span data-ttu-id="2a845-134">位元值</span><span class="sxs-lookup"><span data-stu-id="2a845-134">Bit value</span></span>  |
|----------------------|-------------------|------------|
| <span data-ttu-id="2a845-135">Date</span><span class="sxs-lookup"><span data-stu-id="2a845-135">Date</span></span>                 | <span data-ttu-id="2a845-136">是</span><span class="sxs-lookup"><span data-stu-id="2a845-136">Yes</span></span>               | <span data-ttu-id="2a845-137">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2a845-137">0x00000001</span></span> |
| <span data-ttu-id="2a845-138">Time</span><span class="sxs-lookup"><span data-stu-id="2a845-138">Time</span></span>                 | <span data-ttu-id="2a845-139">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-139">Yes</span></span>               | <span data-ttu-id="2a845-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2a845-140">0x00000002</span></span> |
| <span data-ttu-id="2a845-141">伺服器電腦名稱稱</span><span class="sxs-lookup"><span data-stu-id="2a845-141">Server Computer Name</span></span> | <span data-ttu-id="2a845-142">No</span><span class="sxs-lookup"><span data-stu-id="2a845-142">No</span></span>                | <span data-ttu-id="2a845-143">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2a845-143">0x00000020</span></span> |
| <span data-ttu-id="2a845-144">用戶端 IP 位址</span><span class="sxs-lookup"><span data-stu-id="2a845-144">Client IP Address</span></span>    | <span data-ttu-id="2a845-145">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-145">Yes</span></span>               | <span data-ttu-id="2a845-146">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2a845-146">0x00000004</span></span> |
| <span data-ttu-id="2a845-147">用戶端埠</span><span class="sxs-lookup"><span data-stu-id="2a845-147">Client Port</span></span>          | <span data-ttu-id="2a845-148">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-148">Yes</span></span>               | <span data-ttu-id="2a845-149">0x00400000</span><span class="sxs-lookup"><span data-stu-id="2a845-149">0x00400000</span></span> |
| <span data-ttu-id="2a845-150">伺服器 IP 位址</span><span class="sxs-lookup"><span data-stu-id="2a845-150">Server IP Address</span></span>    | <span data-ttu-id="2a845-151">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-151">Yes</span></span>               | <span data-ttu-id="2a845-152">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2a845-152">0x00000040</span></span> |
| <span data-ttu-id="2a845-153">伺服器通訊埠</span><span class="sxs-lookup"><span data-stu-id="2a845-153">Server Port</span></span>          | <span data-ttu-id="2a845-154">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-154">Yes</span></span>               | <span data-ttu-id="2a845-155">0x00008000</span><span class="sxs-lookup"><span data-stu-id="2a845-155">0x00008000</span></span> |
| <span data-ttu-id="2a845-156">通訊協定版本</span><span class="sxs-lookup"><span data-stu-id="2a845-156">Protocol Version</span></span>     | <span data-ttu-id="2a845-157">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-157">Yes</span></span>               | <span data-ttu-id="2a845-158">0x00080000</span><span class="sxs-lookup"><span data-stu-id="2a845-158">0x00080000</span></span> |
| <span data-ttu-id="2a845-159">方法</span><span class="sxs-lookup"><span data-stu-id="2a845-159">Method</span></span>               | <span data-ttu-id="2a845-160">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-160">Yes</span></span>               | <span data-ttu-id="2a845-161">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2a845-161">0x00000080</span></span> |
| <span data-ttu-id="2a845-162">URI</span><span class="sxs-lookup"><span data-stu-id="2a845-162">URI</span></span>                  | <span data-ttu-id="2a845-163">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-163">Yes</span></span>               | <span data-ttu-id="2a845-164">0x00800000</span><span class="sxs-lookup"><span data-stu-id="2a845-164">0x00800000</span></span> |
| <span data-ttu-id="2a845-165">使用者代理程式</span><span class="sxs-lookup"><span data-stu-id="2a845-165">User Agent</span></span>           | <span data-ttu-id="2a845-166">No</span><span class="sxs-lookup"><span data-stu-id="2a845-166">No</span></span>                | <span data-ttu-id="2a845-167">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2a845-167">0x00010000</span></span> |
| <span data-ttu-id="2a845-168">Cookie</span><span class="sxs-lookup"><span data-stu-id="2a845-168">Cookie</span></span>               | <span data-ttu-id="2a845-169">No</span><span class="sxs-lookup"><span data-stu-id="2a845-169">No</span></span>                | <span data-ttu-id="2a845-170">0x00020000</span><span class="sxs-lookup"><span data-stu-id="2a845-170">0x00020000</span></span> |
| <span data-ttu-id="2a845-171">引薦</span><span class="sxs-lookup"><span data-stu-id="2a845-171">referrer</span></span>             | <span data-ttu-id="2a845-172">No</span><span class="sxs-lookup"><span data-stu-id="2a845-172">No</span></span>                | <span data-ttu-id="2a845-173">0x00040000</span><span class="sxs-lookup"><span data-stu-id="2a845-173">0x00040000</span></span> |
| <span data-ttu-id="2a845-174">主機</span><span class="sxs-lookup"><span data-stu-id="2a845-174">Host</span></span>                 | <span data-ttu-id="2a845-175">No</span><span class="sxs-lookup"><span data-stu-id="2a845-175">No</span></span>                | <span data-ttu-id="2a845-176">0x00100000</span><span class="sxs-lookup"><span data-stu-id="2a845-176">0x00100000</span></span> |
| <span data-ttu-id="2a845-177">通訊協定狀態</span><span class="sxs-lookup"><span data-stu-id="2a845-177">Protocol Status</span></span>      | <span data-ttu-id="2a845-178">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-178">Yes</span></span>               | <span data-ttu-id="2a845-179">0x00000400</span><span class="sxs-lookup"><span data-stu-id="2a845-179">0x00000400</span></span> |
| <span data-ttu-id="2a845-180">SC-Bytes</span><span class="sxs-lookup"><span data-stu-id="2a845-180">SC-Bytes</span></span>             | <span data-ttu-id="2a845-181">No</span><span class="sxs-lookup"><span data-stu-id="2a845-181">No</span></span>                | <span data-ttu-id="2a845-182">0x00001000</span><span class="sxs-lookup"><span data-stu-id="2a845-182">0x00001000</span></span> |
| <span data-ttu-id="2a845-183">CS-Bytes</span><span class="sxs-lookup"><span data-stu-id="2a845-183">CS-Bytes</span></span>             | <span data-ttu-id="2a845-184">No</span><span class="sxs-lookup"><span data-stu-id="2a845-184">No</span></span>                | <span data-ttu-id="2a845-185">0x00002000</span><span class="sxs-lookup"><span data-stu-id="2a845-185">0x00002000</span></span> |
| <span data-ttu-id="2a845-186">花費的時間</span><span class="sxs-lookup"><span data-stu-id="2a845-186">Time Taken</span></span>           | <span data-ttu-id="2a845-187">No</span><span class="sxs-lookup"><span data-stu-id="2a845-187">No</span></span>                | <span data-ttu-id="2a845-188">0x00004000</span><span class="sxs-lookup"><span data-stu-id="2a845-188">0x00004000</span></span> |
| <span data-ttu-id="2a845-189">SiteId</span><span class="sxs-lookup"><span data-stu-id="2a845-189">SiteId</span></span>               | <span data-ttu-id="2a845-190">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-190">Yes</span></span>               | <span data-ttu-id="2a845-191">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2a845-191">0x01000000</span></span> |
| <span data-ttu-id="2a845-192">原因片語</span><span class="sxs-lookup"><span data-stu-id="2a845-192">Reason Phrase</span></span>        | <span data-ttu-id="2a845-193">Yes</span><span class="sxs-lookup"><span data-stu-id="2a845-193">Yes</span></span>               | <span data-ttu-id="2a845-194">0x02000000</span><span class="sxs-lookup"><span data-stu-id="2a845-194">0x02000000</span></span> |
| <span data-ttu-id="2a845-195">佇列名稱</span><span class="sxs-lookup"><span data-stu-id="2a845-195">Queue Name</span></span>           | <span data-ttu-id="2a845-196">No</span><span class="sxs-lookup"><span data-stu-id="2a845-196">No</span></span>                | <span data-ttu-id="2a845-197">0x04000000</span><span class="sxs-lookup"><span data-stu-id="2a845-197">0x04000000</span></span> |
| <span data-ttu-id="2a845-198">串流識別碼</span><span class="sxs-lookup"><span data-stu-id="2a845-198">Stream Id</span></span>            | <span data-ttu-id="2a845-199">No</span><span class="sxs-lookup"><span data-stu-id="2a845-199">No</span></span>                | <span data-ttu-id="2a845-200">0x????????</span><span class="sxs-lookup"><span data-stu-id="2a845-200">0x????????</span></span> |



 

## <a name="time-and-date-rollover"></a><span data-ttu-id="2a845-201">日期和時間變換</span><span class="sxs-lookup"><span data-stu-id="2a845-201">Time and Date Rollover</span></span>

<span data-ttu-id="2a845-202">根據預設，當目前的記錄檔達到指定的大小時，會建立新的 HTTP 錯誤記錄檔 (稱為檔案變換) 。</span><span class="sxs-lookup"><span data-stu-id="2a845-202">By default, a new HTTP error log file is created (termed file rollover) when the current log file reaches a specified size.</span></span> <span data-ttu-id="2a845-203">從 Windows Server 2003 （含 SP1）開始，可以根據日期和時間建立新的錯誤記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a845-203">Starting with Windows Server 2003 with SP1, new error log files can be created based on date and time.</span></span> <span data-ttu-id="2a845-204">時間和日期變換是由兩個新的登錄值所控制： **ErrorLoggingRolloverType** 和 **ErrorLoggingLocaltimeRollover**。</span><span class="sxs-lookup"><span data-stu-id="2a845-204">Time and date rollover are controlled by two new registry values: **ErrorLoggingRolloverType** and **ErrorLoggingLocaltimeRollover**.</span></span> <span data-ttu-id="2a845-205">若要啟用時間和日期變換，必須將這些登錄值新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="2a845-205">To enable time and date rollover, these registry values must be added to the registry.</span></span> <span data-ttu-id="2a845-206">當這些金鑰新增至登錄時，必須重新開機 Http 服務。</span><span class="sxs-lookup"><span data-stu-id="2a845-206">The Http service must be restarted when these keys are added to the registry.</span></span> <span data-ttu-id="2a845-207">記錄檔變換登錄機碼會在下列機碼底下建立：</span><span class="sxs-lookup"><span data-stu-id="2a845-207">The log file rollover registry keys are created under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

<span data-ttu-id="2a845-208">**ErrorLoggingRolloverType** 登錄機碼會指出所需的變換類型，而且預設會設定為以大小為基礎的變換。</span><span class="sxs-lookup"><span data-stu-id="2a845-208">The **ErrorLoggingRolloverType** registry key indicates the type of rollover desired and is by default set to size based rollover.</span></span> <span data-ttu-id="2a845-209">變換也可以設定為每日、每週、每月或每小時進行。</span><span class="sxs-lookup"><span data-stu-id="2a845-209">Rollover can also be set to occur on a daily, weekly, monthly, or hourly basis.</span></span> <span data-ttu-id="2a845-210">當檔案變換以時間為基礎時， **ErrorLoggingLocaltimeRollover** 值為0表示變換時間以 GMT 表示，而值為1則表示變換時間以當地時程表示。</span><span class="sxs-lookup"><span data-stu-id="2a845-210">When file rollover is based on time, an **ErrorLoggingLocaltimeRollover** value of 0 indicates that the rollover time is expressed in GMT, and a value of 1 indicates that the rollover time is expressed in local time.</span></span> <span data-ttu-id="2a845-211">**ErrorLoggingRolloverType** 索引鍵可採用從0到4的值，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="2a845-211">The **ErrorLoggingRolloverType** key can take a value from 0 to 4 as listed in the following table.</span></span>



| <span data-ttu-id="2a845-212">變換類型值</span><span class="sxs-lookup"><span data-stu-id="2a845-212">Rollover type value</span></span> | <span data-ttu-id="2a845-213">描述</span><span class="sxs-lookup"><span data-stu-id="2a845-213">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a845-214">0</span><span class="sxs-lookup"><span data-stu-id="2a845-214">0</span></span>                   | <span data-ttu-id="2a845-215">以大小為基礎的變換。</span><span class="sxs-lookup"><span data-stu-id="2a845-215">Size based rollover.</span></span> <span data-ttu-id="2a845-216">當檔案到達 **ErrorLogFileTruncateSize** 登錄機碼中定義的大小時，就會變換記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a845-216">Log files are rolled over when the file reaches the size defined in the **ErrorLogFileTruncateSize** registry key.</span></span> |
| <span data-ttu-id="2a845-217">1</span><span class="sxs-lookup"><span data-stu-id="2a845-217">1</span></span>                   | <span data-ttu-id="2a845-218">記錄檔變換每日發生一次。</span><span class="sxs-lookup"><span data-stu-id="2a845-218">Log file rollover occurs daily.</span></span>                                                                                                         |
| <span data-ttu-id="2a845-219">2</span><span class="sxs-lookup"><span data-stu-id="2a845-219">2</span></span>                   | <span data-ttu-id="2a845-220">記錄檔變換每週進行一次。</span><span class="sxs-lookup"><span data-stu-id="2a845-220">Log file rollover occurs weekly.</span></span>                                                                                                        |
| <span data-ttu-id="2a845-221">3</span><span class="sxs-lookup"><span data-stu-id="2a845-221">3</span></span>                   | <span data-ttu-id="2a845-222">每月都會進行記錄檔變換。</span><span class="sxs-lookup"><span data-stu-id="2a845-222">Log file rollover occurs monthly.</span></span>                                                                                                       |
| <span data-ttu-id="2a845-223">4</span><span class="sxs-lookup"><span data-stu-id="2a845-223">4</span></span>                   | <span data-ttu-id="2a845-224">記錄檔變換每小時進行一次。</span><span class="sxs-lookup"><span data-stu-id="2a845-224">Log file rollover occurs hourly.</span></span>                                                                                                        |



 

<span data-ttu-id="2a845-225">儲存錯誤記錄檔之檔案的命名慣例，與大小、日期和以時間為基礎的變換不同。</span><span class="sxs-lookup"><span data-stu-id="2a845-225">The naming conventions for files that store the error logs are different for size, date, and time based rollover.</span></span> <span data-ttu-id="2a845-226">下表列出 Http 記錄檔的命名慣例。</span><span class="sxs-lookup"><span data-stu-id="2a845-226">The following table lists the naming conventions for Http log files.</span></span>



| <span data-ttu-id="2a845-227">Tollover 類型</span><span class="sxs-lookup"><span data-stu-id="2a845-227">Tollover type</span></span> | <span data-ttu-id="2a845-228">記錄檔名稱</span><span class="sxs-lookup"><span data-stu-id="2a845-228">Log file name</span></span>  | <span data-ttu-id="2a845-229">Description</span><span class="sxs-lookup"><span data-stu-id="2a845-229">Description</span></span>                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a845-230">大小</span><span class="sxs-lookup"><span data-stu-id="2a845-230">Size</span></span>          | <span data-ttu-id="2a845-231">HTTPERRn .LOG</span><span class="sxs-lookup"><span data-stu-id="2a845-231">HTTPERRn.LOG</span></span>   | <span data-ttu-id="2a845-232">當記錄檔到達特定大小時，就會回收記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a845-232">The log file is recycled when it reaches a specific size.</span></span> <span data-ttu-id="2a845-233">n 是檔案編號，而且會在記錄檔變換時遞增。</span><span class="sxs-lookup"><span data-stu-id="2a845-233">n is the file number and is incremented when the log file is rolled over.</span></span> |
| <span data-ttu-id="2a845-234">每日</span><span class="sxs-lookup"><span data-stu-id="2a845-234">Daily</span></span>         | <span data-ttu-id="2a845-235">htYYMMDD .log</span><span class="sxs-lookup"><span data-stu-id="2a845-235">htYYMMDD.log</span></span>   | <span data-ttu-id="2a845-236">記錄檔每天都會回收。</span><span class="sxs-lookup"><span data-stu-id="2a845-236">The log file is recycled daily.</span></span>                                                                                                     |
| <span data-ttu-id="2a845-237">每週</span><span class="sxs-lookup"><span data-stu-id="2a845-237">Weekly</span></span>        | <span data-ttu-id="2a845-238">htYYMMww .log</span><span class="sxs-lookup"><span data-stu-id="2a845-238">htYYMMww.log</span></span>   | <span data-ttu-id="2a845-239">每週都會回收記錄檔，其中 ww 是當月的第幾周。</span><span class="sxs-lookup"><span data-stu-id="2a845-239">The log file is recycled weekly, where ww is the week of the month.</span></span>                                                                 |
| <span data-ttu-id="2a845-240">每月</span><span class="sxs-lookup"><span data-stu-id="2a845-240">Monthly</span></span>       | <span data-ttu-id="2a845-241">htYYMM .log</span><span class="sxs-lookup"><span data-stu-id="2a845-241">htYYMM.log</span></span>     | <span data-ttu-id="2a845-242">每個月都會回收記錄檔。</span><span class="sxs-lookup"><span data-stu-id="2a845-242">The log file is recycled every month.</span></span>                                                                                               |
| <span data-ttu-id="2a845-243">每小時</span><span class="sxs-lookup"><span data-stu-id="2a845-243">Hourly</span></span>        | <span data-ttu-id="2a845-244">htYYMMDDhh .log</span><span class="sxs-lookup"><span data-stu-id="2a845-244">htYYMMDDhh.log</span></span> | <span data-ttu-id="2a845-245">記錄檔會每小時回收一次，其中 hh 是以0-24 小時標記法表示的一天中的小時。</span><span class="sxs-lookup"><span data-stu-id="2a845-245">The log file is recycled hourly, where hh is the hour of the day expressed in 0-24 hour notation.</span></span>                                   |



 

 

 




