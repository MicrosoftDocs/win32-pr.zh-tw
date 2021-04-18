---
title: 標準控制項的 UI 自動化支援
description: 本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。 只有 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6的控制項才會提供完整的支援。
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
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507080"
---
# <a name="ui-automation-support-for-standard-controls"></a>標準控制項的 UI 自動化支援

本主題將識別 Microsoft 消費者介面自動化支援的標準 Windows 控制項。 只有 (Windows XP 及更新版本) 提供的 ComCtrl32.dll 版本6的控制項才會提供完整的支援。

> [!Note]  
> RichEdit 控制項僅支援 Windows Vista (RichEd20.dll 3.1 版和更新版本中隨附的版本，以及 MsftEdit.dll 4.1 版和更新版本的) 。

 

下表列出支援的標準控制項的類別名稱，以及對應的消費者介面自動化控制項類型。



| 類別名稱          | 控制項類型        |
|---------------------|---------------------|
| Button              | Button              |
| Button              | RadioButton         |
| 按鈕              | Group               |
| 按鈕              | 核取方塊            |
| 按鈕              | Hyperlink           |
| 按鈕              | SplitButton         |
| 按鈕              | 核取方塊            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| 編輯                | 文件            |
| 編輯                | 編輯                |
| SysLink             | Hyperlink           |
| Static              | Text                |
| Static              | Image               |
| SysIPAddress32      | 自訂              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | List                |
| ListBox             | List                |
| ListBox             | ListItem            |
| \#32768             | 功能表                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | 進度列         |
| RichEdit            | 文件。 請參閱附註。 |
| RichEdit20A         | 文件            |
| RichEdit20W         | 文件            |
| RichEdit50W         | 文件            |
| ScrollBar           | 滑桿              |
| msctls \_ trackbar32  | 滑桿              |
| msctls \_ updown32    | Spinner             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | 索引標籤                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | 按鈕              |
| ToolbarWindow32     | 核取方塊            |
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
| SysAnimate32                                  | Image        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | 自訂       |
| SysMonthCal32                                 | Calendar     |
| MS \_ WINNOTE                                   | 工具提示      |
| VBBubble                                      | 工具提示      |
| ScrollBar (當做獨立控制項使用時) | 滑桿       |
| SuperGrid                                     | 自訂       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




