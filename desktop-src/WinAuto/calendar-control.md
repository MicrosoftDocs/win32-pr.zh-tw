---
title: '行事曆控制項 (MSAA UI 元素參考) '
description: 行事曆控制項提供簡單且直覺的方式，讓使用者從熟悉的介面中選取日期。
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839664"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>行事曆控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題說明用於 MSAA UI 專案參考之行事 **曆控制項** 物件的用途。 此處未說明如何在各種 UI 架構中建立行事 **曆控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

行事曆控制項提供簡單且直覺的方式，讓使用者從熟悉的介面中選取日期。

月曆控制項的視窗類別名稱是 MONTHCAL \_ 類別，其定義為 Commctrl 中的 "SysMonthCal32"。 本主題中的資訊適用于 Commctrl 第5版中的月曆控制項。

## <a name="iaccessible-methods"></a>IAccessible 方法

行事曆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

行事曆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | **Name** 屬性是從標記行事曆控制項的靜態文字控制項取得。 當您建立控制項時，伺服器開發人員必須確保靜態文字控制項會緊接在定位順序中所標記的控制項之前。                                                                                                                                                                                                                 |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                             |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | **Role** 屬性是 [**role \_ SYSTEM \_ CLIENT**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態系統無法 \_ \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)的狀態系統焦點狀態系統可 \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





