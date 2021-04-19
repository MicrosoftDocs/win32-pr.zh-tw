---
title: 執行 CEchoPropPage OnInitDialog
description: 執行 CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEchoPropPage OnInitDialog 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967610"
---
# <a name="implementing-cechoproppageoninitdialog"></a><span data-ttu-id="37905-109">執行 CEchoPropPage：： OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="37905-109">Implementing CEchoPropPage::OnInitDialog</span></span>

<span data-ttu-id="37905-110">**CEchoPropPage：： OnInitDialog** 方法是在 EchoPropPage 中執行。</span><span class="sxs-lookup"><span data-stu-id="37905-110">The **CEchoPropPage::OnInitDialog** method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="37905-111">它會在叫用 [屬性頁] 對話方塊時執行。</span><span class="sxs-lookup"><span data-stu-id="37905-111">It executes when the property page dialog box is invoked.</span></span> <span data-ttu-id="37905-112">此方法中的程式碼需要取出目前的屬性值，並將它們顯示在正確的編輯方塊中。</span><span class="sxs-lookup"><span data-stu-id="37905-112">The code in this method needs to retrieve the current property values and display them in the correct edit box.</span></span> <span data-ttu-id="37905-113">外掛程式 wizard 範例程式碼會為單一屬性提供實作為。</span><span class="sxs-lookup"><span data-stu-id="37905-113">The plug-in wizard sample code provides an implementation for a single property.</span></span> <span data-ttu-id="37905-114">您可以針對其中一個 Echo 範例屬性修改此程式碼，然後加入程式碼以取得第二個屬性值。</span><span class="sxs-lookup"><span data-stu-id="37905-114">You can modify this code for one of the Echo sample properties, and then add code to retrieve the second property value.</span></span>

## <a name="declaring-the-oninitdialog-method-variables"></a><span data-ttu-id="37905-115">宣告 OnInitDialog 方法變數</span><span class="sxs-lookup"><span data-stu-id="37905-115">Declaring the OnInitDialog Method Variables</span></span>

<span data-ttu-id="37905-116">首先，您必須移除 fScaleFactor 的宣告，並將其取代為下列變數聲明：</span><span class="sxs-lookup"><span data-stu-id="37905-116">First, you must remove the declaration of fScaleFactor and replace it with the following variable declarations:</span></span>


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a><span data-ttu-id="37905-117">從外掛程式中取出目前的值</span><span class="sxs-lookup"><span data-stu-id="37905-117">Retrieving the Current Values from the Plug-in</span></span>

<span data-ttu-id="37905-118">接著，程式碼應該會嘗試從回應外掛程式取得目前的屬性值。</span><span class="sxs-lookup"><span data-stu-id="37905-118">The code should next attempt to retrieve the current property values from the Echo plug-in.</span></span> <span data-ttu-id="37905-119">下列範例會嘗試取得每個屬性：</span><span class="sxs-lookup"><span data-stu-id="37905-119">The following example attempts to retrieve each property:</span></span>


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



<span data-ttu-id="37905-120">此對話方塊會將效果層級值顯示為整數，但外掛程式會將值儲存為浮點數。</span><span class="sxs-lookup"><span data-stu-id="37905-120">The dialog box displays the effects level value to the user as an integer, but the plug-in stores the value as a floating-point number.</span></span> <span data-ttu-id="37905-121">因此，程式碼會將浮點值轉換為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="37905-121">Therefore, the code converts the floating-point value to a **DWORD** value.</span></span>

## <a name="retrieving-the-current-values-from-the-registry"></a><span data-ttu-id="37905-122">從登錄中取出目前的值</span><span class="sxs-lookup"><span data-stu-id="37905-122">Retrieving the Current Values from the Registry</span></span>

<span data-ttu-id="37905-123">如果屬性頁無法從外掛程式取得目前的值，它必須嘗試從登錄讀取它們。</span><span class="sxs-lookup"><span data-stu-id="37905-123">If the property page cannot retrieve the current values from the plug-in, it must attempt to read them from the registry.</span></span> <span data-ttu-id="37905-124">下列程式碼會讀取每個屬性值：</span><span class="sxs-lookup"><span data-stu-id="37905-124">The following code reads each property value:</span></span>


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



<span data-ttu-id="37905-125">請注意您先前建立的登錄常數的使用。</span><span class="sxs-lookup"><span data-stu-id="37905-125">Notice the use of the registry constants you created previously.</span></span>

## <a name="displaying-the-values-to-the-user"></a><span data-ttu-id="37905-126">向使用者顯示值</span><span class="sxs-lookup"><span data-stu-id="37905-126">Displaying the Values to the User</span></span>

<span data-ttu-id="37905-127">最後，屬性頁必須在正確的編輯方塊控制項中顯示值。</span><span class="sxs-lookup"><span data-stu-id="37905-127">Finally, the property page must display the values in the correct edit box controls.</span></span> <span data-ttu-id="37905-128">下列範例程式碼示範：</span><span class="sxs-lookup"><span data-stu-id="37905-128">The following example code demonstrates this:</span></span>


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a><span data-ttu-id="37905-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="37905-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37905-130">**修改 Echo 範例屬性頁**</span><span class="sxs-lookup"><span data-stu-id="37905-130">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




