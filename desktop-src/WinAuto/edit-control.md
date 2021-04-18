---
title: '編輯控制項 (MSAA UI 元素參考) '
description: 編輯控制項可讓使用者查看和編輯文字。
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dde6e562b651b91376bc7d675b2b71ac999cf48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507456"
---
# <a name="edit-control-msaa-ui-element-reference"></a>編輯控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明如何 **編輯控制項** 物件，以用於 MSAA UI 元素參考。 此處未說明如何在不同的 UI 架構中建立 **編輯控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

編輯控制項可讓使用者查看和編輯文字。 您可以使用許多不同的樣式來建立編輯控制項，例如 ES \_ 多行。 此樣式會建立多行編輯控制項（例如 [記事本] 的工作區）和 [ES \_ READONLY]，以建立唯讀編輯控制項。

Microsoft Active Accessibility 不會區分以視窗類別名稱 "EDIT" 建立的編輯控制項，以及以視窗類別名稱 "RichEdit" 或 "RichEdit20A" 建立的 rich edit 控制項。

## <a name="iaccessible-methods"></a>IAccessible 方法

編輯控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

編輯控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是編輯控制項的存取金鑰，在編輯控制項的標籤文字中是加上底線的字元。 例如，在標準檔案開啟對話方塊（例如 WordPad）中，標示為 "Filename：" 的編輯控制項的 **KeyboardShortcut** 是 "Alt + n"。                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | **Name** 屬性是靜態文字控制項中標記編輯控制項的文字。 例如，在標準的 [開啟] 對話方塊中（例如在 [WordPad] 中），編輯控制項的 [ **名稱** ] 屬性為 [檔案名：]。                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**角色 \_ 系統 \_ 文字**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 不可見**](object-state-constants.md) \| [**狀態系統可 \_ \_ 設定焦點**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 唯讀**](object-state-constants.md) \| [**狀態系統 \_ \_ 保護**](object-state-constants.md) \| [**狀態系統 \_ \_ 正常**](object-state-constants.md)<br/> |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | **Value** 屬性是包含編輯控制項中文字的單一字串。 但是，如果控制項受到密碼保護，則 **Value** 屬性會傳回 E \_ ACCESSDENIED。 若為多行編輯控制項，此字串會在每一行的結尾包含換行字元和分行符號。                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>備註

-   Microsoft Active Accessibility 不支援選取 [編輯] 和 [rich edit] 控制項中包含的文字，因為該文字會在物件的 [ **值** ] 屬性中公開為字串。
-   Riched20.dll (所提供的 rich edit 控制項（用於 Windows 98 中的 WordPad）) 在文字選取期間變更插入號位置時，不會傳送任何 WinEvents。 當使用者按下 SHIFT 和方向鍵選取文字時，插入號物件不會觸發 [**事件 \_ 物件 \_ LOCATIONCHANGE**](event-constants.md) new-winevent。 當您透過 rich edit 訊息以程式設計方式設定選取專案時，插入號物件不會傳送任何事件來指出其新位置。

    使用 Riched20.dll 的所有應用程式都會出現此問題。 使用較舊版本之 rich edit 控制項的應用程式，會根據選取專案正確地傳送事件。

-   密碼編輯控制項的 **狀態** 值一律包含 [**\_ \_ 受保護**](object-state-constants.md)的位旗標狀態系統。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





