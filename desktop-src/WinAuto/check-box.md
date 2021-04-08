---
title: '核取方塊 (MSAA UI 元素參考) '
description: 核取方塊可用來啟用或停用集合中的一或多個特徵或選項，通常是在對話方塊中。 一般而言，核取方塊會包含具有相鄰文字的小型方塊。 選取選項時，方塊中會出現核取記號。
ms.assetid: cdbaa152-82c2-4a5b-82a8-fed9b8ed63b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8baacf729e9512b24a6d576a81cab093cffc93c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023775"
---
# <a name="check-box-msaa-ui-element-reference"></a>核取方塊 (MSAA UI 元素參考) 

> [!Note]  
> 本主題將描述用於 MSAA UI 元素參考之的 **核取方塊** 物件。 此處未說明如何在不同的 UI 架構中建立 **核取方塊** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

核取方塊可用來啟用或停用集合中的一或多個特徵或選項，通常是在對話方塊中。 一般而言，核取方塊會包含具有相鄰文字的小型方塊。 選取選項時，方塊中會出現核取記號。

核取方塊的視窗類別名稱為 "BUTTON"。

## <a name="iaccessible-methods"></a>IAccessible 方法

核取方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | [**AccDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)方法會使用 [**BM \_ click**](/windows/desktop/Controls/bm-click)按鈕訊息來呼叫 [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) ，以按一下該核取方塊。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                  |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                  |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                  |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                  |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

核取方塊支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                        | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)        | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)  | 核取方塊的 **DefaultAction** 屬性取決於是否已選取。 未選取的核取方塊會以「檢查」作為其 **DefaultAction**，而選取的核取方塊會將「取消核取」為其 **DefaultAction**。 三個狀態核取方塊的 **DefaultAction** 是 "切換"。                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是核取方塊的存取金鑰，也就是控制項視窗文字中的加底線字元。 此字串包含附加至字串 "Alt +" 的存取金鑰字元。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) 中取得，並顯示覆選框。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) 中取得，並顯示覆選框。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱屬性和視窗類別名稱。**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性為 [**role \_ SYSTEM \_ CHECKBUTTON**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態系統可 \_ \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 混合**](object-state-constants.md)狀態系統 \| [**\_ \_ 已檢查**](object-state-constants.md)狀態系統 \| [**\_ \_ 正常**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

