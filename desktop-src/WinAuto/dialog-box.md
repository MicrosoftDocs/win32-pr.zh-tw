---
title: '對話方塊 (MSAA UI 元素參考) '
description: 對話方塊是一種暫存視窗，可讓應用程式建立以抓取使用者輸入。
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682416"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>對話方塊 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **對話方塊** 物件。 此處未說明如何在各種 UI 架構中建立 **對話方塊** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

對話方塊是一種暫存視窗，可讓應用程式建立以抓取使用者輸入。 應用程式會使用對話方塊來提示使用者輸入使用者從功能表中選擇之命令的其他相關資訊。 對話方塊包含一或多個控制項 (子視窗) 使用者輸入文字、選擇選項，或指示命令的動作。

對話方塊的視窗類別名稱是 " \# 32770"。

## <a name="iaccessible-methods"></a>IAccessible 方法

對話方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | 如果對話方塊包含預設的 [按下] 按鈕， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)方法會使用 [**BM \_ 按一下**](/windows/desktop/Controls/bm-click)按鈕訊息來呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，以按一下預設的 [推送] 按鈕。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

對話方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | **ChildCount** 屬性等於對話方塊上的子視窗控制項數目。                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | 如果對話方塊包含預設的 [按下] 按鈕， **DefaultAction** 屬性就會是 "push"。                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | 對話方塊通常沒有鍵盤快速鍵。 如果對話方塊的視窗文字包含 & 符號 (&) 字元，Microsoft Active Accessibility 會傳回非 Null 字串做為 **KeyboardShortcut** 屬性。                                                                                                                                                                                                                                        |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | [ **名稱** ] 屬性是顯示在對話方塊標題列中的視窗文字或標題。                                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | **父** 屬性是 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，此視窗會圍繞對話方塊，而且具有與對話方塊相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                        |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | **Role** 屬性是 [**角色 \_ 系統 \_ 對話方塊**](object-roles.md)或 [**角色 \_ 系統 \_ PROPERTYPAGE**](object-roles.md)。                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>備註

對話方塊物件不支援 [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) 方法。 若要取得對話方塊上控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標，用戶端必須取得控制項的視窗控制碼，然後呼叫 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

