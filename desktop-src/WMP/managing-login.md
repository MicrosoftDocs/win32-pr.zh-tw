---
title: 管理登入
description: 管理登入
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player 線上商店、管理登入
- 線上商店、管理登入
- 輸入1個線上商店，管理登入
- Windows Media Player 線上商店，登入
- 線上商店，登入
- 輸入1個線上商店，登入
- Windows Media Player 線上商店、標準登入程式
- 線上商店、標準登入流程
- 輸入1個線上商店、標準登入流程
- Windows Media Player 線上商店、登出進程
- 線上商店、登出進程
- 輸入1個線上商店、登出進程
- 標準登入進程
- 登出進程
- 登入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374474"
---
# <a name="managing-login"></a><span data-ttu-id="5ffbd-118">管理登入</span><span class="sxs-lookup"><span data-stu-id="5ffbd-118">Managing Login</span></span>

<span data-ttu-id="5ffbd-119">Windows Media Player 支援各種不同的方法，讓使用者登入類型1線上商店。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="5ffbd-120">播放程式會提供標準的登入對話方塊，但線上商店可以提供作為標準對話方塊替代方案的網頁。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="5ffbd-121">使用者可以藉由與 Windows Media Player 使用者介面互動，或與線上商店所提供的探索頁面互動，來起始登入嘗試。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="5ffbd-122">如果使用者透過與探索頁面互動來起始登入嘗試，[探索] 頁面上的腳本會呼叫 [attemptLogin](external-attemptlogin.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="5ffbd-123">使用者的登入狀態是由線上商店所維護。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="5ffbd-124">當使用者的登入狀態變更，或登入嘗試失敗時，線上商店的外掛程式會藉由呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)、在 *類型* 參數中傳遞 wmpcnLoginStateChange，來通知 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="5ffbd-125">播放程式會藉由引發 [OnLoginChange](external-onloginchange-event.md) 事件，將通知傳遞至探索頁面。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="5ffbd-126">對 **OnLoginChange** 的呼叫不一定表示使用者的登入狀態已變更;這可能表示嘗試登入失敗。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="5ffbd-127">若要判斷使用者的登入狀態， **OnLoginChange** 事件處理常式可以檢查 [userLoggedIn](external-userloggedin.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="5ffbd-128">下列各節說明標準登入程式、替代的登入程式，以及登出進程。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="5ffbd-129">標準登入</span><span class="sxs-lookup"><span data-stu-id="5ffbd-129">Standard Log-in</span></span>

<span data-ttu-id="5ffbd-130">標準登入套裝程式含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5ffbd-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="5ffbd-131">使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登入嘗試。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="5ffbd-132">Windows Media Player 會顯示一個對話方塊，提示使用者輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="5ffbd-133">當使用者按一下對話方塊中的 [登 **入** ] 按鈕時，Windows Media Player 會呼叫 [IWMPContentPartner：： Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)（由線上商店的外掛程式所執行）。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="5ffbd-134">外掛程式會與線上存放區通訊，且成功或無法登入使用者。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="5ffbd-135">如果登入嘗試成功，則外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT TRUE。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="5ffbd-136">如果登入嘗試失敗，外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並在 *PCoNtext* 參數的 **ulVal** 成員中傳遞32位值。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="5ffbd-137">然後，播放程式會將該32位值傳遞給 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) ，以取得可處理失敗之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="5ffbd-138">替代登入</span><span class="sxs-lookup"><span data-stu-id="5ffbd-138">Alternative Login</span></span>

