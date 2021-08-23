---
title: 標準控制項的 UI 自動化支援
description: 本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。 完整的支援僅適用于 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6中的控制項。
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- 用戶端，消費者介面自動化標準控制項的支援
- 用戶端，標準控制項支援
- 用戶端、Win32 控制項
- 消費者介面自動化，標準控制項的支援
- 消費者介面自動化，標準控制項支援
- 消費者介面自動化，Win32 控制項
- 標準控制項的支援
- 標準控制項支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5bbc8c481490e9ba0ea385199b750591873d94ef9321b4ac0555231b9b4370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993928"
---
# <a name="ui-automation-support-for-standard-controls"></a>標準控制項的 UI 自動化支援

本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。 完整的支援僅適用于 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6中的控制項。

> [!Note]  
> RichEdit 控制項僅支援 RichEd20.dll 3.1 版和更新版本中 Windows Vista (隨附的版本，以及 MsftEdit.dll 4.1 版和更新版本的) 。

 

下表列出支援的標準控制項的類別名稱，以及對應的消費者介面自動化控制項類型。



| 類別名稱          | 控制項類型        |
|---------------------|---------------------|
| Button              | Button              |
| Button              | RadioButton         |
| Button              | Group               |
| Button              | CheckBox            |
| Button              | Hyperlink           |
| Button              | SplitButton         |
| Button              | CheckBox            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| 編輯                | 文件            |
| 編輯                | 編輯                |
| SysLink             | Hyperlink           |
| 靜態              | Text                |
| 靜態              | 映像               |
| SysIPAddress32      | 自訂              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | List                |
| ListBox             | List                |
| ListBox             | ListItem            |
| \#32768             | 功能表                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | ProgressBar         |
| RichEdit            | 文件。 請參閱附註。 |
| RichEdit20A         | 文件            |
| RichEdit20W         | 文件            |
| RichEdit50W         | 文件            |
| ScrollBar           | Slider              |
| msctls \_ trackbar32  | Slider              |
| msctls \_ updown32    | Spinner             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | 索引標籤                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Button              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Separator           |
| 工具提示 \_ class32   | ToolTip             |
| \#32774             | ToolTip             |
| ReBarWindow32       | 工具列             |
| SysTreeView32       | 樹狀結構                |
| SysTreeView32       | TreeItem            |



 

下表所列的控制項不受支援。



| 類別名稱                                    | 控制項類型 |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | 映像        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | 自訂       |
| SysMonthCal32                                 | Calendar     |
| MS \_ WINNOTE                                   | 工具提示      |
| VBBubble                                      | 工具提示      |
| ScrollBar (當做獨立控制項使用時) | Slider       |
| SuperGrid                                     | 自訂       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




