---
description: 事件記錄檔包含下列標準記錄和自訂記錄：
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Eventlog 索引鍵
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965c850dd31ab722786cf4da41c7d3a67f5d980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692507"
---
# <a name="eventlog-key"></a><span data-ttu-id="f7eab-103">Eventlog 索引鍵</span><span class="sxs-lookup"><span data-stu-id="f7eab-103">Eventlog Key</span></span>

<span data-ttu-id="f7eab-104">事件記錄檔包含下列標準記錄和自訂記錄：</span><span class="sxs-lookup"><span data-stu-id="f7eab-104">The event log contains the following standard logs as well as custom logs:</span></span>



| <span data-ttu-id="f7eab-105">記錄檔</span><span class="sxs-lookup"><span data-stu-id="f7eab-105">Log</span></span>             | <span data-ttu-id="f7eab-106">描述</span><span class="sxs-lookup"><span data-stu-id="f7eab-106">Description</span></span>                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eab-107">**應用程式**</span><span class="sxs-lookup"><span data-stu-id="f7eab-107">**Application**</span></span> | <span data-ttu-id="f7eab-108">包含應用程式所記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-108">Contains events logged by applications.</span></span> <span data-ttu-id="f7eab-109">例如，資料庫應用程式可能會記錄檔案錯誤。</span><span class="sxs-lookup"><span data-stu-id="f7eab-109">For example, a database application might record a file error.</span></span> <span data-ttu-id="f7eab-110">應用程式開發人員會決定要記錄哪些事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-110">The application developer decides which events to record.</span></span>                                                                             |
| <span data-ttu-id="f7eab-111">**安全性**</span><span class="sxs-lookup"><span data-stu-id="f7eab-111">**Security**</span></span>    | <span data-ttu-id="f7eab-112">包含事件，例如有效和不正確登入嘗試，以及與資源使用相關的事件，例如建立、開啟或刪除檔案或其他物件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-112">Contains events such as valid and invalid logon attempts, as well as events related to resource use such as creating, opening, or deleting files or other objects.</span></span> <span data-ttu-id="f7eab-113">系統管理員可以開始進行審核，以將事件記錄在安全性記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="f7eab-113">An administrator can start auditing to record events in the security log.</span></span> |
| <span data-ttu-id="f7eab-114">**系統**</span><span class="sxs-lookup"><span data-stu-id="f7eab-114">**System**</span></span>      | <span data-ttu-id="f7eab-115">包含系統元件所記錄的事件，例如，驅動程式失敗或其他系統元件在啟動時載入。</span><span class="sxs-lookup"><span data-stu-id="f7eab-115">Contains events logged by system components, such as the failure of a driver or other system component to load during startup.</span></span>                                                                                                               |
| <span data-ttu-id="f7eab-116">*>customlog*</span><span class="sxs-lookup"><span data-stu-id="f7eab-116">*CustomLog*</span></span>     | <span data-ttu-id="f7eab-117">包含建立自訂記錄檔的應用程式所記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-117">Contains events logged by applications that create a custom log.</span></span> <span data-ttu-id="f7eab-118">使用自訂記錄檔可讓應用程式控制記錄檔的大小或附加 Acl，以利安全起見，而不會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7eab-118">Using a custom log enables an application to control the size of the log or attach ACLs for security purposes without affecting other applications.</span></span>                         |



 

<span data-ttu-id="f7eab-119">事件記錄服務會使用儲存在 **Eventlog** 登錄機碼中的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7eab-119">The event logging service uses the information stored in the **Eventlog** registry key.</span></span> <span data-ttu-id="f7eab-120">**Eventlog** 索引鍵包含數個子機碼，稱為「*記錄*」。</span><span class="sxs-lookup"><span data-stu-id="f7eab-120">The **Eventlog** key contains several subkeys, called *logs*.</span></span> <span data-ttu-id="f7eab-121">每個記錄檔都包含事件記錄服務在應用程式寫入事件記錄檔和讀取時，用來尋找資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7eab-121">Each log contains information that the event logging service uses to locate resources when an application writes to and reads from the event log.</span></span>

