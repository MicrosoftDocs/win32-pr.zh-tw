---
title: '用戶端物件 (MSAA UI 元素參考) '
description: 工作區是視窗的一部分，其中應用程式會顯示輸出，例如文字或圖形。 例如，桌面發佈應用程式會在工作區中顯示檔的目前頁面。
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092852"
---
# <a name="client-object-msaa-ui-element-reference"></a>用戶端物件 (MSAA UI 元素參考) 

工作區是視窗的一部分，其中應用程式會顯示輸出，例如文字或圖形。 例如，桌面發佈應用程式會在工作區中顯示檔的目前頁面。

伺服器應用程式開發人員負責建立可存取的物件，以提供應用程式工作區內容的相關資訊。

如果用戶端應用程式要求應用程式內自訂 UI 元素的相關資訊，以及不支援 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的自訂 ui 元素，Microsoft Active Accessibility 會以最基本的資訊建立預設的可存取物件。

## <a name="iaccessible-methods"></a>IAccessible 方法

工作區支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

工作區支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | 傳送 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) 訊息以取得視窗文字。                                                                                                                                                                                                                                                                                                                                                                                |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**role \_ SYSTEM \_ CLIENT**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

