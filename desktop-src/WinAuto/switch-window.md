---
title: '切換視窗 (MSAA UI 元素參考) '
description: 每當使用者按下 ALT + TAB 切換至不同的應用程式時，就會顯示 [切換] 視窗。 切換視窗包含每個目前正在執行之應用程式的圖示。
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443979"
---
# <a name="switch-window-msaa-ui-element-reference"></a>切換視窗 (MSAA UI 元素參考) 

每當使用者按下 ALT + TAB 切換至不同的應用程式時，就會顯示 [切換] 視窗。 切換視窗包含每個目前正在執行之應用程式的圖示。

切換視窗的視窗類別名稱是 " \# 32771"。

## <a name="iaccessible-methods"></a>IAccessible 方法

切換視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法：



| 方法                                                                    | 註解                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | 切換視窗物件本身沒有 **DefaultAction** 屬性。 在 [切換] 視窗中，每個專案的 [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) 方法會啟用指定的專案。 |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>IAccessible 屬性

切換視窗支援下列 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性：



|      屬性                                                                          |      描述                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | **ChildCount** 屬性為零。                                                                                                                                                                                           |
| [**取得 \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | 切換視窗物件本身沒有 **DefaultAction** 屬性。 切換視窗中每個專案的 **DefaultAction** 屬性為 "switch"。                                                                     |
| [**取得 \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | 切換視窗父物件無法接收焦點;只有個別子女才能獲得焦點。                                                                                                                          |
| [**取得 \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | 切換視窗物件本身沒有 **名稱** 屬性。 切換視窗中每個應用程式圖示的 [ **名稱** ] 屬性與顯示的應用程式名稱相同。                                         |
| [**取得 \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | 切換視窗物件本身具有 "window 32771" 的 **Role** 屬性 \[ \] 。 此外，切換視窗中的每個應用程式圖示都有 **角色** 屬性 [**角色系統的 [ \_ 系統 \_**](object-roles.md)]。 |
| [**取得 \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | 切換視窗物件本身不支援 **State** 屬性。 清單視圖專案的 **狀態** 值是 [**狀態系統可 \_ \_ 設定**](object-state-constants.md)的。                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IAccessible 介面](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




