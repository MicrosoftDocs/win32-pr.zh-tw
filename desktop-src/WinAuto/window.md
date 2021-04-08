---
title: '視窗 (MSAA UI 元素參考) '
description: Microsoft Active Accessibility 將一般視窗物件建立為另一個物件的容器。 用戶端開發人員不會將資訊從視窗物件傳遞給終端使用者，因為這些物件不包含有用的資訊。
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672380"
---
# <a name="window-msaa-ui-element-reference"></a>視窗 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之的 **視窗** 物件。 此處未說明如何在各種 UI 架構中建立 **視窗** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

Microsoft Active Accessibility 將一般視窗物件建立為另一個物件的容器。 用戶端開發人員不會將資訊從視窗物件傳遞給終端使用者，因為這些物件不包含有用的資訊。

如果伺服器應用程式建立自訂控制項，Microsoft Active Accessibility 會建立一個包含自訂控制項的 window 物件，但是伺服器會建立一個可存取的物件，以提供控制項內容的相關資訊。 系統會產生 window 物件的物件層級事件，但是伺服器必須傳送可存取物件的事件，以提供控制項的相關資訊。

## <a name="iaccessible-methods"></a>IAccessible 方法

Window 物件支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

Window 物件支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | 抓取指定之子系的 [IDispatch](idispatch-interface.md) 介面。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為7。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | 視窗物件本身沒有 **Description** 屬性。 您可以透過 window 物件抓取子物件的 **Description** 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | 視窗物件本身沒有 **KeyboardShortcut** 屬性。 子物件的 **KeyboardShortcut** 屬性是透過 window 物件來抓取。                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Window 物件的 **Name** 屬性與子物件相同。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**角色 \_ 系統 \_ 視窗**](object-roles.md)。 子物件的 **角色** 是透過 window 物件來抓取。                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 相當大**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 可移動**](object-state-constants.md)狀態 \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)系統的可設定狀態系統焦點<br/> |



 

## <a name="notes"></a>備註

Window 物件不會傳送 events [**事件 \_ 系統 \_ DRAGDROPSTART**](event-constants.md)、 [**事件 \_ 系統 \_ DRAGDROPEND**](event-constants.md)、 [**事件 \_ 物件 \_ 隱藏**](event-constants.md)和 [**事件 \_ 物件 \_ PARENTCHANGE**](event-constants.md) 。 這是已知的問題，並已解決。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





