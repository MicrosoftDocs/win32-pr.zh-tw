---
title: '下拉式方塊 (MSAA UI 元素參考) '
description: 下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。
ms.assetid: 3fb2c0b0-507f-4520-845b-b3fbfd9e7b60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce42bb3b0316b0fb2668fed23564b8f904fc793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673599"
---
# <a name="combo-box-msaa-ui-element-reference"></a>下拉式方塊 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之 **下拉式列示方塊** 物件的用途。 此處未說明如何在各種 UI 架構中建立 **下拉式列示方塊** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。 控制項的清單方塊部分會隨時顯示，或只有在使用者選取下拉式箭號時，才會顯示下拉式箭號 (也就是控制項旁邊) 的 [按下] 按鈕。 如果選取欄位是編輯控制項，則使用者可以輸入不在清單中的資訊;否則，使用者只能選取清單中的專案。

下拉式方塊的視窗類別名稱是「COMBOBOX」。

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)屬性的內容取決於用戶端查詢下拉式方塊的下列哪些部分：

-   下拉式方塊視窗
-   編輯控制項或靜態文字控制項
-   下拉箭號 (是按下按鈕) 
-   清單方塊
-   清單方塊中的清單專案

## <a name="iaccessible-methods"></a>IAccessible 方法

下拉式方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

下拉式方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：

-   [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)
-   [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)-下表顯示下拉式方塊中不同部分的子計數值。 

    | 下拉式方塊元件   | ChildCount               |
    |------------------|--------------------------|
    | 下拉式方塊視窗 | 3                        |
    | 編輯控制項     | 0                        |
    | 下拉箭號  | 0                        |
    | 清單方塊         | 清單專案的數目 |
    | 清單項目        | 0                        |

    

     

-   [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)-下表顯示下拉式方塊中不同部分的 **DefaultAction** 屬性。 

    | 下拉式方塊元件   | DefaultAction                                                  |
    |------------------|----------------------------------------------------------------|
    | 下拉式方塊視窗 | 無                                                           |
    | 編輯控制項     | 無                                                           |
    | 下拉箭號  | [開啟] 或 [關閉]，視下拉式清單的狀態而定 |
    | 清單方塊         | 無                                                           |
    | 清單項目        | [按兩下]                                                 |

    

     

-   [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)
-   [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)
-   [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)
-   [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)-下表顯示下拉式方塊中不同部分的 **KeyboardShortcut** 屬性。 

    | 下拉式方塊元件   | KeyboardShortcut               |
    |------------------|--------------------------------|
    | 下拉式方塊視窗 | 相關標籤的存取金鑰 |
    | 編輯控制項     | 無                           |
    | 下拉箭號  | "Alt + 向下鍵"               |
    | 清單方塊         | 無                           |
    | 清單項目        | 無                           |

    

     

    下拉式方塊的存取金鑰是標示下拉式方塊之相關聯靜態文字控制項文字中的加底線字元。 例如，在開啟檔案的標準開啟對話方塊（例如 Microsoft WordPad）中，標示為 "Files of type：" 的下拉式方塊具有 **KeyboardShortcut** "Alt + t"。

-   [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)-下表顯示下拉式方塊中不同部分的 **名稱** 屬性。 

    | 下拉式方塊元件   | Name                                                           |
    |------------------|----------------------------------------------------------------|
    | 下拉式方塊視窗 | 當做標籤使用的靜態文字控制項                            |
    | 編輯控制項     | 當做標籤使用的靜態文字控制項                            |
    | 下拉箭號  | [開啟] 或 [關閉]，視下拉式清單的狀態而定 |
    | 清單方塊         | 相關聯的標籤                                               |
    | 清單項目        | 清單專案的文字                                          |

    

     

    下拉式方塊的 [ **名稱** ] 屬性、其子編輯控制項，以及其子清單方塊，都是關聯的靜態文字控制項中標示下拉式方塊的文字。 例如，在開啟檔案的標準開啟對話方塊中（例如在 WordPad 中），兩個下拉式方塊的 **名稱** 屬性是「查詢：」和「檔案類型：」。

