---
title: 選取範圍和焦點屬性和方法
description: 如同在 Microsoft Windows 作業系統上執行的應用程式中的許多元素，可存取的物件會選取並接收鍵盤焦點。 這些屬性可讓使用者與應用程式元素互動、變更值，並以其他方式操作。
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf5c5bc4a60e664c124e7181f998d9e0a7af6ab82ef9b2d4f030f7541d530ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745227"
---
# <a name="selection-and-focus-properties-and-methods"></a>選取範圍和焦點屬性和方法

如同在 Microsoft Windows 作業系統上執行的應用程式中的許多元素，可存取的物件會 *選取* 並接收鍵盤 *焦點*。 這些屬性可讓使用者與應用程式元素互動、變更值，並以其他方式操作。

物件選取和物件焦點之間有一些主要差異：

-   焦點物件是整個作業系統中的一個物件，可接收鍵盤輸入。 具有鍵盤焦點的物件是使用中視窗或使用中視窗的子物件。
-   選取的物件會標示為參與某種類型的群組作業。

例如，使用者可以在清單視圖控制項中選取數個專案，但焦點只會提供給系統中的一個物件一次。 請注意，焦點專案來自于選取專案。

用戶端會藉由呼叫 [**IAccessible：： get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)，判斷特定的可存取物件或子項目是否具有焦點。 用戶端會藉由呼叫 [**IAccessible：： get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)，判斷是否已選取物件，或選取可存取物件內的子系。 針對選取多個子系的清單視圖控制項之類的物件，父物件必須支援 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面，這可讓用戶端列舉選取的子系。

## <a name="events-triggered-in-menus"></a>在功能表中觸發的事件

Microsoft Active Accessibility 會公開以 Microsoft Win32 功能表 Api 和資源檔建立的標準功能表。 若要與標準功能表一致，當使用者反白顯示功能表項目時，具有自訂功能表的伺服器會觸發 [**事件 \_ 物件 \_ 焦點**](event-constants.md)，而不是 [**事件 \_ 物件 \_ 選取**](event-constants.md)。

> [!Note]  
> Microsoft Active Accessibility 不支援選取 [編輯] 和 [rich edit] 控制項中包含的文字，因為文字會在這些控制項的 [ [**值**](value-property.md) ] 屬性中公開為單一字串。

 

## <a name="in-this-section"></a>本節內容

-   [選取子物件](selecting-child-objects.md)

 

 