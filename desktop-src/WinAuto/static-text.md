---
title: '靜態文字 (MSAA UI 元素參考) '
description: 靜態文字控制項提供便利的方式來顯示對話方塊和其他視窗上的文字。 靜態文字控制項通常作為其他控制項的標籤。
ms.assetid: 2c4b29bc-54e6-4c96-93a3-1fcb96d68269
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da892a102caa8a1af1729bdb4fc2258f461828adf1f7622e8ff5abf8a2a0bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052486"
---
# <a name="static-text-msaa-ui-element-reference"></a>靜態文字 (MSAA UI 元素參考) 

靜態文字控制項提供便利的方式來顯示對話方塊和其他視窗上的文字。 靜態文字控制項通常作為其他控制項的標籤。

靜態文字控制項的視窗類別名稱是「靜態」。

## <a name="iaccessible-methods"></a>IAccessible 方法

靜態文字控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

靜態文字控制項支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                             | 註解                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | **ChildCount** 屬性為零。                                                                                                                                                                                                                                                          |
| [**取得 \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                               |
| [**取得 \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | **KeyboardShortcut** 屬性是存取金鑰，也就是文字中加上底線的字元，可啟用與靜態文字相關聯的控制項。 傳回的字串包含附加至字串 "Alt +" 的存取金鑰字元。                                           |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | [ **名稱** ] 屬性與靜態文字控制項中的文字相同。                                                                                                                                                                                                                     |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | **父** 屬性是在控制項周圍 ([**角色 \_ 系統 \_ 視窗**](object-roles.md)) 的視窗，而且具有與控制項相同的 **名稱** 屬性和視窗類別名稱。                                                                                   |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | **Role** 屬性為 [**role \_ SYSTEM \_ STATICTEXT**](object-roles.md)。                                                                                                                                                                                             |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 唯讀**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 不可見**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>備註

-   [](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) \_ \_ 當使用靜態文字物件上的 [**SELFLAG \_ TAKEFOCUS**](selflag.md)來呼叫時，accSelect 方法會傳回出現的 E MEMBERNOTFOUND。
-   具有 SS 圖示樣式的靜態控制項，會 \_ 在 **Name** 屬性中傳回不正確資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





