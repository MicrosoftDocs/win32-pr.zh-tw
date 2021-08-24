---
title: '捲軸 (MSAA UI 元素參考) '
description: 捲軸可讓使用者選擇方向和距離，以在相關的視窗或清單方塊中滾動資訊。 捲軸的視窗類別名稱是 \ 0034;捲軸 \ 0034;。
ms.assetid: a4ec1708-d751-4526-bd69-9796c43872a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6acb609ee56d6e766a2f94cf75406211741ba0a711699f4e8c912790dc71cffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734328"
---
# <a name="scroll-bar-msaa-ui-element-reference"></a>捲軸 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **捲軸** 物件。 此處未說明如何在各種 UI 架構中建立 **捲軸** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

捲軸可讓使用者選擇方向和距離，以在相關的視窗或清單方塊中滾動資訊。 捲軸的視窗類別名稱是「捲軸」。

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於捲軸是垂直或水準，以及用戶端是否正在查詢捲軸的下列部分：

-   捲軸本身
-   右上箭號或向右箭號按鈕
-   右下箭號或向左箭號按鈕
-   捲動方塊 (thumb) 
-   Page up 或 page right 區域
-   Page down 或 page left 區域

## <a name="iaccessible-methods"></a>IAccessible 方法

捲軸支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)-捲軸物件本身和捲動方塊不支援 **accDoDefaultAction** 方法。

    針對垂直捲動條上的其他捲軸部分， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，並將 *wParam* 設定為下列值的 [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)訊息。

    

    | 按鈕/區域       | Vaule        |
    |---------------------|--------------|
    | 上方箭號按鈕    | SB \_ 系列   |
    | 底部箭號按鈕 | SB \_ LINEDOWN |
    | Page up 區域      | SB \_ PAGEUP   |
    | Page down 區域    | SB \_ PAGEDOWN |

    

     

    針對水準捲軸上的其他捲軸部分， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)會呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，並將 *wParam* 設定為下列值的 [**WM \_ HSCROLL**](/windows/desktop/Controls/wm-hscroll)訊息。

    

    | 按鈕/區域      | 值         |
    |--------------------|---------------|
    | 向左箭號按鈕  | SB \_ LINELEFT  |
    | 右箭頭按鈕 | SB \_ LINERIGHT |
    | 左方頁面區域   | SB \_ PAGELEFT  |
    | 頁面右側區域  | SB \_ PAGERIGHT |

    

     

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>IAccessible 屬性

捲軸支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：

-   [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)-捲軸物件的 **ChildCount** 屬性為五。 若為其他捲軸部分， **ChildCount** 屬性為零。
-   [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)-捲軸物件本身和捲動方塊不支援 **DefaultAction** 屬性。 箭號按鈕的 **DefaultAction** 屬性和捲動方塊兩側的陰影區域是「按下」。
-   [**取得 \_ AccDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)： **Description** 屬性取決於所查詢捲軸的部分。

    垂直捲動條的部分具有下列描述。

    

    | 部分                | 描述                                                                         |
    |---------------------|-------------------------------------------------------------------------------------|
    | 捲軸本身   | "用來變更垂直視圖區域"                                          |
    | 上方箭號按鈕    | 「將垂直位置向上移動一行」                                           |
    | 底部箭號按鈕 | 「將垂直位置向下移動一行」                                         |
    | 捲動方塊        | 「表示目前的垂直位置，並且可以拖曳來直接變更」。 |
    | Page up 區域      | 「將垂直位置向上移動幾行」                                  |
    | Page down 區域    | 「表示目前的垂直位置，並且可以拖曳來直接變更」。 |

    

     

    水準捲軸的部分具有下列描述。

    

    | 部分               | 描述                                                                           |
    |--------------------|---------------------------------------------------------------------------------------|
    | 捲軸本身  | "用來變更水準視圖區域"                                          |
    | 向左箭號按鈕  | 「將水準位置向左移動一欄」                                       |
    | 右箭頭按鈕 | 「將水準位置向右移動一欄」                                      |
    | 捲動方塊       | 「表示目前的水準位置，並且可以拖曳來直接變更」 |
    | 左方頁面區域   | 「將水準位置向左移動幾個資料行」                              |
    | 頁面右側區域  | 「表示目前的垂直位置，並且可以拖曳來直接變更」。   |

    

     

-   [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)： [ **名稱** ] 屬性取決於所查詢捲軸的部分。

    垂直捲動條的部分具有下列名稱。

    | 部分                | 名稱        |
    |---------------------|-------------|
    | 捲軸視窗   | 縱  |
    | 上方箭號按鈕    | 「行出」   |
    | 底部箭號按鈕 | 「行出」 |
    | 捲動方塊        | 居  |
    | Page up 區域      | 「Page up」   |
    | Page down 區域    | 「下一頁」 |

    

     

    水準捲軸的部分具有下列名稱。

    

    | 部分               | 名稱           |
    |--------------------|----------------|
    | 捲軸視窗  | 方向   |
    | 向左箭號按鈕  | 「左方資料行」  |
    | 右箭頭按鈕 | 「資料行右」 |
    | 捲動方塊       | 居     |
    | 頁面右側區域  | 「Page right」   |
    | 左方頁面區域   | 「左方頁面」    |

    

     

-   [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)：箭號按鈕的 **父** 屬性、捲動方塊，以及 thumb 兩側的陰影區域是捲軸視窗。 捲軸視窗的 **父** 屬性是視窗 (角色 \_ 系統 \_ 視窗) ，它會圍繞控制項，而且具有相同的 **名稱** 屬性和視窗類別名稱。
-   [**取得 \_ AccRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)- **Role** 屬性取決於所查詢捲軸的部分。 捲軸的部分具有下列角色。 

    | 部分                                                  | 角色                                                                    |
    |-------------------------------------------------------|-------------------------------------------------------------------------|
    | 捲軸本身                                     | [**角色 \_ 系統 \_ 捲軸**](object-roles.md)   |
    | 頂端、向下、向左和向右箭號按鈕              | [**角色 \_ 系統 \_ 按鍵**](object-roles.md) |
    | 捲動方塊                                          | [**角色 \_ 系統 \_ 指標**](object-roles.md)   |
    | Page up、page down、page left 和 page right 區域 | [**角色 \_ 系統 \_ 按鍵**](object-roles.md) |

    

     

-   [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)：每個捲軸元件的 **State** 屬性包含下列 [值](object-state-constants.md)的組合。

    | 狀態                                                                                 | 值                                                                                                                                                                                                                       |
    |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md)     | 如果是捲軸本身，表示指定的垂直或水準捲軸不存在。 若為 page up 或 page down 區域，這表示 thumb 的位置不存在。 |
    | [**狀態 \_ 系統 \_ 外**](object-state-constants.md)     | 如果是捲軸本身，這表示視窗已調整大小，因此目前未顯示指定的垂直或水準捲軸。                                                                         |
    | [**已 \_ \_ 按下狀態系統**](object-state-constants.md)         | 按下箭號按鈕或頁面區域。                                                                                                                                                                                 |
    | [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) | 元件已停用。                                                                                                                                                                                                  |

    

     

-   [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)-捲軸視窗的 [ **值** ] 屬性工作表示捲軸位置，而是包含從 "0" 到 "100" 之整數的字串。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 