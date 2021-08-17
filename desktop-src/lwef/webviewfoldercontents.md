---
title: WebViewFolderContents 物件 (Shldisp.h)
description: 由 Shell 所執行，可在 Web 工作內使用。
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- WebViewFolderContents 物件舊版 Windows 環境功能
- WebViewFolderContents 物件舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fe0146f49d0e5172410ca119953a7b3f245af20c0e4c2d83ff78fa23b93e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035956"
---
# <a name="webviewfoldercontents-object"></a>WebViewFolderContents 物件

由 Shell 所執行，可在 *web* 工作內使用。 **WebViewFolderContents** 會自動將自己初始化為 web 上的目前資料夾。 它會建立 Shell 資料夾檢視，以下列五種格式的其中一種來顯示資料夾的內容：小型圖示、大型圖示、清單、詳細資料或縮圖。 它在 Web 程式外部無效。

**WebViewFolderContents** 所公開的方法和屬性與 [**ShellFolderView**](/windows/desktop/shell/shellfolderview)物件的方法和屬性相同。

## <a name="members"></a>成員

**WebViewFolderContents** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**WebViewFolderContents** 物件具有這些事件。



| 事件                                                              | 描述                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | 發生于視圖中任何專案或專案的選取狀態變更時。<br/> |



 

### <a name="methods"></a>方法

**WebViewFolderContents** 物件有這些方法。



| 方法                                                       | 描述                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | 為指定的專案建立快捷方式功能表，並傳回選取的命令字串。<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | 取得 [**FolderItems**](../shell/folderitems.md) 物件，這個物件表示視圖中所有選取的專案。<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | 在視圖中設定專案的選取狀態。<br/>                                                          |



 

### <a name="properties"></a>屬性

**WebViewFolderContents** 物件具有這些屬性。



| 屬性                                                            | 存取類型          | 描述                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](webviewfoldercontents-application.md)<br/> | 唯讀<br/> | 未實作。<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | 唯讀<br/> | 取得代表具有輸入焦點之專案的 [**FolderItem**](../shell/folderitem.md) 物件。<br/>                           |
| [**資料夾**](webviewfoldercontents-folder.md)<br/>           | 唯讀<br/> | 取得代表視圖的 [**資料夾**](../shell/folder.md) 物件。<br/>                                                            |
| [**父代**](webviewfoldercontents-parent.md)<br/>           | 唯讀<br/> | 未實作。<br/>                                                                                                              |
| [**指令碼**](webviewfoldercontents-script.md)<br/>           | 唯讀<br/> | 取得視圖的腳本物件。<br/>                                                                                       |
| [**ViewOptions**](webviewfoldercontents-viewoptions.md)<br/> | 唯讀<br/> | 取得一組 [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) 旗標，指出視圖的目前選項。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

