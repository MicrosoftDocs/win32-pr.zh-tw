---
title: '快顯功能表 (MSAA UI 元素參考) '
description: 快顯功能表會顯示功能表命令的清單。
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840380"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>快顯功能表 (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明用於 MSAA UI 專案參考之 **快顯功能表** 物件的用途。 這裡未說明如何在各種 UI 架構中建立 **快顯功能表** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

快顯功能表會顯示功能表命令的清單。 當功能表列中的功能表項目開啟時，Microsoft Active Accessibility 建立功能表快顯物件。 Microsoft Active Accessibility 也會建立快顯功能表的功能表快顯物件，當使用者以滑鼠右鍵按一下使用者介面專案時，就會顯示此物件。

快顯功能表的視窗類別名稱是 " \# 32768"。

## <a name="iaccessible-methods"></a>IAccessible 方法

快顯功能表支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

快顯功能表支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | 針對指定的功能表項目抓取 [**IDispatch**](idispatch-interface.md) 。 功能表項目的子識別碼會依序從上到下編號，從1開始。                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | **ChildCount** 屬性是功能表中功能表項目的數目，包括功能表分隔符號。                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | 快顯功能表的 [ **名稱** ] 屬性與功能表的名稱相同。 內容功能表的 [ **名稱** ] 屬性是「內容」。                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | **父** 屬性是視窗 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) ，它會圍繞快顯功能表，而且具有與快顯功能表相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                      |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | **Role** 屬性為 [**role \_ SYSTEM \_ MENUPOPUP**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>備註

-   快顯功能表物件不會觸發 [**事件 \_ 物件 \_ 建立**](event-constants.md) 和 [**事件 \_ 物件 \_**](event-constants.md) 終結事件。
-   多重資料行功能表不支援 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)方法的 [**NAVDIR \_ LEFT**](navigation-constants.md)或 [**NAVDIR \_ RIGHT**](navigation-constants.md)旗標。
-   Events [**事件 \_ 系統 \_ MENUPOPUPSTART**](event-constants.md) 和 [**event \_ system \_ MENUPOPUPEND**](event-constants.md) 不會以一致方式傳送。 這是已知的問題，並已解決。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**功能表列**](menu-bar.md)
</dt> <dt>

[**功能表項目**](menu-item.md)
</dt> </dl>

 

 





