---
title: '快速鍵控制 (MSAA UI 元素參考) '
description: 快速鍵控制項可讓使用者輸入按鍵的組合，用來做為快速鍵，讓他們能夠快速執行動作。 快速鍵控制項會顯示使用者輸入的按鍵，並確保使用者選取有效的按鍵組合。
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53829b371ea026c92388e8ed0dac11ee0303514ff930ad1a64ada4b5583bfa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734438"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>快速鍵控制 (MSAA UI 元素參考) 

快速鍵控制項可讓使用者輸入按鍵的組合，用來做為快速鍵，讓他們能夠快速執行動作。 快速鍵控制項會顯示使用者輸入的按鍵，並確保使用者選取有效的按鍵組合。

快速鍵控制項的視窗類別名稱是快速鍵 \_ 類別，在 Commctrl 中定義為 "msctls \_ hotkey32"。

## <a name="iaccessible-methods"></a>IAccessible 方法

快速鍵控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

快速鍵控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性一律為零。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是快速鍵控制項的存取金鑰，也就是快速鍵控制項標籤文字中的加底線字元。 傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。                                                                                                                                                                                                                                 |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | **Name** 屬性是靜態文字控制項中標示快速鍵控制項的文字。                                                                                                                                                                                                                                                                                                                                                                            |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                              |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性為 [**role \_ SYSTEM \_ HOTKEYFIELD**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | **Value** 屬性是一個字串，其中包含快速鍵欄位中的文字。                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





