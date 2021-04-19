---
title: Spinner
description: 微調項是由遞增按鈕、遞減按鈕和編輯控制項所組成的複合控制項，它們全都是用來提供十進位值給應用程式。
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0875fb31d0dac73c88f3bd502746c473dc1c2b1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "106969944"
---
# <a name="spinner"></a><span data-ttu-id="ebfd7-103">Spinner</span><span class="sxs-lookup"><span data-stu-id="ebfd7-103">Spinner</span></span>

<span data-ttu-id="ebfd7-104">微調項是由遞增按鈕、遞減按鈕和編輯控制項所組成的複合控制項，它們全都是用來提供十進位值給應用程式。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-104">The Spinner is a composite control that consists of an increment button, a decrement button, and an edit control, all of which are used to provide decimal values to the application.</span></span>

-   [<span data-ttu-id="ebfd7-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="ebfd7-105">Details</span></span>](#details)
-   [<span data-ttu-id="ebfd7-106">微調屬性</span><span class="sxs-lookup"><span data-stu-id="ebfd7-106">Spinner Properties</span></span>](#spinner-properties)
-   [<span data-ttu-id="ebfd7-107">備註</span><span class="sxs-lookup"><span data-stu-id="ebfd7-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ebfd7-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebfd7-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="ebfd7-109">詳細資料</span><span class="sxs-lookup"><span data-stu-id="ebfd7-109">Details</span></span>

<span data-ttu-id="ebfd7-110">下列螢幕擷取畫面說明功能區微調。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-110">The following screen shot illustrates the Ribbon Spinner.</span></span>

![windows live moviemaker 功能區中微調控制項的螢幕擷取畫面。](images/controls/spinner.png)

## <a name="spinner-properties"></a><span data-ttu-id="ebfd7-112">微調屬性</span><span class="sxs-lookup"><span data-stu-id="ebfd7-112">Spinner Properties</span></span>

<span data-ttu-id="ebfd7-113">功能區架構會為微調控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Spinner control.</span></span>

<span data-ttu-id="ebfd7-114">一般來說，在功能區 UI 中，會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法來使與控制項相關聯的命令失效，以更新微調屬性。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-114">Typically, a Spinner property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="ebfd7-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="ebfd7-116">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="ebfd7-117">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="ebfd7-118">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="ebfd7-119">下表列出與微調控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-119">The following table lists the property keys that are associated with the Spinner control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebfd7-120">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="ebfd7-120">Property Key</span></span></th>
<th><span data-ttu-id="ebfd7-121">備註</span><span class="sxs-lookup"><span data-stu-id="ebfd7-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebfd7-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span></span></td>
<td><span data-ttu-id="ebfd7-123">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-123">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span></span></td>
<td><span data-ttu-id="ebfd7-125">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ebfd7-126">如果與控制項相關聯的命令透過呼叫 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework：： InvalidateUICommand</strong></a>而失效，則架構 <code>UI_INVALIDATIONS_VALUE</code> 會在傳遞做為 <em>旗標</em>的值時查詢此屬性。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="ebfd7-128">支援 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework：： GetUICommandProperty</strong></a> 和 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework：： SetUICommandProperty</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span></span></td>
<td><span data-ttu-id="ebfd7-130">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span></span></td>
<td><span data-ttu-id="ebfd7-132">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="ebfd7-134">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="ebfd7-136">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="ebfd7-138">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="ebfd7-140">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span></span></td>
<td><span data-ttu-id="ebfd7-142">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span></span></td>
<td><span data-ttu-id="ebfd7-144">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span></span></td>
<td><span data-ttu-id="ebfd7-146">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="ebfd7-148">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="ebfd7-150">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ebfd7-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="ebfd7-152">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-152">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebfd7-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="ebfd7-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="ebfd7-154">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-154">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ebfd7-155">下列程式碼區段會示範如何在 [**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) 方法中更新微調控制項的各種屬性。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-155">The following section of code demonstrates how various properties of the Spinner control are updated in the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method.</span></span>


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="ebfd7-156">備註</span><span class="sxs-lookup"><span data-stu-id="ebfd7-156">Remarks</span></span>

<span data-ttu-id="ebfd7-157">如果微調按鈕 ([UI \_ PKEY \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) 的最小值已初始化為0.0，應用程式應該確保控制項提供的任何後續值都不等於-0.0 (負零) 。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-157">If the minimum value ([UI\_PKEY\_MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) of a Spinner is initialized to 0.0, the application should ensure that any subsequent value supplied by the control does not equal -0.0 (negative zero).</span></span> <span data-ttu-id="ebfd7-158">如果微調項的值為-0.0，則應用程式應該使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法將這個值重設為 0.0 (正零) ，如微調控制項的 [**IUICommandHandler：： Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) 方法範例所示。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-158">If the Spinner supplies a value of -0.0, the application should reset this value to 0.0 (positive zero) using the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method as shown in the following example of an [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Spinner control.</span></span>

> [!Note]  
> <span data-ttu-id="ebfd7-159">如果未執行此測試，且值未更正，則控制項的 [編輯] 欄位會顯示字串 "Auto"。</span><span class="sxs-lookup"><span data-stu-id="ebfd7-159">If this test is not performed and the value left uncorrected, the edit field of the control displays the string "Auto".</span></span>

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ebfd7-160">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebfd7-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebfd7-161">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="ebfd7-161">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="ebfd7-162">**微調標記元素**</span><span class="sxs-lookup"><span data-stu-id="ebfd7-162">**Spinner markup element**</span></span>](windowsribbon-element-spinner.md)
</dt> </dl>

