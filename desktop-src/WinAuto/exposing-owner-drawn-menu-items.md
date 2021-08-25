---
title: 公開 Owner-Drawn 功能表項目
description: 公開 Owner-Drawn 功能表項目
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84a2630b5227937d4a1c9621360d9fb028676bba03516970f93e314b382035b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860498"
---
# <a name="exposing-owner-drawn-menu-items"></a>公開 Owner-Drawn 功能表項目

應用程式開發人員可以使用 [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 結構來公開主控描繪功能表項目的名稱。 藉由將此結構與主控描繪功能表項目資料產生關聯，您就不需要使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)公開功能表項目。

建立主控描繪功能表時，定義主控描繪功能表項目資料的類別或結構，並為每個功能表項目建立此類別的實例。 將專案加入至功能表時，傳遞專案資料的指標。

若要公開功能表項目的名稱， [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 結構必須是定義應用程式特定專案資料之結構的第一個成員，如下列範例所示：


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



[**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo)結構不能是包含虛擬函式之類別中的成員。 編譯器代碼時，類別的第一個成員一律是編譯器產生的虛擬函式資料表指標。 若要解決這個問題，請建立包含 **MSAAMENUINFO** 做為第一個成員的專案資料結構。 第二個成員是類別實例的指標，該類別會定義擁有者繪製的資料。 下列範例示範這項技巧。


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



將專案加入至功能表時，請將指標傳遞至包含 [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) 的結構實例，以公開功能表項目的名稱。

 

 




