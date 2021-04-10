---
title: 從命令列呼叫 WDS
description: 您可以使用 windowssearch.exe 命令列語法，從另一個應用程式或使用瀏覽器協助程式物件的網頁，啟動 Microsoft Windows 桌面搜尋 (WDS) 使用者介面， (BHO) 。
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/19/2020
ms.locfileid: "103681537"
---
# <a name="calling-wds-from-the-command-line"></a><span data-ttu-id="89cc5-103">從命令列呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="89cc5-103">Calling WDS from the Command Line</span></span>

> [!NOTE]
> <span data-ttu-id="89cc5-104">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="89cc5-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="89cc5-105">在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="89cc5-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="89cc5-106">您可以使用 windowssearch.exe 命令列語法，從另一個應用程式或使用瀏覽器協助程式物件的網頁，啟動 Microsoft Windows 桌面搜尋 (WDS) 使用者介面， (BHO) 。</span><span class="sxs-lookup"><span data-stu-id="89cc5-106">You can launch the Microsoft Windows Desktop Search (WDS) user interface with a specific filter, store, and query from another application or a webpage that uses the Browser Helper Object (BHO) by using the windowssearch.exe command line syntax.</span></span> <span data-ttu-id="89cc5-107">從命令列呼叫 WDS 時，不會將使用者在 WDS 視窗中的動作或選取專案的相關資訊傳回給呼叫的應用程式或網頁。</span><span class="sxs-lookup"><span data-stu-id="89cc5-107">When calling WDS from the command line, no information about the user's actions or selection in the WDS window is returned to the calling application or webpage.</span></span>

<span data-ttu-id="89cc5-108">WDS 安裝路徑是在 InstallDir 登錄設定的 [ \\ \\ Microsoft Windows 桌面搜尋 HKEY_LOCAL_MACHINE 軟體] 下指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="89cc5-108">The WDS installation path is specified in the InstallDir registry setting under HKEY_LOCAL_MACHINE\\Software\\Microsoft\\Windows Desktop Search.</span></span> <span data-ttu-id="89cc5-109">安裝 windowssearch.exe 的預設路徑是 [Program Files] \\ Windows Desktop Search。</span><span class="sxs-lookup"><span data-stu-id="89cc5-109">The default path that windowssearch.exe is installed to is Program Files\\Windows Desktop Search.</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="89cc5-110">命令列語法</span><span class="sxs-lookup"><span data-stu-id="89cc5-110">Command Line Syntax</span></span>

<span data-ttu-id="89cc5-111">下列語法適用于 Windows Desktop Search 2.x 命令列介面。</span><span class="sxs-lookup"><span data-stu-id="89cc5-111">The following syntax applies to the Windows Desktop Search 2.x command-line interface.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89cc5-112">選項</span><span class="sxs-lookup"><span data-stu-id="89cc5-112">Options</span></span></th>
<th><span data-ttu-id="89cc5-113">參數</span><span class="sxs-lookup"><span data-stu-id="89cc5-113">Parameter</span></span></th>
<th><span data-ttu-id="89cc5-114">意義</span><span class="sxs-lookup"><span data-stu-id="89cc5-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89cc5-115">/startup</span><span class="sxs-lookup"><span data-stu-id="89cc5-115">/startup</span></span></td>

<td><span data-ttu-id="89cc5-116">初始化 Windows 桌面搜尋</span><span class="sxs-lookup"><span data-stu-id="89cc5-116">Initializes Windows Desktop Search</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89cc5-117">/indexnow</span><span class="sxs-lookup"><span data-stu-id="89cc5-117">/indexnow</span></span></td>

<td><span data-ttu-id="89cc5-118">關閉編制索引的功能，並重新掃描所有索引位置</span><span class="sxs-lookup"><span data-stu-id="89cc5-118">Turns off indexing back-off and rescans all index locations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89cc5-119">/showstatus</span><span class="sxs-lookup"><span data-stu-id="89cc5-119">/showstatus</span></span></td>

<td><span data-ttu-id="89cc5-120">顯示索引狀態視窗</span><span class="sxs-lookup"><span data-stu-id="89cc5-120">Shows the indexing status window</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89cc5-121">/launchsearchwindow 或/url</span><span class="sxs-lookup"><span data-stu-id="89cc5-121">/launchsearchwindow or /url</span></span></td>

