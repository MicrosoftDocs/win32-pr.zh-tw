---
title: 選取範圍和焦點屬性和方法
description: 就像在 Microsoft Windows 作業系統上執行之應用程式中的許多專案一樣，可存取的物件會選取並接收鍵盤焦點。 這些屬性可讓使用者與應用程式元素互動、變更值，並以其他方式操作。
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682640"
---
# <a name="selection-and-focus-properties-and-methods"></a><span data-ttu-id="c48ef-104">選取範圍和焦點屬性和方法</span><span class="sxs-lookup"><span data-stu-id="c48ef-104">Selection and Focus Properties and Methods</span></span>

<span data-ttu-id="c48ef-105">就像在 Microsoft Windows 作業系統上執行之應用程式中的許多專案一樣，可存取的物件會 *選取* 並接收鍵盤 *焦點*。</span><span class="sxs-lookup"><span data-stu-id="c48ef-105">Like many elements in applications running on Microsoft Windows operating systems, accessible objects *select* and receive keyboard *focus*.</span></span> <span data-ttu-id="c48ef-106">這些屬性可讓使用者與應用程式元素互動、變更值，並以其他方式操作。</span><span class="sxs-lookup"><span data-stu-id="c48ef-106">These attributes enable users to interact with application elements, change values, and otherwise manipulate them.</span></span>

<span data-ttu-id="c48ef-107">物件選取和物件焦點之間有一些主要差異：</span><span class="sxs-lookup"><span data-stu-id="c48ef-107">There are some key differences between object selection and object focus:</span></span>

-   <span data-ttu-id="c48ef-108">焦點物件是整個作業系統中的一個物件，可接收鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="c48ef-108">A focused object is the one object in the entire operating system that receives keyboard input.</span></span> <span data-ttu-id="c48ef-109">具有鍵盤焦點的物件是使用中視窗或使用中視窗的子物件。</span><span class="sxs-lookup"><span data-stu-id="c48ef-109">The object with the keyboard focus is either the active window or a child object of the active window.</span></span>
-   <span data-ttu-id="c48ef-110">選取的物件會標示為參與某種類型的群組作業。</span><span class="sxs-lookup"><span data-stu-id="c48ef-110">A selected object is marked to participate in some type of group operation.</span></span>

<span data-ttu-id="c48ef-111">例如，使用者可以在清單視圖控制項中選取數個專案，但焦點只會提供給系統中的一個物件一次。</span><span class="sxs-lookup"><span data-stu-id="c48ef-111">For example, a user can select several items in a list-view control, but the focus is given only to one object in the system at a time.</span></span> <span data-ttu-id="c48ef-112">請注意，焦點專案來自于選取專案。</span><span class="sxs-lookup"><span data-stu-id="c48ef-112">Note that focused items are from a selection of items.</span></span>

<span data-ttu-id="c48ef-113">用戶端會藉由呼叫 [**IAccessible：： get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)，判斷特定的可存取物件或子項目是否具有焦點。</span><span class="sxs-lookup"><span data-stu-id="c48ef-113">Clients determine whether a particular accessible object or child element has the focus by calling [**IAccessible::get\_accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus).</span></span> <span data-ttu-id="c48ef-114">用戶端會藉由呼叫 [**IAccessible：： get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)，判斷是否已選取物件，或選取可存取物件內的子系。</span><span class="sxs-lookup"><span data-stu-id="c48ef-114">Clients determine whether an object is selected, or which children within an accessible object are selected, by calling [**IAccessible::get\_accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection).</span></span> <span data-ttu-id="c48ef-115">針對選取多個子系的清單視圖控制項之類的物件，父物件必須支援 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面，這可讓用戶端列舉選取的子系。</span><span class="sxs-lookup"><span data-stu-id="c48ef-115">For objects such as list-view controls in which more than one child is selected, the parent object must support the [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface, which allows clients to enumerate the selected children.</span></span>

## <a name="events-triggered-in-menus"></a><span data-ttu-id="c48ef-116">在功能表中觸發的事件</span><span class="sxs-lookup"><span data-stu-id="c48ef-116">Events Triggered in Menus</span></span>

<span data-ttu-id="c48ef-117">Microsoft Active Accessibility 會公開以 Microsoft Win32 功能表 Api 和資源檔建立的標準功能表。</span><span class="sxs-lookup"><span data-stu-id="c48ef-117">Microsoft Active Accessibility exposes standard menus created with the Microsoft Win32 menu APIs and resource files.</span></span> <span data-ttu-id="c48ef-118">若要與標準功能表一致，當使用者反白顯示功能表項目時，具有自訂功能表的伺服器會觸發 [**事件 \_ 物件 \_ 焦點**](event-constants.md)，而不是 [**事件 \_ 物件 \_ 選取**](event-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="c48ef-118">To be consistent with standard menus, servers with custom menus trigger [**EVENT\_OBJECT\_FOCUS**](event-constants.md), not [**EVENT\_OBJECT\_SELECTION**](event-constants.md), when a user highlights a menu item.</span></span>

> [!Note]  
> <span data-ttu-id="c48ef-119">Microsoft Active Accessibility 不支援選取 [編輯] 和 [rich edit] 控制項中包含的文字，因為文字會在這些控制項的 [ [**值**](value-property.md) ] 屬性中公開為單一字串。</span><span class="sxs-lookup"><span data-stu-id="c48ef-119">Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a single string in the [**Value**](value-property.md) property for these controls.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c48ef-120">本節內容</span><span class="sxs-lookup"><span data-stu-id="c48ef-120">In this section</span></span>

-   [<span data-ttu-id="c48ef-121">選取子物件</span><span class="sxs-lookup"><span data-stu-id="c48ef-121">Selecting Child Objects</span></span>](selecting-child-objects.md)

 

 