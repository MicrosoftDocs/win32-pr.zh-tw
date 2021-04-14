---
title: 設定 HTTP 伺服器 API 錯誤記錄
description: HTTP 伺服器 API 錯誤記錄是由 HTTP 參數索引鍵下的三個登錄值所控制 \\ 。
ms.assetid: a7712159-939e-42e3-a8d8-73148c2f4f6e
keywords:
- HTTP 伺服器 API，設定錯誤記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f6b5ae81b1933ea745789e0fae33dfc7ebce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372164"
---
# <a name="configuring-http-server-api-error-logging"></a><span data-ttu-id="559ba-104">設定 HTTP 伺服器 API 錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="559ba-104">Configuring HTTP Server API Error Logging</span></span>

<span data-ttu-id="559ba-105">Http 伺服器 API 錯誤記錄是由位於以下位置的 **HTTP** \\ **參數** 機碼底下的三個登錄值所控制：</span><span class="sxs-lookup"><span data-stu-id="559ba-105">The HTTP Server API error logging is controlled by three registry values under an **HTTP**\\**Parameters** key located at:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

> [!Note]  
> <span data-ttu-id="559ba-106">在未來的 Windows 作業系統版本中，設定值的位置和格式可能會變更。</span><span class="sxs-lookup"><span data-stu-id="559ba-106">The location and form of the configuration values may change in future versions of the Windows operating system.</span></span>

 

<span data-ttu-id="559ba-107">使用者必須擁有系統管理員/本機系統許可權，才能修改登錄值，以及查看或修改記錄檔和包含它們的資料夾。</span><span class="sxs-lookup"><span data-stu-id="559ba-107">A user must have Administrator/Local System privileges to modify the registry values, and view or modify the log files and the folder that contains them.</span></span>

<span data-ttu-id="559ba-108">啟動 HTTP 伺服器 API 驅動程式時，會讀取登錄值中的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="559ba-108">Configuration information in the registry values is read when the HTTP Server API driver is started.</span></span> <span data-ttu-id="559ba-109">如此一來，如果設定已變更，則必須停止並重新啟動驅動程式，才能讀取新的值。</span><span class="sxs-lookup"><span data-stu-id="559ba-109">As a result, if the settings are changed the driver must be stopped and restarted to read the new values.</span></span> <span data-ttu-id="559ba-110">您可以使用下列主控台命令來完成這項作業：</span><span class="sxs-lookup"><span data-stu-id="559ba-110">This can be accomplished by using the following console commands:</span></span>

<span data-ttu-id="559ba-111">**net stop HTTP**</span><span class="sxs-lookup"><span data-stu-id="559ba-111">**net stop http**</span></span>

<span data-ttu-id="559ba-112">**net start HTTP**</span><span class="sxs-lookup"><span data-stu-id="559ba-112">**net start http**</span></span>

<span data-ttu-id="559ba-113">記錄檔會使用下列慣例來命名：</span><span class="sxs-lookup"><span data-stu-id="559ba-113">The log files are named by using the following convention:</span></span>

<span data-ttu-id="559ba-114">**HTTPerr +** *SequenceNumber* **+ .log**</span><span class="sxs-lookup"><span data-stu-id="559ba-114">**httperr +** *SequenceNumber* **+ .log**</span></span>

<span data-ttu-id="559ba-115">例如： "HTTPerr4"。</span><span class="sxs-lookup"><span data-stu-id="559ba-115">For example: "httperr4.log".</span></span>

<span data-ttu-id="559ba-116">當記錄檔達到 **ErrorLogFileTruncateSize** 登錄值所指定的大小上限時，就會迴圈記錄檔，而且此值不能小於 1 mb 的 (MB) 。</span><span class="sxs-lookup"><span data-stu-id="559ba-116">Log files are cycled when they reach the maximum size specified by the **ErrorLogFileTruncateSize** registry value, and the value cannot be less than one megabyte (MB).</span></span>

<span data-ttu-id="559ba-117">如果錯誤記錄的設定無效，或寫入記錄檔時發生任何種類的失敗，則 HTTP 伺服器 API 會使用事件記錄來通知系統管理員未進行錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="559ba-117">If the configuration of error logging is invalid or any kind of failure occurs while writing to the log files, the HTTP Server API uses event logging to notify administrators that error logging did not take place.</span></span>

