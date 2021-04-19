---
description: 深入瞭解：可擴充儲存引擎檔案
title: 可擴充儲存引擎檔案
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992662"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="d4430-103">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="d4430-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d4430-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="d4430-105">可擴充儲存引擎檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="d4430-106">可擴充儲存引擎會使用下列類型的檔案：</span><span class="sxs-lookup"><span data-stu-id="d4430-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="d4430-107">交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="d4430-108">暫存交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="d4430-109">保留的交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="d4430-110">檢查點檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="d4430-111">資料庫檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="d4430-112">暫存資料庫</span><span class="sxs-lookup"><span data-stu-id="d4430-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="d4430-113">清除對應檔</span><span class="sxs-lookup"><span data-stu-id="d4430-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="d4430-114">下表包含由 ESE 管理之資料檔案名稱的總覽。</span><span class="sxs-lookup"><span data-stu-id="d4430-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="d4430-115">若為 Windows Vista 和更新版本，JET_paramLegacyNames 設定會影響所使用的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d4430-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="d4430-116">作業系統</span><span class="sxs-lookup"><span data-stu-id="d4430-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="d4430-117">Windows Server 2003 及更早版本</span><span class="sxs-lookup"><span data-stu-id="d4430-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="d4430-118">Windows Vista 和更新版本 (用戶端) </span><span class="sxs-lookup"><span data-stu-id="d4430-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="d4430-119">Windows Server 2008 和更新版本 (Server) </span><span class="sxs-lookup"><span data-stu-id="d4430-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="d4430-120">Windows 10 年度更新版和更新版本 (用戶端) </span><span class="sxs-lookup"><span data-stu-id="d4430-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="d4430-121">Windows Server 2016 和更新版本 (Server) </span><span class="sxs-lookup"><span data-stu-id="d4430-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-122">
        <strong>JET_paramLegacyNames 設定</strong>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-123">
        <strong>N/A</strong>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-124">
        <strong>無</strong>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-126">
        <strong>與 Windows Vista/Server 2008 相同</strong>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-127">目前的記錄</span><span class="sxs-lookup"><span data-stu-id="d4430-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-128">&lt;inst &gt; .log</span><span class="sxs-lookup"><span data-stu-id="d4430-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-129">&lt;inst &gt; . jtx</span><span class="sxs-lookup"><span data-stu-id="d4430-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-130">&lt;inst &gt; .log</span><span class="sxs-lookup"><span data-stu-id="d4430-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-131">預先初始化記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-132">&lt;inst &gt; tmp .log</span><span class="sxs-lookup"><span data-stu-id="d4430-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-133">&lt;inst &gt; tmp. jtx</span><span class="sxs-lookup"><span data-stu-id="d4430-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-134">&lt;inst &gt; tmp .log</span><span class="sxs-lookup"><span data-stu-id="d4430-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-135">輪替的記錄</span><span class="sxs-lookup"><span data-stu-id="d4430-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-136">&lt;inst &gt; XXXXX 記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-137">&lt;inst &gt; XXXXX 在 FFFFF 切換至 &lt; inst xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 之後 jtx &gt; 。 jtx</span><span class="sxs-lookup"><span data-stu-id="d4430-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-138">&lt;&gt;在 FFFFF 切換至 inst xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx 之後，inst XXXXX. 記錄檔 &lt; &gt; 。</span><span class="sxs-lookup"><span data-stu-id="d4430-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-139">
        <a href="gg294069(v=exchg.10).md">檢查點檔案</a>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-140">&lt;inst &gt;</span><span class="sxs-lookup"><span data-stu-id="d4430-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-141">&lt;inst &gt; . jcp</span><span class="sxs-lookup"><span data-stu-id="d4430-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-142">&lt;inst &gt;</span><span class="sxs-lookup"><span data-stu-id="d4430-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-143">
        <a href="gg294069(v=exchg.10).md">暫存資料庫</a>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-144">&lt;暫存資料庫檔案名 &gt; 預設： .tmp</span><span class="sxs-lookup"><span data-stu-id="d4430-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-145">&lt;暫存資料庫檔案名 &gt; 預設： .tmp</span><span class="sxs-lookup"><span data-stu-id="d4430-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-146">&lt;暫存資料庫檔案名 &gt; 預設： .tmp</span><span class="sxs-lookup"><span data-stu-id="d4430-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-147">
        <a href="gg294069(v=exchg.10).md">保留的交易記錄檔</a>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-148">res1 .log &amp; res2</span><span class="sxs-lookup"><span data-stu-id="d4430-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-149">&lt;inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="d4430-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="d4430-150">&lt;inst &gt; RESXXXXX. jrs</span><span class="sxs-lookup"><span data-stu-id="d4430-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-151">
        <a href="gg294069(v=exchg.10).md">資料庫檔案</a>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-152">&lt;資料庫檔案名&gt;</span><span class="sxs-lookup"><span data-stu-id="d4430-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-153">&lt;資料庫檔案名&gt;</span><span class="sxs-lookup"><span data-stu-id="d4430-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-154">&lt;資料庫檔案名&gt;</span><span class="sxs-lookup"><span data-stu-id="d4430-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="d4430-155">
        <a href="gg294069(v=exchg.10).md">清除對應檔</a>
      </span><span class="sxs-lookup"><span data-stu-id="d4430-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-156">N/A</span><span class="sxs-lookup"><span data-stu-id="d4430-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-157">N/A</span><span class="sxs-lookup"><span data-stu-id="d4430-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-158">N/A</span><span class="sxs-lookup"><span data-stu-id="d4430-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="d4430-159">&lt;沒有副檔名的資料庫檔案名 &gt; 。 jfm</span><span class="sxs-lookup"><span data-stu-id="d4430-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="d4430-160">交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-160">Transaction Log Files</span></span>

