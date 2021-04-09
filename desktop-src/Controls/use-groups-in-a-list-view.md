---
title: 如何在 List-View 中使用群組
description: 本主題說明如何建立群組的實例，並將它加入至清單視圖控制項。
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842899"
---
# <a name="how-to-use-groups-in-a-list-view"></a>如何在 List-View 中使用群組

本主題說明如何建立群組的實例，並將它加入至清單視圖控制項。 群組可讓使用者使用水準分隔線和群組標題，將清單排列成以視覺化方式分割在頁面上的專案群組。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


若要在清單視圖控制項中使用群組，請確定控制項包含 [**lvs) \_ ALIGNTOP**](list-view-window-styles.md) 視窗樣式。

當您將專案加入至清單時，請將專案 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iGroupId** 成員設定為群組 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的 **iGroupId** 成員值，將專案指派給群組。 啟用群組視圖時，未指派給群組的專案不會出現在清單中。 若要啟用或停用群組視圖，請使用 [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) 宏。

下列範例示範如何建立具有標題的群組，並將其新增至清單視圖控制項。


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單視圖控制項參考](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 




