---
title: '功能表列 (MSAA UI 元素參考) '
description: 功能表列是緊接在標題列下方的視窗區域，其中包含 [檔案]、[編輯]、[視窗] 和 [說明] 等功能表項目。
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507232"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>功能表列 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之 **功能表列** 物件的用途。 此處未說明如何在各種 UI 架構中建立 **功能表列** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

功能表列是緊接在標題列下方的視窗區域，其中包含 [檔案 **]、[****編輯**]、[**視窗]****和 [** 說明] 等功能表項目。 Microsoft Active Accessibility 也會建立 [系統] 功能表的功能表列物件（標題列左上角的功能表），並包含功能表項目，例如 [ **還原**]、[ **移動**]、[ **大小**]、[ **最小化**] 和 [ **最大化**]。

> [!Note]  
> 因為功能表列控制項不會收到焦點，所以這個控制項不支援 [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 和 [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) 方法。

 

## <a name="iaccessible-methods"></a>IAccessible 方法

功能表列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

功能表列控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | 針對指定的功能表項目抓取 [**IDispatch**](idispatch-interface.md) 。 功能表項目的子識別碼會依序從1開始以左至右編號。                                                                                                                                                                                             |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性是功能表列上的功能表項目數目。 系統功能表的 **ChildCount** 屬性是一個。                                                                                                                                                                                                                                                   |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | 功能表列的 [ **描述** ] 屬性是「包含用來操作目前的視圖或檔的命令」。 系統功能表的 [ **描述** ] 屬性是「包含用來操作視窗的命令」。                                                                                                                                                                   |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | 標題列下方的功能表列的 [ **KeyboardShortcut** ] 屬性是 [Alt]。 系統功能表的 **KeyboardShortcut** 屬性是「Alt + 空格鍵」。                                                                                                                                                                                                                             |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | 標題列下方功能表列的 [ **名稱** ] 屬性是 [應用程式]。 系統功能表的 [ **名稱** ] 屬性是 [system]。                                                                                                                                                                                                                                                |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**role \_ SYSTEM \_ 功能表列**](object-roles.md)。                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 聚焦**](object-state-constants.md)的 \| [**狀態系統可 \_ \_ 設定**](object-state-constants.md)目標<br/> |



 

## <a name="notes"></a>備註

系統會觸發一個以上的 [**事件 \_ 系統 \_ MENUSTART**](event-constants.md) 事件，而不一定會有對應的 [**事件 \_ 系統 \_ MENUEND**](event-constants.md) 事件。 此外，系統不會一致地觸發 [**event \_ system \_ MENUPOPUPSTART**](event-constants.md) 和 [**event \_ system \_ MENUPOPUPEND**](event-constants.md) 事件。 這是已知的問題，並已解決。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**功能表項目**](menu-item.md)
</dt> <dt>

[**快顯功能表**](pop-up-menu.md)
</dt> </dl>

 

 