<span data-ttu-id="5ffbd-139">如果 \_ \_ 已在線上商店外掛程式的 [ **功能** ] 登錄專案中設定訂用帳戶上限 ALTLOGIN 旗標，Windows Media Player 不會使用 [標準登入] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="5ffbd-140">相反地，Windows Media Player 會呼叫 **IWMPContentPartner：： GetItemInfo** 來取得執行登入程式之網頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="5ffbd-141">如需 **功能** 登錄專案的詳細資訊，請參閱 [類型1線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-1-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="5ffbd-142">播放程式會呼叫 **GetItemInfo** 兩次：一次傳遞 g \_ szItemInfo \_ ALTLoginURL 以抓取登入網頁的 URL，以及通過 g \_ szItemInfo \_ ALTLoginCaption 來取得裝載網頁之視窗的標題。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="5ffbd-143">當 **GetItemInfo** 傳回登入網頁的 url 時，可以將下列參數字串附加至 URL，以指定登入視窗的大小：</span><span class="sxs-lookup"><span data-stu-id="5ffbd-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="5ffbd-144">?DlgX =*width*&DlgY =*height*</span><span class="sxs-lookup"><span data-stu-id="5ffbd-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="5ffbd-145">在參數字串中， *寬度* 和 *高度* 是視窗的寬度和高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="5ffbd-146">例如， **GetItemInfo** 可能會傳回下列字串，以指定要在寬度為800圖元且高度為400圖元的視窗中顯示 AltLogin.htm</span><span class="sxs-lookup"><span data-stu-id="5ffbd-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="5ffbd-147">替代的登入套裝程式含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="5ffbd-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="5ffbd-148">使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登入嘗試。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="5ffbd-149">Windows Media Player 會開啟一個強制回應視窗，以顯示線上商店所提供的登入網頁。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="5ffbd-150">網頁會與線上商店通訊，且成功或無法登入使用者。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="5ffbd-151">如果登入嘗試成功，網頁會呼叫 [sendMessage](external-sendmessage.md)來通知線上商店的外掛程式，這會導致呼叫 [IWMPContentPartner：： sendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="5ffbd-152">線上商店的外掛程式會檢查傳遞給 **IWMPContentPartner：： SendMessage** 的參數，以判斷登入嘗試成功。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="5ffbd-153">這些參數不會由 Windows Media Player 來解讀。它們只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="5ffbd-154">外掛程式會呼叫 **IWMPContentPartnerCallback：： Notify**，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT TRUE。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="5ffbd-155">如果登入失敗，線上商店必須決定如何協助使用者。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="5ffbd-156">其中一個可能的原因是在裝載替代登入網頁的強制回應視窗中顯示新網頁。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="5ffbd-157">登出</span><span class="sxs-lookup"><span data-stu-id="5ffbd-157">Log-out</span></span>

<span data-ttu-id="5ffbd-158">登出進程包含下列步驟。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="5ffbd-159">使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登出嘗試。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="5ffbd-160">Windows Media Player 會呼叫 [IWMPContentPartner：：登出](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)，這是由線上商店的外掛程式所執行。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="5ffbd-161">外掛程式會與線上商店通訊，而且會成功或無法登出使用者。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="5ffbd-162">如果登入嘗試成功，外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT FALSE。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="5ffbd-163">嘗試登入或登出成功時，線上商店的外掛程式會呼叫 **IWMPContentPartnerCallback：： Notify**，在 *類型* 參數中傳遞 wmpcnLoginStateChange。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="5ffbd-164">外掛程式會使用 *pCoNtext* 參數來指定使用者目前的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="5ffbd-165">如果外掛程式將 *pCoNtext* -> **boolVal** 設定為 VARIANT \_ TRUE，就會將使用者登入。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="5ffbd-166">如果外掛程式將 *pCoNtext* -> **boolVal** 設定為 VARIANT \_ FALSE，則會將使用者登出。請注意， *pCoNtext* 不會指出嘗試成功或失敗;相反地，它會指出使用者目前的登入狀態。</span><span class="sxs-lookup"><span data-stu-id="5ffbd-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ffbd-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ffbd-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ffbd-168">**AttemptLogin**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="5ffbd-169">**OnLoginChange 事件**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="5ffbd-170">**UserLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="5ffbd-171">**IWMPContentPartner：： Login**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="5ffbd-172">**IWMPContentPartner：：登出**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="5ffbd-173">**類型1線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="5ffbd-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




