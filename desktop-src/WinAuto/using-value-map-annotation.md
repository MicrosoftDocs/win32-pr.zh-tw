---
title: 使用值對應注釋
description: 如需範例程式碼，請參閱值對應注釋範例。
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375425"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="f4683-103">使用值對應注釋</span><span class="sxs-lookup"><span data-stu-id="f4683-103">Using Value Map Annotation</span></span>

<span data-ttu-id="f4683-104">**若要建立值對應**</span><span class="sxs-lookup"><span data-stu-id="f4683-104">**To create a value map**</span></span>

1.  <span data-ttu-id="f4683-105">**建立對應字串。**</span><span class="sxs-lookup"><span data-stu-id="f4683-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="f4683-106">對應字串是控制項數值的清單，這些值會對應至 Unicode 中人們可讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="f4683-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="f4683-107">開頭為 "A："，後面接著一個數位，指出所使用的索引類型。</span><span class="sxs-lookup"><span data-stu-id="f4683-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="f4683-108">僅支援影像索引;因此，索引類型一律為0。</span><span class="sxs-lookup"><span data-stu-id="f4683-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="f4683-109">字串後面接著： index： result 配對。</span><span class="sxs-lookup"><span data-stu-id="f4683-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="f4683-110">「索引」是代表 List-View 或樹狀檢視之影像索引的數位，或是滑杆控制項的值。</span><span class="sxs-lookup"><span data-stu-id="f4683-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="f4683-111">產生的值是當您對應清單視圖或樹狀檢視控制項的角色或狀態屬性時，所取得的數位。</span><span class="sxs-lookup"><span data-stu-id="f4683-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="f4683-112">這類數位會以十進位或十六進位以 "0x" 前置詞表示。</span><span class="sxs-lookup"><span data-stu-id="f4683-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="f4683-113">對應字串一律以最後的冒號結束， ( "：" ) 。</span><span class="sxs-lookup"><span data-stu-id="f4683-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="f4683-114">以下是清單視圖或樹狀檢視控制項中核取方塊的 [狀態] 和 [角色] 屬性的批註對應範例。</span><span class="sxs-lookup"><span data-stu-id="f4683-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="f4683-115">視圖中有兩個代表核取方塊的專案，而且每個專案都有對應至已核取和未核取狀態的影像。</span><span class="sxs-lookup"><span data-stu-id="f4683-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="f4683-116">如需有效的角色和狀態值，請參閱 [物件角色](object-roles.md) 和 [物件狀態常數](object-state-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f4683-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="f4683-117">當您對應滑杆控制項的屬性時，索引值可能是負數。</span><span class="sxs-lookup"><span data-stu-id="f4683-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="f4683-118">當您對應值或描述屬性時，結果會是字串。</span><span class="sxs-lookup"><span data-stu-id="f4683-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="f4683-119">字串不會加上引號，而冒號可作為分隔符號。</span><span class="sxs-lookup"><span data-stu-id="f4683-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="f4683-120">如需詳細資訊，請參閱 [批註對應格式](value-map-annotation.md)。</span><span class="sxs-lookup"><span data-stu-id="f4683-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="f4683-121">**建立注釋管理員，並取得其**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**介面** 的指標。</span><span class="sxs-lookup"><span data-stu-id="f4683-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="f4683-122">以下是如何建立注釋管理員的範例。</span><span class="sxs-lookup"><span data-stu-id="f4683-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="f4683-123">**將對應字串附加至控制項。**</span><span class="sxs-lookup"><span data-stu-id="f4683-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="f4683-124">呼叫 [**IAccPropServices：： SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)，將控制項的 **HWND** 和指標傳遞至對應字串。</span><span class="sxs-lookup"><span data-stu-id="f4683-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="f4683-125">*IdProp* 參數將會是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="f4683-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="f4683-126">參數</span><span class="sxs-lookup"><span data-stu-id="f4683-126">Parameter</span></span>                   | <span data-ttu-id="f4683-127">用途</span><span class="sxs-lookup"><span data-stu-id="f4683-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="f4683-128">MSAAPROPID \_ ROLEMAP</span><span class="sxs-lookup"><span data-stu-id="f4683-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="f4683-129">設定清單視圖或樹狀檢視控制項的角色對應。</span><span class="sxs-lookup"><span data-stu-id="f4683-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="f4683-130">MSAAPROPID \_ STATEMAP</span><span class="sxs-lookup"><span data-stu-id="f4683-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="f4683-131">設定清單視圖或樹狀檢視控制項的狀態對應。</span><span class="sxs-lookup"><span data-stu-id="f4683-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="f4683-132">PROPID \_ ACC \_ DESCRIPTIONMAP</span><span class="sxs-lookup"><span data-stu-id="f4683-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="f4683-133">為清單視圖或樹狀檢視設定描述對應。</span><span class="sxs-lookup"><span data-stu-id="f4683-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="f4683-134">MSAAPROPID \_ VALUEMAP</span><span class="sxs-lookup"><span data-stu-id="f4683-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="f4683-135">設定滑杆控制項的值對應。</span><span class="sxs-lookup"><span data-stu-id="f4683-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="f4683-136">**清除。**</span><span class="sxs-lookup"><span data-stu-id="f4683-136">**Clean up.**</span></span>

    <span data-ttu-id="f4683-137">在您終結任何值對應標注的控制項之前 (例如，處理 [WM \_ ](../winmsg/wm-destroy.md) 終結) 時，您必須清除先前註冊的屬性，並釋放注釋管理員。</span><span class="sxs-lookup"><span data-stu-id="f4683-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="f4683-138">若要這樣做，請適當地呼叫 [**IAccPropServices：： ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) ，並釋放您的指標以進行 [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)。</span><span class="sxs-lookup"><span data-stu-id="f4683-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="f4683-139">如需範例程式碼，請參閱 [值對應注釋範例](value-map-annotation-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="f4683-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 