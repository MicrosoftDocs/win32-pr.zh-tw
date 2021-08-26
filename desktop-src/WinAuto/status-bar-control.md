---
title: '狀態列控制項 (MSAA UI 元素參考) '
description: 狀態列會在應用程式視窗底部的水準視窗中顯示狀態資訊。
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998058"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>狀態列控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之 **狀態列控制項** 物件的用途。 此處未說明如何在各種 UI 架構中建立 **狀態列控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

狀態列會在應用程式視窗底部的水準視窗中顯示狀態資訊。 狀態列通常會分成幾個部分，稱為「窗格」，而每個窗格會顯示不同的狀態資訊。 此外，狀態列也可以包含不同類型的物件，包括按鈕和進度列。 狀態列控制項的視窗類別名稱是 STATUSCLASSNAME，其定義為 Commctrl 中的 "msctls \_ statusbar32"。

## <a name="iaccessible-methods"></a>IAccessible 方法

狀態列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

狀態列支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | **ChildCount** 屬性是狀態列中的窗格數目。                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | 狀態列物件本身沒有 **名稱** 屬性。 狀態列中每個窗格的 [ **名稱** ] 屬性與顯示的文字相同。                                                                                                                                                                                                                                                                                                                   |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | 狀態列物件的 **父** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有與控制項相同的視窗類別名稱。 狀態列中窗格的 **父** 屬性是狀態列物件。                                                                                                                                                                           |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | 狀態列物件本身的 **角色** 屬性是 [**角色 \_ 系統的 \_ 狀態列**](object-roles.md)。 狀態列中顯示的文字具有 [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md) 作為其 **角色** 屬性。                                                                                                                                                                                                 |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>備註

因為狀態列控制項或狀態列上的文字區域不支援鍵盤快速鍵，所以不支援 [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





