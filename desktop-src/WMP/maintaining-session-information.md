---
title: 維護會話資訊
description: 維護會話資訊
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，維護會話資訊
- 線上商店，維護會話資訊
- 輸入2個線上商店，維護會話資訊
- Windows Media Player 線上商店、會話資訊
- 線上商店、會話資訊
- 輸入2個線上商店、會話資訊
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 維護會話資訊
- 會話資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311540"
---
# <a name="maintaining-session-information"></a><span data-ttu-id="7bc4a-117">維護會話資訊</span><span class="sxs-lookup"><span data-stu-id="7bc4a-117">Maintaining Session Information</span></span>

## <a name="how-the-sample-stores-information"></a><span data-ttu-id="7bc4a-118">範例如何儲存資訊</span><span class="sxs-lookup"><span data-stu-id="7bc4a-118">How the Sample Stores Information</span></span>

<span data-ttu-id="7bc4a-119">範例網頁會使用 cookie 來維護資料。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-119">The sample webpage maintains data by using cookies.</span></span> <span data-ttu-id="7bc4a-120">Cookie 只是網頁瀏覽器可為您儲存的持續性名稱/值配對。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-120">Cookies are simply persistent name/value pairs that the Web browser can store for you.</span></span>

<span data-ttu-id="7bc4a-121">當網頁關閉時，就會執行 **關機** 功能。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-121">When the webpage closes, the **Shutdown** function runs.</span></span> <span data-ttu-id="7bc4a-122">**Shutdown** 會呼叫 **SetPendingCookies** 函數。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-122">**Shutdown** calls the function **SetPendingCookies**.</span></span> <span data-ttu-id="7bc4a-123">此函式會透過下載集合清單來迴圈，該清單會儲存在名為 selDLC 的下拉式清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-123">This function loops through the download collection list, stored in the drop-down list box named selDLC.</span></span> <span data-ttu-id="7bc4a-124">如果下載集合包含未完成的專案，則函式會呼叫 **system.windows.application.setcookie** 方法，並傳遞名稱和值。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-124">If a download collection contains incomplete items, the function calls the method **SetCookie**, passing a name and a value.</span></span> <span data-ttu-id="7bc4a-125">名稱字串的判斷方式是將整數值附加至常數值 **WMPDLC**，此值會儲存在名為 g sPreCookie 的變數中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-125">The name string is determined by appending an integer value to a constant value, **WMPDLC**, which is stored in the variable named g\_sPreCookie.</span></span> <span data-ttu-id="7bc4a-126">例如，針對第三個暫止的下載集合，cookie 名稱會是 "WMPDLC2"，因為電腦制是以零為基底。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-126">For instance, for the third pending download collection, the cookie name would be "WMPDLC2", because the counting mechanism is zero-based.</span></span> <span data-ttu-id="7bc4a-127">當每個 cookie 建立時，函式會將全域變數 g 暫止， \_ 以保留暫止下載的計數。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-127">As each cookie is created, the function increments the global variable g\_Pending to keep a count of pending downloads.</span></span> <span data-ttu-id="7bc4a-128">為了方便起見，我們會在這裡重現程式碼：</span><span class="sxs-lookup"><span data-stu-id="7bc4a-128">The code is reproduced here for your convenience:</span></span>


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



<span data-ttu-id="7bc4a-129">**IsDLCComplete** 是 helper 函式，只會在下載集合中的每個下載專案之間進行迴圈，以判斷是否有任何專案擱置。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-129">**IsDLCComplete** is a helper function that simply loops through each download item in the download collection to determine whether any item is pending.</span></span> <span data-ttu-id="7bc4a-130">如果有暫止的專案，函數會傳回 false。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-130">If there is a pending item, the function returns false.</span></span>

<span data-ttu-id="7bc4a-131">**System.windows.application.setcookie** 是建立 cookie 的函式。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-131">**SetCookie** is the function that creates the cookie.</span></span>

<span data-ttu-id="7bc4a-132">當 **SetPendingCookies** 傳回時， **Shutdown** 會建立計數 cookie，以儲存來引數 g 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-132">When **SetPendingCookies** returns, **Shutdown** creates the count cookie, which stores the value from the variable g\_Pending.</span></span> <span data-ttu-id="7bc4a-133">此值很重要，因為網頁需要一種方式來決定重載時要取出的 cookie 數目。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-133">This value is important because the webpage needs a way to determine how many cookies to retrieve when it reloads.</span></span> <span data-ttu-id="7bc4a-134">計數 cookie 名稱會儲存在名為 g sCountCookie 的變數中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-134">The count cookie name is stored in the variable named g\_sCountCookie.</span></span>

## <a name="how-the-sample-retrieves-information"></a><span data-ttu-id="7bc4a-135">範例如何捕獲資訊</span><span class="sxs-lookup"><span data-stu-id="7bc4a-135">How the Sample Retrieves Information</span></span>

<span data-ttu-id="7bc4a-136">當網頁載入時， **Init** 函式就會執行。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-136">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="7bc4a-137">首先，此函式會呼叫 **GetPendingDlCount** 來取得計數 cookie。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-137">First, the function calls **GetPendingDlCount** to retrieve the count cookie.</span></span> <span data-ttu-id="7bc4a-138">接下來，它會將此值儲存在名為 g Pending 的變數中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-138">Next, it stores this value in the variable named g\_Pending.</span></span> <span data-ttu-id="7bc4a-139">然後，它會呼叫 **PopulateDLList** 函式，以抓取每個下載會話 cookie，並將其識別碼新增至下拉式清單方塊。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-139">Then it calls the **PopulateDLList** function to retrieve each download session cookie and add its identifier to the drop-down list box.</span></span> <span data-ttu-id="7bc4a-140">以下是該函式的程式碼：</span><span class="sxs-lookup"><span data-stu-id="7bc4a-140">Here is the code for that function:</span></span>


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



<span data-ttu-id="7bc4a-141">函數 **ClearList** 會從清單方塊中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-141">The function **ClearList** removes all items from the list box.</span></span>

<span data-ttu-id="7bc4a-142">然後，函數會進入迴圈。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-142">The function then enters a loop.</span></span> <span data-ttu-id="7bc4a-143">每個 cookie 名稱都是以字串的形式建立，然後藉由呼叫 helper 函式 **system.windows.application.getcookie** 來取出 cookie。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-143">Each cookie name is built as a string, and then the cookie is retrieved by calling the helper function **GetCookie**.</span></span> <span data-ttu-id="7bc4a-144">一旦抓取之後，cookie 就會藉由呼叫 **DelCookie** 來刪除。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-144">Once retrieved, the cookie is deleted by calling **DelCookie**.</span></span> <span data-ttu-id="7bc4a-145">如果 cookie 有值，則會將值加入清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-145">If the cookie has a value, the value is added to the list box.</span></span> <span data-ttu-id="7bc4a-146">此動作會起始 selDLC 清單的 **onChange** 事件，然後再呼叫名為 **OnSelectDLC** 的處理常式函式。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-146">This action initiates the **onChange** event for the selDLC list, which in turn calls the handler function named **OnSelectDLC**.</span></span> <span data-ttu-id="7bc4a-147">這是使用者選取下載集合時所執行的相同功能;這是填入 [下載專案] 清單方塊的程式碼。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-147">This is the same function that executes when the user selects a download collection; it is the code that fills the download item list box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc4a-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="7bc4a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc4a-149">**使用下載管理員**</span><span class="sxs-lookup"><span data-stu-id="7bc4a-149">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




