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
# <a name="calling-wds-from-the-command-line"></a>從命令列呼叫 WDS

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

您可以使用 windowssearch.exe 命令列語法，從另一個應用程式或使用瀏覽器協助程式物件的網頁，啟動 Microsoft Windows 桌面搜尋 (WDS) 使用者介面， (BHO) 。 從命令列呼叫 WDS 時，不會將使用者在 WDS 視窗中的動作或選取專案的相關資訊傳回給呼叫的應用程式或網頁。

WDS 安裝路徑是在 InstallDir 登錄設定的 [ \\ \\ Microsoft Windows 桌面搜尋 HKEY_LOCAL_MACHINE 軟體] 下指定 \\ 。 安裝 windowssearch.exe 的預設路徑是 [Program Files] \\ Windows Desktop Search。

## <a name="command-line-syntax"></a>命令列語法

下列語法適用于 Windows Desktop Search 2.x 命令列介面。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>參數</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/startup</td>

<td>初始化 Windows 桌面搜尋</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>關閉編制索引的功能，並重新掃描所有索引位置</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>顯示索引狀態視窗</td>
</tr>
<tr class="even">
<td>/launchsearchwindow 或/url</td>

<td>使用空的查詢來開啟 WDS 視窗</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>搜尋： [store | show | query] 查詢字串</td>
<td>使用查詢開啟 WDS 視窗，並根據下列參數進行篩選：
<ul>
<li><p>store-指定要查詢的資料來源： files、outlook、outlookexpress。 如果未指定，則會搜尋所有存放區。 <br/></p>
<blockquote>
[!Note]<br />
雖然 Advanced Query 語法支援將 Microsoft Outlook 參考為 ' oe '，但是命令列上的 store 參數必須是 ' outlookexpress '。
</blockquote>
<p><br/></p></li>
<li><p>顯示-指定要傳回的已知結果類型。 如需完整的類型清單，請參閱 <a href="-search-2x-wds-perceivedtype.md">認知</a> 型別。 如果未指定，則會傳回所有類型。 <br/></p>
<blockquote>
[!Note]<br />
認知的型別值和顯示的值之間有三項差異。 若是 <code>show</code> ，請使用 ' documents '，而非 ' doc '、' pictures ' 而非 ' pictures ' 和 ' textdocuments '，而非 ' text '。
</blockquote>
<p><br/></p></li>
<li>查詢-指定搜尋準則。 此值支援 <a href="-search-2x-wds-aqsreference.md">Advanced Query 語法</a> 參數來精簡結果。 查詢參數必須是 URL 中的最後一個參數。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>範例

例如，若要搜尋所有符合「背景圖樣」準則的檔案，請使用下列命令：

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[進階查詢語法](-search-2x-wds-aqsreference.md)
</dt> <dt>

[認知類型](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[從 Web Pages 呼叫 WDS](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





