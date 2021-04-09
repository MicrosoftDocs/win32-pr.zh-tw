---
title: 如何使用磚視圖
description: 本主題將示範如何設定清單視圖控制項的圖格視圖。
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933728"
---
# <a name="how-to-use-tile-views"></a>如何使用磚視圖

本主題將示範如何設定清單視圖控制項的圖格視圖。 在 [並排顯示] 中，每個專案都是以包含一或多行伴隨文字的大型圖示來表示。 如需圖例，請參閱 [關於 List-View 控制項](list-view-controls-overview.md)。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows 控制項](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows 消費者介面程式設計

## <a name="instructions"></a>指示


使用 [**ListView \_ SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) 宏設定磚視圖的一般顯示參數。 使用傳遞至這個宏的 [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) 結構，以指定文字相對於圖示的位置、每個磚的大小 (包括伴隨的文字) ，以及最大的文字行數。

如果您不想讓磚自動調整大小，您必須在 [**TILESIZE**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo)成員的 **DwFlags** 成員和 **LVTVIM \_ dwMask** 中設定 **LVTVIF \_ FIXEDSIZE** ，以及提供 **LVTILEVIEWINFO** **成員中** 的維度。

下列 c + + 程式碼範例會設定清單視圖控制項的圖格視圖資訊，因此每個專案最多會顯示兩個子專案。 它也會設定每個磚的大小。


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



針對清單中的每個專案，您可以在專案插入清單或更新版本時，設定進一步的參數。 與 [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)搭配使用的 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構包含成員，這些成員會指定要顯示在專案底下的資料行，以及其對齊方式。 這些相同的顯示參數也可以在與 [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo)搭配使用的 [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo)結構中找到。

> [!Note]  
> 此處的「資料行」指的不是要在並排顯示中顯示資料行，而是在 [詳細資料] 視圖中顯示在資料行中的子欄位。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[清單視圖控制項參考](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> <dt>

[使用 List-View 控制項](using-list-view-controls.md)
</dt> </dl>

 

 




