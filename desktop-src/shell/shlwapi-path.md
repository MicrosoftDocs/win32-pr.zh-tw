---
description: 本節說明 Windows Shell 路徑處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。
title: Shell 路徑處理函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991759"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="073ef-104">Shell 路徑處理函式</span><span class="sxs-lookup"><span data-stu-id="073ef-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="073ef-105">本節說明 Windows Shell 路徑處理函式。</span><span class="sxs-lookup"><span data-stu-id="073ef-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="073ef-106">本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。</span><span class="sxs-lookup"><span data-stu-id="073ef-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="073ef-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="073ef-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="073ef-108">主題</span><span class="sxs-lookup"><span data-stu-id="073ef-108">Topic</span></span></th>
<th><span data-ttu-id="073ef-109">描述</span><span class="sxs-lookup"><span data-stu-id="073ef-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="073ef-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackslash 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-111">在字串的結尾加上反斜線，以建立路徑的正確語法。</span><span class="sxs-lookup"><span data-stu-id="073ef-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="073ef-112">如果來源路徑已經有尾端反斜線，則不會新增反斜線。</span><span class="sxs-lookup"><span data-stu-id="073ef-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-113">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-114">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-116">將副檔名新增至路徑字串。</span><span class="sxs-lookup"><span data-stu-id="073ef-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-117">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-118">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>Pathappend 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-120">將一個路徑附加至另一個路徑的結尾。</span><span class="sxs-lookup"><span data-stu-id="073ef-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-121">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-122">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-124">從指定的磁片磁碟機編號建立根路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-126">藉由移除導覽元素（例如 &quot; . &quot; 和.）來簡化路徑 &quot; &quot; ，以產生直接、格式正確的路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-128">將表示正確格式路徑的兩個字串串連成一個路徑;也會串連任何相對路徑元素。</span><span class="sxs-lookup"><span data-stu-id="073ef-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-129">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-130">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-132">比較兩個路徑，以判斷它們是否共用一般前置詞。</span><span class="sxs-lookup"><span data-stu-id="073ef-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="073ef-133">前置詞是下列其中一種類型： &quot; C： \\ &quot; 、 &quot; ... &quot; &quot; &quot; &quot; \\ &quot; .。。</span><span class="sxs-lookup"><span data-stu-id="073ef-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-135">將路徑元件取代為省略號，以截斷檔案路徑以符合給定的圖元寬度。</span><span class="sxs-lookup"><span data-stu-id="073ef-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-137">藉由以省略號取代路徑元件，截斷路徑以容納在特定數目的字元內。</span><span class="sxs-lookup"><span data-stu-id="073ef-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-139">將檔案 URL 轉換成 Microsoft MS-DOS 路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-141">從檔案 URL 建立路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfileexists 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-143">判斷檔案系統物件（例如檔案或資料夾）的路徑是否有效。</span><span class="sxs-lookup"><span data-stu-id="073ef-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-145">搜尋延伸模組的路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-147">搜尋路徑中的檔案名。</span><span class="sxs-lookup"><span data-stu-id="073ef-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-149">剖析路徑，並傳回路徑中第一個反斜線之後的部分。</span><span class="sxs-lookup"><span data-stu-id="073ef-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-151">搜尋檔案。</span><span class="sxs-lookup"><span data-stu-id="073ef-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-153">判斷指定的檔案名是否包含其中一個尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="073ef-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-155">在指定的路徑中尋找命令列引數。</span><span class="sxs-lookup"><span data-stu-id="073ef-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-157">決定與路徑相關的字元類型。</span><span class="sxs-lookup"><span data-stu-id="073ef-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumber 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-159">在路徑中搜尋 ' A ' 到 ' Z ' 範圍內的磁碟機號，並傳回對應的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="073ef-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-161">判斷檔案的已註冊內容類型是否符合指定的內容類型。</span><span class="sxs-lookup"><span data-stu-id="073ef-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="073ef-162">此函式會取得指定之檔案類型的內容類型，並將該字串與 <em>pszContentType</em>比較。</span><span class="sxs-lookup"><span data-stu-id="073ef-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="073ef-163">這項比較不會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="073ef-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-165">確認路徑是否為有效的目錄。</span><span class="sxs-lookup"><span data-stu-id="073ef-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-167">判斷指定的路徑是否為空的目錄。</span><span class="sxs-lookup"><span data-stu-id="073ef-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-169">搜尋路徑中任何路徑分隔字元 (例如 '： ' 或 ' \' ) 。</span><span class="sxs-lookup"><span data-stu-id="073ef-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="073ef-170">如果沒有任何路徑分隔字元，則會將路徑視為檔案規格路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-172">判斷檔案是否為 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="073ef-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="073ef-173">這會根據為檔案副檔名所註冊的內容類型來決定。</span><span class="sxs-lookup"><span data-stu-id="073ef-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-175">判斷檔案名的格式是否完整。</span><span class="sxs-lookup"><span data-stu-id="073ef-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-177">判斷路徑字串是否代表網路資源。</span><span class="sxs-lookup"><span data-stu-id="073ef-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>Pathisprefix 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-179">搜尋路徑以判斷它是否包含 <em>pszPrefix</em>所傳遞之類型的有效前置詞。</span><span class="sxs-lookup"><span data-stu-id="073ef-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="073ef-180">前置詞是下列其中一種類型： &quot; C： \\ &quot; 、 &quot; ... &quot; &quot; &quot; &quot; \\ &quot; .。。</span><span class="sxs-lookup"><span data-stu-id="073ef-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>Pathisrelative 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-182">搜尋路徑並判斷其是否為相對。</span><span class="sxs-lookup"><span data-stu-id="073ef-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-184">判斷路徑字串是否參考磁片區的根目錄。</span><span class="sxs-lookup"><span data-stu-id="073ef-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>Pathissameroot 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-186">比較兩個路徑，判斷它們是否有共同的根元件。</span><span class="sxs-lookup"><span data-stu-id="073ef-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-188">判斷現有的資料夾是否包含將其設為系統資料夾的屬性。</span><span class="sxs-lookup"><span data-stu-id="073ef-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="073ef-189">或者，此函式會指出特定的屬性是否將資料夾限定為系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="073ef-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>Pathisunc 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-191">判斷路徑字串是否為有效的通用命名慣例 (UNC) 路徑，而不是根據磁碟機號的路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-193">判斷字串是否為伺服器路徑的有效 UNC。</span><span class="sxs-lookup"><span data-stu-id="073ef-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-195">判斷字串是否為有效的 UNC 共用路徑，也就是 \\ <em>伺服器</em> \ <em>共用</em>。</span><span class="sxs-lookup"><span data-stu-id="073ef-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-197">測試指定的字串，以判斷它是否符合有效的 URL 格式。</span><span class="sxs-lookup"><span data-stu-id="073ef-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-199">將全部大寫的路徑轉換成所有小寫字元，以提供路徑一致的外觀。</span><span class="sxs-lookup"><span data-stu-id="073ef-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-201">為現有的資料夾提供適當的屬性，使其成為系統資料夾。</span><span class="sxs-lookup"><span data-stu-id="073ef-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>Pathmatchspec 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-203">使用 MS-DOS 萬用字元相符類型來搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="073ef-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-205">比對一或多個檔案名模式的檔案名與路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-207">剖析包含檔案位置和圖示索引的檔案位置字串，並傳回不同的值。</span><span class="sxs-lookup"><span data-stu-id="073ef-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-209">搜尋空格的路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-209">Searches a path for spaces.</span></span> <span data-ttu-id="073ef-210">如果找到空格，則整個路徑會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="073ef-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>Pathrelativepathto 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-212">建立從一個檔案或資料夾到另一個檔案或資料夾的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="073ef-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>Pathremoveargs 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-214">從指定的路徑移除任何引數。</span><span class="sxs-lookup"><span data-stu-id="073ef-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>Pathremovebackslash 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-216">從指定的路徑移除尾端的反斜線。</span><span class="sxs-lookup"><span data-stu-id="073ef-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-217">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="073ef-217">This function is deprecated.</span></span> <span data-ttu-id="073ef-218">建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>Pathremoveblanks 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-220">從字串中移除所有開頭和尾端空格。</span><span class="sxs-lookup"><span data-stu-id="073ef-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>Pathremoveextension 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-222">移除路徑中的副檔名（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="073ef-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-223">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="073ef-223">This function is deprecated.</span></span> <span data-ttu-id="073ef-224">建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="073ef-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>Pathremovefilespec 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-226">從路徑移除尾端的檔案名和反斜線（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="073ef-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-227">這個函數已被取代。</span><span class="sxs-lookup"><span data-stu-id="073ef-227">This function is deprecated.</span></span> <span data-ttu-id="073ef-228">我們建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> 函式。</span><span class="sxs-lookup"><span data-stu-id="073ef-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-230">以新的副檔名取代檔案名的副檔名。</span><span class="sxs-lookup"><span data-stu-id="073ef-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="073ef-231">如果檔案名不包含副檔名，則會將副檔名附加至字串的結尾。</span><span class="sxs-lookup"><span data-stu-id="073ef-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-232">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-233">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-235">判斷指定路徑的格式是否正確且完整。</span><span class="sxs-lookup"><span data-stu-id="073ef-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-237">使用 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>pathcompactpath 式</strong></a> ，在視窗或對話方塊中設定子控制項的文字，以確保該路徑符合控制項。</span><span class="sxs-lookup"><span data-stu-id="073ef-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>Pathskiproot 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-239">抓取路徑中第一個字元的指標，並遵循磁碟機號或 UNC 伺服器/共用路徑元素。</span><span class="sxs-lookup"><span data-stu-id="073ef-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>Pathstrippath 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-241">移除完整路徑和檔案的路徑部分。</span><span class="sxs-lookup"><span data-stu-id="073ef-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>Pathstriptoroot 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-243">移除路徑中的所有檔案和目錄元素，但根資訊除外。</span><span class="sxs-lookup"><span data-stu-id="073ef-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="073ef-244">誤用此函數可能會導致緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="073ef-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="073ef-245">我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> 函數。</span><span class="sxs-lookup"><span data-stu-id="073ef-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-247">從路徑字串中移除裝飾。</span><span class="sxs-lookup"><span data-stu-id="073ef-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-249">以其相關聯的環境字串取代完整路徑中的特定資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="073ef-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-251">從使其成為系統資料夾的資料夾中移除屬性。</span><span class="sxs-lookup"><span data-stu-id="073ef-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="073ef-252">此資料夾實際上必須存在於檔案系統中。</span><span class="sxs-lookup"><span data-stu-id="073ef-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>Pathunquotespaces 式</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-254">從路徑的開頭和結尾移除引號。</span><span class="sxs-lookup"><span data-stu-id="073ef-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-256">檢查系結內容，以查看是否可以安全地系結至特定的元件物件。</span><span class="sxs-lookup"><span data-stu-id="073ef-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-258">判斷指定之 URL 字串的配置，並傳回具有適當前置詞的字串。</span><span class="sxs-lookup"><span data-stu-id="073ef-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-260">將 URL 字串轉換成標準格式。</span><span class="sxs-lookup"><span data-stu-id="073ef-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-262">以相對 URL 和其基底提供時，會傳回標準格式的 URL。</span><span class="sxs-lookup"><span data-stu-id="073ef-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-264">進行兩個 URL 字串的區分大小寫比較。</span><span class="sxs-lookup"><span data-stu-id="073ef-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-266">將 MS-DOS 路徑轉換成正式的 URL。</span><span class="sxs-lookup"><span data-stu-id="073ef-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-268">在透過網際網路傳輸期間可能會改變的 URL 中轉換字元或代理組， (&quot; 不安全 &quot; 的字元) 至其對應的 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="073ef-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="073ef-269">代理配對是32在10FFFF 中 U + 10000 到 U + (之間的字元) ，或 DC00 到 UTF-16) 中的 DFFF (之間。</span><span class="sxs-lookup"><span data-stu-id="073ef-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-271">將空白字元轉換成對應之 escape 序列的宏。</span><span class="sxs-lookup"><span data-stu-id="073ef-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-273">從 URL 取出位置。</span><span class="sxs-lookup"><span data-stu-id="073ef-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-275">接受 URL 字串，並傳回該 URL 的指定部分。</span><span class="sxs-lookup"><span data-stu-id="073ef-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-277">雜湊 URL 字串。</span><span class="sxs-lookup"><span data-stu-id="073ef-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>Urlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-279">測試 URL 是否為指定的類型。</span><span class="sxs-lookup"><span data-stu-id="073ef-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-281">測試 URL 以判斷它是否為檔案 URL。</span><span class="sxs-lookup"><span data-stu-id="073ef-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-283">傳回 URL 是否為瀏覽器通常不包含在導覽記錄中的 URL。</span><span class="sxs-lookup"><span data-stu-id="073ef-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-285">傳回 URL 是否不透明。</span><span class="sxs-lookup"><span data-stu-id="073ef-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="073ef-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-287">將 escape 序列轉換回一般字元。</span><span class="sxs-lookup"><span data-stu-id="073ef-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="073ef-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="073ef-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="073ef-289">將 escape 序列轉換回一般字元，並覆寫原始字串。</span><span class="sxs-lookup"><span data-stu-id="073ef-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




