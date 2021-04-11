---
title: 'Toolbar 控制項 (MSAA UI 元素參考) '
description: 工具列控制項包含執行功能表命令的按鈕，通常包含在功能表列下方的視窗內。
ms.assetid: 2ded8753-0102-4d0b-bf92-0d1084aeca59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213d20bb220ef35d9ebca326962137b784635716
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023532"
---
# <a name="toolbar-control-msaa-ui-element-reference"></a>Toolbar 控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **工具列控制項** 物件。 此處未說明如何在各種 UI 架構中建立 **工具列控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

工具列控制項包含執行功能表命令的按鈕，通常包含在功能表列下方的視窗內。

工具列控制項的視窗類別名稱是 TOOLBARCLASSNAME，在 Commctrl 中定義為 "ToolbarWindow32"。

## <a name="iaccessible-methods"></a>IAccessible 方法

工具列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | 工具列本身支援 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 方法。 針對工具列上的按鈕， **accDoDefaultAction** 會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，並使用 [**BM \_ click**](/windows/desktop/Controls/bm-click) message 來按一下指定的按鈕。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                                          |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                                          |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                                          |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                                          |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

工具列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性是工具列中包含的控制項數目。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | 工具列物件本身沒有 **DefaultAction** 屬性。 工具列按鈕的 **DefaultAction** 屬性取決於工具列按鈕樣式。 具有 [樣式 TBSTYLE \_ ] 下拉式清單的按鈕具有 [開啟] 作為其 **DefaultAction** 屬性。 所有其他工具列按鈕的 **DefaultAction** 屬性為「按下」。                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | 工具列沒有鍵盤快速鍵。 但是，如果工具列的視窗文字包含 (&) 字元的連字號，Microsoft Active Accessibility 會傳回非 Null 字串做為 **KeyboardShortcut** 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | 工具列的 [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) 取得。 此文字不會與工具列一起顯示，因此伺服器開發人員必須在控制項的資源定義語句中提供有意義的文字，以協助用戶端公用程式的使用者識別控制項。 您可以使用 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) 函數來設定視窗文字。                                                                                                                                                                                                                                                                                                                                                            |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**role \_ SYSTEM \_ 工具列**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | 工具列本身的 [**狀態**] 屬性 [值](object-state-constants.md)為零，表示物件是可見的。 工具列按鈕的 [ **狀態** ] 屬性可能的值為： [ [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) ] 或<br/> [**狀態 \_系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 可移動**](object-state-constants.md) \| [**狀態 \_ 系統 \_**](object-state-constants.md)焦點 \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md)目標<br/> |



 

## <a name="notes"></a>備註

工具列上的按鈕會傳送 [**事件 \_ 物件 \_ STATECHANGE**](event-constants.md) 事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

