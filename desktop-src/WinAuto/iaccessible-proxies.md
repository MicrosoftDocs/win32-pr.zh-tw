---
title: IAccessible proxy
description: IAccessible proxy 提供標準 UI 元素的預設協助工具資訊，使用者控制項、使用者功能表，以及來自 COMCTL 和 COMCTL32.DLL 的通用控制項。
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315676"
---
# <a name="iaccessible-proxies"></a>IAccessible proxy

[**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) proxy 提供標準 UI 元素的預設協助工具資訊：使用者控制項、使用者功能表，以及來自 COMCTL 和 comctl32.dll 的通用控制項。 這項預設支援是透過 Oleacc.dll 所建立的 **IAccessible** 物件公開，並提供 Microsoft Active Accessibility 支援，而不需要額外的伺服器開發工作。 然後伺服器可以使用 [動態批註 API](dynamic-annotation-api.md) 來修改 Oleacc.dll 所公開的大部分資訊，但它並沒有完整的控制權。

## <a name="creating-a-proxy"></a>建立 Proxy

若要判斷 UI 專案是否原本就支援 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面，Oleacc.dll 傳送了 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息給它。 非零傳回值表示該元素原本就支援 Microsoft Active Accessibility，並提供它自己的 **IAccessible** 支援。 但是，如果傳回值為零，Oleacc.dll 會提供 UI 元素的 proxy 物件，並嘗試代表其傳回有意義的資訊。 如需有關 **wm \_ getobject** 的詳細資訊，請參閱 [Wm getobject 的 \_ 運作方式](how-wm-getobject-works.md)。

## <a name="what-information-is-exposed"></a>公開的資訊

Oleacc.dll 使用 UI 元素的 Windows 類別名稱，判斷應該針對每個 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性公開哪些資訊，以及如何收集該資訊。 例如，Oleacc.dll 會呼叫 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函式，以抓取標準 push 按鈕的 [**Name**](name-property.md) 屬性，但會呼叫這個相同的函式，以取得標準編輯控制項的 [**Value**](value-property.md) 屬性。 實際上，Oleacc.dll 會將每個 **IAccessible** 方法對應到適當的 Microsoft Win32 或控制項特定的訊息或函式呼叫。 藉由使用這個以類別名稱為基礎的特殊大小寫，它可以透過 **IAccessible** proxy 傳回有意義的資訊，而不需要在伺服器中 Microsoft Active Accessibility 支援。

使用標準 UI 專案所建立的應用程式，通常可獲得完整的 Microsoft Active Accessibility 支援，而不需要額外的開發工作 這項規則的例外狀況是已經過子類別化的控制項，其不會儲存自己的字串 (缺少 **HASSTRINGS** 樣式) 或主控描繪。 在這些情況下，Oleacc.dll 無法收集所需的資訊，因為這項資訊會儲存在控制項之外。 不過，在許多案例中，已建立因應措施，或使用動態注釋，可讓伺服器與 Oleacc.dll 提供的 proxy 合作。

## <a name="generic-proxy-objects"></a>泛型 Proxy 物件

如果 Oleacc.dll 無法辨識 UI 元素的類別名稱，則會建立泛型 proxy，盡可能公開最多的資訊。 大部分情況下，這包括物件的周框、父物件、從 [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext))  (的名稱，以及視窗階層中的任何子系。

 

 