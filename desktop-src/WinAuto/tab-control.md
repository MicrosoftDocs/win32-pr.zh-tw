---
title: '索引標籤控制項 (MSAA UI 元素參考) '
description: 索引標籤控制項會針對視窗或對話方塊的相同區域，定義多個頁面。
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fe3216194da590b0c0802343afc41b1f7765c13d194e533163f9af2c22b287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505658"
---
# <a name="tab-control-msaa-ui-element-reference"></a>索引標籤控制項 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 元素參考的 **索引標籤控制項** 物件。 此處未說明如何在各種 UI 架構中建立 **索引標籤控制項** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

索引標籤控制項會針對視窗或對話方塊的相同區域，定義多個頁面。 每個頁面都包含一組資訊，或是當使用者選取對應的索引標籤時，應用程式所顯示的一組控制項。Windows 作業系統使用索引標籤控制項來顯示工作列按鈕，但 [**開始**] 按鈕除外。

索引標籤控制項的視窗類別名稱是 WC \_ TABCONTROL，其定義為 Commctrl 中的 "SysTabControl"。

## <a name="iaccessible-methods"></a>IAccessible 方法

索引標籤控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | [**AccDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)方法會按一下 [頁面] 索引標籤。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

索引標籤控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | **DefaultAction** 屬性為 "Switch"。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是索引標籤控制項的存取金鑰，也就是控制項視窗文字中的加底線字元。 此字串包含附加至字串 "Alt +" 的存取金鑰字元。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | **Name** 屬性是從控制項的視窗文字 (或標題) （顯示在索引標籤控制項內）取得。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是 ([**角色 \_ 系統 \_ PAGETABLIST**](object-roles.md) ) 的視窗，它會圍繞控制項，而且具有與控制項相同的視窗類別名稱。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性為 [**role \_ SYSTEM \_ PAGETAB**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統可 \_ 選取**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 選取**](object-state-constants.md)的 \| [**狀態系統 \_ \_**](object-state-constants.md)已 \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ 按下**](object-state-constants.md)狀態系統焦點狀態系統<br/> |



 

## <a name="notes"></a>備註

\_當使用 [**SELFLAG \_ TAKEFOCUS**](selflag.md)旗標呼叫 [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)方法時，Tab 控制項會錯誤地傳回 S OK。 索引標籤控制項無法取得鍵盤焦點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





