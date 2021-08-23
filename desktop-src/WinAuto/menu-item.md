---
title: '功能表項目 (MSAA UI 元素參考) '
description: 功能表項目表示功能表列或快顯功能表中的特定專案。
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b90162f386314ac495ed138ccf4d180d2f53b8b1e6126287c79a1d75d40be2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644498"
---
# <a name="menu-item-msaa-ui-element-reference"></a>功能表項目 (MSAA UI 元素參考) 

> [!Note]  
> 本主題描述用於 MSAA UI 專案參考之 **功能表項目** 物件。 此處未說明如何在各種 UI 架構中建立 **功能表項目** 物件。 請參閱您所使用之 UI 架構的 API 參考檔。

 

功能表項目表示功能表列或快顯功能表中的特定專案。 例如，Microsoft Active Accessibility 會 **為功能表列中的 [檔案** ] 功能表建立功能表項目物件。 同樣地，Microsoft Active Accessibility 會 **從 [檔案**] 快顯功能表中建立 [**開啟**] 功能表項目的功能表項目物件。

功能表項目的視窗類別名稱是 " \# 32768"。

## <a name="iaccessible-methods"></a>IAccessible 方法

功能表項目支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | 如果是功能表列中的功能表項目， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 會根據功能表的狀態顯示或關閉功能表。 針對快顯功能表中的功能表項目， **accDoDefaultAction** 按一下功能表項目以執行功能表命令。 |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

功能表項目支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | 抓取此專案之快顯功能表物件的 [**IDispatch**](idispatch-interface.md) 介面。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性是顯示功能表或子功能表的功能表項目。否則， **ChildCount** 屬性為零。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | 顯示功能表或子功能表的功能表項目 **DefaultAction** 屬性為 [開啟] 或 [關閉]，視功能表的狀態而定。 所有其他功能表項目的 **DefaultAction** 屬性為「執行」。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是功能表項目的存取金鑰，也就是功能表項目名稱文字中的加底線字元。 例如，檔功能表項目的 **KeyboardShortcut** 屬性為 "f"。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [ **名稱** ] 屬性與功能表項目的名稱相同。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是包含功能表項目的功能表列或快顯功能表。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性是 [**role \_ SYSTEM \_ MENUITEM**](object-roles.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | [ **狀態** ] 屬性可能是 [ [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md) ] 或下列一或多個值的組合： [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 已核**](object-state-constants.md)取 \| [**狀態 \_ 系統 \_ 預設**](object-state-constants.md) \| [**狀態系統 \_ \_ HOTTRACKED**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 焦點**](object-state-constants.md) \| [**狀態 \_ 系統 \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>備註

-   在功能表項目上使用時， [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 會傳回 \_ [確定]，但如果存取金鑰中使用的字元是?,!, @ 或任何其他需要 SHIFT 鍵或其他輔助按鍵的字元，就無法執行動作。 這也會發生在具有存取金鑰字元的國際鍵盤上，需要按下 ALT GR 鍵。
-   具有 [**SELFLAG \_ TAKEFOCUS**](selflag.md)的 [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)方法不會造成功能表項目開啟或關閉快顯功能表。 用戶端會使用 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 方法來開啟或關閉快顯功能表。
-   未顯示快顯功能表的功能表列專案會針對 [ **名稱** ] 屬性傳回 "Application"，而不是功能表項目的名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**功能表列**](menu-bar.md)
</dt> <dt>

[**快顯功能表**](pop-up-menu.md)
</dt> </dl>

 

 





