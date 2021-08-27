---
description: 本節描述 Shell 所執行的 Windows 物件。
title: 腳本和 Microsoft Visual Basic 的 Shell 物件
ms.topic: article
ms.date: 05/31/2018
ms.assetid: eee58404-808b-451c-8325-8dcd9537fd11
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e4d367b836516259a4c0f73cea9da20e7e13326
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465025"
---
# <a name="shell-objects-for-scripting-and-microsoft-visual-basic"></a>腳本和 Microsoft Visual Basic 的 Shell 物件

本節描述 Shell 所執行的 Windows 物件。

## <a name="in-this-section"></a>本節內容




| 主題 | 描述 | 
|-------|-------------|
| <a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a><br /> | 允許用戶端管理 NTFS 磁片區的全域磁片配額設定。 這個物件讓<a href="didiskquotauser-object.md"><strong>DIDiskQuotaUser</strong></a>介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。<br /> | 
| <a href="diskquotacontrol-object.md"><strong>DiskQuotaControl</strong></a><br /> | 可讓系統管理員管理磁片區的磁片配額屬性。 NTFS 檔案系統可讓系統管理員藉由為每個使用者配置指定的磁碟空間數量或 <em>配額限制</em>，來管理共用磁片區上的磁片使用量。 您可以使用此物件來設定將自動指派給所有新使用者的預設配額限制。<br /> | 
| <a href="dshellwindowsevents.md"><strong>DShellWindowsEvents</strong></a><br /> | 接收 <a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a> 視窗註冊事件。 <br /> | 
| <a href="folder.md"><strong>資料夾</strong></a><br /> | 表示 Shell 資料夾。 此物件包含屬性和方法，可讓您取得資料夾的相關資訊。<br /> | 
| <a href="folder2-object.md"><strong>Folder2</strong></a><br /> | 擴充 <a href="folder.md"><strong>資料夾</strong></a> 物件以支援離線資料夾。<br /> | 
| <a href="folderitem.md"><strong>FolderItem</strong></a><br /> | 表示 Shell 資料夾中的專案。 此物件包含屬性和方法，可讓您取得專案的相關資訊。<br /> | 
| <a href="folderitems.md"><strong>FolderItems</strong></a><br /> | 表示 Shell 資料夾中的專案集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。<br /> | 
| <a href="folderitems2-object.md"><strong>FolderItems2</strong></a><br /> | 擴充 <a href="folderitems.md"><strong>FolderItems</strong></a> 物件。 它支援一個額外的方法。<br /> | 
| <a href="folderitems3-object.md"><strong>FolderItems3</strong></a><br /> | 擴充 <a href="folderitems2-object.md"><strong>FolderItems2</strong></a> 物件。 此物件支援其他方法和屬性。<br /> | 
| <a href="folderitemverb.md"><strong>FolderItemVerb</strong></a><br /> | 表示專案可用的單一動詞。 此物件包含屬性和方法，可讓您取得動詞的相關資訊。<br /> | 
| <a href="folderitemverbs.md"><strong>FolderItemVerbs</strong></a><br /> | 表示 Shell 資料夾中專案的動詞集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。<br /> | 
| <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a><br /> | 表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a><br /> | 使用各種新功能來擴充 <a href="ishelldispatch.md"><strong>IShellDispatch</strong></a> 物件。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a><br /> | 擴充 <a href="ishelldispatch2-object.md"><strong>IShellDispatch2</strong></a> 物件。 除了<strong>IShellDispatch2</strong>支援的屬性和方法之外， <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a>還支援一個新的方法。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a><br /> | 擴充 <a href="ishelldispatch3.md"><strong>IShellDispatch3</strong></a> 物件。 除了 <strong>IShellDispatch3</strong>支援的屬性和方法之外， <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 還支援四個額外的方法。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a><br /> | 擴充 <a href="ishelldispatch4.md"><strong>IShellDispatch4</strong></a> 物件。 除了 <strong>IShellDispatch4</strong>所支援的屬性和方法之外， <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 還新增了在3d 堆疊中顯示開啟視窗的方法。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a><br /> | 擴充 <a href="ishelldispatch5.md"><strong>IShellDispatch5</strong></a> 物件。 除了 <strong>IShellDispatch5</strong>支援的屬性和方法之外， <a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> 也會新增可顯示應用程式搜尋窗格的方法。 <br /><blockquote>[!Note]<br /><a href="ishelldispatch6.md"><strong>IShellDispatch6</strong></a> 是透過 <a href="shell.md"><strong>Shell</strong></a> 物件來執行和存取。</blockquote><br /> | 
| <a href="ishelllinkdual2-object.md"><strong>IShellLinkDual2</strong></a><br /> | 擴充 <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a> 物件，並支援一個額外的屬性。<br /> | 
| <a href="newwdevents.md"><strong>NewWDEvents</strong></a><br /> | 藉由啟用在 wizard 中裝載的伺服器端頁面，來擴充 <a href="webwizardhost.md"><strong>WebWizardHost</strong></a> 物件，以確認使用者已通過 Microsoft 帳戶驗證。<br /> | 
| <a href="shell.md"><strong>Shell</strong></a><br /> | 表示 Shell 中的物件。 系統會提供方法來控制 Shell，並在 Shell 中執行命令。 也有方法可以取得其他與 Shell 相關的物件。<br /> | 
| <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a><br /> | 擴充 <a href="folderitem.md"><strong>FolderItem</strong></a> 物件。 除了 <strong>FolderItem</strong>支援的屬性和方法之外， <a href="shellfolderitem-object.md"><strong>ShellFolderItem</strong></a> 還有兩個額外的方法。<br /> | 
| <a href="shellfolderview.md"><strong>ShellFolderView</strong></a><br /> | 代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。<br /> | 
| <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a><br /> | 將指定之 <a href="shellfolderview.md"><strong>ShellFolderView</strong></a> 物件所引發的事件轉送到對應的 <a href="shellfolderviewoc-object.md"><strong>ShellFolderViewOC</strong></a> 事件處理常式。<br /> | 
| <a href="shelllinkobject-object.md"><strong>ShellLinkObject</strong></a><br /> | 管理 Shell 連結。 這個物件讓 <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a> 介面的許多功能可供腳本應用程式使用。 <br /> | 
| <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a><br /> | 由 shell 所執行，以協助編寫腳本和 Visual Basic 開發人員使用 shell 中提供的一些功能。 <a href="shelluihelper.md"><strong>ShellUIHelper</strong></a>物件沒有任何屬性或事件。 提供方法以將專案新增至 Shell。<br /> | 
| <a href="shellwindows.md"><strong>ShellWindows</strong></a><br /> | 表示屬於 Shell 之開啟視窗的集合。 與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。<br /> | 
| <a href="webwizardhost.md"><strong>WebWizardHost</strong></a><br /> | 公開方法，這些方法可讓您在 wizard 擴充功能中裝載的 HTML 網頁與 wizard 進行通訊。<br /> | 




 

 

 




