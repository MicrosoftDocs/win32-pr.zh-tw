---
title: 取得可存取的物件介面指標
description: Microsoft Active Accessibility 用戶端應用程式使用下列其中一個函式，抓取可存取物件的介面指標。
ms.assetid: b82467f0-0d46-482a-8f6d-ad64f236601e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d4006bf073075f2aa47a9911565213050e3d11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106978584"
---
# <a name="getting-an-accessible-object-interface-pointer"></a>取得可存取的物件介面指標

Microsoft Active Accessibility 用戶端應用程式使用下列其中一個函式，抓取可存取物件的介面指標。

**AccessibleObjectFromEvent**

許多用戶端會查閱產生事件之特定可存取物件的相關資訊。 由於 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面是可存取物件的「閘道」，因此用戶端必須有簡單的方法，將 [WinEvents](winevents-overview.md) 與產生事件之物件的 **IAccessible** 介面產生關聯。 Microsoft Active Accessibility 針對此用途特別提供 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 函數。

> [!Note]  
> 具有內容攔截函式的用戶端必須先呼叫 [IsWindow](/windows/win32/api/winuser/nf-winuser-iswindow)函 [式](in-context-hook-functions.md)，才能呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)。

 

[**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)函式會接受用戶端攔截函式 [*所接收的*](/windows/desktop/api/Winuser/nc-winuser-wineventproc)許多相同資訊。 當用戶端攔截函式收到事件通知時，它會將適當的參數從事件傳遞至 **AccessibleObjectFromEvent**。

此函式會抓取產生事件之使用者介面專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，或元素父物件的介面。 如果傳回父物件的介面指標，用戶端會呼叫父系的屬性和方法，以取得產生事件之子項目的相關資訊。

**AccessibleObjectFromPoint**

若要在螢幕上的指定點取出物件 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的位址，用戶端會使用 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 函數。

**AccessibleObjectFromWindow**

為了從視窗控制碼取出物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，用戶端會使用 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函數。

每次呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)或 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 函數時，伺服器都可以針對相同的使用者介面專案傳回相異的介面指標。 若要判斷兩個指標是否參考相同的使用者介面元素，用戶端開發人員必須比較物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性，而非指標。

 

 