---
title: '其他物件角色和支援的方法 (MSAA UI 元素參考) '
description: 本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443999"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>其他物件角色和支援的方法 (MSAA UI 元素參考) 

本主題提供的物件角色相關資訊，不包含在 UI 元素的前幾個主題中。 每個物件角色都包含物件角色所支援的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法和屬性清單。 雖然其他主題檔支援 UI 元素的 **IAccessible** 方法和屬性，但本主題會列出您可以預期針對特定物件角色支援的方法和屬性。 許多可能具有此處所列其中一個角色的 UI 元素，通常會在瀏覽器中看到。

> [!Note]  
> 請使用本主題作為指導方針。 強烈建議您使用 Microsoft Active Accessibility 工具來確認個別物件角色的預期行為。

 

下表列出 Oleacc.dll 支援的其他物件角色。



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**角色 \_ 系統 \_ 警示**](/windows)                           | [**角色 \_ 系統 \_ DROPLIST**](/windows)       |
| [**角色 \_ 系統 \_ 應用程式**](/windows)               | [**角色 \_ 系統方程式 \_**](/windows)       |
| [**角色 \_ 系統 \_ 框線**](/windows)                         | [**角色 \_ 系統 \_ 圖形**](/windows)         |
| [**角色 \_ 系統 \_ BUTTONDROPDOWN**](/windows)         | [**角色 \_ 系統 \_ HELPBALLOON**](/windows) |
| [**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**](/windows) | [**角色 \_ 系統 \_ IPADDRESS**](/windows)     |
| [**角色 \_ 系統 \_ BUTTONMENU**](/windows)                 | [**角色 \_ 系統 \_ 連結**](/windows)               |
| [**角色 \_ 系統 \_ 儲存格**](/windows)                             | [**角色 \_ 系統 \_ 窗格**](/windows)               |
| [**角色 \_ 系統 \_ 字元**](/windows)                   | [**角色 \_ 系統資料 \_ 列**](/windows)                 |
| [**角色 \_ 系統 \_ 圖表**](/windows)                           | [**角色 \_ 系統 \_ ROWHEADER**](/windows)     |
| [**角色 \_ 系統 \_ 時鐘**](/windows)                           | [**角色 \_ 系統 \_ 分隔符號**](/windows)     |
| [**角色 \_ 系統資料 \_ 行**](/windows)                         | [**角色 \_ 系統 \_ 音效**](/windows)             |
| [**角色 \_ 系統 \_ 圖表**](/windows)                       | [**角色 \_ 系統 \_ SPLITBUTTON**](/windows) |
| [**角色 \_ 系統 \_ 撥號**](/windows)                             | [**角色 \_ 系統 \_ 資料表**](/windows)             |
| [**角色 \_ 系統 \_ 檔**](/windows)                     | [**角色 \_ 系統 \_ 空白字元**](/windows)   |



 

## <a name="role_system_alert"></a>角色 \_ 系統 \_ 警示

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 警示**](object-roles.md)。

**支援的屬性和方法**

-   取得 \_ accName
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_application"></a>角色 \_ 系統 \_ 應用程式

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 應用程式**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_border"></a>角色 \_ 系統 \_ 框線

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 框線**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_buttondropdown"></a>角色 \_ 系統 \_ BUTTONDROPDOWN

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWN**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_buttondropdowngrid"></a>角色 \_ 系統 \_ BUTTONDROPDOWNGRID

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONDROPDOWNGRID**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_buttonmenu"></a>角色 \_ 系統 \_ BUTTONMENU

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ BUTTONMENU**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accDefaultAction
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_cell"></a>角色 \_ 系統 \_ 儲存格

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 儲存格**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_character"></a>角色 \_ 系統 \_ 字元

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 字元**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accDescription
-   取得 \_ accFocus
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_chart"></a>角色 \_ 系統 \_ 圖表

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_clock"></a>角色 \_ 系統 \_ 時鐘

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 時鐘**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_column"></a>角色 \_ 系統資料 \_ 行

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 行**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_diagram"></a>角色 \_ 系統 \_ 圖表

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖表**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_dial"></a>角色 \_ 系統 \_ 撥號

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 撥號**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accDefaultAction
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_document"></a>角色 \_ 系統 \_ 檔

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 檔**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_droplist"></a>角色 \_ 系統 \_ DROPLIST

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ DROPLIST**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_equation"></a>角色 \_ 系統方程式 \_

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_**](object-roles.md)方程式。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accFocus
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_graphic"></a>角色 \_ 系統 \_ 圖形

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 圖形**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_helpballoon"></a>角色 \_ 系統 \_ HELPBALLOON

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ HELPBALLOON**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_ipaddress"></a>角色 \_ 系統 \_ IPADDRESS

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ IPADDRESS**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_link"></a>角色 \_ 系統 \_ 連結

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 連結**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accDescription
-   取得 \_ accFocus
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_pane"></a>角色 \_ 系統 \_ 窗格

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 窗格**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_row"></a>角色 \_ 系統資料 \_ 列

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統資料 \_ 列**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDescription
-   取得 \_ accFocus
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_rowheader"></a>角色 \_ 系統 \_ ROWHEADER

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ ROWHEADER**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDefaultAction
-   取得 \_ accDescription
-   取得 \_ accFocus
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState
-   取得 \_ accValue

## <a name="role_system_separator"></a>角色 \_ 系統 \_ 分隔符號

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 分隔符號**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_sound"></a>角色 \_ 系統 \_ 音效

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 音效**](object-roles.md)。

**支援的屬性和方法**

-   取得 \_ accDescription
-   取得 \_ accName
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_splitbutton"></a>角色 \_ 系統 \_ SPLITBUTTON

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ SPLITBUTTON**](object-roles.md)。

**支援的屬性和方法**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   取得 \_ accDefaultAction
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_table"></a>角色 \_ 系統 \_ 資料表

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 資料表**](object-roles.md)。

**支援的屬性和方法**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   取得 \_ accChild
-   取得 \_ accChildCount
-   取得 \_ accDescription
-   取得 \_ accFocus
-   取得 \_ accHelp
-   取得 \_ accHelpTopic
-   取得 \_ accKeyboardShortcut
-   取得 \_ accName
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

## <a name="role_system_whitespace"></a>角色 \_ 系統 \_ 空白字元

如需此角色的詳細資訊，請參閱 [**角色 \_ 系統 \_ 空白**](object-roles.md)。

**支援的屬性和方法**

-   accLocation
-   accSelect
-   取得 \_ accParent
-   取得 \_ accRole
-   取得 \_ accState

 

 