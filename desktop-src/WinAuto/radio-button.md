---
title: '選項按鈕 (MSAA UI 元素參考) '
description: 選項按鈕是用來選取數個選項的其中一個，通常是在對話方塊中。
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c560e4efa57790980d852ab2716248d5b1d7faff535592f3f2ca892f3dff0715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998138"
---
# <a name="radio-button-msaa-ui-element-reference"></a>選項按鈕 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **選項按鈕** 物件。 此處未說明如何在各種 UI 架構中建立 **選項按鈕** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

選項按鈕是用來選取數個選項的其中一個，通常是在對話方塊中。 選項按鈕包含具有文字旁邊的小圓圈。 選取時，圓形裡面會有較小的實心圓形。 選取集合中的一個按鈕可取消選取先前選取的按鈕，因此一次只會選取集合中的其中一個選項。

選項按鈕的視窗類別名稱是「按鈕」。

## <a name="iaccessible-methods"></a>IAccessible 方法

選項按鈕支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | [**AccDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)方法會按一下選項按鈕。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

選項按鈕支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | 選項按鈕的 **DefaultAction** 屬性為「檢查」。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是選項按鈕的存取金鑰，也就是控制項視窗文字中的加底線字元。 此字串包含附加至字串 "Alt +" 的存取金鑰字元。                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) （與選項按鈕一起顯示）取得。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**role \_ SYSTEM \_ 選項按鈕**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態系統可 \_ \_ 設定**](object-state-constants.md) \| [**狀態系統 \_ \_ 已檢查**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 正常**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**核取方塊**](check-box.md)
</dt> <dt>

[**群組方塊**](group-box.md)
</dt> <dt>

[**按鈕**](push-button.md)
</dt> </dl>

 

 





