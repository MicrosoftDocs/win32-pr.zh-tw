---
description: IFilter 測試套件會驗證您的篩選處理常式。
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: 測試篩選處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2a2b0b6a6728051ab22590a481ad23a7197692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112448"
---
# <a name="testing-filter-handlers"></a><span data-ttu-id="8f95d-103">測試篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-103">Testing Filter Handlers</span></span>

<span data-ttu-id="8f95d-104">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件會驗證您的篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="8f95d-104">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite validates your filter handlers.</span></span> <span data-ttu-id="8f95d-105">測試套件會透過下列方式來執行：呼叫 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 方法，並檢查傳回的值是否符合 **IFilter** 介面規格的規範;而且，檢查區塊識別碼是唯一且不斷增加的， **ifilter** 介面會在重新初始化之後一致地運作，而且具有無效參數的任何 **IFilter** 方法呼叫都會傳回預期的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8f95d-105">The test suite does so by: calling [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) methods and checking the returned values for compliance with the **IFilter** interface specification; and checking that chunk identifiers are unique and increasing, that the **IFilter** interface behaves consistently after re-initialization, and that any **IFilter** method calls with invalid parameters return expected error codes.</span></span> <span data-ttu-id="8f95d-106">測試套件程式也會傾印篩選處理常式所篩選之檔案的輸出，並檢查登錄中的 **IFilter** 註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="8f95d-106">The test suite programs also dump the output of a file filtered by a filter handler, and check the **IFilter** registration information in the registry.</span></span>

