---
title: '滑杆控制項 (MSAA UI 元素參考) '
description: 滑杆控制項也稱為「資料格控制項」，可讓使用者藉由移動滑杆，從某個範圍的值進行選取。 Windows 作業系統中的音量控制就是滑桿 (Slider Control)。
ms.assetid: 8df4ed1d-d63c-49d7-94f1-df2113643484
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03c39d6638557b9dfff90740132d3e22a7e2511
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022020"
---
# <a name="slider-control-msaa-ui-element-reference"></a>滑杆控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之 **滑杆控制項** 物件的用途。 此處未說明如何在各種 UI 架構中建立 **滑杆控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

滑杆控制項也稱為「資料格控制項」，可讓使用者藉由移動滑杆，從某個範圍的值進行選取。 Windows 作業系統中的音量控制就是滑桿 (Slider Control)。

滑杆控制項的視窗類別名稱是 \_ 在 Commctrl 中定義為 "Msctls" 的 [類標] 類別。 \_

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於滑杆是垂直或水準，以及用戶端是否查詢滑杆控制項的下列部分：

-   滑杆視窗
-   滑杆捲軸
-   上方的陰影區域 (或
-    (或) 滑杆捲動方塊右邊的陰影區域

## <a name="iaccessible-methods"></a>IAccessible 方法

滑杆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

滑杆控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：

-   [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**取得 \_ AccKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)： **KeyboardShortcut** 屬性是滑杆視窗的存取金鑰，也就是滑杆的標籤文字中的底線字元。 傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。
-   [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)： [ **名稱** ] 屬性取決於所查詢之滑杆的部分。

    垂直滑杆的部分具有下列名稱：

    

    | 滑杆部分                    | Name                                |
    |--------------------------------|-------------------------------------|
    | 滑杆視窗                  | 當做標籤使用的靜態文字控制項 |
    | 滑杆捲軸                   | 居                          |
    | 上方的陰影區域滑杆捲軸 | 「Page up」                           |
    | 下滑杆捲動方塊的陰影區域 | 「下一頁」                         |

    

     

    水準滑杆的各部分具有下列名稱：

    

    | 滑杆部分                              | Name                                |
    |------------------------------------------|-------------------------------------|
    | 滑杆視窗                            | 當做標籤使用的靜態文字控制項 |
    | 滑杆捲軸                             | 居                          |
    | 滑杆捲動方塊左邊的陰影區域  | 「左方頁面」                         |
    | 滑杆捲動方塊右邊的陰影區域 | 「Page right」                        |

    

     

-   [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)：箭號按鈕的 **父** 屬性、捲動方塊，以及 thumb 兩側的陰影區域是滑杆視窗。 滑杆視窗的 **Parent** 屬性是視窗 ( [**角色 \_ 系統 \_ 視窗**](object-roles.md) ) ，它會圍繞控制項，而且具有相同的 **名稱** 屬性和視窗類別名稱。
-   [**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **Role** 屬性取決於所查詢之滑杆的部分。 

    | 滑杆部分                                     | [角色](object-roles.md)                                                |
    |-------------------------------------------------|-------------------------------------------------------------------------|
    | 滑杆視窗                                   | [**角色 \_ 系統 \_ 滑杆**](object-roles.md)         |
    | 滑杆捲軸                                    | [**角色 \_ 系統 \_ 指標**](object-roles.md)   |
    | 滑杆捲動方塊兩側的陰影區域 | [**角色 \_ 系統 \_ 按鍵**](object-roles.md) |

    

     

-   [**取得 \_ AccState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)： **State** 屬性的 [值](object-state-constants.md)取決於所查詢之滑杆的部分。 

    | 滑杆部分                                     | 可能的狀態值                                                                                                                                                                                                                                                                                                                                                                                                           |
    |-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 滑杆視窗                                   | [**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md) |
    | 滑杆捲軸                                    | 零 (0) ，表示物件是可見的，或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的狀態 \| [**\_ 系統 \_ 無法使用**](object-state-constants.md)狀態系統 \| [**\_ \_ 正常**](object-state-constants.md)                                                                                                                       |
    | 滑杆捲動方塊兩側的陰影區域 | 零 (0) ，表示物件是可見的，或 [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)的狀態 \| [**\_ 系統 \_ 無法使用**](object-state-constants.md)狀態系統 \| [**\_ \_ 正常**](object-state-constants.md)                                                                                                                       |

    

     

-   [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)：滑杆視窗的 **Value** 屬性會指出 thumb 的位置，而是包含從 "0" 到 "100" 之整數的字串。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**捲軸**](scroll-bar.md)
</dt> </dl>

 

 