<span data-ttu-id="559ba-118">下表說明登錄設定值。</span><span class="sxs-lookup"><span data-stu-id="559ba-118">Registry configuration values are described in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="559ba-119">登錄值</span><span class="sxs-lookup"><span data-stu-id="559ba-119">Registry Value</span></span></th>
<th><span data-ttu-id="559ba-120">Description</span><span class="sxs-lookup"><span data-stu-id="559ba-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="559ba-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span><span class="sxs-lookup"><span data-stu-id="559ba-121"><span id="EnableErrorLogging"></span><span id="enableerrorlogging"></span><span id="ENABLEERRORLOGGING"></span>EnableErrorLogging</span></span><br/></td>
<td><span data-ttu-id="559ba-122">可以設定為<strong>TRUE</strong>以啟用錯誤記錄的<strong>DWORD</strong> ，或設定為<strong>FALSE</strong>以停用它。</span><span class="sxs-lookup"><span data-stu-id="559ba-122">A <strong>DWORD</strong> that can be set to <strong>TRUE</strong> to enable error logging, or <strong>FALSE</strong> to disable it.</span></span> <span data-ttu-id="559ba-123">預設值為 <strong>TRUE</strong>。</span><span class="sxs-lookup"><span data-stu-id="559ba-123">The default value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="559ba-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span><span class="sxs-lookup"><span data-stu-id="559ba-124"><span id="ErrorLogFileTruncateSize"></span><span id="errorlogfiletruncatesize"></span><span id="ERRORLOGFILETRUNCATESIZE"></span>ErrorLogFileTruncateSize</span></span><br/></td>
<td><span data-ttu-id="559ba-125"><strong>DWORD</strong> ，指定錯誤記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="559ba-125">A <strong>DWORD</strong> that specifies the maximum size of an error log file, in bytes.</span></span> <span data-ttu-id="559ba-126">預設值是 (0x100000) 的一 MB。</span><span class="sxs-lookup"><span data-stu-id="559ba-126">The default value is one MB (0x100000).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="559ba-127">指定的值不能小於預設值。</span><span class="sxs-lookup"><span data-stu-id="559ba-127">The specified value cannot be smaller than the default value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="559ba-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span><span class="sxs-lookup"><span data-stu-id="559ba-128"><span id="ErrorLoggingDir"></span><span id="errorloggingdir"></span><span id="ERRORLOGGINGDIR"></span>ErrorLoggingDir</span></span><br/></td>
<td><span data-ttu-id="559ba-129"><strong>字串</strong>，指定 HTTP 伺服器 API 用來放置記錄檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="559ba-129">A <strong>String</strong> that specifies the folder under which the HTTP Server API places its logging files.</span></span> <br/> <span data-ttu-id="559ba-130">HTTP 伺服器 API &quot; &quot; 會在放置記錄檔的指定資料夾下建立名為 HTTPERR 的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="559ba-130">The HTTP Server API creates a subfolder named &quot;HTTPERR&quot; under the specified folder into which the log files are placed.</span></span> <span data-ttu-id="559ba-131">這個子資料夾和記錄檔都會收到相同的許可權設定，這表示系統管理員和本機系統帳戶具有完整存取權，而其他使用者則沒有存取權。</span><span class="sxs-lookup"><span data-stu-id="559ba-131">This subfolder and the log files receive the same permission settings, which means that Administrator and Local System Accounts have full access, while other users do not have access.</span></span><br/> <span data-ttu-id="559ba-132">如果登錄中未指定資料夾，預設資料夾如下：</span><span class="sxs-lookup"><span data-stu-id="559ba-132">If a folder is not specified in the registry, the default folder is the following:</span></span><br/> <span data-ttu-id="559ba-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span><span class="sxs-lookup"><span data-stu-id="559ba-133">&quot;%SystemRoot%\System32\LogFiles&quot;</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="559ba-134">ErrorLoggingDir 字串值必須是完整路徑，但它可以包含 &quot; % SystemRoot% &quot; 。</span><span class="sxs-lookup"><span data-stu-id="559ba-134">The ErrorLoggingDir string value must be a fully qualified path, but it can contain &quot;%SystemRoot%&quot;.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

 

 





