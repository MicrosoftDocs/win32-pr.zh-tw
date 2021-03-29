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
# <a name="shell-path-handling-functions"></a>Shell 路徑處理函式

本節說明 Windows Shell 路徑處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>主題</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackslash 式</strong></a><br/></td>
<td>在字串的結尾加上反斜線，以建立路徑的正確語法。 如果來源路徑已經有尾端反斜線，則不會新增反斜線。 <br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension 式</strong></a><br/></td>
<td>將副檔名新增至路徑字串。<br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>Pathappend 式</strong></a><br/></td>
<td>將一個路徑附加至另一個路徑的結尾。 <br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot 式</strong></a><br/></td>
<td>從指定的磁片磁碟機編號建立根路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize 式</strong></a><br/></td>
<td>藉由移除導覽元素（例如 &quot; . &quot; 和.）來簡化路徑 &quot; &quot; ，以產生直接、格式正確的路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine 式</strong></a><br/></td>
<td>將表示正確格式路徑的兩個字串串連成一個路徑;也會串連任何相對路徑元素。 <br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix 式</strong></a><br/></td>
<td>比較兩個路徑，以判斷它們是否共用一般前置詞。 前置詞是下列其中一種類型： &quot; C： \\ &quot; 、 &quot; ... &quot; &quot; &quot; &quot; \\ &quot; .。。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath 式</strong></a><br/></td>
<td>將路徑元件取代為省略號，以截斷檔案路徑以符合給定的圖元寬度。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex 式</strong></a><br/></td>
<td>藉由以省略號取代路徑元件，截斷路徑以容納在特定數目的字元內。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br/></td>
<td>將檔案 URL 轉換成 Microsoft MS-DOS 路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br/></td>
<td>從檔案 URL 建立路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfileexists 式</strong></a><br/></td>
<td>判斷檔案系統物件（例如檔案或資料夾）的路徑是否有效。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension 式</strong></a><br/></td>
<td>搜尋延伸模組的路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename 式</strong></a><br/></td>
<td>搜尋路徑中的檔案名。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br/></td>
<td>剖析路徑，並傳回路徑中第一個反斜線之後的部分。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br/></td>
<td>搜尋檔案。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br/></td>
<td>判斷指定的檔案名是否包含其中一個尾碼清單。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br/></td>
<td>在指定的路徑中尋找命令列引數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br/></td>
<td>決定與路徑相關的字元類型。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumber 式</strong></a><br/></td>
<td>在路徑中搜尋 ' A ' 到 ' Z ' 範圍內的磁碟機號，並傳回對應的磁碟機號。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br/></td>
<td>判斷檔案的已註冊內容類型是否符合指定的內容類型。 此函式會取得指定之檔案類型的內容類型，並將該字串與 <em>pszContentType</em>比較。 這項比較不會區分大小寫。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory 式</strong></a><br/></td>
<td>確認路徑是否為有效的目錄。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br/></td>
<td>判斷指定的路徑是否為空的目錄。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br/></td>
<td>搜尋路徑中任何路徑分隔字元 (例如 '： ' 或 ' \' ) 。 如果沒有任何路徑分隔字元，則會將路徑視為檔案規格路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br/></td>
<td>判斷檔案是否為 HTML 檔案。 這會根據為檔案副檔名所註冊的內容類型來決定。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br/></td>
<td>判斷檔案名的格式是否完整。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br/></td>
<td>判斷路徑字串是否代表網路資源。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>Pathisprefix 式</strong></a><br/></td>
<td>搜尋路徑以判斷它是否包含 <em>pszPrefix</em>所傳遞之類型的有效前置詞。 前置詞是下列其中一種類型： &quot; C： \\ &quot; 、 &quot; ... &quot; &quot; &quot; &quot; \\ &quot; .。。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>Pathisrelative 式</strong></a><br/></td>
<td>搜尋路徑並判斷其是否為相對。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot 式</strong></a><br/></td>
<td>判斷路徑字串是否參考磁片區的根目錄。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>Pathissameroot 式</strong></a><br/></td>
<td>比較兩個路徑，判斷它們是否有共同的根元件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br/></td>
<td>判斷現有的資料夾是否包含將其設為系統資料夾的屬性。 或者，此函式會指出特定的屬性是否將資料夾限定為系統資料夾。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>Pathisunc 式</strong></a><br/></td>
<td>判斷路徑字串是否為有效的通用命名慣例 (UNC) 路徑，而不是根據磁碟機號的路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver 式</strong></a><br/></td>
<td>判斷字串是否為伺服器路徑的有效 UNC。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare 式</strong></a><br/></td>
<td>判斷字串是否為有效的 UNC 共用路徑，也就是 \\ <em>伺服器</em> \ <em>共用</em>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br/></td>
<td>測試指定的字串，以判斷它是否符合有效的 URL 格式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br/></td>
<td>將全部大寫的路徑轉換成所有小寫字元，以提供路徑一致的外觀。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br/></td>
<td>為現有的資料夾提供適當的屬性，使其成為系統資料夾。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>Pathmatchspec 式</strong></a><br/></td>
<td>使用 MS-DOS 萬用字元相符類型來搜尋字串。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br/></td>
<td>比對一或多個檔案名模式的檔案名與路徑。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br/></td>
<td>剖析包含檔案位置和圖示索引的檔案位置字串，並傳回不同的值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br/></td>
<td>搜尋空格的路徑。 如果找到空格，則整個路徑會以引號括住。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>Pathrelativepathto 式</strong></a><br/></td>
<td>建立從一個檔案或資料夾到另一個檔案或資料夾的相對路徑。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>Pathremoveargs 式</strong></a><br/></td>
<td>從指定的路徑移除任何引數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>Pathremovebackslash 式</strong></a><br/></td>
<td>從指定的路徑移除尾端的反斜線。<br/>
<blockquote>
[!Note]<br />
這個函數已被取代。 建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>Pathremoveblanks 式</strong></a><br/></td>
<td>從字串中移除所有開頭和尾端空格。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>Pathremoveextension 式</strong></a><br/></td>
<td>移除路徑中的副檔名（如果有的話）。 <br/>
<blockquote>
[!Note]<br />
這個函數已被取代。 建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> 。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>Pathremovefilespec 式</strong></a><br/></td>
<td>從路徑移除尾端的檔案名和反斜線（如果有的話）。<br/>
<blockquote>
[!Note]<br />
這個函數已被取代。 我們建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> 函式。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br/></td>
<td>以新的副檔名取代檔案名的副檔名。 如果檔案名不包含副檔名，則會將副檔名附加至字串的結尾。<br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br/></td>
<td>判斷指定路徑的格式是否正確且完整。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br/></td>
<td>使用 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>pathcompactpath 式</strong></a> ，在視窗或對話方塊中設定子控制項的文字，以確保該路徑符合控制項。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>Pathskiproot 式</strong></a><br/></td>
<td>抓取路徑中第一個字元的指標，並遵循磁碟機號或 UNC 伺服器/共用路徑元素。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>Pathstrippath 式</strong></a><br/></td>
<td>移除完整路徑和檔案的路徑部分。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>Pathstriptoroot 式</strong></a><br/></td>
<td>移除路徑中的所有檔案和目錄元素，但根資訊除外。<br/>
<blockquote>
[!Note]<br />
誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> 函數。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br/></td>
<td>從路徑字串中移除裝飾。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br/></td>
<td>以其相關聯的環境字串取代完整路徑中的特定資料夾名稱。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br/></td>
<td>從使其成為系統資料夾的資料夾中移除屬性。 此資料夾實際上必須存在於檔案系統中。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>Pathunquotespaces 式</strong></a><br/></td>
<td>從路徑的開頭和結尾移除引號。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br/></td>
<td>檢查系結內容，以查看是否可以安全地系結至特定的元件物件。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br/></td>
<td>判斷指定之 URL 字串的配置，並傳回具有適當前置詞的字串。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br/></td>
<td>將 URL 字串轉換成標準格式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br/></td>
<td>以相對 URL 和其基底提供時，會傳回標準格式的 URL。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br/></td>
<td>進行兩個 URL 字串的區分大小寫比較。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br/></td>
<td>將 MS-DOS 路徑轉換成正式的 URL。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br/></td>
<td>在透過網際網路傳輸期間可能會改變的 URL 中轉換字元或代理組， (&quot; 不安全 &quot; 的字元) 至其對應的 escape 序列。 代理配對是32在10FFFF 中 U + 10000 到 U + (之間的字元) ，或 DC00 到 UTF-16) 中的 DFFF (之間。 <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br/></td>
<td>將空白字元轉換成對應之 escape 序列的宏。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br/></td>
<td>從 URL 取出位置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br/></td>
<td>接受 URL 字串，並傳回該 URL 的指定部分。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br/></td>
<td>雜湊 URL 字串。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>Urlls</strong></a><br/></td>
<td>測試 URL 是否為指定的類型。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br/></td>
<td>測試 URL 以判斷它是否為檔案 URL。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br/></td>
<td>傳回 URL 是否為瀏覽器通常不包含在導覽記錄中的 URL。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br/></td>
<td>傳回 URL 是否不透明。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br/></td>
<td>將 escape 序列轉換回一般字元。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br/></td>
<td>將 escape 序列轉換回一般字元，並覆寫原始字串。<br/></td>
</tr>
</tbody>
</table>



 

 

 




