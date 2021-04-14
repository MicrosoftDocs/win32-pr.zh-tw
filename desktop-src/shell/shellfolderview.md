---
description: 代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: 'ShellFolderView 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991722"
---
# <a name="shellfolderview-object"></a>ShellFolderView 物件

代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。

## <a name="members"></a>成員

**ShellFolderView** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**ShellFolderView** 物件具有這些事件。



| 事件                                                        | 描述                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | 發生于視圖中任何專案或專案的選取狀態變更時。<br/> |



 

### <a name="methods"></a>方法

**ShellFolderView** 物件有這些方法。



| 方法                                                 | 描述                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | 為指定的專案建立快捷方式功能表，並傳回選取的命令字串。<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | 取得 [**FolderItems**](folderitems.md) 物件，這個物件表示視圖中所有選取的專案。<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | 在視圖中設定專案的選取狀態。<br/>                                                        |



 

### <a name="properties"></a>屬性

**ShellFolderView** 物件具有這些屬性。



| 屬性                                                      | 存取類型          | Description                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Application**](shellfolderview-application.md)<br/> | 唯讀<br/> | 包含物件的應用程式物件。<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | 唯讀<br/> | 取得代表具有輸入焦點之專案的 [**FolderItem**](folderitem.md) 物件。<br/> |
| [**資料夾**](shellfolderview-folder.md)<br/>           | 唯讀<br/> | 取得代表視圖的 [**資料夾**](folder.md) 物件。<br/>                                  |
| [**父代**](shellfolderview-parent.md)<br/>           | 唯讀<br/> | 未實作。<br/>                                                                                  |
| [**腳本**](shellfolderview-script.md)<br/>           | 唯讀<br/> | 已取代。<br/>                                                                                       |
| [**ViewOptions**](shellfolderview-viewoptions.md)<br/> | 唯讀<br/> | 取得一組旗標，指出視圖的目前選項。<br/>                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |
| IID<br/>                      | CLSID \_ ShellFolderView<br/>                                                                              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShellFolderViewOptions 旗標**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




