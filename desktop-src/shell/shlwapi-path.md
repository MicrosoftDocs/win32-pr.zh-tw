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
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481964"
---
# <a name="shell-path-handling-functions"></a>Shell 路徑處理函式

本節說明 Windows Shell 路徑處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackslash 式</strong></a><br /> | 在字串的結尾加上反斜線，以建立路徑的正確語法。 如果來源路徑已經有尾端反斜線，則不會新增反斜線。 <br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension 式</strong></a><br /> | 將副檔名新增至路徑字串。<br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>Pathappend 式</strong></a><br /> | 將一個路徑附加至另一個路徑的結尾。 <br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot 式</strong></a><br /> | 從指定的磁片磁碟機編號建立根路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize 式</strong></a><br /> | 藉由移除導覽元素（例如 "." 和 "..."）來簡化路徑，以產生直接、格式正確的路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine 式</strong></a><br /> | 將表示正確格式路徑的兩個字串串連成一個路徑;也會串連任何相對路徑元素。 <br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix 式</strong></a><br /> | 比較兩個路徑，以判斷它們是否共用一般前置詞。 前置詞是下列其中一種類型： "C： \\ "、"."、"..."、"... \\ "。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath 式</strong></a><br /> | 將路徑元件取代為省略號，以截斷檔案路徑以符合給定的圖元寬度。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex 式</strong></a><br /> | 藉由以省略號取代路徑元件，截斷路徑以容納在特定數目的字元內。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br /> | 將檔案 URL 轉換成 Microsoft MS-DOS 路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br /> | 從檔案 URL 建立路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfileexists 式</strong></a><br /> | 判斷檔案系統物件（例如檔案或資料夾）的路徑是否有效。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension 式</strong></a><br /> | 搜尋延伸模組的路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename 式</strong></a><br /> | 搜尋路徑中的檔案名。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br /> | 剖析路徑，並傳回路徑中第一個反斜線之後的部分。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br /> | 搜尋檔案。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br /> | 判斷指定的檔案名是否包含其中一個尾碼清單。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br /> | 在指定的路徑中尋找命令列引數。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br /> | 決定與路徑相關的字元類型。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumber 式</strong></a><br /> | 在路徑中搜尋 ' A ' 到 ' Z ' 範圍內的磁碟機號，並傳回對應的磁碟機號。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br /> | 判斷檔案的已註冊內容類型是否符合指定的內容類型。 此函式會取得指定之檔案類型的內容類型，並將該字串與 <em>pszContentType</em>比較。 這項比較不會區分大小寫。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory 式</strong></a><br /> | 確認路徑是否為有效的目錄。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br /> | 判斷指定的路徑是否為空的目錄。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br /> | 搜尋路徑中任何路徑分隔字元 (例如 '： ' 或 ' \' ) 。 如果沒有任何路徑分隔字元，則會將路徑視為檔案規格路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br /> | 判斷檔案是否為 HTML 檔案。 這會根據為檔案副檔名所註冊的內容類型來決定。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br /> | 判斷檔案名的格式是否完整。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br /> | 判斷路徑字串是否代表網路資源。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>Pathisprefix 式</strong></a><br /> | 搜尋路徑以判斷它是否包含 <em>pszPrefix</em>所傳遞之類型的有效前置詞。 前置詞是下列其中一種類型： "C： \\ "、"."、"..."、"... \\ "。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>Pathisrelative 式</strong></a><br /> | 搜尋路徑並判斷其是否為相對。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot 式</strong></a><br /> | 判斷路徑字串是否參考磁片區的根目錄。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>Pathissameroot 式</strong></a><br /> | 比較兩個路徑，判斷它們是否有共同的根元件。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br /> | 判斷現有的資料夾是否包含將其設為系統資料夾的屬性。 或者，此函式會指出特定的屬性是否將資料夾限定為系統資料夾。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>Pathisunc 式</strong></a><br /> | 判斷路徑字串是否為有效的通用命名慣例 (UNC) 路徑，而不是根據磁碟機號的路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver 式</strong></a><br /> | 判斷字串是否為伺服器路徑的有效 UNC。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare 式</strong></a><br /> | 判斷字串是否為有效的 UNC 共用路徑，也就是 \\ <em>伺服器</em> \<em> 共用 </em> 。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br /> | 測試指定的字串，以判斷它是否符合有效的 URL 格式。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br /> | 將全部大寫的路徑轉換成所有小寫字元，以提供路徑一致的外觀。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br /> | 為現有的資料夾提供適當的屬性，使其成為系統資料夾。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>Pathmatchspec 式</strong></a><br /> | 使用 MS-DOS 萬用字元相符類型來搜尋字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br /> | 比對一或多個檔案名模式的檔案名與路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br /> | 剖析包含檔案位置和圖示索引的檔案位置字串，並傳回不同的值。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br /> | 搜尋空格的路徑。 如果找到空格，則整個路徑會以引號括住。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>Pathrelativepathto 式</strong></a><br /> | 建立從一個檔案或資料夾到另一個檔案或資料夾的相對路徑。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>Pathremoveargs 式</strong></a><br /> | 從指定的路徑移除任何引數。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>Pathremovebackslash 式</strong></a><br /> | 從指定的路徑移除尾端的反斜線。<br /><blockquote>[!Note]<br />這個函數已被取代。 建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> 或 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>Pathremoveblanks 式</strong></a><br /> | 從字串中移除所有開頭和尾端空格。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>Pathremoveextension 式</strong></a><br /> | 移除路徑中的副檔名（如果有的話）。 <br /><blockquote>[!Note]<br />這個函數已被取代。 建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> 。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>Pathremovefilespec 式</strong></a><br /> | 從路徑移除尾端的檔案名和反斜線（如果有的話）。<br /><blockquote>[!Note]<br />這個函數已被取代。 我們建議您在其位置使用 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> 函式。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br /> | 以新的副檔名取代檔案名的副檔名。 如果檔案名不包含副檔名，則會將副檔名附加至字串的結尾。<br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br /> | 判斷指定路徑的格式是否正確且完整。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br /> | 使用 <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>pathcompactpath 式</strong></a> ，在視窗或對話方塊中設定子控制項的文字，以確保該路徑符合控制項。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>Pathskiproot 式</strong></a><br /> | 抓取路徑中第一個字元的指標，並遵循磁碟機號或 UNC 伺服器/共用路徑元素。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>Pathstrippath 式</strong></a><br /> | 移除完整路徑和檔案的路徑部分。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>Pathstriptoroot 式</strong></a><br /> | 移除路徑中的所有檔案和目錄元素，但根資訊除外。<br /><blockquote>[!Note]<br />誤用此函數可能會導致緩衝區溢位。 我們建議您在其位置使用更安全的 <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> 函數。</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br /> | 從路徑字串中移除裝飾。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br /> | 以其相關聯的環境字串取代完整路徑中的特定資料夾名稱。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br /> | 從使其成為系統資料夾的資料夾中移除屬性。 此資料夾實際上必須存在於檔案系統中。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>Pathunquotespaces 式</strong></a><br /> | 從路徑的開頭和結尾移除引號。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br /> | 檢查系結內容，以查看是否可以安全地系結至特定的元件物件。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br /> | 判斷指定之 URL 字串的配置，並傳回具有適當前置詞的字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br /> | 將 URL 字串轉換成標準格式。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br /> | 以相對 URL 和其基底提供時，會傳回標準格式的 URL。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br /> | 進行兩個 URL 字串的區分大小寫比較。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br /> | 將 MS-DOS 路徑轉換成正式的 URL。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br /> | 在透過網際網路傳輸期間可能會改變的 URL 中轉換字元或代理組（ ( 「unsafe」字元) 至其對應的 escape 序列）。 代理配對是32在10FFFF 中 U + 10000 到 U + (之間的字元) ，或 DC00 到 UTF-16) 中的 DFFF (之間。 <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br /> | 將空白字元轉換成對應之 escape 序列的宏。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br /> | 從 URL 取出位置。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br /> | 接受 URL 字串，並傳回該 URL 的指定部分。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br /> | 雜湊 URL 字串。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>Urlls</strong></a><br /> | 測試 URL 是否為指定的類型。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br /> | 測試 URL 以判斷它是否為檔案 URL。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br /> | 傳回 URL 是否為瀏覽器通常不包含在導覽記錄中的 URL。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br /> | 傳回 URL 是否不透明。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br /> | 將 escape 序列轉換回一般字元。<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br /> | 將 escape 序列轉換回一般字元，並覆寫原始字串。<br /> | 




 

 

 