<td><span data-ttu-id="89cc5-122">使用空的查詢來開啟 WDS 視窗</span><span class="sxs-lookup"><span data-stu-id="89cc5-122">Opens a WDS window with an empty query</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89cc5-123">/url</span><span class="sxs-lookup"><span data-stu-id="89cc5-123">/url</span></span></td>
<td><span data-ttu-id="89cc5-124">搜尋： [store | show | query] 查詢字串</span><span class="sxs-lookup"><span data-stu-id="89cc5-124">search:[store|show|query] query string</span></span></td>
<td><span data-ttu-id="89cc5-125">使用查詢開啟 WDS 視窗，並根據下列參數進行篩選：</span><span class="sxs-lookup"><span data-stu-id="89cc5-125">Opens a WDS window with a query and filter based on the following parameters:</span></span>
<ul>
<li><p><span data-ttu-id="89cc5-126">store-指定要查詢的資料來源： files、outlook、outlookexpress。</span><span class="sxs-lookup"><span data-stu-id="89cc5-126">store - Specifies the data source to query: files, outlook, outlookexpress.</span></span> <span data-ttu-id="89cc5-127">如果未指定，則會搜尋所有存放區。</span><span class="sxs-lookup"><span data-stu-id="89cc5-127">If not specified all stores will be searched.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="89cc5-128">雖然 Advanced Query 語法支援將 Microsoft Outlook 參考為 ' oe '，但是命令列上的 store 參數必須是 ' outlookexpress '。</span><span class="sxs-lookup"><span data-stu-id="89cc5-128">While Advanced Query Syntax supports referencing Microsoft Outlook as 'oe', the store parameter on the command line must be 'outlookexpress'.</span></span>
</blockquote>
<p><br/></p></li>
<li><p><span data-ttu-id="89cc5-129">顯示-指定要傳回的已知結果類型。</span><span class="sxs-lookup"><span data-stu-id="89cc5-129">show - Specifies which perceived type of results to return.</span></span> <span data-ttu-id="89cc5-130">如需完整的類型清單，請參閱 <a href="-search-2x-wds-perceivedtype.md">認知</a> 型別。</span><span class="sxs-lookup"><span data-stu-id="89cc5-130">See <a href="-search-2x-wds-perceivedtype.md">Perceived Types</a> for a complete list of types.</span></span> <span data-ttu-id="89cc5-131">如果未指定，則會傳回所有類型。</span><span class="sxs-lookup"><span data-stu-id="89cc5-131">If not specified, all types will be returned.</span></span> <br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="89cc5-132">認知的型別值和顯示的值之間有三項差異。</span><span class="sxs-lookup"><span data-stu-id="89cc5-132">There are three differences between the perceived type values and the values for show.</span></span> <span data-ttu-id="89cc5-133">若是 <code>show</code> ，請使用 ' documents '，而非 ' doc '、' pictures ' 而非 ' pictures ' 和 ' textdocuments '，而非 ' text '。</span><span class="sxs-lookup"><span data-stu-id="89cc5-133">For <code>show</code>, use 'documents' instead of 'doc', 'pictures' instead of 'pics', and 'textdocuments' instead of 'text'.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="89cc5-134">查詢-指定搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="89cc5-134">query - Specifies the search criteria.</span></span> <span data-ttu-id="89cc5-135">此值支援 <a href="-search-2x-wds-aqsreference.md">Advanced Query 語法</a> 參數來精簡結果。</span><span class="sxs-lookup"><span data-stu-id="89cc5-135">This value supports <a href="-search-2x-wds-aqsreference.md">Advanced Query Syntax</a> parameters to refine the results.</span></span> <span data-ttu-id="89cc5-136">查詢參數必須是 URL 中的最後一個參數。</span><span class="sxs-lookup"><span data-stu-id="89cc5-136">The query parameter must be the last parameter in the URL.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a><span data-ttu-id="89cc5-137">範例</span><span class="sxs-lookup"><span data-stu-id="89cc5-137">Example</span></span>

<span data-ttu-id="89cc5-138">例如，若要搜尋所有符合「背景圖樣」準則的檔案，請使用下列命令：</span><span class="sxs-lookup"><span data-stu-id="89cc5-138">For example, to search all files for pictures matching the criteria 'wallpaper' use the following command:</span></span>

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a><span data-ttu-id="89cc5-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="89cc5-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89cc5-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="89cc5-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89cc5-141">進階查詢語法</span><span class="sxs-lookup"><span data-stu-id="89cc5-141">Advanced Query Syntax</span></span>](-search-2x-wds-aqsreference.md)
</dt> <dt>

[<span data-ttu-id="89cc5-142">認知類型</span><span class="sxs-lookup"><span data-stu-id="89cc5-142">Perceived Types</span></span>](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[<span data-ttu-id="89cc5-143">從 Web Pages 呼叫 WDS</span><span class="sxs-lookup"><span data-stu-id="89cc5-143">Calling WDS from Web Pages</span></span>](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





