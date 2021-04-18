---
title: 公開 Owner-Drawn 功能表項目
description: 公開 Owner-Drawn 功能表項目
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507336"
---
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="864b2-103">公開 Owner-Drawn 功能表項目</span><span class="sxs-lookup"><span data-stu-id="864b2-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="864b2-104">應用程式開發人員可以使用 [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 結構來公開主控描繪功能表項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="864b2-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="864b2-105">藉由將此結構與主控描繪功能表項目資料產生關聯，您就不需要使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)公開功能表項目。</span><span class="sxs-lookup"><span data-stu-id="864b2-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="864b2-106">建立主控描繪功能表時，定義主控描繪功能表項目資料的類別或結構，並為每個功能表項目建立此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="864b2-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="864b2-107">將專案加入至功能表時，傳遞專案資料的指標。</span><span class="sxs-lookup"><span data-stu-id="864b2-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="864b2-108">若要公開功能表項目的名稱， [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 結構必須是定義應用程式特定專案資料之結構的第一個成員，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="864b2-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



<span data-ttu-id="864b2-109">[**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo)結構不能是包含虛擬函式之類別中的成員。</span><span class="sxs-lookup"><span data-stu-id="864b2-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="864b2-110">編譯器代碼時，類別的第一個成員一律是編譯器產生的虛擬函式資料表指標。</span><span class="sxs-lookup"><span data-stu-id="864b2-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="864b2-111">若要解決這個問題，請建立包含 **MSAAMENUINFO** 做為第一個成員的專案資料結構。</span><span class="sxs-lookup"><span data-stu-id="864b2-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="864b2-112">第二個成員是類別實例的指標，該類別會定義擁有者繪製的資料。</span><span class="sxs-lookup"><span data-stu-id="864b2-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="864b2-113">下列範例示範這項技巧。</span><span class="sxs-lookup"><span data-stu-id="864b2-113">The following example demonstrates this technique.</span></span>


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



<span data-ttu-id="864b2-114">將專案加入至功能表時，請將指標傳遞至包含 [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 的結構實例，以公開功能表項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="864b2-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




