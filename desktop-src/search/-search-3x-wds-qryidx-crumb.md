---
description: 連結引數支援完整的 Advanced Query 語法 (AQS) 語句，特別適用于控制搜尋範圍的方法。
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: '連結引數 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112480"
---
# <a name="crumb-argument-windows-search"></a><span data-ttu-id="f591d-103">連結引數 (Windows Search) </span><span class="sxs-lookup"><span data-stu-id="f591d-103">CRUMB Argument (Windows Search)</span></span>

<span data-ttu-id="f591d-104">`crumb`引數支援 (AQS) 語句的完整先進查詢語法，特別適用于控制搜尋範圍的方法。</span><span class="sxs-lookup"><span data-stu-id="f591d-104">The `crumb` argument supports full Advanced Query Syntax (AQS) statements and is especially useful as a means of controlling the scope of a search.</span></span> <span data-ttu-id="f591d-105">除了 AQS ements 之外， `crumb` 引數也可以 `location` 在 Windows Vista 上採用特殊參數， `kind` 並使用 `store` XP 上的參數，如本主題稍後所述。</span><span class="sxs-lookup"><span data-stu-id="f591d-105">In addition to AQS ements, the `crumb` argument can take a special `location` parameter on Windows Vista and `kind` and `store` parameters on XP, as described later in this topic.</span></span>

