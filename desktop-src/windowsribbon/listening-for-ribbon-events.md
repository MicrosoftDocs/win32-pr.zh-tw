---
title: 接聽功能區事件
description: Windows 功能區架構使用 Windows 的事件追蹤 (ETW) 基礎結構，讓開發人員瞭解使用者如何與應用程式的功能區互動。
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows 功能區，事件
- 功能區、事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316615"
---
# <a name="listening-for-ribbon-events"></a>接聽功能區事件

Windows 功能區架構使用 [windows 的事件追蹤 (ETW) ](../etw/event-tracing-portal.md) 基礎結構，讓開發人員瞭解使用者如何與應用程式的功能區互動。

## <a name="introduction"></a>簡介

功能區架構事件機制的設計，是為了讓架構將功能區 UI 附隨報告到應用程式，讓您可以監視使用者活動、瞭解其互動模式，以及評估使用趨勢。 這項資訊可用來改善您的功能區應用程式未來反覆運算的使用者體驗。

使用功能區架構事件包含下列各項：

1.  功能區應用程式必須註冊 [Windows (ETW) ](../etw/event-tracing-portal.md) 接聽程式的事件追蹤，才能從功能區架構接收功能區事件通知。
2.  如果應用程式已 [為 Windows (ETW) ](../etw/event-tracing-portal.md) 接聽程式註冊事件追蹤，則功能區架構會在執行時間引發功能區 UI 事件回呼。

## <a name="supported-events"></a>支援的事件

下表說明對功能區應用程式公開的事件。 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>事件</th>
<th>附隨報告</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>索引標籤已啟用</td>
<td>命令 ID<br/> 命令名稱<br/> 事件動詞<br/></td>
</tr>
<tr class="even">
<td>已啟用內容索引標籤</td>
<td>命令 ID<br/> 命令名稱<br/> 事件動詞<br/></td>
</tr>
<tr class="odd">
<td>開啟的應用程式功能表</td>
<td>事件動詞<br/></td>
</tr>
<tr class="even">
<td>應用程式功能表已關閉</td>
<td>事件動詞<br/></td>
</tr>
<tr class="odd">
<td>功能表 (一般或圖庫) 開啟</td>
<td>命令 ID<br/> 命令名稱<br/> 事件動詞<br/>
<blockquote>
[!Note]<br />
QAT 功能表事件不會公開。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td> (一般或圖庫) 關閉的功能表</td>
<td>命令 ID<br/> 命令名稱<br/> 事件動詞<br/>
<blockquote>
[!Note]<br />
QAT 功能表事件不會公開。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>命令</td>
<td>命令 ID<br/> 命令名稱<br/> 事件動詞<br/> 下列其中一個事件位置：
<ul>
<li>絲帶</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> 父命令識別碼<br/> 父命令名稱<br/> 下列其中一種調用方法：
<ul>
<li>點擊</li>
<li>KEYTIP</li>
<li>鍵盤</li>
<li>觸摸</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
專案資源庫和下拉式方塊包括選取的專案索引，但不包含字串和整數值。 Spinners 不包含整數值。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>功能區最小化</td>
<td>事件動詞<br/></td>
</tr>
<tr class="odd">
<td>功能區展開 (展開按鈕，或按一下釘選的) </td>
<td>事件動詞<br/></td>
</tr>
<tr class="even">
<td>應用程式模式切換</td>
<td>事件動詞<br/> 透過 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>) 設定的模式識別碼 (值<br/>
<blockquote>
[!Note]<br />
應用程式會負責將此整數解壓縮，以判斷已設定的模式。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>顯示工具提示</td>
<td>事件動詞<br/> 父命令識別碼<br/> 父命令名稱<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 功能區架構開發人員指南](windowsribbon-guides-entry.md)
</dt> <dt>

[使用功能區標記宣告命令和控制項](./windowsribbon-schema.md)
</dt> <dt>

[功能區使用者體驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[功能區設計流程](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

