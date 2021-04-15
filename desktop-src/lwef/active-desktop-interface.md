---
title: 使用 Active Desktop 物件
description: 本文包含屬於 Windows Shell API 一部分之 ActiveDesktop 物件的資訊。 此物件透過其 IActiveDesktop 介面，可讓您新增、移除和變更桌面上的專案。
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- ActiveDesktop 物件
- Active Desktop
- 列舉，桌面專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462989"
---
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="32e2d-107">使用 Active Desktop 物件</span><span class="sxs-lookup"><span data-stu-id="32e2d-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="32e2d-108">\[只有在 Windows XP 或更早版本才支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="32e2d-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="32e2d-109">\]</span><span class="sxs-lookup"><span data-stu-id="32e2d-109">\]</span></span>

<span data-ttu-id="32e2d-110">本文包含屬於 Windows Shell API 一部分之 **ActiveDesktop** 物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="32e2d-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="32e2d-111">此物件透過其 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面，可讓您新增、移除和變更桌面上的專案。</span><span class="sxs-lookup"><span data-stu-id="32e2d-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="32e2d-112">Active Desktop 介面總覽</span><span class="sxs-lookup"><span data-stu-id="32e2d-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="32e2d-113">存取 Active Desktop</span><span class="sxs-lookup"><span data-stu-id="32e2d-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="32e2d-114">新增桌面專案</span><span class="sxs-lookup"><span data-stu-id="32e2d-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="32e2d-115">列舉桌面專案</span><span class="sxs-lookup"><span data-stu-id="32e2d-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="32e2d-116">Active Desktop 是 Microsoft Internet Explorer 4.0 中引進的一項功能，可讓您將 HTML 檔案和專案 (例如 Microsoft ActiveX 控制項和 JAVA applet) 直接加入您的桌面。</span><span class="sxs-lookup"><span data-stu-id="32e2d-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="32e2d-117">[**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)介面是 WINDOWS Shell API 的一部分，用來以程式設計方式加入、移除和修改桌面上的專案。</span><span class="sxs-lookup"><span data-stu-id="32e2d-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="32e2d-118">您也可以使用 (CDF) 檔的通道定義格式來新增 Active Desktop 專案。</span><span class="sxs-lookup"><span data-stu-id="32e2d-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="32e2d-119">存取 Active Desktop</span><span class="sxs-lookup"><span data-stu-id="32e2d-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="32e2d-120">若要存取 Active Desktop，用戶端應用程式必須使用 CoCreateInstance 函式建立 ActiveDesktop 物件的實例， (CLSID \_ ActiveDesktop) [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，並取得物件 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="32e2d-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="32e2d-121">下列範例顯示如何取出 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="32e2d-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a><span data-ttu-id="32e2d-122">新增桌面專案</span><span class="sxs-lookup"><span data-stu-id="32e2d-122">Adding a Desktop Item</span></span>

<span data-ttu-id="32e2d-123">您可以使用三種方法來新增桌面專案： [**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)、 [**IActiveDesktop：： AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)和 [**IActiveDesktop：： AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl)。</span><span class="sxs-lookup"><span data-stu-id="32e2d-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="32e2d-124">每個新增至 Active Desktop 的桌面專案都必須有不同的來源 URL。</span><span class="sxs-lookup"><span data-stu-id="32e2d-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="32e2d-125">[**IActiveDesktop：： AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)和 [**IActiveDesktop：： AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl)方法都會提供選項，以顯示可在將桌面專案加入 Active Desktop 之前顯示的各種使用者介面。</span><span class="sxs-lookup"><span data-stu-id="32e2d-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="32e2d-126">介面會驗證使用者是否要將桌面專案新增至其 Active Desktop。</span><span class="sxs-lookup"><span data-stu-id="32e2d-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="32e2d-127">這些介面也會通知使用者 URL 安全性區域設定所保證的任何安全性風險，如果使用者想要建立此桌面專案的訂用帳戶，他們會要求他們。</span><span class="sxs-lookup"><span data-stu-id="32e2d-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="32e2d-128">這兩種方法也提供隱藏使用者介面的方法。</span><span class="sxs-lookup"><span data-stu-id="32e2d-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="32e2d-129">[**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)方法需要呼叫 [**IActiveDesktop：： ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) ，才能更新登錄。</span><span class="sxs-lookup"><span data-stu-id="32e2d-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="32e2d-130">若為 **IActiveDesktop：： AddDesktopItemWithUI**，用戶端應用程式必須立即釋放 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面，然後使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函式來抓取 **ActiveDesktop** 物件實例的介面，該實例包含新加入的桌面專案。</span><span class="sxs-lookup"><span data-stu-id="32e2d-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="32e2d-131">[**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)方法會在沒有任何使用者介面的情況下，將指定的桌面專案新增至 Active Desktop，除非 URL 安全性區域設定阻止它。</span><span class="sxs-lookup"><span data-stu-id="32e2d-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="32e2d-132">如果 URL 安全性區域設定不允許在不提示使用者的情況下新增桌面專案，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="32e2d-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="32e2d-133">**IActiveDesktop：： AddDesktopItem** 也需要呼叫 [**IActiveDesktop：： ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) ，才能更新登錄。</span><span class="sxs-lookup"><span data-stu-id="32e2d-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="32e2d-134">下列範例示範如何使用 [**IActiveDesktop：： AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) 方法新增桌面專案。</span><span class="sxs-lookup"><span data-stu-id="32e2d-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="32e2d-135">列舉桌面專案</span><span class="sxs-lookup"><span data-stu-id="32e2d-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="32e2d-136">若要列舉目前安裝在 Active Desktop 上的桌面專案，用戶端應用程式必須使用 [**IActiveDesktop：： GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount)方法來取出安裝的桌面專案總數，然後建立一個使用桌面專案索引來呼叫 [**IActiveDesktop：： GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem)方法，以抓取每個桌面專案 [**元件**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component)結構的迴圈。</span><span class="sxs-lookup"><span data-stu-id="32e2d-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="32e2d-137">下列範例示範一種列舉桌面專案的方式。</span><span class="sxs-lookup"><span data-stu-id="32e2d-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 