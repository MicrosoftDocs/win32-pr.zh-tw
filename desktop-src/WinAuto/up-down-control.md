---
title: 'Up-Down 控制項 (MSAA UI 元素參考) '
description: 由上而下的控制項（也稱為微調控制項）結合了一組顯示為箭號的按鈕與一個好友編輯控制項。 按一下箭號會遞增或遞減編輯控制項中的值。
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b9475d8bbca24d2bf536a4eb9a9decf078297e788a37aa4d8560029a67e50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114623"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Up-Down 控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題將針對 MSAA UI 元素參考的目的，描述 **最新的控制項** 物件。 此處不會說明如何在各種 UI 架構中建立 **最下層的控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

由上而下的控制項（也稱為微調控制項）結合了一組顯示為箭號的按鈕與一個好友編輯控制項。 按一下箭號會遞增或遞減編輯控制項中的值。

上下按鈕控制項的視窗類別名稱是上下按鈕 \_ 類別，其定義為 Commctrl 中的 "msctls \_ updown32"。

## <a name="iaccessible-methods"></a>IAccessible 方法

上下控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

上下控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | **ChildCount** 屬性為 "2" (向上箭號和向下箭號按鈕) 。                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | 上下按鈕控制項物件的 [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) 取得。 此文字不會與上下按鈕控制項一起顯示，因此伺服器開發人員必須在控制項的資源定義語句中提供有意義的文字，以協助用戶端公用程式的使用者識別控制項。 上下箭號控制項中上方箭號按鈕的 [ **名稱** ] 屬性是 [更多]，而底部箭號按鈕的 [ **名稱** ] 屬性則是「Less」。 |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | 上下按鈕控制項的 **Parent** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。 向上和向下箭號按鈕的 **父** 屬性是上下按鈕控制項物件。                                                                                                                                                    |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | 由上而下控制物件的 **role** 屬性是 [**由 \_ 角色 \_ 系統**](object-roles.md)調整。 箭號按鈕的 **role** 屬性是 [**角色 \_ 系統 \_ 按鍵**](object-roles.md)。                                                                                                                                                                                                                          |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | 由上而下控制物件的 state 屬性是下列其中一個 [值](object-state-constants.md)：以 [**狀態 \_ 系統為 \_ 焦點**](object-state-constants.md)的 \| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>備註

Microsoft Active Accessibility 會將好友編輯控制項公開為個別的物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





