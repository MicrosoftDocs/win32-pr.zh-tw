---
title: 選取子物件
description: 用戶端會呼叫 IAccessible accSelect 方法，以修改物件中子系之間的選取範圍或鍵盤焦點。 以呼叫指定的 SELFLAG 常數會定義要執行的作業。
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300335"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="9a8cf-104">選取子物件</span><span class="sxs-lookup"><span data-stu-id="9a8cf-104">Selecting Child Objects</span></span>

<span data-ttu-id="9a8cf-105">用戶端會呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 方法，以修改物件中子系之間的選取範圍或鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="9a8cf-106">以呼叫指定的 [SELFLAG 常數](selflag.md) 會定義要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="9a8cf-107">如果以具有 **HWND** 的子物件上的 [**SELFLAG \_ TAKEFOCUS**](selflag.md)旗標呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，只有當物件的父系具有焦點時，此旗標才會生效。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="9a8cf-108">執行複雜的選取作業</span><span class="sxs-lookup"><span data-stu-id="9a8cf-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="9a8cf-109">以下描述呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 來執行複雜的選取作業時所要指定的 SELFLAG 值。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="9a8cf-110">**若要模擬按一下**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-110">**To simulate a click**</span></span>

-   <span data-ttu-id="9a8cf-111">[**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="9a8cf-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="9a8cf-112">**藉由模擬 CTRL + 按一下來選取目標專案**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="9a8cf-113">[**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="9a8cf-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="9a8cf-114">**藉由模擬 CTRL + 按一下，取消選取目標專案**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="9a8cf-115">[**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="9a8cf-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="9a8cf-116">**模擬 SHIFT + 按一下**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="9a8cf-117">[**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="9a8cf-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="9a8cf-118">**若要選取物件的範圍，並將焦點放在最後一個物件上**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="9a8cf-119">指定起始物件的 [**SELFLAG \_ TAKEFOCUS**](selflag.md) ，以設定選取範圍錨點。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="9a8cf-120">再次呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，並在最後一個物件上指定 [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="9a8cf-121">**取消選取所有物件**</span><span class="sxs-lookup"><span data-stu-id="9a8cf-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="9a8cf-122">在任何物件上指定 [**SELFLAG \_ TAKESELECTION**](selflag.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="9a8cf-123">此旗標會將所有選取的物件（除了剛剛選取的物件之外）取消選取。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="9a8cf-124">再次呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，並在剩餘的物件上指定 [**SELFLAG \_ REMOVESELECTION**](selflag.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a8cf-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




