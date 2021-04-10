---
title: Type 2 線上商店的登錄機碼和專案
description: Type 2 線上商店的登錄機碼和專案
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player 線上商店，登錄
- 線上商店、登錄
- 輸入2個線上商店、登錄
- 登錄，類型2線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104092578"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="80c96-107">Type 2 線上商店的登錄機碼和專案</span><span class="sxs-lookup"><span data-stu-id="80c96-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="80c96-108">本章節描述專為線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="80c96-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="80c96-109">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="80c96-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="80c96-110">若要在 Windows Media Player 中提供類型2線上商店，線上商店提供者必須在使用者的電腦上建立下列登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="80c96-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="80c96-111">在上述的登錄語法中，以斜體表示的符號是 (Guid) 的名稱和全域唯一識別碼的預留位置，這些是線上商店專屬的識別碼。</span><span class="sxs-lookup"><span data-stu-id="80c96-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="80c96-112">下表描述這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="80c96-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="80c96-113">預留位置</span><span class="sxs-lookup"><span data-stu-id="80c96-113">Placeholder</span></span>    | <span data-ttu-id="80c96-114">描述</span><span class="sxs-lookup"><span data-stu-id="80c96-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c96-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="80c96-115">*keyName*</span></span>      | <span data-ttu-id="80c96-116">在 Microsoft 與線上商店之間同意的字串。</span><span class="sxs-lookup"><span data-stu-id="80c96-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="80c96-117">這個字串可唯一識別線上商店。範例： "Proseware"</span><span class="sxs-lookup"><span data-stu-id="80c96-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="80c96-118">*flags*</span><span class="sxs-lookup"><span data-stu-id="80c96-118">*flags*</span></span>        | <span data-ttu-id="80c96-119">一或多個外掛程式功能旗標的位 **or** 會指定 Windows Media Player 是否應該呼叫 [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) 和 [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)的特定方法。</span><span class="sxs-lookup"><span data-stu-id="80c96-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="80c96-120">如需支援之旗標的詳細資訊，請參閱此表格後面的外掛程式功能旗標表。範例：00000037</span><span class="sxs-lookup"><span data-stu-id="80c96-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="80c96-121">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="80c96-121">*clsid*</span></span>        | <span data-ttu-id="80c96-122">GUID，也就是在線上商店的外掛程式中執行 **IWMPSubscriptionService** 之類別的類別識別碼 (CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="80c96-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="80c96-123">此 GUID 必須是登錄格式，以大括弧完成。格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="80c96-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="80c96-124">*友好*</span><span class="sxs-lookup"><span data-stu-id="80c96-124">*friendlyname*</span></span> | <span data-ttu-id="80c96-125">線上商店的易記名稱。範例：「Proseware 音樂服務」</span><span class="sxs-lookup"><span data-stu-id="80c96-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="80c96-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="80c96-126">*pluginName*</span></span>   | <span data-ttu-id="80c96-127">線上商店外掛程式的名稱。範例： "Proseware Service 外掛程式"</span><span class="sxs-lookup"><span data-stu-id="80c96-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="80c96-128">*className*</span><span class="sxs-lookup"><span data-stu-id="80c96-128">*className*</span></span>    | <span data-ttu-id="80c96-129">在線上商店的外掛程式中，用來執行 **IWMPSubscriptionService** 的類別名稱。範例： "CProsewareService"</span><span class="sxs-lookup"><span data-stu-id="80c96-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="80c96-130">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="80c96-130">*moduleName*</span></span>   | <span data-ttu-id="80c96-131">執行線上存放區外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="80c96-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="80c96-132">下表描述外掛程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="80c96-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="80c96-133">旗標</span><span class="sxs-lookup"><span data-stu-id="80c96-133">Flag</span></span>                                    | <span data-ttu-id="80c96-134">值</span><span class="sxs-lookup"><span data-stu-id="80c96-134">Value</span></span> | <span data-ttu-id="80c96-135">描述</span><span class="sxs-lookup"><span data-stu-id="80c96-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c96-136">訂用帳戶 \_ 上限 \_ ALLOWPLAY</span><span class="sxs-lookup"><span data-stu-id="80c96-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="80c96-137">0X1</span><span class="sxs-lookup"><span data-stu-id="80c96-137">0X1</span></span>   | <span data-ttu-id="80c96-138">Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)。</span><span class="sxs-lookup"><span data-stu-id="80c96-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="80c96-139">訂用帳戶 \_ 上限 \_ ALLOWCDBURN</span><span class="sxs-lookup"><span data-stu-id="80c96-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="80c96-140">0X2</span><span class="sxs-lookup"><span data-stu-id="80c96-140">0X2</span></span>   | <span data-ttu-id="80c96-141">Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn)。</span><span class="sxs-lookup"><span data-stu-id="80c96-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="80c96-142">訂用帳戶 \_ 上限 \_ ALLOWPDATRANSFER</span><span class="sxs-lookup"><span data-stu-id="80c96-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="80c96-143">0X4</span><span class="sxs-lookup"><span data-stu-id="80c96-143">0X4</span></span>   | <span data-ttu-id="80c96-144">Windows Media Player 應呼叫 [IWMPSubscriptionService：： allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)。</span><span class="sxs-lookup"><span data-stu-id="80c96-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="80c96-145">訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING</span><span class="sxs-lookup"><span data-stu-id="80c96-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="80c96-146">0X8</span><span class="sxs-lookup"><span data-stu-id="80c96-146">0X8</span></span>   | <span data-ttu-id="80c96-147">Windows Media Player 應呼叫 [IWMPSubscriptionService：： startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing)。</span><span class="sxs-lookup"><span data-stu-id="80c96-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="80c96-148">訂用帳戶 \_ 上限 \_ DEVICEAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="80c96-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="80c96-149">0X10</span><span class="sxs-lookup"><span data-stu-id="80c96-149">0X10</span></span>  | <span data-ttu-id="80c96-150">Windows Media Player 應呼叫 [IWMPSubscriptionService2：:D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)。</span><span class="sxs-lookup"><span data-stu-id="80c96-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="80c96-151">訂用帳戶 \_ 上限 \_ PREPAREFORSYNC</span><span class="sxs-lookup"><span data-stu-id="80c96-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="80c96-152">0X20</span><span class="sxs-lookup"><span data-stu-id="80c96-152">0X20</span></span>  | <span data-ttu-id="80c96-153">Windows Media Player 應呼叫 [IWMPSubscriptionService2：:P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync)。</span><span class="sxs-lookup"><span data-stu-id="80c96-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="80c96-154">訂用帳戶 \_ V1 \_ cap</span><span class="sxs-lookup"><span data-stu-id="80c96-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="80c96-155">0XF</span><span class="sxs-lookup"><span data-stu-id="80c96-155">0XF</span></span>   | <span data-ttu-id="80c96-156">預設值。</span><span class="sxs-lookup"><span data-stu-id="80c96-156">Default.</span></span> <span data-ttu-id="80c96-157">如果未註冊任何，則會使用此值。</span><span class="sxs-lookup"><span data-stu-id="80c96-157">This value is used if none is registered.</span></span> <span data-ttu-id="80c96-158">這相當於合併訂用帳戶 \_ cap \_ ALLOWPLAY、訂用帳戶 \_ 上限 ALLOWCDBURN、訂用帳戶上限 \_ \_ \_ ALLOWPDATRANSFER 和訂用帳戶 \_ 上限 \_ BACKGROUNDPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="80c96-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="80c96-159">**用於開發和測試的登錄專案**</span><span class="sxs-lookup"><span data-stu-id="80c96-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="80c96-160">當您開始開發線上商店時，Microsoft 會提供您兩個金鑰：測試金鑰和生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="80c96-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="80c96-161">在開發和測試階段中，只有當您的測試金鑰或生產金鑰位於使用者電腦的登錄中時，您的線上商店才會出現在 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="80c96-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="80c96-162">如需有關測試和生產金鑰的詳細資訊，請參閱 [類型2線上商店的測試和生產金鑰](test-and-production-keys-for-a-type-2-online-store.md)。</span><span class="sxs-lookup"><span data-stu-id="80c96-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="80c96-163">將您的測試或生產金鑰放在登錄中的下列位置。</span><span class="sxs-lookup"><span data-stu-id="80c96-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="80c96-164">請注意，TestParameter 登錄專案的值可以指定多個測試或生產金鑰。</span><span class="sxs-lookup"><span data-stu-id="80c96-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="80c96-165">例如，假設 Proseware 的測試金鑰為 "1234"，而 Contoso 的測試金鑰為 "2345"。</span><span class="sxs-lookup"><span data-stu-id="80c96-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="80c96-166">下列登錄專案指定 Proseware 和 Contoso 的測試存放區將會出現在 Windows Media Player 中。</span><span class="sxs-lookup"><span data-stu-id="80c96-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="80c96-167">**ActiveService 登錄專案**</span><span class="sxs-lookup"><span data-stu-id="80c96-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="80c96-168">當使用者啟動線上商店時，Windows Media Player 寫入登錄中的資訊，以識別作用中的線上商店。</span><span class="sxs-lookup"><span data-stu-id="80c96-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="80c96-169">Windows Media Player 將資訊放在使用者電腦上登錄的下列位置中。</span><span class="sxs-lookup"><span data-stu-id="80c96-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="80c96-170">在上述的登錄語法中， *serviceInfo* 是字串的預留位置，其中包含作用中線上商店的描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="80c96-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80c96-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="80c96-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80c96-172">**類型 2 線上商店的參考**</span><span class="sxs-lookup"><span data-stu-id="80c96-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





