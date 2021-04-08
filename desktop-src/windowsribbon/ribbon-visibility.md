---
title: 顯示功能區
description: Windows 功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區 UI 的方式。
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows 功能區，自訂色彩
- 功能區、自訂色彩
- 自訂 Windows 功能區色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023768"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="2f952-106">顯示功能區</span><span class="sxs-lookup"><span data-stu-id="2f952-106">Displaying the Ribbon</span></span>

<span data-ttu-id="2f952-107">Windows 功能區架構會公開一組屬性，可讓應用程式指定在執行時間顯示功能區 UI 的方式。</span><span class="sxs-lookup"><span data-stu-id="2f952-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="2f952-108">簡介</span><span class="sxs-lookup"><span data-stu-id="2f952-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2f952-109">最小化功能區</span><span class="sxs-lookup"><span data-stu-id="2f952-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="2f952-110">隱藏功能區</span><span class="sxs-lookup"><span data-stu-id="2f952-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="2f952-111">範例</span><span class="sxs-lookup"><span data-stu-id="2f952-111">Example</span></span>](#example)
-   [<span data-ttu-id="2f952-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f952-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="2f952-113">簡介</span><span class="sxs-lookup"><span data-stu-id="2f952-113">Introduction</span></span>

<span data-ttu-id="2f952-114">若要將檔空間的可用區域最大化 (或查看功能區架構應用程式的 [埠]) ，應用程式可以指定功能區 UI 是可見或隱藏，而且在可見時，功能區是否為展開或折迭狀態。</span><span class="sxs-lookup"><span data-stu-id="2f952-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="2f952-115">下表所列的 [framework 屬性索引鍵](windowsribbon-reference-properties-framework.md) 可用來明確設定功能區架構應用程式中功能區 UI 的顯示特性。</span><span class="sxs-lookup"><span data-stu-id="2f952-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="2f952-116">這些屬性不會影響 [內容快顯功能表](windowsribbon-controls-contextpopup.md) 控制項的顯示。</span><span class="sxs-lookup"><span data-stu-id="2f952-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="2f952-117">顯示狀態</span><span class="sxs-lookup"><span data-stu-id="2f952-117">Display State</span></span>         | <span data-ttu-id="2f952-118">功能區屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="2f952-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="2f952-119">展開或折迭</span><span class="sxs-lookup"><span data-stu-id="2f952-119">Expanded or collapsed</span></span> | [<span data-ttu-id="2f952-120">\_ \_ 最小化 UI PKEY</span><span class="sxs-lookup"><span data-stu-id="2f952-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="2f952-121">可見或隱藏</span><span class="sxs-lookup"><span data-stu-id="2f952-121">Visible or hidden</span></span>     | [<span data-ttu-id="2f952-122">UI \_ PKEY \_ 可見</span><span class="sxs-lookup"><span data-stu-id="2f952-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="2f952-123">最小化功能區</span><span class="sxs-lookup"><span data-stu-id="2f952-123">Minimize the Ribbon</span></span>

<span data-ttu-id="2f952-124">功能區架構應用程式可以將 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性索引鍵的值設定為 **true** 或 **false**，以動態方式設定功能區命令列的最小化狀態。</span><span class="sxs-lookup"><span data-stu-id="2f952-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="2f952-125">顯示狀態</span><span class="sxs-lookup"><span data-stu-id="2f952-125">Display State</span></span> | <span data-ttu-id="2f952-126">屬性索引鍵值</span><span class="sxs-lookup"><span data-stu-id="2f952-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="2f952-127">展開</span><span class="sxs-lookup"><span data-stu-id="2f952-127">Expanded</span></span>      | <span data-ttu-id="2f952-128">**false**</span><span class="sxs-lookup"><span data-stu-id="2f952-128">**false**</span></span>          |
| <span data-ttu-id="2f952-129">Collapsed</span><span class="sxs-lookup"><span data-stu-id="2f952-129">Collapsed</span></span>     | <span data-ttu-id="2f952-130">**true**</span><span class="sxs-lookup"><span data-stu-id="2f952-130">**true**</span></span>           |



 

<span data-ttu-id="2f952-131">當功能區 UI 處於最小化狀態時，[功能區] 索引標籤資料列會維持可見且功能完整。</span><span class="sxs-lookup"><span data-stu-id="2f952-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="2f952-132">下列螢幕擷取畫面顯示最小化狀態的功能區。</span><span class="sxs-lookup"><span data-stu-id="2f952-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![顯示最小化功能區 ui 的螢幕擷取畫面。](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="2f952-134">功能區架構會透過功能區內容功能表的 [將功能區最小化] 選項，向終端使用者公開此功能。</span><span class="sxs-lookup"><span data-stu-id="2f952-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="2f952-135">隱藏功能區</span><span class="sxs-lookup"><span data-stu-id="2f952-135">Hide the Ribbon</span></span>

<span data-ttu-id="2f952-136">功能區架構應用程式可以將 [UI \_ PKEY 可 \_ 查看](windowsribbon-reference-properties-uipkey-viewable.md) 屬性索引鍵的值設定為 **true** 或 **false**，以動態方式設定功能區命令列的可見狀態。</span><span class="sxs-lookup"><span data-stu-id="2f952-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="2f952-137">顯示狀態</span><span class="sxs-lookup"><span data-stu-id="2f952-137">Display State</span></span> | <span data-ttu-id="2f952-138">屬性索引鍵值</span><span class="sxs-lookup"><span data-stu-id="2f952-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="2f952-139">可見</span><span class="sxs-lookup"><span data-stu-id="2f952-139">Visible</span></span>       | <span data-ttu-id="2f952-140">**false**</span><span class="sxs-lookup"><span data-stu-id="2f952-140">**false**</span></span>          |
| <span data-ttu-id="2f952-141">Hidden</span><span class="sxs-lookup"><span data-stu-id="2f952-141">Hidden</span></span>        | <span data-ttu-id="2f952-142">**true**</span><span class="sxs-lookup"><span data-stu-id="2f952-142">**true**</span></span>           |



 

<span data-ttu-id="2f952-143">相較于 [UI \_ PKEY \_ 最小化](windowsribbon-reference-properties-uipkey-minimized.md) 屬性，將 [ui PKEY 設定為 \_ \_](windowsribbon-reference-properties-uipkey-viewable.md) **false** ，可將功能區 ui 隱藏，而使用者完全無法使用。</span><span class="sxs-lookup"><span data-stu-id="2f952-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="2f952-144">下列螢幕擷取畫面顯示處於隱藏狀態的功能區。</span><span class="sxs-lookup"><span data-stu-id="2f952-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![顯示隱藏功能區 ui 的螢幕擷取畫面。](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="2f952-146">範例</span><span class="sxs-lookup"><span data-stu-id="2f952-146">Example</span></span>

<span data-ttu-id="2f952-147">下列範例示範如何在執行時間設定功能區 UI 的狀態。</span><span class="sxs-lookup"><span data-stu-id="2f952-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="2f952-148">在此情況下， [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 函式是用來根據 [切換按鈕](windowsribbon-controls-togglebutton.md)的切換狀態來展開或折迭功能區 UI。</span><span class="sxs-lookup"><span data-stu-id="2f952-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2f952-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f952-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f952-150">功能區屬性</span><span class="sxs-lookup"><span data-stu-id="2f952-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 