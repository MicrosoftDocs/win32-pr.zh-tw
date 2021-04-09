---
title: 實施 CEchoPropPage 適用
description: 實施 CEchoPropPage 適用
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEchoPropPage Apply 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840199"
---
# <a name="implementing-cechoproppageapply"></a><span data-ttu-id="3e69c-109">執行 CEchoPropPage：： Apply</span><span class="sxs-lookup"><span data-stu-id="3e69c-109">Implementing CEchoPropPage::Apply</span></span>

<span data-ttu-id="3e69c-110">CEchoPropPage：： Apply 方法是在 EchoPropPage 中執行。</span><span class="sxs-lookup"><span data-stu-id="3e69c-110">The CEchoPropPage::Apply method is implemented in EchoPropPage.cpp.</span></span> <span data-ttu-id="3e69c-111">當使用者在 Windows Media Player 的 [屬性頁] 對話方塊 **中按一下 [** 套用] 時，就會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="3e69c-111">It executes when the user clicks **Apply** in the property page dialog box in Windows Media Player.</span></span> <span data-ttu-id="3e69c-112">外掛程式 wizard 範例程式碼會提供處理單一屬性的執行。</span><span class="sxs-lookup"><span data-stu-id="3e69c-112">The plug-in wizard sample code provides an implementation to handle a single property.</span></span> <span data-ttu-id="3e69c-113">您可以針對其中一個 Echo 範例屬性修改此程式碼，然後加入程式碼以儲存其他屬性值。</span><span class="sxs-lookup"><span data-stu-id="3e69c-113">You can modify this code for one of the Echo sample properties, and then add code to store the other property value.</span></span>

## <a name="declaring-the-apply-method-variables"></a><span data-ttu-id="3e69c-114">宣告 Apply 方法變數</span><span class="sxs-lookup"><span data-stu-id="3e69c-114">Declaring the Apply Method Variables</span></span>

<span data-ttu-id="3e69c-115">首先，您必須移除 fScaleFactor 的宣告。</span><span class="sxs-lookup"><span data-stu-id="3e69c-115">First, you must remove the declaration of fScaleFactor.</span></span> <span data-ttu-id="3e69c-116">然後，新增您將需要的變數宣告。</span><span class="sxs-lookup"><span data-stu-id="3e69c-116">Then, add variable declarations that you will need.</span></span> <span data-ttu-id="3e69c-117">下列範例顯示已完成的變數宣告：</span><span class="sxs-lookup"><span data-stu-id="3e69c-117">The following example shows the completed variable declarations:</span></span>


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a><span data-ttu-id="3e69c-118">從屬性頁中取出值</span><span class="sxs-lookup"><span data-stu-id="3e69c-118">Retrieving the Values from the Property Page</span></span>

<span data-ttu-id="3e69c-119">您必須執行程式碼，以取出並驗證使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="3e69c-119">You must implement code to retrieve and validate the user input.</span></span> <span data-ttu-id="3e69c-120">下列程式碼範例會從 IDC \_ DELAYTIME 編輯方塊中抓取延遲時間值，然後確認值是否在指定的範圍內：</span><span class="sxs-lookup"><span data-stu-id="3e69c-120">The following code example retrieves the delay time value from the IDC\_DELAYTIME edit box, and then verifies that the value is within a specified range:</span></span>


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



<span data-ttu-id="3e69c-121">如果使用者輸入不在指定的範圍內，則程式碼會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="3e69c-121">If the user input is not in the specified range, the code displays a message box.</span></span> <span data-ttu-id="3e69c-122">請注意您稍早為錯誤訊息所建立的字串資源使用。</span><span class="sxs-lookup"><span data-stu-id="3e69c-122">Notice the use of the string resource you created earlier for the error message.</span></span>

<span data-ttu-id="3e69c-123">下列範例會從 IDC \_ WETMIX 編輯方塊中抓取效果等級，然後驗證值是否在指定的範圍內：</span><span class="sxs-lookup"><span data-stu-id="3e69c-123">The following example retrieves the effect level from the IDC\_WETMIX edit box and then verifies that the value is within a specified range:</span></span>


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a><span data-ttu-id="3e69c-124">將屬性值儲存在登錄中</span><span class="sxs-lookup"><span data-stu-id="3e69c-124">Storing the Property Values in the Registry</span></span>

<span data-ttu-id="3e69c-125">接下來，您的程式碼必須將新的屬性值保存到登錄中。</span><span class="sxs-lookup"><span data-stu-id="3e69c-125">Next, your code must persist the new property values to the registry.</span></span> <span data-ttu-id="3e69c-126">下列程式碼會儲存這兩個屬性值：</span><span class="sxs-lookup"><span data-stu-id="3e69c-126">The following code stores both property values:</span></span>


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a><span data-ttu-id="3e69c-127">更新 Echo 外掛程式屬性值</span><span class="sxs-lookup"><span data-stu-id="3e69c-127">Updating the Echo Plug-in Property Values</span></span>

<span data-ttu-id="3e69c-128">**Apply** 方法必須通知回應外掛程式屬性值已變更。</span><span class="sxs-lookup"><span data-stu-id="3e69c-128">The **Apply** method must inform the Echo plug-in that the property values have changed.</span></span> <span data-ttu-id="3e69c-129">下列程式碼會使用在 CEchoPropPage：： SetObjects 中抓取的介面指標，呼叫每個屬性的屬性 put 方法：</span><span class="sxs-lookup"><span data-stu-id="3e69c-129">The following code calls the property put method for each property using the interface pointer retrieved in CEchoPropPage::SetObjects:</span></span>


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



<span data-ttu-id="3e69c-130">請注意，濕混合值會在傳遞至外掛程式之前轉換成浮點數。</span><span class="sxs-lookup"><span data-stu-id="3e69c-130">Notice that the wet mix value is converted to floating point before being passed to the plug-in.</span></span>

## <a name="disabling-the-apply-button"></a><span data-ttu-id="3e69c-131">停用 [套用] 按鈕</span><span class="sxs-lookup"><span data-stu-id="3e69c-131">Disabling the Apply Button</span></span>

<span data-ttu-id="3e69c-132">在最後一個步驟中，您的程式碼應該會在 [屬性頁] 對話方塊中停用 [套用]，以通知使用者值已成功更新。</span><span class="sxs-lookup"><span data-stu-id="3e69c-132">As a final step, your code should disable Apply in the property page dialog box as a signal to the user that the values have been successfully updated.</span></span> <span data-ttu-id="3e69c-133">這需要下列一行程式碼：</span><span class="sxs-lookup"><span data-stu-id="3e69c-133">This requires the following single line of code:</span></span>


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a><span data-ttu-id="3e69c-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e69c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e69c-135">**修改 Echo 範例屬性頁**</span><span class="sxs-lookup"><span data-stu-id="3e69c-135">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




