---
description: Windows Installer 為套件開發人員提供撰寫具有多個功能層級之內部使用者介面的功能。
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: 消費者介面層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195260"
---
# <a name="user-interface-levels"></a>消費者介面層級

Windows Installer 為套件開發人員提供撰寫具有多個功能層級之內部使用者介面的功能。 因為內部 UI 必須由套件的作者所建立，所以完整 UI 的行為、縮減的 UI、基本 UI 和無層級取決於安裝套件。 下表說明一般歸屬至 UI 層級的功能。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>UI 層級</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>完整 UI</td>
<td>顯示已撰寫至內部 UI 的強制回應和非強制回應對話方塊。 顯示撰寫的 <a href="error-dialog.md">錯誤對話方塊</a> 。
<blockquote>
[!Note]<br />
強制回應對話方塊需要使用者輸入，才能繼續安裝，而且可以在<a href="dialog-table.md">對話方塊</a>資料表的 [屬性] 資料行中設定<a href="modal-dialog-style-bit.md">強制回應對話方塊樣式位</a>來指定。 非強制回應對話方塊不需要使用者輸入，就能繼續進行安裝。
</blockquote>
<br/> 完整的 UI 通常會顯現 <a href="user-interface-wizard-behavior.md">消費者介面的 Wizard 行為</a>。<br/></td>
</tr>
<tr class="even">
<td>縮小 UI</td>
<td>顯示任何已在 UI 中撰寫的非強制回應對話方塊。 不會顯示任何撰寫的強制回應對話方塊。 顯示撰寫的 <a href="error-dialog.md">錯誤對話方塊</a> 。 顯示 <a href="authoring-disk-prompt-messages.md">磁片提示</a> 訊息。 顯示 <a href="filesinuse-dialog.md">FilesInUse 對話方塊</a> 。</td>
</tr>
<tr class="odd">
<td>基本 UI</td>
<td>顯示顯示進度訊息的內建非強制回應對話方塊。 顯示內建的錯誤對話方塊。 不會顯示任何撰寫的對話方塊。 藉由顯示包含 <a href="diskprompt.md"><strong>DiskPrompt</strong></a> 屬性值的對話方塊，提示使用者插入磁片。</td>
</tr>
<tr class="even">
<td>無</td>
<td>None 表示無訊息安裝，不會顯示任何 UI。</td>
</tr>
</tbody>
</table>



 

您可以使用 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)來設定內部 UI 的層級。 安裝程式會將 [**UILevel**](uilevel.md) 屬性設定為目前的 UI 層級。

如果設定了 [**LIMITUI**](limitui.md) 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。

如需 UI 撰寫的範例，請參閱 [安裝範例](an-installation-example.md)。

 

 