<span data-ttu-id="f591d-106">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="f591d-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f591d-107">連結語法</span><span class="sxs-lookup"><span data-stu-id="f591d-107">Crumb Syntax</span></span>](#crumb-syntax)
    -   [<span data-ttu-id="f591d-108">一般範例</span><span class="sxs-lookup"><span data-stu-id="f591d-108">General Examples</span></span>](#general-examples)
-   [<span data-ttu-id="f591d-109">使用連結搭配 Vista (位置) </span><span class="sxs-lookup"><span data-stu-id="f591d-109">Using crumb with Vista (location)</span></span>](#using-crumb-with-vista-location)
    -   [<span data-ttu-id="f591d-110">Vista 範例</span><span class="sxs-lookup"><span data-stu-id="f591d-110">Vista Examples</span></span>](#vista-examples)
    -   [<span data-ttu-id="f591d-111">一般資料夾的常數</span><span class="sxs-lookup"><span data-stu-id="f591d-111">Constants for Common Folders</span></span>](#constants-for-common-folders)
-   [<span data-ttu-id="f591d-112">使用連結搭配 Windows XP (種類和存放區) </span><span class="sxs-lookup"><span data-stu-id="f591d-112">Using crumb with Windows XP (kind and store)</span></span>](#using-crumb-with-windows-xp-kind-and-store)
    -   [<span data-ttu-id="f591d-113">XP 範例</span><span class="sxs-lookup"><span data-stu-id="f591d-113">XP Examples</span></span>](#xp-examples)
-   [<span data-ttu-id="f591d-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="f591d-114">Related topics</span></span>](#related-topics)

 

## <a name="crumb-syntax"></a><span data-ttu-id="f591d-115">連結語法</span><span class="sxs-lookup"><span data-stu-id="f591d-115">Crumb Syntax</span></span>

<span data-ttu-id="f591d-116">連結語法如下所示：</span><span class="sxs-lookup"><span data-stu-id="f591d-116">The crumb syntax is as follows:</span></span>


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



<span data-ttu-id="f591d-117"><column>部分是屬性系統中的任何屬性，而</span><span class="sxs-lookup"><span data-stu-id="f591d-117">The <column> portion is any property in the property system, and the</span></span> <value> <span data-ttu-id="f591d-118">部分是該屬性的有效值。</span><span class="sxs-lookup"><span data-stu-id="f591d-118">portion is a valid value for that property.</span></span> <span data-ttu-id="f591d-119"><label>部分是顯示為使用者介面提示之屬性的選擇性別名。</span><span class="sxs-lookup"><span data-stu-id="f591d-119">The <label> portion is an optional alias for the property that displays as a user interface hint.</span></span>

### <a name="general-examples"></a><span data-ttu-id="f591d-120">一般範例</span><span class="sxs-lookup"><span data-stu-id="f591d-120">General Examples</span></span>


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a><span data-ttu-id="f591d-121">使用連結搭配 Vista (位置) </span><span class="sxs-lookup"><span data-stu-id="f591d-121">Using crumb with Vista (location)</span></span>

<span data-ttu-id="f591d-122">在連結參數中，Windows Vista 支援完整 AQS 和 `location` 屬性，只有在 Windows vista 上才有提供特殊的執行功能。</span><span class="sxs-lookup"><span data-stu-id="f591d-122">In the crumb parameter, Windows Vista supports full AQS and also the `location` property, which has a special implementation available only on Windows Vista.</span></span> <span data-ttu-id="f591d-123">您可以在 `location` 單一連結參數中使用 AQS 字串或屬性，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="f591d-123">You can use either an AQS string or the `location` property within a single crumb parameter, but not both.</span></span> <span data-ttu-id="f591d-124">如果連結參數包含 AQS，則會忽略該連結參數中的其他專案。</span><span class="sxs-lookup"><span data-stu-id="f591d-124">If the crumb parameter includes AQS, everything else in that crumb parameter is ignored.</span></span>

<span data-ttu-id="f591d-125">`location`屬性可讓您指定要搜尋的路徑。</span><span class="sxs-lookup"><span data-stu-id="f591d-125">The `location` property enables you to specify a path to search.</span></span> <span data-ttu-id="f591d-126">如果位置是在索引子的編目範圍之外，Windows Vista 可以略過索引子並直接進行目錄。</span><span class="sxs-lookup"><span data-stu-id="f591d-126">Windows Vista can bypass the Indexer and traverse the directory directly if the location is outside the Indexer's crawl scope.</span></span> <span data-ttu-id="f591d-127">因此，這些搜尋可能會比使用索引子的搜尋更慢。</span><span class="sxs-lookup"><span data-stu-id="f591d-127">Consequently, these searches may be slower than searches that use the Indexer.</span></span>

<span data-ttu-id="f591d-128">當您指定 `location` 屬性時，支援兩個額外的參數和選擇性參數：</span><span class="sxs-lookup"><span data-stu-id="f591d-128">When you specify a `location` property, two additional parameters are supported and optional:</span></span>



| <span data-ttu-id="f591d-129">參數</span><span class="sxs-lookup"><span data-stu-id="f591d-129">Parameter</span></span> | <span data-ttu-id="f591d-130">值</span><span class="sxs-lookup"><span data-stu-id="f591d-130">Values</span></span>                  | <span data-ttu-id="f591d-131">描述</span><span class="sxs-lookup"><span data-stu-id="f591d-131">Description</span></span>                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f591d-132">包含</span><span class="sxs-lookup"><span data-stu-id="f591d-132">inclusion</span></span> | <span data-ttu-id="f591d-133">包含、排除</span><span class="sxs-lookup"><span data-stu-id="f591d-133">include, exclude</span></span>        | <span data-ttu-id="f591d-134">指定查詢是否應包含或排除該路徑的專案。</span><span class="sxs-lookup"><span data-stu-id="f591d-134">Specifies whether the query should include or exclude items from that path.</span></span> <span data-ttu-id="f591d-135">"Include" 是預設值。</span><span class="sxs-lookup"><span data-stu-id="f591d-135">"Include" is the default.</span></span> <span data-ttu-id="f591d-136">Windows Vista 不支援排除專案，不含任何專案。</span><span class="sxs-lookup"><span data-stu-id="f591d-136">Windows Vista does not support exclusions without inclusions.</span></span> <span data-ttu-id="f591d-137"> (請參閱範例) </span><span class="sxs-lookup"><span data-stu-id="f591d-137">(See example)</span></span> |
| <span data-ttu-id="f591d-138">遞迴</span><span class="sxs-lookup"><span data-stu-id="f591d-138">recursion</span></span> | <span data-ttu-id="f591d-139">遞迴、非遞迴</span><span class="sxs-lookup"><span data-stu-id="f591d-139">recursive, nonrecursive</span></span> | <span data-ttu-id="f591d-140">指定搜尋是否應從位置中定義的值開始遞迴所有子資料夾：</span><span class="sxs-lookup"><span data-stu-id="f591d-140">Specifies whether the search should recurse all subfolders starting from the value defined in the location:</span></span><value><span data-ttu-id="f591d-141">.</span><span class="sxs-lookup"><span data-stu-id="f591d-141">.</span></span> <span data-ttu-id="f591d-142">「遞迴」是預設值。</span><span class="sxs-lookup"><span data-stu-id="f591d-142">"Recursive" is the default.</span></span>                             |



 

<span data-ttu-id="f591d-143">若要使用 search-ms： protocol 設定搜尋範圍，您有不同的選項，視範圍的目標而定。</span><span class="sxs-lookup"><span data-stu-id="f591d-143">To scope a search using the search-ms: protocol, you have different options depending on the target of the scope.</span></span>

<span data-ttu-id="f591d-144">本機電腦上的資料夾：</span><span class="sxs-lookup"><span data-stu-id="f591d-144">Folder on a local machine:</span></span>

-   <span data-ttu-id="f591d-145">使用 AQS (連結 = folder： <URL 編碼路徑>) </span><span class="sxs-lookup"><span data-stu-id="f591d-145">Use AQS (crumb=folder:<URL-encoded path>)</span></span>
-   <span data-ttu-id="f591d-146">使用位置引數 (連結 = location： <URL 編碼路徑>) </span><span class="sxs-lookup"><span data-stu-id="f591d-146">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="f591d-147">遠端電腦/網路上的資料夾：</span><span class="sxs-lookup"><span data-stu-id="f591d-147">Folder on a remote machine/network:</span></span>

-   <span data-ttu-id="f591d-148">使用位置引數 (連結 = location： <URL 編碼路徑>) </span><span class="sxs-lookup"><span data-stu-id="f591d-148">Use location argument (crumb=location:<URL-encoded path>)</span></span>

<span data-ttu-id="f591d-149">經由已知 UNC 通訊協定處理常式存取的資料夾：</span><span class="sxs-lookup"><span data-stu-id="f591d-149">Folder accessed via a known UNC protocol handler:</span></span>

-   <span data-ttu-id="f591d-150">使用 AQS (連結 = store： <UNC protocol handler name>) </span><span class="sxs-lookup"><span data-stu-id="f591d-150">Use AQS (crumb=store:<UNC protocol handler name>)</span></span>
-   <span data-ttu-id="f591d-151">使用位置引數 (連結 = location： <URL 編碼路徑>) </span><span class="sxs-lookup"><span data-stu-id="f591d-151">Use location argument (crumb=location:<URL-encoded path>)</span></span>

### <a name="vista-examples"></a><span data-ttu-id="f591d-152">Vista 範例</span><span class="sxs-lookup"><span data-stu-id="f591d-152">Vista Examples</span></span>


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



<span data-ttu-id="f591d-153">第一個範例會從 shell://Personal 位置開始搜尋「休假」 (使用者的我的檔資料夾) 的特殊快捷方式，包括該資料夾和所有子資料夾。</span><span class="sxs-lookup"><span data-stu-id="f591d-153">The first example executes a search for "vacation" starting at the shell://Personal location (a special shortcut to the user's My Documents folder), including that folder and all subfolders.</span></span> <span data-ttu-id="f591d-154">請參閱下表。</span><span class="sxs-lookup"><span data-stu-id="f591d-154">See table below.</span></span>

<span data-ttu-id="f591d-155">第二個範例會在 C： pictures 內執行搜尋 \\ ，但無法在 c： \\ pictures \\ 重複。</span><span class="sxs-lookup"><span data-stu-id="f591d-155">The second example executes a search within C:\\Pictures, but not in C:\\Pictures\\Duplicates.</span></span>

<span data-ttu-id="f591d-156">第三個範例會在 C：檔內執行搜尋 \\ ，其限制為 [kind] 屬性設定為 [圖片] 的檔案。</span><span class="sxs-lookup"><span data-stu-id="f591d-156">The third example executes a search within C:\\Documents, limited to files with the kind property set to pics.</span></span>

### <a name="constants-for-common-folders"></a><span data-ttu-id="f591d-157">一般資料夾的常數</span><span class="sxs-lookup"><span data-stu-id="f591d-157">Constants for Common Folders</span></span>

<span data-ttu-id="f591d-158">Windows Vista 可讓您使用 [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) 值，以提供獨特的系統獨立方式來識別應用程式經常使用的特殊資料夾，但在任何指定的系統上可能不會有相同的名稱或位置。</span><span class="sxs-lookup"><span data-stu-id="f591d-158">Windows Vista enables the use of [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) values that provide a unique system-independent way to identify special folders used frequently by applications, but which may not have the same name or location on any given system.</span></span> <span data-ttu-id="f591d-159">例如，系統資料夾在一個系統上可能是 "C： \\ Windows"，另一個則為 "c： \\ Winnt"。</span><span class="sxs-lookup"><span data-stu-id="f591d-159">For example, the system folder may be "C:\\Windows" on one system and "C:\\Winnt" on another.</span></span> <span data-ttu-id="f591d-160">在 Windows Vista 之前，使用 [CSIDLs](/windows/desktop/shell/csidl) 。</span><span class="sxs-lookup"><span data-stu-id="f591d-160">Prior to Windows Vista, [CSIDLs](/windows/desktop/shell/csidl) were used.</span></span>

<span data-ttu-id="f591d-161">使用下列語法來使用這些位置：</span><span class="sxs-lookup"><span data-stu-id="f591d-161">Use these locations with this syntax:</span></span>


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a><span data-ttu-id="f591d-162">使用連結搭配 Windows XP (種類和存放區) </span><span class="sxs-lookup"><span data-stu-id="f591d-162">Using crumb with Windows XP (kind and store)</span></span>

<span data-ttu-id="f591d-163">針對 Windows XP (WDS 3.x) 上的 Windows Search，AQS 條款「kind」和「store」具有特殊的實作為。</span><span class="sxs-lookup"><span data-stu-id="f591d-163">For Windows Search on Windows XP (WDS 3.x), the AQS terms "kind" and "store" have a special implementation.</span></span> <span data-ttu-id="f591d-164">「種類」值與 [WDS 2.x 中使用的值](../lwef/-search-2x-wds-perceivedtype.md)相同。</span><span class="sxs-lookup"><span data-stu-id="f591d-164">The "kind" values are the same [values used in WDS 2.x](../lwef/-search-2x-wds-perceivedtype.md).</span></span> <span data-ttu-id="f591d-165">"Store" 值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="f591d-165">The "store" values include the following:</span></span>

-   <span data-ttu-id="f591d-166">Mapi</span><span class="sxs-lookup"><span data-stu-id="f591d-166">mapi</span></span>
-   <span data-ttu-id="f591d-167">file</span><span class="sxs-lookup"><span data-stu-id="f591d-167">file</span></span>
-   <span data-ttu-id="f591d-168">outlookexpress</span><span class="sxs-lookup"><span data-stu-id="f591d-168">outlookexpress</span></span>
-   <span data-ttu-id="f591d-169">任意</span><span class="sxs-lookup"><span data-stu-id="f591d-169">any</span></span>

### <a name="xp-examples"></a><span data-ttu-id="f591d-170">XP 範例</span><span class="sxs-lookup"><span data-stu-id="f591d-170">XP Examples</span></span>


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



<span data-ttu-id="f591d-171">第一個範例會從 John 傳回具有自訂標籤 "OE Mail" 的 Microsoft Outlook Express 電子郵件。</span><span class="sxs-lookup"><span data-stu-id="f591d-171">The first example returns Microsoft Outlook Express emails from John with the custom label, "OE Mail".</span></span> <span data-ttu-id="f591d-172">第二個範例會執行搜尋來自 John 的任何通訊。</span><span class="sxs-lookup"><span data-stu-id="f591d-172">The second example executes a search for any communication from John.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f591d-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="f591d-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f591d-174">具有 Parameter-Value 引數的開始使用</span><span class="sxs-lookup"><span data-stu-id="f591d-174">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="f591d-175">地區設定識別碼引數</span><span class="sxs-lookup"><span data-stu-id="f591d-175">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="f591d-176">語法引數</span><span class="sxs-lookup"><span data-stu-id="f591d-176">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="f591d-177">STACKEDBY 引數</span><span class="sxs-lookup"><span data-stu-id="f591d-177">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="f591d-178">子查詢引數</span><span class="sxs-lookup"><span data-stu-id="f591d-178">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
