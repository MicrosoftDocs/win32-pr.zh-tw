---
title: '推送按鈕 (MSAA UI 元素參考) '
description: '[推送] 按鈕是用來執行動作的小型矩形物件。 例如，對話方塊中的 [確定] 和 [取消] 按鈕是推播按鈕。'
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4056b1b2bd8f80e79916db0056de176962bd7d3d86c2b62420deaf57f90e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644488"
---
# <a name="push-button-msaa-ui-element-reference"></a>推送按鈕 (MSAA UI 元素參考) 

[推送] 按鈕是用來執行動作的小型矩形物件。 例如，對話方塊中的 **[確定] 和 [** **取消** ] 按鈕是推播按鈕。

推播按鈕的視窗類別名稱是「按鈕」。

## <a name="iaccessible-methods"></a>IAccessible 方法

推送按鈕支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | [**AccDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)方法會按一下 [推送] 按鈕。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

[推送] 按鈕支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為零或多個。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | **DefaultAction** 屬性為 "按"。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是按鈕的存取金鑰，也就是按鈕視窗文字文字中的加底線字元。 例如，"Alt + o" 是 **[確定]** 按鈕的 **KeyboardShortcut** 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [ **名稱** ] 屬性是從控制項的視窗文字 (或標題) （顯示在 [推送] 按鈕中）取得。 例如，[確定] 是 **[確定]** 按鈕的 [**名稱**] 屬性。                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**角色 \_ 系統 \_ 按鍵**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態系統可 \_ \_ 設定**](object-state-constants.md) \| [**狀態 \_ 系統已 \_ 按下**](object-state-constants.md) \| [**狀態系統 \_ \_ 預設**](object-state-constants.md)值<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**核取方塊**](check-box.md)
</dt> <dt>

[**群組方塊**](group-box.md)
</dt> <dt>

[**選項按鈕**](radio-button.md)
</dt> </dl>

 

 





