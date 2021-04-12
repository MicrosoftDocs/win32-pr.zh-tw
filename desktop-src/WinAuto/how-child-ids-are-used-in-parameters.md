---
title: 如何在參數中使用子識別碼
description: 本主題描述輸入參數、輸出參數，以及解讀 IAccessible 方法所傳回之子識別碼的特殊案例。
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375809"
---
# <a name="how-child-ids-are-used-in-parameters"></a>如何在參數中使用子識別碼

本主題描述輸入參數、輸出參數，以及解讀 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法所傳回之子識別碼的特殊案例。

## <a name="input-parameters"></a>輸入參數

許多 Microsoft Active Accessibility 函式和大部分的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性都採用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構做為輸入參數。 針對大部分的 **IAccessible** 屬性，此參數可讓用戶端開發人員指定是否要取得物件本身或物件的其中一個簡單元素的相關資訊。

Microsoft Active Accessibility 提供常數 **CHILDID 本身 \_** ，表示需要物件本身的資訊。 為了取得簡單元素的相關資訊，用戶端開發人員會在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 參數中指定其子系識別碼。

初始化 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)參數時，請務必在 **vt** 成員中指定 **vt \_ I4** ，除了指定子識別碼值 (或 CHILDID **lVal** 成員中 **的 \_ SELF**) 之外。

例如，若要取得物件的名稱，而不是物件的其中一個子專案，請將 IAccessible：： get accName 的第一個參數的 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)初始化為 [**：： Get \_**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ SELF** in **vt**) member 中的 **lVal** 成員和 **vt \_ I4** ，然後呼叫 **IAccessible：： get \_ accName**。

## <a name="output-parameters"></a>輸出參數

有幾個 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)函式和方法具有 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) \* output 參數，其中包含子物件的子系識別碼或 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)介面指標。 用戶端必須採取不同的步驟，取決於它們是否會收到 **VT \_ I4** 子系識別碼 (簡單元素) 或使用 **CHILDID \_ SELF** (full object) 的 **IDispatch** 介面指標。 遵循這些步驟將提供 **IAccessible** 介面指標和子系識別碼，讓用戶端能夠使用 **IAccessible** 方法和屬性。 這些步驟適用于 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)、 [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)和 [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) 方法。 它們也適用于 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)、 [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)和 [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) 用戶端函式。

下表列出傳回的可能結果，以及所需的後續處理步驟，讓用戶端有 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標和子系識別碼。



| 傳回的結果                                      | 傳回值的後置處理                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) 介面指標 | 這是完整的物件。呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以存取 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標。<br/> 使用 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標搭配 **CHILDID \_ SELF** 來存取 **IAccessible** 方法和屬性。<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| VT \_ I4 子識別碼                                      | 使用子系識別碼呼叫 [**IAccessible：： get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) ，以查看您是否有 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) 介面指標。如果您取得 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) 介面指標，請使用它搭配 **CHILDID \_ SELF** 來存取 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面方法和屬性。<br/> 如果 [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) 的呼叫失敗，您就會有一個簡單的元素。 使用原始的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標 (您在呼叫上述方法或函式時所使用的指標，) 具有呼叫傳回的 **VT \_ I4** 子識別碼。<br/> |



 

在您可以使用 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 參數之前，您必須呼叫 [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) 元件物件模型 (COM) 函數來將它初始化。 完成結構之後，請呼叫 [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) 來釋放為該 **變異** 保留的記憶體。

## <a name="special-cases"></a>特殊案例

上表中的指導方針有一些例外狀況，例如 [**IAccessible：： accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) 方法傳回子系識別碼時。 如果子系是可存取的物件，則伺服器必須傳回 [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) 介面。 如果 **IAccessible：： accHitTest** 傳回子系識別碼，則子系是簡單元素。

此外，也有特殊的 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)案例。 如需詳細資訊，請參閱 **IAccessible：： accNavigate** 和 [空間與邏輯導覽](spatial-and-logical-navigation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[IDispatch 介面](idispatch-interface.md)
</dt> <dt>

[VARIANT 結構](variant-structure.md)
</dt> </dl>

 