<span data-ttu-id="d4430-161">交易記錄檔包含對資料庫檔案的作業。</span><span class="sxs-lookup"><span data-stu-id="d4430-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="d4430-162">它們包含足夠的資訊，可在非預期的進程終止或系統關機之後，讓資料庫保持邏輯一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4430-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="d4430-163">記錄檔的名稱相依于三個字母的基底名稱，可使用 [JET_paramBaseName](./transaction-log-parameters.md)設定。</span><span class="sxs-lookup"><span data-stu-id="d4430-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="d4430-164">下列範例會使用 "edb" 的基底名稱，因為這是預設的基底名稱。</span><span class="sxs-lookup"><span data-stu-id="d4430-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="d4430-165">交易記錄檔的副檔名會是 .log 或. jtx，視 JET_bitESE98FileNames 是否在 JET_paramLegacyFileNames 參數中設定而定。</span><span class="sxs-lookup"><span data-stu-id="d4430-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="d4430-166">如需詳細資訊，請參閱 [可擴充儲存引擎系統參數](./extensible-storage-engine-system-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d4430-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="d4430-167">交易記錄檔的名稱為 \<base\> \<generation-number\> .log，從1開始。</span><span class="sxs-lookup"><span data-stu-id="d4430-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="d4430-168">記錄產生編號採用十六進位格式。</span><span class="sxs-lookup"><span data-stu-id="d4430-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="d4430-169">例如，edb00001 是第一個記錄檔，而 edb000ff 則是255th 記錄。</span><span class="sxs-lookup"><span data-stu-id="d4430-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="d4430-170">記錄檔的記錄檔名稱中有五個十六進位數位，在1048576th 記錄檔之前，記錄檔的開頭是以11.3 格式命名 (例如 edb00100000) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="d4430-171">\<base\>.log 一律是目前正在使用的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="d4430-172">如果資料庫引擎不在使用中，則可以使用下列命令來識別世代的世代： **esentutl.exe-ml .edb**. a. log。</span><span class="sxs-lookup"><span data-stu-id="d4430-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="d4430-173">雖然交易記錄檔具有。記錄檔延伸通常與文字檔相關聯，而交易記錄檔則是二進位格式，而且不應該由使用者編輯。資料庫作業會先寫入至記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="d4430-174">資料可以稍後寫入資料庫檔案;可能會在稍後可能會有很多。</span><span class="sxs-lookup"><span data-stu-id="d4430-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="d4430-175">如果未預期的進程或系統終止，作業仍會存在於記錄檔中，而不完整的交易則可以復原。</span><span class="sxs-lookup"><span data-stu-id="d4430-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="d4430-176">重新執行交易記錄檔的動作稱為「 *軟* 復原」，其會在呼叫 [JetInit](./jetinit-function.md) 或 [JetInit2](./jetinit2-function.md) 時自動完成。</span><span class="sxs-lookup"><span data-stu-id="d4430-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="d4430-177">您也可以使用 Esentutl.exe 程式的 "-r" 選項，以手動方式執行軟復原。</span><span class="sxs-lookup"><span data-stu-id="d4430-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="d4430-178">在從備份還原的資料庫上重新執行交易記錄檔的動作，稱為「 *硬* 復原」。</span><span class="sxs-lookup"><span data-stu-id="d4430-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="d4430-179">記錄檔是固定大小，可透過 [JET_paramLogFileSize](./transaction-log-parameters.md)自訂。</span><span class="sxs-lookup"><span data-stu-id="d4430-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="d4430-180">當目前的記錄檔 (時，將會填入 .edb) ，它會重新命名為 \<base\> \<generation-number\> .log，而交易記錄資料流程中需要新的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="d4430-181">每個資料庫實例都有與其相關聯的單一記錄檔順序。</span><span class="sxs-lookup"><span data-stu-id="d4430-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="d4430-182">Windows XP 引進了 [JetCreateInstance](./jetcreateinstance-function.md)，可讓單一進程使用多個交易記錄檔順序。</span><span class="sxs-lookup"><span data-stu-id="d4430-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="d4430-183">但是，不能有多個交易記錄檔順序存在於相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="d4430-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="d4430-184">交易記錄檔幾乎不應手動操作、重新命名、移動或刪除，因為可能會導致資料損毀。</span><span class="sxs-lookup"><span data-stu-id="d4430-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="d4430-185">資料庫引擎會在完整備份期間刪除交易記錄檔 (如有啟用迴圈記錄，請參閱 [JetBackup](./jetbackup-function.md)、 [JetTruncateLog](./jettruncatelog-function.md)、 [JetTruncateLogInstance](./jettruncateloginstance-function.md)) 或正常作業期間。</span><span class="sxs-lookup"><span data-stu-id="d4430-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="d4430-186">填滿交易記錄檔之後，資料庫引擎必須建立新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="d4430-187">迴圈記錄是一種方法，也就是資料庫引擎在損毀復原不再需要記錄檔時，會自動清除記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="d4430-188">此程式是將記錄檔當作執行備份的產品來移除的替代方案。</span><span class="sxs-lookup"><span data-stu-id="d4430-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="d4430-189">您可以使用 [JET_paramCircularLog](./transaction-log-parameters.md) 系統參數來控制迴圈記錄。</span><span class="sxs-lookup"><span data-stu-id="d4430-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="d4430-190">交易記錄檔不應使用任何其他方法來刪除。</span><span class="sxs-lookup"><span data-stu-id="d4430-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="d4430-191">暫存交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="d4430-192">當 edb. log 填滿時，ESE 必須建立新的檔案。</span><span class="sxs-lookup"><span data-stu-id="d4430-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="d4430-193">新的記錄檔交易檔在 ESE 使用之前稱為暫存交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="d4430-194">當建立新的記錄檔，並將其大小延伸時，就會被稱為 \<base\> tmp .log。</span><span class="sxs-lookup"><span data-stu-id="d4430-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="d4430-195">建立新檔案可能是可能耗費成本的作業，因此 ESE 會以背景工作的方式主動建立下一個記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="d4430-196">由於暫存交易記錄檔是在需要新交易記錄檔的情況下建立的，因此不包含任何有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d4430-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="d4430-197">保留的交易記錄檔</span><span class="sxs-lookup"><span data-stu-id="d4430-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="d4430-198">當引擎開始允許記錄重要作業以取得正常關機時，會建立保留的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="d4430-199">**Windows Vista：** 在 Windows Vista 和更新版本中，保留的交易記錄檔會命名為 \<base\> RESXXXXX. jrs。</span><span class="sxs-lookup"><span data-stu-id="d4430-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="d4430-200">**Windows Server 2003：** 在 Windows Server 2003 及更早版本中，保留的交易記錄檔會命名為 res1 .log 和 res2。</span><span class="sxs-lookup"><span data-stu-id="d4430-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="d4430-201">當資料庫引擎用盡磁碟空間時，就無法建立新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="d4430-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="d4430-202">最安全的作法是完全關閉，但仍必須記錄某些作業 (例如復原作業) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="d4430-203">在這個階段中，大部分的資料庫作業都會失敗。</span><span class="sxs-lookup"><span data-stu-id="d4430-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="d4430-204">由於保留的交易記錄檔是在非磁片案例中，針對交易記錄檔的需要而建立的，因此不包含任何有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="d4430-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="d4430-205">檢查點檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-205">Checkpoint Files</span></span>

<span data-ttu-id="d4430-206">檢查點檔案會儲存特定交易記錄檔順序的檢查點。</span><span class="sxs-lookup"><span data-stu-id="d4430-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="d4430-207">檢查點檔案的名稱是 \<base\> .chk 或 \<base\> jcp，取決於 JET_bitESE98FileNames 是否在 JET_paramLegacyFileNames 參數中設定，而且它的位置是由 [JET_paramSystemPath](./transaction-log-parameters.md)提供。</span><span class="sxs-lookup"><span data-stu-id="d4430-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="d4430-208">資料庫作業會先寫入記錄檔，然後再快取到記憶體中。</span><span class="sxs-lookup"><span data-stu-id="d4430-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="d4430-209">稍後會將作業寫入資料庫檔案，但基於效能的考慮，作業寫入資料庫檔案的順序可能不符合最初記錄這些作業的順序。</span><span class="sxs-lookup"><span data-stu-id="d4430-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="d4430-210">寫入交易記錄檔的作業會處於下列其中一種狀態：</span><span class="sxs-lookup"><span data-stu-id="d4430-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="d4430-211">寫入交易記錄檔和資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="d4430-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="d4430-212">寫入交易記錄檔，但尚未寫入資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="d4430-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="d4430-213">許多資料庫作業都可以儲存在單一交易記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="d4430-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="d4430-214">給定的記錄檔可以包含下列專案：</span><span class="sxs-lookup"><span data-stu-id="d4430-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="d4430-215">寫入資料庫檔案的所有作業。</span><span class="sxs-lookup"><span data-stu-id="d4430-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="d4430-216">未將任何作業寫入資料庫檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-216">No operations written to the database file</span></span>

  - <span data-ttu-id="d4430-217">寫入資料庫檔案和尚未寫入資料庫檔案之作業的混合作業。</span><span class="sxs-lookup"><span data-stu-id="d4430-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="d4430-218">檢查點指的是交易記錄資料流程中，檢查點之前所有作業都已寫入資料庫檔案的時間點。</span><span class="sxs-lookup"><span data-stu-id="d4430-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="d4430-219">檢查點之後發生的作業並不會有任何保證。有些可能會在記憶體中，有些則可能寫入資料庫中。</span><span class="sxs-lookup"><span data-stu-id="d4430-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="d4430-220">因為檢查點之前記錄檔中的所有作業都是在資料庫檔案中表示，所以只需要檢查點之後的交易記錄檔即可進行軟復原，使特定資料庫進入乾淨狀態。</span><span class="sxs-lookup"><span data-stu-id="d4430-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="d4430-221">資料庫檔案</span><span class="sxs-lookup"><span data-stu-id="d4430-221">Database Files</span></span>

<span data-ttu-id="d4430-222">資料庫檔案包含資料庫中所有資料表的架構、資料庫中所有資料表的記錄，以及資料表的索引。</span><span class="sxs-lookup"><span data-stu-id="d4430-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="d4430-223">其位置會使用 [JetCreateDatabase](./jetcreatedatabase-function.md)、 [JetCreateDatabase2](./jetcreatedatabase2-function.md)、 [JetAttachDatabase](./jetattachdatabase-function.md)或 [JetAttachDatabase2](./jetattachdatabase2-function.md)來提供。</span><span class="sxs-lookup"><span data-stu-id="d4430-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="d4430-224">只有在成功呼叫 [JetTerm](./jetterm-function.md) 或 [JetTerm2](./jetterm2-function.md)之後，資料庫才會完全關閉。</span><span class="sxs-lookup"><span data-stu-id="d4430-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="d4430-225">Esentutl.exe 的程式可以使用 "-mh" 選項來偵測資料庫是否已完全關閉。</span><span class="sxs-lookup"><span data-stu-id="d4430-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="d4430-226">例如，"esentutl.exe mh sample" 將會讀取名為 sample 之資料庫的資料庫標頭，並印出範例 .edb 的狀態。</span><span class="sxs-lookup"><span data-stu-id="d4430-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="d4430-227">它可能會印出「狀態：乾淨關機」或「狀態：中途關機」。</span><span class="sxs-lookup"><span data-stu-id="d4430-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="d4430-228">未完全關機的資料庫處於中途關機狀態。</span><span class="sxs-lookup"><span data-stu-id="d4430-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="d4430-229">在 Windows XP 之前，此狀態稱為「 *不一致*」。</span><span class="sxs-lookup"><span data-stu-id="d4430-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="d4430-230">不一致的 (不一致的) 資料庫可透過軟復原進入乾淨狀態。</span><span class="sxs-lookup"><span data-stu-id="d4430-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="d4430-231">損毀的資料庫與 ( 「不一致」的 ) 資料庫不同。</span><span class="sxs-lookup"><span data-stu-id="d4430-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="d4430-232">損毀的資料庫指的是實體或邏輯損毀，而且無法使用軟修復來修正。</span><span class="sxs-lookup"><span data-stu-id="d4430-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="d4430-233">實體損毀可以是位翻轉，通常會由資料庫頁面上的總和檢查碼捕捉。</span><span class="sxs-lookup"><span data-stu-id="d4430-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="d4430-234">資料庫檔案中的總和檢查碼失敗，會將本身列為 JET_errReadVerifyFailure 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4430-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="d4430-235">只有完全關機的資料庫可以安全地四處移動或重新命名。</span><span class="sxs-lookup"><span data-stu-id="d4430-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="d4430-236">如果資料庫未完全關閉，就無法自動安全地移動或重新命名。</span><span class="sxs-lookup"><span data-stu-id="d4430-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="d4430-237">多個資料庫可以與單一交易記錄檔順序相關聯。</span><span class="sxs-lookup"><span data-stu-id="d4430-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="d4430-238">暫存資料庫</span><span class="sxs-lookup"><span data-stu-id="d4430-238">Temporary Databases</span></span>

<span data-ttu-id="d4430-239">暫存資料庫是用來做為 temptables 的備份存放區，而且也會在建立索引時使用。</span><span class="sxs-lookup"><span data-stu-id="d4430-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="d4430-240">名稱和位置會設定 [JET_paramTempPath](./temporary-database-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="d4430-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="d4430-241">Temptables 是使用 [JetOpenTempTable](./jetopentemptable-function.md)、 [JetOpenTempTable2](./jetopentemptable2-function.md)、 [JetOpenTempTable3](./jetopentemptable3-function.md)、 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="d4430-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="d4430-242">它們也會由某些 API 呼叫來建立，並用來傳回架構資訊 (例如 [JetGetIndexInfo](./jetgetindexinfo-function.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="d4430-243">清除對應檔</span><span class="sxs-lookup"><span data-stu-id="d4430-243">Flush Map Files</span></span>

<span data-ttu-id="d4430-244">從 Windows 10 年度更新版 (用戶端) 和 Windows Server 2016 (Server) 開始，ESE 新增額外的保護層級，以防止遺失寫入 (或遺失排清) 1，讓它能夠偵測這類事件跨進程重新 initialization2。</span><span class="sxs-lookup"><span data-stu-id="d4430-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="d4430-245">這項功能需要將中繼資料保存到稱為「排清對應」檔案的個別檔案。</span><span class="sxs-lookup"><span data-stu-id="d4430-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="d4430-246">為每個資料庫檔案建立一個排清對應檔案，而且位於相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="d4430-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="d4430-247">檔案的命名方式與資料庫檔案類似，但副檔名不同。</span><span class="sxs-lookup"><span data-stu-id="d4430-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="d4430-248">例如，如果用戶端應用程式建立具有完整路徑 C： \\ MyDirectory MyDabatase 的資料庫 \\ ，其對應的排清對應檔案為 c： \\ MyDirectory \\ MyDabatase. jfm。</span><span class="sxs-lookup"><span data-stu-id="d4430-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="d4430-249">這項增強功能導入了兩個資料庫檔案必須命名的需求：</span><span class="sxs-lookup"><span data-stu-id="d4430-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="d4430-250">相同目錄中的兩個資料庫不能具有具有不同副檔名的相同檔案名。</span><span class="sxs-lookup"><span data-stu-id="d4430-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="d4430-251">例如： C： \\ MyDirectory \\ MyDabatase. Db1 和 C： \\ MyDirectory \\ MyDabatase db2。</span><span class="sxs-lookup"><span data-stu-id="d4430-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="d4430-252">2 \。</span><span class="sxs-lookup"><span data-stu-id="d4430-252">2\.</span></span> <span data-ttu-id="d4430-253">資料庫不能有 jfm 副檔名。</span><span class="sxs-lookup"><span data-stu-id="d4430-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="d4430-254">當您手動複製或移動資料庫檔案時，其對應的排清對應檔案也應該分別複製或移至相同的目的地目錄。</span><span class="sxs-lookup"><span data-stu-id="d4430-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="d4430-255">如果在新的資料庫附件 (透過 [JetAttachDatabase](./jetattachdatabase-function.md)時不存在排清對應檔案，則會建立新的對應檔案，並視需要重新填入，因為頁面會從資料庫中讀取。</span><span class="sxs-lookup"><span data-stu-id="d4430-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="d4430-256">混合不相符的資料庫和清除對應檔案是由 ESE 處理，並強制刪除不相符的排清對應，並從頭開始重新建立。</span><span class="sxs-lookup"><span data-stu-id="d4430-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="d4430-257">排清對應檔案的大小會與相關聯的資料庫檔案直接成正比，大約等於 (所有大小（以位元組為單位），因此必須將結果進位至 8192) 的下一個倍數：</span><span class="sxs-lookup"><span data-stu-id="d4430-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="d4430-258">例如：針對使用32KB 頁面大小的 1.5 GB 資料庫，排清對應的近似大小為24576個位元組 (或 24KB) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="d4430-259">清除對應檔必須在資料庫頁面排清時重新整理。</span><span class="sxs-lookup"><span data-stu-id="d4430-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="d4430-260">如果已啟用交易式記錄 (例如， [JET_paramRecovery](./transaction-log-parameters.md) 設定為 "on"，則會在用戶端應用程式對資料庫進行修改時，執行重新整理排清對應的預設) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="d4430-261">平均而言，會將整個排清對應寫入至非變動媒體一次，以產生每20% 的 [JET_paramCheckpointDepthMax](./database-cache-parameters.md) 值得的交易記錄) 的位元組 (。</span><span class="sxs-lookup"><span data-stu-id="d4430-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="d4430-262">寫入作業的數目取決於資料庫在整個資料庫中的散發方式。</span><span class="sxs-lookup"><span data-stu-id="d4430-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="d4430-263">但最多可 (位元組大小) ：</span><span class="sxs-lookup"><span data-stu-id="d4430-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="d4430-264">如果已停用交易式記錄 (例如， [JET_paramRecovery](./transaction-log-parameters.md)設定為 "off" ) ，則只有在透過[JetDetachDatabase](./jetdetachdatabase-function.md)明確卸 (離資料庫時，才會重新整理排清對應一次，或者只要 (未傳遞 JET_bitTermDirty，[就會以](./jetterm2-function.md)隱含方式明確地卸離其[相關聯的](./jetterm-function.md)ESE 實例) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="d4430-265">1遺失的寫入 (或遺失排清) 定義為寫入作業，該作業會從作業系統成功傳回至 ESE 資料庫引擎，但實際資料永遠不會保存到非暫時性媒體中的資料庫檔案。</span><span class="sxs-lookup"><span data-stu-id="d4430-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="d4430-266">這通常是因為存放裝置堆疊的故障或設定不正確所致 (軟體或硬體) 。</span><span class="sxs-lookup"><span data-stu-id="d4430-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="d4430-267">如果資料位於進行遺失寫入事件的區域中，用戶端應用程式可能會從需要從資料庫讀取資料的 ESE 函數收到 [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d4430-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="d4430-268">2在進程存留期內偵測遺失寫入的功能，在 Windows 8 (用戶端) 和 Windows Server 2012 (Server) 之後已經存在。</span><span class="sxs-lookup"><span data-stu-id="d4430-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
