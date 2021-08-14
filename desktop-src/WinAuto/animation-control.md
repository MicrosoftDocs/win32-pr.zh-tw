---
title: '動畫控制項 (MSAA UI 元素參考) '
description: 動畫控制項以無訊息模式顯示交錯 (AVI) 剪輯的音訊影片。 動畫控制項通常會在複製檔案時，或在執行其他一些耗時的工作時顯示。
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c7f134d5acdd3496f76e3399e5aafd1fcb2664aed37e042bb7c2cfca60f922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326852"
---
# <a name="animation-control-msaa-ui-element-reference"></a>動畫控制項 (MSAA UI 元素參考) 

動畫控制項以無訊息模式顯示交錯 (AVI) 剪輯的音訊影片。 動畫控制項通常會在複製檔案時，或在執行其他一些耗時的工作時顯示。

動畫控制項的視窗類別名稱是在 \_ Commctrl 中定義為 "SysAnimate32" 的動畫類別。

## <a name="iaccessible-methods"></a>IAccessible 方法

動畫控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

動畫控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | 動畫控制項沒有鍵盤快速鍵。 但是，如果控制項的標籤包含存取金鑰 (控制項標籤的文字中有加底線的字元) ， [**get \_ accKeyboardShortcut 就**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) 會傳回非 Null 字串。 此字串包含附加至字串 "Alt +" 的存取金鑰字元。 例如，如果標籤為「正在下載檔案」， **KeyboardShortcut** 會是 "Alt + d"。                                                                                        |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | **Name** 屬性是從標記動畫控制項的靜態文字控制項取得。 當您建立控制項時，伺服器開發人員必須確保靜態文字控制項會緊接在定位順序中所標記的控制項之前。                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**角色 \_ 系統 \_ 動畫**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是一或多個下列物件狀態常數的組合：[**狀態 \_ 系統 \_ 不可見**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 聚焦**](object-state-constants.md)的 \| [**狀態 \_ 系統 \_ 動畫**](object-state-constants.md)<br/> 如需詳細資訊，請參閱 [物件狀態常數](object-state-constants.md)。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





