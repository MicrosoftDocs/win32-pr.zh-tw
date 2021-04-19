---
title: 類型1線上商店的登錄機碼和專案
description: 類型1線上商店的登錄機碼和專案
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player 線上商店，登錄
- 線上商店、登錄
- 輸入1個線上商店、登錄
- 登錄，請輸入1個線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966440"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="c8ecd-107">類型1線上商店的登錄機碼和專案</span><span class="sxs-lookup"><span data-stu-id="c8ecd-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="c8ecd-108">若要在 Windows Media Player 中提供類型1線上商店，線上商店提供者必須在使用者的電腦上建立下列登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="c8ecd-109">將 DllSurrogate 的值設為空字串，表示 COM 執行時間會將線上商店的外掛程式載入預設 DLL 代理，dllhost.exe。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="c8ecd-110">在上述的登錄語法中，以斜體表示的符號是 (Guid) 的名稱和全域唯一識別碼的預留位置，這些是線上商店專屬的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="c8ecd-111">下表描述這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="c8ecd-112">預留位置</span><span class="sxs-lookup"><span data-stu-id="c8ecd-112">Placeholder</span></span>    | <span data-ttu-id="c8ecd-113">描述</span><span class="sxs-lookup"><span data-stu-id="c8ecd-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ecd-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-114">*keyName*</span></span>      | <span data-ttu-id="c8ecd-115">在 Microsoft 與線上商店之間同意的字串。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="c8ecd-116">這個字串可唯一識別線上商店。範例： "Proseware"</span><span class="sxs-lookup"><span data-stu-id="c8ecd-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="c8ecd-117">*flags*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-117">*flags*</span></span>        | <span data-ttu-id="c8ecd-118">一或多個外掛程式功能旗標的位 **or** 會指定 Windows Media Player 是否應該呼叫 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)的特定方法。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="c8ecd-119">如需支援之旗標的詳細資訊，請參閱此表格後面的外掛程式功能旗標表。範例：00000058</span><span class="sxs-lookup"><span data-stu-id="c8ecd-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="c8ecd-120">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-120">*clsid*</span></span>        | <span data-ttu-id="c8ecd-121">GUID，也就是在線上商店的外掛程式中執行 **IWMPContentPartner** 之類別的類別識別碼 (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="c8ecd-122">此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="c8ecd-123">*友好*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-123">*friendlyname*</span></span> | <span data-ttu-id="c8ecd-124">線上商店的易記名稱。範例：「Proseware 音樂服務」</span><span class="sxs-lookup"><span data-stu-id="c8ecd-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="c8ecd-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-125">*appid*</span></span>        | <span data-ttu-id="c8ecd-126">GUID，這是線上商店的外掛程式 (AppID) 的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="c8ecd-127">此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="c8ecd-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-128">*pluginName*</span></span>   | <span data-ttu-id="c8ecd-129">線上商店外掛程式的名稱。範例： "Proseware Content Partner 外掛程式"</span><span class="sxs-lookup"><span data-stu-id="c8ecd-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="c8ecd-130">*className*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-130">*className*</span></span>    | <span data-ttu-id="c8ecd-131">在線上商店的外掛程式中，用來執行 **IWMPContentpartner** 的類別名稱。範例： "CProsewarePartner"</span><span class="sxs-lookup"><span data-stu-id="c8ecd-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="c8ecd-132">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-132">*moduleName*</span></span>   | <span data-ttu-id="c8ecd-133">執行線上存放區外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="c8ecd-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="c8ecd-134">*執行緒*</span><span class="sxs-lookup"><span data-stu-id="c8ecd-134">*threading*</span></span>    | <span data-ttu-id="c8ecd-135">外掛程式執行所在的公寓型別。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="c8ecd-136">">threadingmodel" = "公寓" 表示外掛程式會在單一執行緒的單元 (STA) 中執行。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="c8ecd-137">">threadingmodel" = "Free" 表示外掛程式會在多執行緒單元 (MTA) 中執行。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="c8ecd-138">下表描述外掛程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="c8ecd-139">旗標</span><span class="sxs-lookup"><span data-stu-id="c8ecd-139">Flag</span></span>                                    | <span data-ttu-id="c8ecd-140">值</span><span class="sxs-lookup"><span data-stu-id="c8ecd-140">Value</span></span> | <span data-ttu-id="c8ecd-141">描述</span><span class="sxs-lookup"><span data-stu-id="c8ecd-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ecd-142">訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="c8ecd-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="c8ecd-143">0x8</span><span class="sxs-lookup"><span data-stu-id="c8ecd-143">0x8</span></span>   | <span data-ttu-id="c8ecd-144">Windows Media Player 應呼叫 [IWMPContentPartner：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) ，以通知外掛程式應該啟動並停止背景處理。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="c8ecd-145">訂用帳戶 \_ 上限 \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c8ecd-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="c8ecd-146">0x10</span><span class="sxs-lookup"><span data-stu-id="c8ecd-146">0x10</span></span>  | <span data-ttu-id="c8ecd-147">Windows Media Player 應呼叫 [IWMPContentPartner：： UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice)。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="c8ecd-148">訂用帳戶 \_ 上限 \_ 為 \_ CONTENTPARTNER</span><span class="sxs-lookup"><span data-stu-id="c8ecd-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="c8ecd-149">0x40</span><span class="sxs-lookup"><span data-stu-id="c8ecd-149">0x40</span></span>  | <span data-ttu-id="c8ecd-150">通知 Windows Media Player 外掛程式會執行 **IWMPContentPartner** 介面。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="c8ecd-151">所有類型1線上商店外掛程式都必須設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="c8ecd-152">訂用帳戶 \_ 上限 \_ ALTLOGIN</span><span class="sxs-lookup"><span data-stu-id="c8ecd-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="c8ecd-153">0x80</span><span class="sxs-lookup"><span data-stu-id="c8ecd-153">0x80</span></span>  | <span data-ttu-id="c8ecd-154">通知 Windows Media Player 外掛程式支援替代登入。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="c8ecd-155">如果外掛程式支援替代登入，Windows Media Player 會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，以抓取替代登入 URL 和標題。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="c8ecd-156">**用於開發和測試的登錄專案**</span><span class="sxs-lookup"><span data-stu-id="c8ecd-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="c8ecd-157">當您開始開發線上商店時，Microsoft 會提供您兩個金鑰：測試金鑰和生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="c8ecd-158">在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，您的線上商店才會出現在 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="c8ecd-159">如需有關測試和生產金鑰的詳細資訊，請參閱 [類型1線上商店的測試和生產金鑰](test-and-production-keys-for-a-type-1-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="c8ecd-160">將您的測試或生產金鑰放在登錄中的下列位置。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="c8ecd-161">請注意，TestParameter 登錄專案的值可以指定多個測試或生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="c8ecd-162">例如，假設 Proseware 的測試金鑰為 "1234"，而 Contoso 的測試金鑰為 "2345"。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="c8ecd-163">下列登錄專案指定 Proseware 和 Contoso 的測試存放區將會出現在 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="c8ecd-164">**ActiveService 登錄專案**</span><span class="sxs-lookup"><span data-stu-id="c8ecd-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="c8ecd-165">當使用者啟動線上商店時，Windows Media Player 寫入登錄中的資訊，以識別作用中的線上商店。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="c8ecd-166">Windows Media Player 將資訊放在使用者電腦上登錄的下列位置中。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="c8ecd-167">在上述的登錄語法中， *serviceInfo* 是字串的預留位置，其中包含作用中線上商店的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="c8ecd-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ecd-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8ecd-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ecd-169">**類型 1 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="c8ecd-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