<span data-ttu-id="8f95d-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="8f95d-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="8f95d-108">命令列調用</span><span class="sxs-lookup"><span data-stu-id="8f95d-108">Command-Line Invocation</span></span>](#command-line-invocation)
  - [<span data-ttu-id="8f95d-109">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-109">ifilttst.exe</span></span>](#ifilttstexe)
  - [<span data-ttu-id="8f95d-110">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-110">filtdump.exe</span></span>](#filtdumpexe)
  - [<span data-ttu-id="8f95d-111">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-111">filtreg.exe</span></span>](#filtregexe)
  - [<span data-ttu-id="8f95d-112">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="8f95d-112">ifilttst.ini</span></span>](#ifilttstini)
- [<span data-ttu-id="8f95d-113">IFilter 測試程式</span><span class="sxs-lookup"><span data-stu-id="8f95d-113">IFilter Test Procedure</span></span>](#ifilter-test-procedure)
  - [<span data-ttu-id="8f95d-114">驗證測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-114">Validation Test</span></span>](#validation-test)
  - [<span data-ttu-id="8f95d-115">一致性測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-115">Consistency Test</span></span>](#consistency-test)
  - [<span data-ttu-id="8f95d-116">不正確輸入測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-116">Invalid Input Test</span></span>](#invalid-input-test)
  - [<span data-ttu-id="8f95d-117">測試不同的 IFilter 設定</span><span class="sxs-lookup"><span data-stu-id="8f95d-117">Testing Different IFilter Configurations</span></span>](#testing-different-ifilter-configurations)
- [<span data-ttu-id="8f95d-118">確定已註冊的專案已編制索引</span><span class="sxs-lookup"><span data-stu-id="8f95d-118">Ensuring Registered Items Get Indexed</span></span>](#ensuring-registered-items-get-indexed)
  - [<span data-ttu-id="8f95d-119">範例記錄檔</span><span class="sxs-lookup"><span data-stu-id="8f95d-119">Sample Log File</span></span>](#sample-log-file)
  - [<span data-ttu-id="8f95d-120">範例傾印檔案</span><span class="sxs-lookup"><span data-stu-id="8f95d-120">Sample Dump File</span></span>](#sample-dump-file)
- [<span data-ttu-id="8f95d-121">其他資源</span><span class="sxs-lookup"><span data-stu-id="8f95d-121">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="8f95d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f95d-122">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="8f95d-123">如果將檔案類型的新篩選處理常式安裝為現有篩選註冊的取代，則安裝程式應儲存目前的註冊，並在新的篩選器處理常式卸載時還原。</span><span class="sxs-lookup"><span data-stu-id="8f95d-123">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="8f95d-124">沒有任何機制可連結篩選。</span><span class="sxs-lookup"><span data-stu-id="8f95d-124">There is no mechanism to chain filters.</span></span> <span data-ttu-id="8f95d-125">因此，新的篩選處理常式會負責複寫舊篩選器的任何必要功能。</span><span class="sxs-lookup"><span data-stu-id="8f95d-125">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="command-line-invocation"></a><span data-ttu-id="8f95d-126">Command-Line 調用</span><span class="sxs-lookup"><span data-stu-id="8f95d-126">Command-Line Invocation</span></span>

<span data-ttu-id="8f95d-127">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件包含三個命令列應用程式- [ifilttst.exe](#ifilttstexe)、 [filtdump.exe](#filtdumpexe)和 [filtreg.exe](#filtregexe) ，以及 [ifilttst.ini](#ifilttstini)的初始化檔。</span><span class="sxs-lookup"><span data-stu-id="8f95d-127">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite consists of three command-line applications - [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe), and [filtreg.exe](#filtregexe) and an initialization file, [ifilttst.ini](#ifilttstini).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8f95d-128">在 Windows 7 和更新版本中，會明確封鎖以 managed 程式碼撰寫的篩選。</span><span class="sxs-lookup"><span data-stu-id="8f95d-128">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="8f95d-129">您必須以機器碼撰寫篩選器，因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。</span><span class="sxs-lookup"><span data-stu-id="8f95d-129">Filters MUST be written in native code due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="ifilttstexe"></a><span data-ttu-id="8f95d-130">ifilttst.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-130">ifilttst.exe</span></span>

<span data-ttu-id="8f95d-131">ifilttst.exe 程式會執行數個測試，以驗證篩選處理常式。</span><span class="sxs-lookup"><span data-stu-id="8f95d-131">The ifilttst.exe program runs several tests to validate a filter handler.</span></span> <span data-ttu-id="8f95d-132">下列範例說明如何從命令列叫用 ifilttst.exe 程式：</span><span class="sxs-lookup"><span data-stu-id="8f95d-132">The following example illustrates how to invoke the ifilttst.exe program from the command line:</span></span>


```
ifilttst /i test.htm /l /d /v 1
```

<span data-ttu-id="8f95d-133">此範例會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="8f95d-133">The example performs the following tasks:</span></span>

- <span data-ttu-id="8f95d-134">指示程式篩選檔案 test.htm</span><span class="sxs-lookup"><span data-stu-id="8f95d-134">Directs the program to filter the file test.htm</span></span>
- <span data-ttu-id="8f95d-135">將記錄檔訊息重新導向至 test.htm .log。</span><span class="sxs-lookup"><span data-stu-id="8f95d-135">Redirects the log messages to test.htm.log</span></span>
- <span data-ttu-id="8f95d-136">將傾印訊息重新導向至 test.htm dmp</span><span class="sxs-lookup"><span data-stu-id="8f95d-136">Redirects the dump messages to test.htm.dmp</span></span>
- <span data-ttu-id="8f95d-137">將詳細資訊設定為1</span><span class="sxs-lookup"><span data-stu-id="8f95d-137">Sets the verbosity to 1</span></span>

<span data-ttu-id="8f95d-138">若要讓上述命令能夠運作，您必須在目前的工作目錄中找到三個檔案： `test.htm` 、 [ifilttst.exe](#ifilttstexe)和 [ifilttst.ini](#ifilttstini)。</span><span class="sxs-lookup"><span data-stu-id="8f95d-138">For the preceding command to work, three files must be located in the current working directory: `test.htm`, [ifilttst.exe](#ifilttstexe), and [ifilttst.ini](#ifilttstini).</span></span> <span data-ttu-id="8f95d-139">命令列參數列于下表中。</span><span class="sxs-lookup"><span data-stu-id="8f95d-139">Command-line switches are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f95d-140">切換和可能的變數</span><span class="sxs-lookup"><span data-stu-id="8f95d-140">Switch and possible variables</span></span></th>
<th><span data-ttu-id="8f95d-141">Description</span><span class="sxs-lookup"><span data-stu-id="8f95d-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f95d-142"><strong>/i 檔案名</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-142"><strong>/i file name</strong></span></span></td>
<td><span data-ttu-id="8f95d-143">要篩選的輸入檔或目錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-143">The input file or directory to be filtered.</span></span> <span data-ttu-id="8f95d-144">檔案名可以包含萬用字元 <code>\*</code> 和 <code>?</code> 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-144">The file name can contain the wildcard characters <code>\*</code> and <code>?</code>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f95d-145"><strong>/l</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-145"><strong>/l</strong></span></span></td>
<td><span data-ttu-id="8f95d-146">記錄訊息會被導向至檔案，而不是畫面。</span><span class="sxs-lookup"><span data-stu-id="8f95d-146">Log messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="8f95d-147">記錄訊息會描述所執行的個別測試，以及測試的通過/失敗結果。</span><span class="sxs-lookup"><span data-stu-id="8f95d-147">Log messages describe the individual tests performed and the pass/fail results of the tests.</span></span> <span data-ttu-id="8f95d-148">記錄檔名稱與輸入檔案名相同，但副檔名為 .log。</span><span class="sxs-lookup"><span data-stu-id="8f95d-148">The log file name is the same as the input file name but with a .log extension.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f95d-149"><strong>/d</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-149"><strong>/d</strong></span></span></td>
<td><span data-ttu-id="8f95d-150">傾印訊息會被導向至檔案，而不是畫面。</span><span class="sxs-lookup"><span data-stu-id="8f95d-150">Dump messages are directed to a file instead of the screen.</span></span> <span data-ttu-id="8f95d-151">傾印訊息會描述區塊的內容。</span><span class="sxs-lookup"><span data-stu-id="8f95d-151">Dump messages describe the contents of the chunks.</span></span> <span data-ttu-id="8f95d-152">當詳細程度層級為3時，會傾印區塊結構。</span><span class="sxs-lookup"><span data-stu-id="8f95d-152">The chunk structure is dumped when the verbosity level is 3.</span></span> <span data-ttu-id="8f95d-153">傾印檔案名與輸入檔名稱相同，但副檔名為 dmp。</span><span class="sxs-lookup"><span data-stu-id="8f95d-153">The dump file name is the same as the input file name but with a .dmp extension.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f95d-154"><strong>/-l</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-154"><strong>/-l</strong></span></span></td>
<td><span data-ttu-id="8f95d-155">停用記錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-155">Disable logging.</span></span> <span data-ttu-id="8f95d-156">此旗標會覆寫 <code>/l</code> 參數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-156">This flag overrides the <code>/l</code> switch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f95d-157"><strong>/-d</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-157"><strong>/-d</strong></span></span></td>
<td><span data-ttu-id="8f95d-158">停用傾印。</span><span class="sxs-lookup"><span data-stu-id="8f95d-158">Disable dumping.</span></span> <span data-ttu-id="8f95d-159">此旗標會覆寫 <code>/d</code> 參數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-159">This flag overrides the <code>/d</code> switch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f95d-160"><strong>/v 整數</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-160"><strong>/v integer</strong></span></span></td>
<td><span data-ttu-id="8f95d-161">詳細等級。</span><span class="sxs-lookup"><span data-stu-id="8f95d-161">The verbosity level.</span></span> <span data-ttu-id="8f95d-162">預設值為 3。</span><span class="sxs-lookup"><span data-stu-id="8f95d-162">The default is 3.</span></span>
<ul>
<li><span data-ttu-id="8f95d-163">0-測試只會記錄有關特定 <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> 介面失敗的訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-163">0 - The test logs only messages concerning specific <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> interface failures.</span></span> <span data-ttu-id="8f95d-164">測試會傾印區塊內容。</span><span class="sxs-lookup"><span data-stu-id="8f95d-164">The test dumps the chunk contents.</span></span></li>
<li><span data-ttu-id="8f95d-165">1-測試會記錄警告訊息以及層級0的訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-165">1 - The test logs warning messages as well as those for level 0.</span></span></li>
<li><span data-ttu-id="8f95d-166">2-測試會記錄有關傳遞的測試和層級1的訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-166">2 - The test logs messages concerning tests that passed as well as those for level 1.</span></span></li>
<li><span data-ttu-id="8f95d-167">3-測試會記錄參考用訊息以及層級2的訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-167">3 - The test logs informational messages as well as those for level 2.</span></span> <span data-ttu-id="8f95d-168">此外，測試會傾印區塊的結構。</span><span class="sxs-lookup"><span data-stu-id="8f95d-168">In addition, the test dumps the structure of the chunk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f95d-169"><strong>/t 整數</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-169"><strong>/t integer</strong></span></span></td>
<td><span data-ttu-id="8f95d-170">要啟動的執行緒數目。</span><span class="sxs-lookup"><span data-stu-id="8f95d-170">The number of threads to launch.</span></span> <span data-ttu-id="8f95d-171">預設值是 1。</span><span class="sxs-lookup"><span data-stu-id="8f95d-171">The default is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f95d-172"><strong>/r 整數</strong>]</span><span class="sxs-lookup"><span data-stu-id="8f95d-172"><strong>/r integer</strong>]</span></span></td>
<td><span data-ttu-id="8f95d-173">以遞迴方式篩選子目錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-173">Recursively filters subdirectories.</span></span> <span data-ttu-id="8f95d-174">選擇性的整數參數會指定要對其執行遞迴的深度。</span><span class="sxs-lookup"><span data-stu-id="8f95d-174">The optional integer parameter specifies the depth to which to exercise recursion.</span></span> <span data-ttu-id="8f95d-175">如果未指定整數，或整數為0，則會假設為完整遞迴。</span><span class="sxs-lookup"><span data-stu-id="8f95d-175">If no integer is specified, or if the integer is 0, full recursion is assumed.</span></span> <span data-ttu-id="8f95d-176">根據預設，遞迴深度為1。</span><span class="sxs-lookup"><span data-stu-id="8f95d-176">By default, the recursion depth is 1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f95d-177"><strong>/c 整數</strong></span><span class="sxs-lookup"><span data-stu-id="8f95d-177"><strong>/c integer</strong></span></span></td>
<td><span data-ttu-id="8f95d-178">要迴圈的次數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-178">The number of times to loop.</span></span> <span data-ttu-id="8f95d-179">如果整數是0，則測試會無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="8f95d-179">If the integer is 0, the test loops infinitely.</span></span> <span data-ttu-id="8f95d-180">根據預設，測試只會迴圈一次。</span><span class="sxs-lookup"><span data-stu-id="8f95d-180">By default, the test loops only once.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]  
> <span data-ttu-id="8f95d-181">您必須在命令列參數與值之間加上空格。</span><span class="sxs-lookup"><span data-stu-id="8f95d-181">You must include a space between the command line switch and the value.</span></span>

### <a name="filtdumpexe"></a><span data-ttu-id="8f95d-182">filtdump.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-182">filtdump.exe</span></span>

<span data-ttu-id="8f95d-183">filtdump.exe 程式會載入指定檔的篩選處理常式，並列印 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 所產生的輸出。</span><span class="sxs-lookup"><span data-stu-id="8f95d-183">The filtdump.exe program loads a filter handler for a specified document and prints the output produced by the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL.</span></span> <span data-ttu-id="8f95d-184">下列範例說明如何叫用 filtdump.exe 程式。</span><span class="sxs-lookup"><span data-stu-id="8f95d-184">The following example illustrates how to invoke the filtdump.exe program.</span></span>

```
filtdump filename.ext
```
<span data-ttu-id="8f95d-185">Filtdump.exe 使用 [ILoadFilter：： LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) 方法載入適用于指定副檔名的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL，並列印結果。</span><span class="sxs-lookup"><span data-stu-id="8f95d-185">Filtdump.exe uses the [ILoadFilter::LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) method to load the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL appropriate for the specified file name extension and prints the results.</span></span> <span data-ttu-id="8f95d-186">例如，下列命令會指示 filtdump.exe 載入擴充功能的 smpfilt.dll 篩選處理常式、從 myfile.txt 檔案中解壓縮所有文字和屬性，然後列印結果。</span><span class="sxs-lookup"><span data-stu-id="8f95d-186">For example, the following command instructs filtdump.exe to load the smpfilt.dll filter handler for the extension .smp, extract all text and properties from the file myfile.smp, and print the results.</span></span>

```
filtdump myfile.smp
```

### <a name="filtregexe"></a><span data-ttu-id="8f95d-187">filtreg.exe</span><span class="sxs-lookup"><span data-stu-id="8f95d-187">filtreg.exe</span></span>

<span data-ttu-id="8f95d-188">filtreg.exe 程式會檢查登錄中的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 安裝資訊。</span><span class="sxs-lookup"><span data-stu-id="8f95d-188">The filtreg.exe program inspects [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) installation information in the registry.</span></span> <span data-ttu-id="8f95d-189">您可以藉由輸入命令列的名稱，從命令列叫用 filtreg.exe 程式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="8f95d-189">You invoke the filtreg.exe program from the command line by typing its name, as in the following example.</span></span>

```
filtreg
```

<span data-ttu-id="8f95d-190">Filtreg.exe 會針對延伸模組列印副檔名和 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL 的名稱，以列舉所有具有相關聯篩選器處理常式的副檔名。</span><span class="sxs-lookup"><span data-stu-id="8f95d-190">Filtreg.exe enumerates all file name extensions that have filter handlers associated with them by printing the file name extension and the name of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLL for the extension.</span></span> <span data-ttu-id="8f95d-191">這是驗證 **IFilter** 正確安裝的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="8f95d-191">This is a simple way to verify the correct installation of an **IFilter**.</span></span>

### <a name="ifilttstini"></a><span data-ttu-id="8f95d-192">ifilttst.ini</span><span class="sxs-lookup"><span data-stu-id="8f95d-192">ifilttst.ini</span></span>

<span data-ttu-id="8f95d-193">藉由呼叫 [**ifilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法來初始化 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面。</span><span class="sxs-lookup"><span data-stu-id="8f95d-193">An [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface is initialized by calling the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="8f95d-194">**IFilter：： Init** 方法會採用下列四個參數：</span><span class="sxs-lookup"><span data-stu-id="8f95d-194">The **IFilter::Init** method takes the following four parameters:</span></span>

1. <span data-ttu-id="8f95d-195">*grfFlags*</span><span class="sxs-lookup"><span data-stu-id="8f95d-195">*grfFlags*</span></span>
2. <span data-ttu-id="8f95d-196">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="8f95d-196">*cAttributes*</span></span>
3. <span data-ttu-id="8f95d-197">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="8f95d-197">*aAttributes*</span></span>
4. <span data-ttu-id="8f95d-198">*pdwFlags*</span><span class="sxs-lookup"><span data-stu-id="8f95d-198">*pdwFlags*</span></span>

<span data-ttu-id="8f95d-199">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)測試套件 ifilttst.exe 程式的使用者可以在稱為 ifilttst.ini 的檔案中指定這些參數的值。</span><span class="sxs-lookup"><span data-stu-id="8f95d-199">The user of the ifilttst.exe program of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) test suite can specify the values for these parameters in a file called ifilttst.ini.</span></span> <span data-ttu-id="8f95d-200">下表描述 ifilttst.ini 檔案中的專案，以指定) 輸入參數 (前三個參數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-200">The following table describes the entries in the ifilttst.ini file that specify the first three parameters(the input parameters).</span></span> <span data-ttu-id="8f95d-201">如需範例檔案，請參閱 [範例 ifilttst.ini](#sample-ifilttstini-file)檔。</span><span class="sxs-lookup"><span data-stu-id="8f95d-201">For a sample file, see [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span>

> [!NOTE]  
> <span data-ttu-id="8f95d-202">*PdwFlags* 參數沒有資料表專案，因為它是輸出參數。在呼叫 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法之前，不需要有任何特殊值。</span><span class="sxs-lookup"><span data-stu-id="8f95d-202">There is no table entry for the *pdwFlags* parameter because it is an output parameter; it does not need to have any special value prior to the call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

 | <span data-ttu-id="8f95d-203">進入</span><span class="sxs-lookup"><span data-stu-id="8f95d-203">Entry</span></span>         | <span data-ttu-id="8f95d-204">Description</span><span class="sxs-lookup"><span data-stu-id="8f95d-204">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f95d-205">Flags</span><span class="sxs-lookup"><span data-stu-id="8f95d-205">Flags</span></span>         | <span data-ttu-id="8f95d-206">要由 OR 運算子聯結的 [**ifilter \_ INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85))旗標名稱，以形成 [**ifilter：： INIT**](/windows/win32/api/filter/nf-filter-ifilter-init)方法的 *grfFlags* 參數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-206">The names of the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) flags that are to be joined by the OR operator to form the *grfFlags* parameter of the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span> <span data-ttu-id="8f95d-207">旗標名稱必須全部都是大寫，並且在同一行上。</span><span class="sxs-lookup"><span data-stu-id="8f95d-207">The flag names must all be uppercase, and on the same line.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="8f95d-208">*cAttributes*</span><span class="sxs-lookup"><span data-stu-id="8f95d-208">*cAttributes*</span></span> | <span data-ttu-id="8f95d-209">表示 *cAttributes* 參數值的十進位整數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-209">A decimal integer representing the value of the *cAttributes* parameter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="8f95d-210">*aAttributes*</span><span class="sxs-lookup"><span data-stu-id="8f95d-210">*aAttributes*</span></span> | <span data-ttu-id="8f95d-211">這個專案必須以 *aAttributes* 開頭，且必須與區段內的其他 *aAttributes* 專案不同。</span><span class="sxs-lookup"><span data-stu-id="8f95d-211">This entry must start with *aAttributes* and must be different from the other *aAttributes* entries within the section.</span></span> <span data-ttu-id="8f95d-212">*AAttributes* 專案的法定名稱如下： *aAttributes*、 *aAttributes1*、 *aAttributes2* 等等。</span><span class="sxs-lookup"><span data-stu-id="8f95d-212">Legal names for the *aAttributes* entry are: *aAttributes*, *aAttributes1*, *aAttributes2*, and so forth.</span></span> <span data-ttu-id="8f95d-213">第一個 token 必須是 GUID。</span><span class="sxs-lookup"><span data-stu-id="8f95d-213">The first token must be a GUID.</span></span> <span data-ttu-id="8f95d-214">GUID 的格式必須完全如同 `[Test3]` [範例 ifilttst.ini](#sample-ifilttstini-file)檔案一節中所述。</span><span class="sxs-lookup"><span data-stu-id="8f95d-214">The GUID must be formatted exactly as illustrated in the `[Test3]` section of the [Sample ifilttst.ini File](#sample-ifilttstini-file).</span></span> <span data-ttu-id="8f95d-215">第二個權杖可以是屬性識別碼 (PID) 由十六進位標記法中的數位組成，或 (lpwstr) 的寬字元字串指標。</span><span class="sxs-lookup"><span data-stu-id="8f95d-215">The second token can be either a property identifier (PID) consisting of a number in hexadecimal notation, or a pointer to a wide character string (lpwstr).</span></span> <span data-ttu-id="8f95d-216">您可以用雙引號括住字串來指定 lpwstr，如範例 ifilttst.ini 檔中的 `[Test6]` 一節所示。</span><span class="sxs-lookup"><span data-stu-id="8f95d-216">A lpwstr can be specified by enclosing the string in double quotes, as illustrated in the `[Test6]` section of the Sample ifilttst.ini File.</span></span> |

<span data-ttu-id="8f95d-217">如果未指定 Flags 和 *cAttributes* 專案，則會預設為0。</span><span class="sxs-lookup"><span data-stu-id="8f95d-217">If the Flags and *cAttributes* entries are not specified, they default to 0.</span></span> <span data-ttu-id="8f95d-218">如果您將 *cAttributes* 設定為等於2，您應該指定兩個 *aAttributes* 名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-218">If you set *cAttributes* equal to 2, you should specify two *aAttributes* names.</span></span> <span data-ttu-id="8f95d-219">在 `[Test5]` 範例的區段中， *cAttributes* 為1，但未指定 *aAttributes* 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-219">In the `[Test5]` section of the sample, *cAttributes* is 1, but no *aAttributes* have been specified.</span></span> <span data-ttu-id="8f95d-220">然後，測試會呼叫 *cAttributes* 等於1且 *aAttributes* 等於 **Null** 的 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)方法。</span><span class="sxs-lookup"><span data-stu-id="8f95d-220">The test then calls the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method with *cAttributes* equal to 1 and *aAttributes* equal to **NULL**.</span></span> <span data-ttu-id="8f95d-221">這是很有用的測試案例，因為它可能會導致 **IFilter：： Init** 方法發生存取違規。</span><span class="sxs-lookup"><span data-stu-id="8f95d-221">This is a useful test case because it is likely to cause an access violation in the **IFilter::Init** method.</span></span>

<span data-ttu-id="8f95d-222">如果 ifilttst.exe 在工作目錄中找不到名為 ifilttst.ini 的檔案，則會使用預設設定來初始化 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init) 物件。</span><span class="sxs-lookup"><span data-stu-id="8f95d-222">If ifilttst.exe cannot find a file named ifilttst.ini in the working directory, a default configuration is used to initialize the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) object.</span></span> <span data-ttu-id="8f95d-223">下列範例說明預設設定。</span><span class="sxs-lookup"><span data-stu-id="8f95d-223">The following example illustrates the default configuration.</span></span>

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a><span data-ttu-id="8f95d-224">範例 ifilttst.ini 檔案</span><span class="sxs-lookup"><span data-stu-id="8f95d-224">Sample ifilttst.ini File</span></span>

<span data-ttu-id="8f95d-225">ifilttst.ini 檔會組織成區段，並以方括弧括住區段名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-225">The ifilttst.ini file is organized in sections, with the section name enclosed in square brackets.</span></span> <span data-ttu-id="8f95d-226">在此範例中，區段的名稱為 `[Test1]` 、等等 `[Test2]` 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-226">In the example, the sections are named `[Test1]`, `[Test2]`, and so forth.</span></span> <span data-ttu-id="8f95d-227">所有區段名稱都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8f95d-227">All section names must be unique.</span></span> <span data-ttu-id="8f95d-228">測試會從第一個區段讀取值，並使用這些值來初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-228">The test reads the values from the first section and initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) with those values.</span></span> <span data-ttu-id="8f95d-229">然後使用此 **IFilter** 設定來執行所有測試。</span><span class="sxs-lookup"><span data-stu-id="8f95d-229">Then all the tests are run using this **IFilter** configuration.</span></span> <span data-ttu-id="8f95d-230">然後使用上述的參數釋出並重新初始化 **IFilter** 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-230">Then the **IFilter** is released and reinitialized, using parameters that are listed above.</span></span> <span data-ttu-id="8f95d-231">此程式會重複，直到所有設定都經過測試為止。</span><span class="sxs-lookup"><span data-stu-id="8f95d-231">The process is repeated until all configurations are tested.</span></span>

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a><span data-ttu-id="8f95d-232">IFilter 測試程式</span><span class="sxs-lookup"><span data-stu-id="8f95d-232">IFilter Test Procedure</span></span>

<span data-ttu-id="8f95d-233">在將 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 初始化之後，ifilttst.exe 程式會在 **ifilter** 上進行一系列的測試。</span><span class="sxs-lookup"><span data-stu-id="8f95d-233">After the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) has been initialized, the ifilttst.exe program conducts a series of tests on the **IFilter**.</span></span> <span data-ttu-id="8f95d-234">除了將 **ifilter** 測試程式進行之後，請確定您的 **IFilter** 實行採用安全的程式碼作法。</span><span class="sxs-lookup"><span data-stu-id="8f95d-234">In addition to following the **IFilter** test procedures, ensure that your **IFilter** implementation employs secure code practices.</span></span> <span data-ttu-id="8f95d-235">請參閱 [Windows Search 中執行篩選處理常式](-search-ifilter-constructing-filters.md)的「Windows Search 的安全程式碼實務」。</span><span class="sxs-lookup"><span data-stu-id="8f95d-235">See "Secure Code Practices for Windows Search" in [Implementing Filter Handlers in Windows Search](-search-ifilter-constructing-filters.md).</span></span>

### <a name="validation-test"></a><span data-ttu-id="8f95d-236">驗證測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-236">Validation Test</span></span>

<span data-ttu-id="8f95d-237">驗證測試會以一次一個區塊的物件為單位來檢查每個個別區塊和所有傳回碼。</span><span class="sxs-lookup"><span data-stu-id="8f95d-237">The validation test steps through the object one chunk at a time, verifying each individual chunk and all return codes.</span></span> <span data-ttu-id="8f95d-238">驗證測試會將所有傳回的 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk) 結構儲存在清單中。</span><span class="sxs-lookup"><span data-stu-id="8f95d-238">The validation test saves all returned [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structures in a list.</span></span>

<span data-ttu-id="8f95d-239">驗證測試會驗證下列條件：</span><span class="sxs-lookup"><span data-stu-id="8f95d-239">The validation test verifies the following conditions:</span></span>

- <span data-ttu-id="8f95d-240">[**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*idChunk* 區塊識別碼必須是唯一的，而且必須是遞增的。</span><span class="sxs-lookup"><span data-stu-id="8f95d-240">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunk* chunk IDs must be unique and increasing.</span></span>
- <span data-ttu-id="8f95d-241">[**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*旗標* 參數是可辨識的區塊狀態，例如 [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate)、區塊 \_ 文字或 CenabledHUNK \_ 值常數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-241">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*flags* parameter is a recognized chunk state, such as [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), CHUNK\_TEXT, or CenabledHUNK\_VALUE constants.</span></span>
- <span data-ttu-id="8f95d-242">[**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*breakType* 參數是可辨識的分隔類型 (0、1、2、3、4) 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-242">The [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*breakType* parameter is a recognized break type (0, 1, 2, 3, 4).</span></span>
- <span data-ttu-id="8f95d-243">如果 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 初始化屬性指定 **ifilter** 只傳回包含內部數值型別屬性的區塊，則 *idChunkSource* 必須等於0。</span><span class="sxs-lookup"><span data-stu-id="8f95d-243">If the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) initialization attributes specify that the **IFilter** should return only chunks containing internal value-type properties, then *idChunkSource* must equal 0.</span></span>
- <span data-ttu-id="8f95d-244">如果區塊不是衍生的，則為，如果它不是內部數值型別的屬性，則為 [**STAT \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)。*idChunkSource* 必須等於 **STAT \_ 區塊**。*idChunk*。</span><span class="sxs-lookup"><span data-stu-id="8f95d-244">If the chunk is not derived that is, if it is not an internal value-type property, then [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* must equal **STAT\_CHUNK**.*idChunk*.</span></span>
- <span data-ttu-id="8f95d-245">[**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回 \_ [確定] 或其他可接受的傳回值，例如 [篩選 \_ e \_ 區塊結尾] \_ 、[ \_ 篩選 \_ e \_ 連結 \_ 無法使用] 等等。</span><span class="sxs-lookup"><span data-stu-id="8f95d-245">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>
- <span data-ttu-id="8f95d-246">如果區塊包含文字，則 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 會傳回 S \_ OK、 \_ FILTER \_ LAST \_ text 或 filter \_ E \_ NO \_ \_ text。</span><span class="sxs-lookup"><span data-stu-id="8f95d-246">If the chunk contains text, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns S\_OK, FILTER\_S\_LAST\_TEXT, or FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="8f95d-247">如果 [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 傳回篩選 \_ 條件 \_ 的最後一個 \_ 文字，則下次對 **IFilter：： GetText** 的呼叫會傳回篩選 E，而不會傳回 \_ \_ 任何 \_ \_ 文字。</span><span class="sxs-lookup"><span data-stu-id="8f95d-247">If [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_S\_LAST\_TEXT, the next call to **IFilter::GetText** returns FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="8f95d-248">如果區塊包含值， [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 會傳回 S \_ OK 或 FILTER \_ E \_ NO \_ \_ VALUES。</span><span class="sxs-lookup"><span data-stu-id="8f95d-248">If the chunk contains a value, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns S\_OK or FILTER\_E\_NO\_MORE\_VALUES.</span></span>

### <a name="consistency-test"></a><span data-ttu-id="8f95d-249">一致性測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-249">Consistency Test</span></span>

<span data-ttu-id="8f95d-250">ifilttxt.exe 程式會使用與驗證測試中相同的參數來重新初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面，並執行一致性測試。</span><span class="sxs-lookup"><span data-stu-id="8f95d-250">The ifilttxt.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters as in the validation test and performs a consistency test.</span></span> <span data-ttu-id="8f95d-251">如果 **ifilter** 實作為以 [**ifilter \_ 初始**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85))ifilter \_ 初始 \_ 編制索引旗標初始化 \_ ，則測試會在對 [**ifilter：： INIT**](/windows/win32/api/filter/nf-filter-ifilter-init)方法進行另一次呼叫之前，先釋出 **ifilter** 介面並重新系結。</span><span class="sxs-lookup"><span data-stu-id="8f95d-251">If the **IFilter** implementation has been initialized with the [**IFILTER\_INIT**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFILTER\_INIT\_INDEXING\_ONLY flag, the test releases the **IFilter** interface and re-binds it before making another call to the [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init) method.</span></span>

<span data-ttu-id="8f95d-252">一致性測試會驗證下列條件：</span><span class="sxs-lookup"><span data-stu-id="8f95d-252">The consistency test verifies the following conditions:</span></span>

- <span data-ttu-id="8f95d-253">[**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)方法所傳回的每個 [**stat \_ 區塊**](/windows/win32/api/filter/ns-filter-stat_chunk)結構，與驗證測試中所傳回的對應 **STAT \_ 區塊** 相同。</span><span class="sxs-lookup"><span data-stu-id="8f95d-253">Each [**STAT\_CHUNK**](/windows/win32/api/filter/ns-filter-stat_chunk) structure returned by the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method is identical to the corresponding **STAT\_CHUNK** returned in the validation test.</span></span>
- <span data-ttu-id="8f95d-254">[**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 會傳回 \_ [確定] 或其他可接受的傳回值，例如 [篩選 \_ e \_ 區塊結尾] \_ 、[ \_ 篩選 \_ e \_ 連結 \_ 無法使用] 等等。</span><span class="sxs-lookup"><span data-stu-id="8f95d-254">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns S\_OK or other acceptable return value, such as FILTER\_E\_END\_OF\_CHUNKS, FILTER\_E\_LINK\_UNAVAILABLE, and so forth.</span></span>

### <a name="invalid-input-test"></a><span data-ttu-id="8f95d-255">不正確輸入測試</span><span class="sxs-lookup"><span data-stu-id="8f95d-255">Invalid Input Test</span></span>

<span data-ttu-id="8f95d-256">ifilttst.exe 程式會使用相同的參數重新初始化 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面，並執行不正確輸入測試。</span><span class="sxs-lookup"><span data-stu-id="8f95d-256">The ifilttst.exe program re-initializes the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface with the same parameters,and performs an invalid input test.</span></span> <span data-ttu-id="8f95d-257">這項測試會逐步解說檔的一個區塊，讓函式呼叫不正確，例如，當目前的 chuck 包含文字時呼叫 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 方法。</span><span class="sxs-lookup"><span data-stu-id="8f95d-257">This test steps through the document one chunk at a time making function calls incorrectly, such as calling the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method when the current chuck contains text.</span></span> <span data-ttu-id="8f95d-258">此測試會檢查所有傳回碼是否符合 **IFilter** 規格。</span><span class="sxs-lookup"><span data-stu-id="8f95d-258">The test checks all return codes for compliance with the **IFilter** specification.</span></span>

<span data-ttu-id="8f95d-259">不正確輸入測試會驗證下列條件：</span><span class="sxs-lookup"><span data-stu-id="8f95d-259">The invalid input test verifies the following conditions:</span></span>

- <span data-ttu-id="8f95d-260">如果目前的區塊包含文字， [**ifilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 會傳回篩選 \_ E \_ 沒有 \_ 值，且對 [**IFilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 的呼叫會成功。</span><span class="sxs-lookup"><span data-stu-id="8f95d-260">If the current chunk contains text, [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns FILTER\_E\_NO\_VALUES, and a call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) succeeds.</span></span>
- <span data-ttu-id="8f95d-261">如果目前的區塊包含值， [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 會傳回 FILTER \_ E \_ NO \_ TEXT，且對 [**IFilter：： GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 的呼叫會成功。</span><span class="sxs-lookup"><span data-stu-id="8f95d-261">If the current chunk contains a value, [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returns FILTER\_E\_NO\_TEXT, and a call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) succeeds.</span></span>
- <span data-ttu-id="8f95d-262">如果先前對 [**ifilter：： GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) 的呼叫傳回篩選 \_ E，則不會再傳回 \_ 任何 \_ \_ 文字，而對 **ifilter：： GetText** 的後續呼叫會傳回篩選 \_ e \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-262">If the previous call to [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) returned FILTER\_E\_NO\_MORE\_TEXT, successive calls to **IFilter::GetText** return FILTER\_E\_NO\_MORE\_TEXT.</span></span>
- <span data-ttu-id="8f95d-263">如果之前對 [**ifilter：： getvalue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) 的呼叫傳回篩選器 \_ e \_ 沒有 \_ 其他 \_ 值，則對 **ifilter：： getvalue** 的連續呼叫會傳回篩選 \_ e \_ 沒有 \_ 其他 \_ 值。</span><span class="sxs-lookup"><span data-stu-id="8f95d-263">If the previous call to [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returned FILTER\_E\_NO\_MORE\_VALUES, successive calls to **IFilter::GetValue** return FILTER\_E\_NO\_MORE\_VALUES.</span></span>
- <span data-ttu-id="8f95d-264">如果之前對 [**ifilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 的呼叫傳回篩選 \_ E \_ \_ 區塊結尾 \_ ，則連續呼叫 **ifilter：： GetChunk** 會傳回濾波器 \_ e \_ \_ 區塊結尾 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-264">If the previous call to [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returned FILTER\_E\_END\_OF\_CHUNKS, successive calls to **IFilter::GetChunk** return FILTER\_E\_END\_OF\_CHUNKS.</span></span>

> [!NOTE]  
> <span data-ttu-id="8f95d-265">不正確輸入測試會比較目前的區塊結構與驗證測試中傳回的結構，以確保它們完全相同。</span><span class="sxs-lookup"><span data-stu-id="8f95d-265">The invalid input test compares the current chunk structures to those returned in the validation test to make sure they are identical.</span></span>

### <a name="testing-different-ifilter-configurations"></a><span data-ttu-id="8f95d-266">測試不同的 IFilter 設定</span><span class="sxs-lookup"><span data-stu-id="8f95d-266">Testing Different IFilter Configurations</span></span>

<span data-ttu-id="8f95d-267">ifilttst.exe 程式會釋出 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面並重新系結，這次使用下一組參數將它初始化。</span><span class="sxs-lookup"><span data-stu-id="8f95d-267">The ifilttst.exe program releases the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface and rebinds, this time initializing it with the next set of parameters.</span></span> <span data-ttu-id="8f95d-268">測試會重複執行迴圈：驗證測試、一致性測試和不正確輸入測試，直到 [ifilttst.ini](#ifilttstini)檔案中指定的所有所需的 **IFilter** 設定都經過測試為止。</span><span class="sxs-lookup"><span data-stu-id="8f95d-268">The test repeats the cycle: validation test, consistency test, and invalid input test, until all the desired **IFilter** configurations specified in [ifilttst.ini](#ifilttstini) file have been tested.</span></span>

## <a name="ensuring-registered-items-get-indexed"></a><span data-ttu-id="8f95d-269">確定已註冊的專案已編制索引</span><span class="sxs-lookup"><span data-stu-id="8f95d-269">Ensuring Registered Items Get Indexed</span></span>

<span data-ttu-id="8f95d-270">您的 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 最終測試可確保您的 **ifilter** 已正確註冊，而且會叫用它來為您註冊用它的專案編制索引。</span><span class="sxs-lookup"><span data-stu-id="8f95d-270">The final test of your [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ensures that your **IFilter** is properly registered and that it is invoked to index the items that you registered to use it.</span></span> <span data-ttu-id="8f95d-271">您可以使用目錄管理員來起始重新建立索引，或使用編目範圍管理員 (CSM) 來設定預設規則，指出您想要讓索引子編目的 Url。</span><span class="sxs-lookup"><span data-stu-id="8f95d-271">You can use the Catalog Manager to initiate re-indexing, or use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl.</span></span> <span data-ttu-id="8f95d-272">完成索引之後，請使用 Windows Search UI 來搜尋專案內容或屬性中的字串。</span><span class="sxs-lookup"><span data-stu-id="8f95d-272">After indexing is complete, use the Windows Search UI to search for a string in the content or properties of items.</span></span> <span data-ttu-id="8f95d-273">如果專案已編制索引，這些專案會出現在搜尋結果中。</span><span class="sxs-lookup"><span data-stu-id="8f95d-273">If the items were indexed, they will appear in the search results.</span></span>

<span data-ttu-id="8f95d-274">如需重新編制索引的詳細資訊，請參閱 [使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md) 和 [使用編目範圍管理員](-search-3x-wds-extidx-csm.md)。</span><span class="sxs-lookup"><span data-stu-id="8f95d-274">For more information about re-indexing, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span> <span data-ttu-id="8f95d-275">ReindexMatchingUrls 程式碼範例會示範如何指定要重新建立索引的檔案和方法。</span><span class="sxs-lookup"><span data-stu-id="8f95d-275">The ReindexMatchingUrls code sample demonstrates ways to specify which files to re-index and how.</span></span> <span data-ttu-id="8f95d-276">CrawlScopeCommandLine 程式碼範例會示範如何定義編目範圍管理員 (CSM) 索引編制作業的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="8f95d-276">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span> <span data-ttu-id="8f95d-277">這兩個程式碼範例都可在 [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)上取得。</span><span class="sxs-lookup"><span data-stu-id="8f95d-277">Both code samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

### <a name="sample-log-file"></a><span data-ttu-id="8f95d-278">範例記錄檔</span><span class="sxs-lookup"><span data-stu-id="8f95d-278">Sample Log File</span></span>

<span data-ttu-id="8f95d-279">在要求時，Ifilttst.exe 程式可以產生記錄，其中包含執行期間所需步驟的描述。</span><span class="sxs-lookup"><span data-stu-id="8f95d-279">Upon request, the Ifilttst.exe program can produce a log containing a description of the steps it takes during execution.</span></span> <span data-ttu-id="8f95d-280">下列範例是記錄檔中的摘錄，其詳細資訊設定為最高的可能值3。</span><span class="sxs-lookup"><span data-stu-id="8f95d-280">The following examples are excerpts from a log file, with the verbosity set to the highest possible value 3.</span></span>

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

<span data-ttu-id="8f95d-281">第一行是告知性訊息，表示已從 ifilttst.ini 檔案載入新的設定。</span><span class="sxs-lookup"><span data-stu-id="8f95d-281">The first line is an informational message, indicating that a new configuration has been loaded from the ifilttst.ini file.</span></span> <span data-ttu-id="8f95d-282">第 (3 行) 表示已讀取目前設定之 ifilttst.ini 檔案中的區段名稱。</span><span class="sxs-lookup"><span data-stu-id="8f95d-282">Line (3) indicates the section name in the ifilttst.ini file from which the current configuration has been read.</span></span> <span data-ttu-id="8f95d-283">行 (4) 到 (7) 列出 [**IFilter：： Init**](/windows/win32/api/filter/nf-filter-ifilter-init)的參數。</span><span class="sxs-lookup"><span data-stu-id="8f95d-283">Lines (4) through (7) list the parameters to [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init).</span></span> <span data-ttu-id="8f95d-284">開頭的行 `INFO` 是關於 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 系結和驗證測試開頭的參考訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-284">The lines starting with `INFO` are informational messages about the binding of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and the start of the validation test.</span></span> <span data-ttu-id="8f95d-285">開頭的行 `PASS` 是關於已通過之特定測試的訊息。</span><span class="sxs-lookup"><span data-stu-id="8f95d-285">Lines starting with `PASS` are messages regarding specific tests that have passed.</span></span>

<span data-ttu-id="8f95d-286">下列記錄範例中的程式程式碼為警告。</span><span class="sxs-lookup"><span data-stu-id="8f95d-286">The line in the following log example is a warning.</span></span> <span data-ttu-id="8f95d-287">警告會注意到有問題的 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 行為（雖然合法）。</span><span class="sxs-lookup"><span data-stu-id="8f95d-287">Warnings call attention to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) behavior that is problematic, although legal.</span></span> <span data-ttu-id="8f95d-288">此警告表示 [**IFilter：： GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) 方法傳回的文字區塊不包含任何文字。</span><span class="sxs-lookup"><span data-stu-id="8f95d-288">This warning indicates that the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) method has returned a text chunk that contains no text.</span></span>

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

<span data-ttu-id="8f95d-289">下列範例錯誤訊息表示 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 發出未要求的區塊。</span><span class="sxs-lookup"><span data-stu-id="8f95d-289">The following example error message indicates that the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk that was not requested.</span></span>

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

<span data-ttu-id="8f95d-290">在此範例錯誤訊息的情況下， [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 發出了具有 PID 的區塊 `0x5` 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-290">In the case of this example error message, the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) emitted a chunk with a PID of `0x5`.</span></span> <span data-ttu-id="8f95d-291">檢查 `[Test1]` ifilttst.ini 中的區段會顯示已將 **IFilter** 設定為不使用此 PID 發出區塊。</span><span class="sxs-lookup"><span data-stu-id="8f95d-291">Inspection of section `[Test1]` in ifilttst.ini would show that the **IFilter** was configured to not emit chunks with this PID.</span></span> <span data-ttu-id="8f95d-292">例如，如果 IFILTER init 套用 \_ \_ \_ 索引屬性， \_ 或 Ifilter init 套用了 \_ \_ \_ \_ Flags 專案中指定的其他屬性，而如果 *CATTRIBUTES* 為0，則 **ifilter** 只會發出 pid 為的區塊， `0x13` 並對應至 pid \_ stg. \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="8f95d-292">For example, if neither IFILTER\_INIT\_APPLY\_INDEX\_ATTRIBUTES nor IFILTER\_INIT\_APPLY\_OTHER\_ATTRIBUTES were specified in the Flags entry and if *cAttributes* were 0, then **IFilter** would emit only chunks with a PID of `0x13` and corresponding to PID\_STG\_CONTENTS.</span></span>

### <a name="sample-dump-file"></a><span data-ttu-id="8f95d-293">範例傾印檔案</span><span class="sxs-lookup"><span data-stu-id="8f95d-293">Sample Dump File</span></span>

<span data-ttu-id="8f95d-294">在要求時，Ifilttst.exe 程式可能會產生一個傾印，其中包含所找到的區塊及其內容。</span><span class="sxs-lookup"><span data-stu-id="8f95d-294">Upon request, the Ifilttst.exe program can produce a dump containing the chunks it finds and their content.</span></span> <span data-ttu-id="8f95d-295">下列範例是這類傾印檔案的摘錄。</span><span class="sxs-lookup"><span data-stu-id="8f95d-295">The following example is an excerpt from such a dump file.</span></span>

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

<span data-ttu-id="8f95d-296">前九行描述目前的區塊結構。</span><span class="sxs-lookup"><span data-stu-id="8f95d-296">The first nine lines describe the current chunk structure.</span></span> <span data-ttu-id="8f95d-297">GUID 和 PID 對應于 PSGUID \_ STORAGE/PID \_ stg. \_ 內容。</span><span class="sxs-lookup"><span data-stu-id="8f95d-297">The GUID and the PID correspond to PSGUID\_STORAGE / PID\_STG\_CONTENTS.</span></span> <span data-ttu-id="8f95d-298">這是包含純文字的區塊。</span><span class="sxs-lookup"><span data-stu-id="8f95d-298">This is a chunk containing plain text.</span></span> <span data-ttu-id="8f95d-299">文字位於下列區塊結構中：</span><span class="sxs-lookup"><span data-stu-id="8f95d-299">The text is in the following chunk structure:</span></span>

```
10. This is an HTML IFilter test page
```

<span data-ttu-id="8f95d-300">下一個區塊（從第11行開始）有不同的 GUID，對應至與 `HTML IFilter` HTML HREF 對應的和不同的 PID。</span><span class="sxs-lookup"><span data-stu-id="8f95d-300">The next chunk, starting at line 11, has a different GUID, corresponding to the `HTML IFilter`, and a different PID, corresponding to an HTML HREF.</span></span> <span data-ttu-id="8f95d-301">這是由匯出的內部實值型別屬性 `HTML IFilter` 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-301">This is an internal value-type property, exported by the `HTML IFilter`.</span></span>

<span data-ttu-id="8f95d-302">下一個區塊（從第21行開始）有相同的 GUID 和 PID，但是它的區塊狀態是 `VALUE` 而非 `TEXT` 。</span><span class="sxs-lookup"><span data-stu-id="8f95d-302">The next chunk, starting at line 21, has the same GUID and PID, but its chunk state is `VALUE` instead of `TEXT`.</span></span> <span data-ttu-id="8f95d-303">請注意，最後兩個區塊中的文字與第一個區塊的文字相同。</span><span class="sxs-lookup"><span data-stu-id="8f95d-303">Note that the text in these last two chunks is the same as for the first chunk.</span></span> <span data-ttu-id="8f95d-304">但因為 [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) 是針對三個屬性所設計 (純文字、html href 做為文字，而 html href 作為值) 套用至這個片語，則會以三個不同的區塊來發出結果。</span><span class="sxs-lookup"><span data-stu-id="8f95d-304">But because the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is designed for three attributes (plain text, HTML HREF as text, and HTML HREF as a value) to be applied to this phrase, the results are emitted in three separate chunks.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f95d-305">其他資源</span><span class="sxs-lookup"><span data-stu-id="8f95d-305">Additional Resources</span></span>

- <span data-ttu-id="8f95d-306">[GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)上提供的 [IFilterSample](-search-sample-ifiltersample.md)程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter)介面的 ifilter 基礎類別。</span><span class="sxs-lookup"><span data-stu-id="8f95d-306">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="8f95d-307">如需索引編制程式的總覽，請參閱 [索引](-search-indexing-process-overview.md)程式。</span><span class="sxs-lookup"><span data-stu-id="8f95d-307">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="8f95d-308">如需檔案類型的總覽，請參閱 [檔案類型](../shell/fa-file-types.md)。</span><span class="sxs-lookup"><span data-stu-id="8f95d-308">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="8f95d-309">若要查詢檔案類型的檔案關聯屬性，請參閱 [PerceivedTypes、SystemFileAssociations 和應用程式註冊](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="8f95d-309">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f95d-310">相關主題</span><span class="sxs-lookup"><span data-stu-id="8f95d-310">Related topics</span></span>

[<span data-ttu-id="8f95d-311">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-311">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="8f95d-312">關於 Windows Search 中的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-312">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="8f95d-313">在 Windows Search 中建立篩選處理常式的最佳作法</span><span class="sxs-lookup"><span data-stu-id="8f95d-313">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="8f95d-314">從篩選處理常式傳回屬性</span><span class="sxs-lookup"><span data-stu-id="8f95d-314">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="8f95d-315">Windows 隨附的篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-315">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="8f95d-316">在 Windows Search 中執行篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-316">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="8f95d-317">註冊篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="8f95d-317">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
