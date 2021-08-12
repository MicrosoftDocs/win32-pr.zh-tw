---
title: 'MDI 用戶端視窗 (MSAA UI 元素參考) '
description: 多重文件介面 (MDI) 是一種規格，定義針對 Windows 撰寫之應用程式的標準使用者介面。 MDI 應用程式可讓使用者一次使用一個以上的檔。
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff8279e9934c953e30a7d91710565562cb538d3140d971b1f74ff8963ca7345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565129"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>MDI 用戶端視窗 (MSAA UI 元素參考) 

多重文件介面 (MDI) 是一種規格，定義針對 Windows 撰寫之應用程式的標準使用者介面。 MDI 應用程式可讓使用者一次使用一個以上的檔。

MDI 應用程式有三種視窗：框架視窗、用戶端視窗和一些子視窗。 框架視窗就像是應用程式的主視窗，它會圍住用戶端視窗。 用戶端視窗是框架視窗的子系，作為子視窗的背景。 用戶端視窗也提供建立和操作在其中顯示檔之子視窗的支援。

MDI 用戶端視窗的視窗類別名稱是 "MDIClient"。

## <a name="iaccessible-methods"></a>IAccessible 方法

MDI 用戶端視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible 屬性

MDI 用戶端視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



| 屬性                                                                 | 註解                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | **ChildCount** 屬性是顯示檔的子視窗數目。                                                                                                                                                                                                                                                                                                                                                                              |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | **Name** 屬性為 "Workspace"。                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**取得 \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | **父** 屬性是 MDI 框架視窗。                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | **Role** 屬性是 [**role \_ SYSTEM \_ 用戶端**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**取得 \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | **State** 屬性是下列一或多個 [值](object-state-constants.md)的組合：[**狀態 \_ 系統 \_ 隱藏**](object-state-constants.md) \| [**狀態 \_ 系統 \_ 無法使用**](object-state-constants.md)狀態 \| [**\_ 系統 \_ 焦點**](object-state-constants.md)狀態系統可 \| [**\_ \_ 設定焦點**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