<span data-ttu-id="f7eab-122">**Eventlog** 索引鍵的結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="f7eab-122">The structure of the **Eventlog** key is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

<span data-ttu-id="f7eab-123">請注意，網域控制站會在 **目錄服務** 和檔案複寫 **服務** 記錄檔中記錄事件，並且在 **dns 伺服器** 中記錄事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-123">Note that domain controllers record events in the **Directory service** and **File Replication service** logs and DNS servers record events in the **DNS server**.</span></span>

<span data-ttu-id="f7eab-124">每個記錄檔都可以包含下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-124">Each log can contain the following registry values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7eab-125">登錄值</span><span class="sxs-lookup"><span data-stu-id="f7eab-125">Registry value</span></span></th>
<th><span data-ttu-id="f7eab-126">Description</span><span class="sxs-lookup"><span data-stu-id="f7eab-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f7eab-127"><strong>CustomSD</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-127"><strong>CustomSD</strong></span></span></td>
<td><span data-ttu-id="f7eab-128">限制對事件記錄檔的存取。</span><span class="sxs-lookup"><span data-stu-id="f7eab-128">Restricts access to the event log.</span></span> <span data-ttu-id="f7eab-129">此值的類型為 REG_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-129">This value is of type REG_SZ.</span></span> <span data-ttu-id="f7eab-130">使用的格式為 <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">安全描述項定義語言</a> (SDDL) 。</span><span class="sxs-lookup"><span data-stu-id="f7eab-130">The format used is <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL).</span></span> <span data-ttu-id="f7eab-131">建立授與下列一或多個許可權的 ACL：</span><span class="sxs-lookup"><span data-stu-id="f7eab-131">Construct an ACL that grants one or more of the following rights:</span></span><dl> <span data-ttu-id="f7eab-132">清除 (0x0004) </span><span class="sxs-lookup"><span data-stu-id="f7eab-132">Clear (0x0004)</span></span><br />
<span data-ttu-id="f7eab-133">閱讀 (0x0001) </span><span class="sxs-lookup"><span data-stu-id="f7eab-133">Read (0x0001)</span></span><br />
<span data-ttu-id="f7eab-134">撰寫 (0x0002) </span><span class="sxs-lookup"><span data-stu-id="f7eab-134">Write (0x0002)</span></span><br />
</dl> <span data-ttu-id="f7eab-135">若要成為語法有效的 SDDL，CustomSD 值必須指定擁有者和群組擁有者 (例如 O:BAG： SY) ，但不會使用擁有者和群組擁有者。</span><span class="sxs-lookup"><span data-stu-id="f7eab-135">To be a syntactically valid SDDL, the CustomSD value must specify an owner and a group owner (for example, O:BAG:SY), but the owner and group owner are not used.</span></span> <span data-ttu-id="f7eab-136">如果 CustomSD 設定為錯誤的值，當事件記錄檔服務啟動時，系統事件記錄檔中就會引發事件，而事件記錄檔會取得與應用程式記錄檔原始 CustomSD 值相同的預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="f7eab-136">If CustomSD is set to a wrong value, an event is fired in the System event log when the event log service starts, and the event log gets a default security descriptor which is identical to the original CustomSD value for the Application log.</span></span> <span data-ttu-id="f7eab-137">不支援 Sacl。</span><span class="sxs-lookup"><span data-stu-id="f7eab-137">SACLs are not supported.</span></span><br/> <span data-ttu-id="f7eab-138">如需詳細資訊，請參閱 <a href="event-logging-security.md">事件記錄安全性</a>。</span><span class="sxs-lookup"><span data-stu-id="f7eab-138">For more information, see <a href="event-logging-security.md">Event Logging Security</a>.</span></span><br/> <span data-ttu-id="f7eab-139"><strong>Windows Server 2003：</strong> 支援 Sacl。</span><span class="sxs-lookup"><span data-stu-id="f7eab-139"><strong>Windows Server 2003:</strong> SACLs are supported.</span></span><br/> <span data-ttu-id="f7eab-140"><strong>WINDOWS XP/2000：</strong> 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-140"><strong>Windows XP/2000:</strong> This value is not supported.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7eab-141"><strong>DisplayNameFile</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-141"><strong>DisplayNameFile</strong></span></span></td>
<td><span data-ttu-id="f7eab-142">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-142">This value is not used.</span></span> <span data-ttu-id="f7eab-143"><strong>Windows Server 2003 和 WINDOWS XP/2000：  </strong> 儲存事件記錄檔之當地語系化名稱的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f7eab-143"><strong>Windows Server 2003 and Windows XP/2000:  </strong> Name of the file that stores the localized name of the event log.</span></span> <span data-ttu-id="f7eab-144">儲存在此檔案中的名稱會顯示為事件檢視器中的記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f7eab-144">The name stored in this file appears as the log name in Event Viewer.</span></span> <span data-ttu-id="f7eab-145">如果事件記錄檔的登錄中未出現此專案，事件檢視器會將登錄子機碼的名稱顯示為記錄檔名稱。</span><span class="sxs-lookup"><span data-stu-id="f7eab-145">If this entry does not appear in the registry for an event log, Event Viewer displays the name of the registry subkey as the log name.</span></span> <span data-ttu-id="f7eab-146">此值的類型為 REG_EXPAND_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-146">This value is of type REG_EXPAND_SZ.</span></span> <span data-ttu-id="f7eab-147">預設值為% SystemRoot% \system32\els.dll。</span><span class="sxs-lookup"><span data-stu-id="f7eab-147">The default value is %SystemRoot%\system32\els.dll.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7eab-148"><strong>DisplayNameID</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-148"><strong>DisplayNameID</strong></span></span></td>
<td><span data-ttu-id="f7eab-149">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-149">This value is not used.</span></span> <span data-ttu-id="f7eab-150"><strong>Windows Server 2003 和 WINDOWS XP/2000：  </strong> 記錄檔名稱字串的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7eab-150"><strong>Windows Server 2003 and Windows XP/2000:  </strong> Message identification number of the log name string.</span></span> <span data-ttu-id="f7eab-151">此數位表示顯示當地語系化顯示名稱的訊息。</span><span class="sxs-lookup"><span data-stu-id="f7eab-151">This number indicates the message in which the localized display name appears.</span></span> <span data-ttu-id="f7eab-152">訊息會儲存在 <strong>DisplayNameFile</strong> 值所指定的檔案中。</span><span class="sxs-lookup"><span data-stu-id="f7eab-152">The message is stored in the file specified by the <strong>DisplayNameFile</strong> value.</span></span> <span data-ttu-id="f7eab-153">此值的類型為 REG_DWORD。</span><span class="sxs-lookup"><span data-stu-id="f7eab-153">This value is of type REG_DWORD.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7eab-154"><strong>檔案</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-154"><strong>File</strong></span></span></td>
<td><span data-ttu-id="f7eab-155">儲存每個事件記錄檔之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f7eab-155">Fully qualified path to the file where each event log is stored.</span></span> <span data-ttu-id="f7eab-156">這可讓事件檢視器和其他應用程式尋找記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f7eab-156">This enables Event Viewer and other applications to find the log files.</span></span> <span data-ttu-id="f7eab-157">此值的類型為 REG_SZ 或 REG_EXPAND_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-157">This value is of type REG_SZ or REG_EXPAND_SZ.</span></span> <span data-ttu-id="f7eab-158">這是選擇性的值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-158">This value is optional.</span></span> <span data-ttu-id="f7eab-159">如果未指定值，則預設為%SystemRoot%\system32\winevt\logs\，後面接著以事件記錄檔登錄機碼名稱為基礎的檔案名。特定事件記錄檔路徑應該使用命令列公用程式來設定 wevtutil.exe 或使用 <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> 函式搭配傳遞至 <em>PropertyId</em> 參數的 EvtChannelLoggingConfigLogFilePath。</span><span class="sxs-lookup"><span data-stu-id="f7eab-159">If the value is not specified, it defaults to %SystemRoot%\system32\winevt\logs\ followed by a file name that is based on the event log registry key name.The specific event log file path should be set using the command line utility wevtutil.exe or by using the <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> function with EvtChannelLoggingConfigLogFilePath passed into the <em>PropertyId</em> parameter.</span></span><br/> <span data-ttu-id="f7eab-160">如果已設定特定檔案，請確定事件記錄檔服務具有該檔案的完整許可權。</span><span class="sxs-lookup"><span data-stu-id="f7eab-160">If a specific file is set, make sure that the event log service has full permissions on the file.</span></span><br/> <span data-ttu-id="f7eab-161">此值必須是位於本機目錄的檔案的有效檔案名， (不是遠端電腦，而不是 DOS 裝置、非磁片磁碟機，而不是管道) 。</span><span class="sxs-lookup"><span data-stu-id="f7eab-161">This value needs to be a valid file name for a file that is located on a local directory (not a remote computer, not a DOS device, not a floppy, and not a pipe).</span></span> <span data-ttu-id="f7eab-162">如果檔案設定錯誤，當事件記錄檔服務啟動時，系統事件記錄檔中就會引發事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-162">If the file setting is wrong, an event is fired in the System event log when the event log service starts.</span></span><br/> <span data-ttu-id="f7eab-163">請勿在檔案路徑中使用環境變數，該檔案在事件記錄檔服務的內容中無法展開。</span><span class="sxs-lookup"><span data-stu-id="f7eab-163">Do not use environment variables, in the path to the file, that cannot be expanded in the context of the event log service.</span></span><br/> <span data-ttu-id="f7eab-164"><strong>Windows Server 2003 和 WINDOWS XP/2000：</strong> 此值預設為%SystemRoot%\system32\config\，後面接著以事件記錄檔登錄機碼名稱為基礎的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f7eab-164"><strong>Windows Server 2003 and Windows XP/2000:</strong> This value defaults to %SystemRoot%\system32\config\ followed by a file name that is based on the event log registry key name.</span></span> <span data-ttu-id="f7eab-165">如果檔案設定設為不正確值，記錄檔將不會正確地初始化，或所有要求都會以無訊息模式移至預設記錄 (應用程式) 。</span><span class="sxs-lookup"><span data-stu-id="f7eab-165">If the File setting is set to an invalid value, the log will either not be initialized properly, or all requests will silently go to the default log (Application).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7eab-166"><strong>MaxSize</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-166"><strong>MaxSize</strong></span></span></td>
<td><span data-ttu-id="f7eab-167">記錄檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7eab-167">Maximum size, in bytes, of the log file.</span></span> <span data-ttu-id="f7eab-168">此值的類型為 REG_DWORD。</span><span class="sxs-lookup"><span data-stu-id="f7eab-168">This value is of type REG_DWORD.</span></span> <span data-ttu-id="f7eab-169">系統、應用程式或安全性記錄檔的值必須設定為64K 的倍數。</span><span class="sxs-lookup"><span data-stu-id="f7eab-169">The value must be set to a multiple of 64K for a System, Application, or Security log.</span></span> <span data-ttu-id="f7eab-170">預設值為1MB。<strong>Windows Server 2003 和 WINDOWS XP/2000：</strong> 此值限制為0xFFFFFFFF，預設值為512K。</span><span class="sxs-lookup"><span data-stu-id="f7eab-170">The default value is 1MB.<strong>Windows Server 2003 and Windows XP/2000:</strong> The value is limited to 0xFFFFFFFF, and the default value is 512K.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7eab-171"><strong>PrimaryModule</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-171"><strong>PrimaryModule</strong></span></span></td>
<td><span data-ttu-id="f7eab-172">未使用此值。<strong>Windows Server 2003 和 WINDOWS XP/2000：</strong> 此值是子機碼的名稱，其中包含事件來源之子機碼中專案的預設值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-172">This value is not used.<strong>Windows Server 2003 and Windows XP/2000:</strong> This value is the name of the subkey that contains the default values for the entries in the subkey for the event source.</span></span> <span data-ttu-id="f7eab-173">此值的類型為 REG_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-173">This value is of type REG_SZ.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7eab-174"><strong>保留</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-174"><strong>Retention</strong></span></span></td>
<td><span data-ttu-id="f7eab-175">此值的類型為 REG_DWORD。</span><span class="sxs-lookup"><span data-stu-id="f7eab-175">This value is of type REG_DWORD.</span></span> <span data-ttu-id="f7eab-176">預設值為 0。</span><span class="sxs-lookup"><span data-stu-id="f7eab-176">The default value is 0.</span></span> <span data-ttu-id="f7eab-177">如果這個值為0，則一律會覆寫事件的記錄。</span><span class="sxs-lookup"><span data-stu-id="f7eab-177">If this value is 0, the records of events are always overwritten.</span></span> <span data-ttu-id="f7eab-178">如果這個值是0xFFFFFFFF 或任何非零值，則永遠不會覆寫記錄。</span><span class="sxs-lookup"><span data-stu-id="f7eab-178">If this value is 0xFFFFFFFF or any nonzero value, records are never overwritten.</span></span> <span data-ttu-id="f7eab-179">當記錄檔達到大小上限時，您必須手動清除記錄檔;否則會捨棄新的事件。</span><span class="sxs-lookup"><span data-stu-id="f7eab-179">When the log file reaches its maximum size, you must clear the log manually; otherwise, new events are discarded.</span></span> <span data-ttu-id="f7eab-180">您也必須先清除記錄檔，才能變更其大小。<strong>Windows Server 2003 和 WINDOWS XP/2000：  </strong> 此值是受保護的事件記錄不受覆寫的時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f7eab-180">You must also clear the log before you can change its size.<strong>Windows Server 2003 and Windows XP/2000:  </strong> This value is the time interval, in seconds, that records of events are protected from being overwritten.</span></span> <span data-ttu-id="f7eab-181">當事件的存留期達到或超過此值時，就可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="f7eab-181">When the age of an event reaches or exceeds this value, it can be overwritten.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7eab-182"><strong>來源</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-182"><strong>Sources</strong></span></span></td>
<td><span data-ttu-id="f7eab-183">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-183">This value is not used.</span></span> <span data-ttu-id="f7eab-184"><strong>Windows Server 2003 和 WINDOWS XP/2000：  </strong> 將事件寫入此記錄檔的應用程式、服務或應用程式群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7eab-184"><strong>Windows Server 2003 and Windows XP/2000:  </strong> Names of the applications, services, or groups of applications that write events to this log.</span></span> <span data-ttu-id="f7eab-185">此值應僅供讀取，且不會改變。</span><span class="sxs-lookup"><span data-stu-id="f7eab-185">This value should only be read and not altered.</span></span> <span data-ttu-id="f7eab-186">事件記錄服務會根據記錄檔下子機碼中列出的每個程式來維護清單。</span><span class="sxs-lookup"><span data-stu-id="f7eab-186">The event log service maintains the list based on each program listed in a subkey under the log.</span></span> <span data-ttu-id="f7eab-187">此值的類型為 REG_MULTI_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-187">This value is of type REG_MULTI_SZ.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7eab-188"><strong>AutoBackupLogFiles</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-188"><strong>AutoBackupLogFiles</strong></span></span></td>
<td><span data-ttu-id="f7eab-189">此值的類型為 REG_DWORD，且事件記錄檔服務會使用此值來判斷是否應該自動儲存事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f7eab-189">This value is of type REG_DWORD, and is used by the event log service to determine whether an event log should be automatically saved.</span></span> <span data-ttu-id="f7eab-190">預設值為0，這會停用自動備份。</span><span class="sxs-lookup"><span data-stu-id="f7eab-190">The default value is 0, which disables auto-backup.</span></span> <span data-ttu-id="f7eab-191">只有當保留值為-1 (0xFFFFFFFF) 時，服務才會備份記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f7eab-191">The service will back up the log file only if the retention value is -1 (0xFFFFFFFF).</span></span> <span data-ttu-id="f7eab-192">其他值將會被忽略。<strong>Windows Server 2003：  </strong> 保留可以設定為-1 (0xFFFFFFFF) 或 1 (0x00000001) 讓 AutoBackupLogFiles 運作。</span><span class="sxs-lookup"><span data-stu-id="f7eab-192">Other values will be ignored.<strong>Windows Server 2003:  </strong> Retention can be set to -1 (0xFFFFFFFF) or 1 (0x00000001) for AutoBackupLogFiles to work.</span></span> <span data-ttu-id="f7eab-193">其他值將會被忽略。</span><span class="sxs-lookup"><span data-stu-id="f7eab-193">Other values will be ignored.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f7eab-194"><strong>RestrictGuestAccess</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-194"><strong>RestrictGuestAccess</strong></span></span></td>
<td><span data-ttu-id="f7eab-195">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="f7eab-195">This value is not used.</span></span> <span data-ttu-id="f7eab-196"><strong>WINDOWS XP/2000：  </strong> 此值的類型為 REG_DWORD，預設值為1。</span><span class="sxs-lookup"><span data-stu-id="f7eab-196"><strong>Windows XP/2000:  </strong> This value is of type REG_DWORD, and the default value is 1.</span></span> <span data-ttu-id="f7eab-197">當值設定為1時，會限制來賓和匿名帳戶對事件記錄檔的存取，當這個值為0時，它會允許 Guest 帳戶存取事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="f7eab-197">When the value is set to 1, it restricts the Guest and Anonymous account access to the event log, and when this value is 0, it allows Guest account access to the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f7eab-198"><strong>隔離</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-198"><strong>Isolation</strong></span></span></td>
<td><span data-ttu-id="f7eab-199">定義記錄檔的預設存取權限。</span><span class="sxs-lookup"><span data-stu-id="f7eab-199">Defines the default access permissions for the log.</span></span> <span data-ttu-id="f7eab-200">此值的類型為 REG_SZ。</span><span class="sxs-lookup"><span data-stu-id="f7eab-200">This value is of type REG_SZ.</span></span> <span data-ttu-id="f7eab-201">您可以指定下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="f7eab-201">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="f7eab-202"><strong>應用程式</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-202"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="f7eab-203"><strong>系統</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-203"><strong>System</strong></span></span></li>
<li><span data-ttu-id="f7eab-204"><strong>Custom</strong></span><span class="sxs-lookup"><span data-stu-id="f7eab-204"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="f7eab-205">預設隔離為 [ <strong>應用程式</strong>]。</span><span class="sxs-lookup"><span data-stu-id="f7eab-205">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="f7eab-206"><strong>應用程式</strong>的預設許可權 (使用 SDDL) 來顯示：</span><span class="sxs-lookup"><span data-stu-id="f7eab-206">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
<span data-ttu-id="f7eab-207"><strong>系統</strong>的預設許可權 (使用 SDDL) 來顯示：</span><span class="sxs-lookup"><span data-stu-id="f7eab-207">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
<span data-ttu-id="f7eab-208"><strong>自訂</strong>隔離的預設許可權與應用程式相同。</span><span class="sxs-lookup"><span data-stu-id="f7eab-208">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span><br/> <span data-ttu-id="f7eab-209"><strong>Windows Server 2003 和 WINDOWS XP/2000：  </strong> 此值無法使用。</span><span class="sxs-lookup"><span data-stu-id="f7eab-209"><strong>Windows Server 2003 and Windows XP/2000:  </strong> This value is not available.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f7eab-210">每個記錄檔也都包含事件來源。</span><span class="sxs-lookup"><span data-stu-id="f7eab-210">Each log also contains event sources.</span></span> <span data-ttu-id="f7eab-211">如需詳細資訊，請參閱 [事件來源](event-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="f7eab-211">For more information, see [Event Sources](event-sources.md).</span></span>

