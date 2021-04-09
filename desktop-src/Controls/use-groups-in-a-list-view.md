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
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="dee6a-103">如何在 List-View 中使用群組</span><span class="sxs-lookup"><span data-stu-id="dee6a-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="dee6a-104">本主題說明如何建立群組的實例，並將它加入至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="dee6a-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="dee6a-105">群組可讓使用者使用水準分隔線和群組標題，將清單排列成以視覺化方式分割在頁面上的專案群組。</span><span class="sxs-lookup"><span data-stu-id="dee6a-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dee6a-106">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="dee6a-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dee6a-107">技術</span><span class="sxs-lookup"><span data-stu-id="dee6a-107">Technologies</span></span>

-   [<span data-ttu-id="dee6a-108">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="dee6a-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dee6a-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="dee6a-109">Prerequisites</span></span>

-   <span data-ttu-id="dee6a-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="dee6a-110">C/C++</span></span>
-   <span data-ttu-id="dee6a-111">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="dee6a-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dee6a-112">指示</span><span class="sxs-lookup"><span data-stu-id="dee6a-112">Instructions</span></span>


<span data-ttu-id="dee6a-113">若要在清單視圖控制項中使用群組，請確定控制項包含 [**lvs) \_ ALIGNTOP**](list-view-window-styles.md) 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="dee6a-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="dee6a-114">當您將專案加入至清單時，請將專案 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **iGroupId** 成員設定為群組 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的 **iGroupId** 成員值，將專案指派給群組。</span><span class="sxs-lookup"><span data-stu-id="dee6a-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="dee6a-115">啟用群組視圖時，未指派給群組的專案不會出現在清單中。</span><span class="sxs-lookup"><span data-stu-id="dee6a-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="dee6a-116">若要啟用或停用群組視圖，請使用 [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) 宏。</span><span class="sxs-lookup"><span data-stu-id="dee6a-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="dee6a-117">下列範例示範如何建立具有標題的群組，並將其新增至清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="dee6a-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="dee6a-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="dee6a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dee6a-119">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="dee6a-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dee6a-120">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="dee6a-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="dee6a-121">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="dee6a-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