-   [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)-下表顯示下拉式方塊中不同部分的父值。 

    | 下拉式方塊元件                        | 父代                                                                                                                                                                                                         |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 下拉式方塊視窗                      | 具有 [**角色 \_ 系統 \_ 視窗**](object-roles.md)的 **role** 屬性的視窗，此視窗會圍繞下拉式方塊，且具有與下拉式方塊相同的 **名稱** 屬性和視窗類別名稱。 |
    | 編輯控制項 (或靜態文字控制項)  | 下拉式方塊視窗。                                                                                                                                                                                          |
    | 下拉箭號                       | 下拉式方塊視窗。                                                                                                                                                                                          |
    | 清單方塊父視窗                | 下拉式方塊視窗。 此視窗會圍繞在清單方塊中。                                                                                                                                                      |
    | 清單方塊                              | 清單方塊父視窗。                                                                                                                                                                                    |
    | 清單項目                             | 清單方塊。                                                                                                                                                                                                  |

    

     

-   [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)-下表顯示下拉式方塊中不同部分的 **角色** 屬性。 

    | 下拉式方塊元件                        | [角色](object-roles.md)                                                                                                               |
    |---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
    | 下拉式方塊視窗                      | [**角色 \_ 系統 \_ COMBOBOX**](object-roles.md)                                                                    |
    | 編輯控制項 (或靜態文字控制項)  | [**角色 \_系統 \_ 文字**](object-roles.md) 或 [**角色 \_ 系統 \_ STATICTEXT**](object-roles.md) |
    | 下拉箭號                       | [**角色 \_ 系統 \_ 按鍵**](object-roles.md)                                                                |
    | 清單方塊                              | [**角色 \_ 系統 \_ 清單**](object-roles.md)                                                                            |
    | 清單項目                             | [**角色 \_ 系統 \_**](object-roles.md)                                                                    |

    

     

-   [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)-下表顯示下拉式方塊的不同部分的 **狀態** 屬性。 

    | 下拉式方塊元件   | [可能的狀態](object-state-constants.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
    |------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 下拉式方塊視窗 | [**狀態 \_系統 \_ 隱藏**](object-state-constants.md)式 \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 一般**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 展開**](object-state-constants.md) \| [**狀態 \_ \_**](object-state-constants.md)系統已折迭 |
    | 編輯控制項     | [**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)                                                                                                                                                                         |
    | 下拉箭號  | 0，表示按鈕為可見且未按下。或 [**狀態 \_ 系統已 \_ 按下**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| 狀態 \_ 系統 \_ 正常                                                                                                                                                                                                                                                                                                                                                    |
    | 清單方塊         | [**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 浮動**](object-state-constants.md) \| [**狀態系統 \_ \_ 正常**](object-state-constants.md)                                                                                      |
    | 清單項目        | [**狀態 \_系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 設定焦點**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 選取**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 選取**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)                                                                                        |

    

     

-   [**取得 \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)-下表顯示下拉式方塊中不同部分的 [ **值** ] 屬性。 

    | 下拉式方塊元件   | 值                                |
    |------------------|--------------------------------------|
    | 下拉式方塊視窗 | 目前選取清單專案的文字 |
    | 編輯控制項     | 目前選取清單專案的文字 |
    | 下拉箭號  | 無                                 |
    | 清單方塊         | 無                                 |
    | 清單項目        | 無                                 |

    

     

## <a name="notes"></a>備註

-   在下拉式方塊的清單方塊中，使用 [ [**NAVDIR \_ 下一個**](navigation-constants.md)] 旗標呼叫 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)時，它會在應該傳回 **VT \_ 空白** 的情況下，不正確地流覽至系統匣視窗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




