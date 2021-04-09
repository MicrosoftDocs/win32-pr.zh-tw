---
title: 如何將專案加入至標題控制項
description: 本主題示範如何將專案加入至標題控制項。
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933741"
---
# <a name="how-to-add-an-item-to-a-header-control"></a><span data-ttu-id="7b945-103">如何將專案加入至標題控制項</span><span class="sxs-lookup"><span data-stu-id="7b945-103">How to Add an Item to a Header Control</span></span>

<span data-ttu-id="7b945-104">本主題示範如何將專案加入至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="7b945-104">This topic demonstrates how to add an item to a header control.</span></span> <span data-ttu-id="7b945-105">標題控制項通常會有數個定義控制項資料行的標頭專案。</span><span class="sxs-lookup"><span data-stu-id="7b945-105">A header control typically has several header items that define the columns of the control.</span></span> <span data-ttu-id="7b945-106">您可以藉由將 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息傳送至控制項，將專案加入至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="7b945-106">You can add an item to a header control by sending the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7b945-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7b945-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7b945-108">技術</span><span class="sxs-lookup"><span data-stu-id="7b945-108">Technologies</span></span>

-   [<span data-ttu-id="7b945-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="7b945-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7b945-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="7b945-110">Prerequisites</span></span>

-   <span data-ttu-id="7b945-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7b945-111">C/C++</span></span>
-   <span data-ttu-id="7b945-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="7b945-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7b945-113">指示</span><span class="sxs-lookup"><span data-stu-id="7b945-113">Instructions</span></span>


<span data-ttu-id="7b945-114">使用 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息，將專案加入至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="7b945-114">Use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message to add an item to the header control.</span></span> <span data-ttu-id="7b945-115">訊息必須包含 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="7b945-115">The message must include the address of an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="7b945-116">此結構會定義標頭專案的屬性，其中可包括字串、點陣圖影像、初始大小，以及應用程式定義的32位值。</span><span class="sxs-lookup"><span data-stu-id="7b945-116">This structure defines the properties of the header item, which can include a string, a bitmapped image, an initial size, and an application-defined 32-bit value.</span></span>

<span data-ttu-id="7b945-117">下列範例說明如何使用 [**HDM \_ INSERTITEM**](hdm-insertitem.md) 訊息和 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構，將專案加入至標題控制項。</span><span class="sxs-lookup"><span data-stu-id="7b945-117">The following example illustrates how to use the [**HDM\_INSERTITEM**](hdm-insertitem.md) message and the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure to add an item to a header control.</span></span> <span data-ttu-id="7b945-118">新的專案是由在專案矩形內靠左對齊的字串所組成。</span><span class="sxs-lookup"><span data-stu-id="7b945-118">The new item consists of a string that is left-justified within the item rectangle.</span></span>



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a><span data-ttu-id="7b945-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b945-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b945-120">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="7b945-120">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="7b945-121">標題控制項參考</span><span class="sxs-lookup"><span data-stu-id="7b945-121">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7b945-122">使用標題控制項</span><span class="sxs-lookup"><span data-stu-id="7b945-122">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 




