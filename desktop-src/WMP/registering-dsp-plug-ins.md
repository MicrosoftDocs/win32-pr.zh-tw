---
title: 註冊 DSP 外掛程式
description: 註冊 DSP 外掛程式
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player 外掛程式、登錄專案
- 外掛程式，登錄專案
- 數位信號處理外掛程式，登錄專案
- DSP 外掛程式，登錄專案
- 登錄、DSP 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932937"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="ce848-108">註冊 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="ce848-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="ce848-109">若要在 Windows Media Player 中提供您的 DSP 外掛程式，您必須在使用者的電腦上建立下列登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="ce848-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="ce848-110">在上述的登錄語法中，斜體的符號是 (Guid 外掛程式專屬的 Guid) 的名稱和全域唯一識別碼的預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce848-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="ce848-111">下表描述這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce848-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="ce848-112">預留位置</span><span class="sxs-lookup"><span data-stu-id="ce848-112">Placeholder</span></span>               | <span data-ttu-id="ce848-113">描述</span><span class="sxs-lookup"><span data-stu-id="ce848-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce848-114">*PluginClsid*</span><span class="sxs-lookup"><span data-stu-id="ce848-114">*PluginClsid*</span></span>             | <span data-ttu-id="ce848-115">GUID，這是 DSP 外掛程式主要類別的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce848-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="ce848-116">這是實 **IMediaObject**、 **IPluginEnable** 和可能 **ISpecifyPropertyPages** 的類別。</span><span class="sxs-lookup"><span data-stu-id="ce848-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="ce848-117">在雙重模式的外掛程式中，此類別也會執行 **IMFTransform** 和 **IMFGetService**。此 GUID 必須是登錄格式，以大括弧完成。</span><span class="sxs-lookup"><span data-stu-id="ce848-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="ce848-118">格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="ce848-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="ce848-119">*PluginClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="ce848-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="ce848-120">DSP 外掛程式主要類別的易記名稱。範例： "ProsewareDSP Class"</span><span class="sxs-lookup"><span data-stu-id="ce848-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ce848-121">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="ce848-121">*PluginModuleName*</span></span>        | <span data-ttu-id="ce848-122">執行 DSP 外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="ce848-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="ce848-123">*執行緒*</span><span class="sxs-lookup"><span data-stu-id="ce848-123">*Threading*</span></span>               | <span data-ttu-id="ce848-124">字串，指定外掛程式的執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="ce848-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="ce848-125">如果外掛程式要在 Windows Vista 上以 Windows Media Player 11 執行，此登錄專案必須等於「兩者」。</span><span class="sxs-lookup"><span data-stu-id="ce848-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="ce848-126">如果外掛程式即將在 Windows XP 或較舊的作業系統上執行，此登錄專案可以等於 "公寓" 或 "Both"。</span><span class="sxs-lookup"><span data-stu-id="ce848-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="ce848-127">如果您的 DSP 外掛程式會執行自訂介面，且外掛程式即將在 Windows Vista 上的 Windows Media Player 11 中執行，您必須在使用者的電腦上建立下列登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="ce848-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="ce848-128">在上述的登錄語法中，以斜體表示的符號是名稱、數值和全域唯一識別碼的預留位置， (Guid 外掛程式專屬的 Guid) 。</span><span class="sxs-lookup"><span data-stu-id="ce848-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="ce848-129">下表描述這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce848-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="ce848-130">預留位置</span><span class="sxs-lookup"><span data-stu-id="ce848-130">Placeholder</span></span>           | <span data-ttu-id="ce848-131">描述</span><span class="sxs-lookup"><span data-stu-id="ce848-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce848-132">*ProxyStubClsid*</span><span class="sxs-lookup"><span data-stu-id="ce848-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="ce848-133">GUID，這是類別的類別識別碼，可針對 DSP 外掛程式的自訂介面，執行 proxy 和存根。此 GUID 必須是登錄格式，以大括弧完成。</span><span class="sxs-lookup"><span data-stu-id="ce848-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="ce848-134">格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="ce848-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="ce848-135">*ProxyStubModuleName*</span><span class="sxs-lookup"><span data-stu-id="ce848-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="ce848-136">針對 DSP 外掛程式執行 proxy 和存根介面之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="ce848-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="ce848-137">*CustomInterfaceId*</span><span class="sxs-lookup"><span data-stu-id="ce848-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="ce848-138">GUID，這是由 DSP 外掛程式所執行之自訂介面的介面識別碼。此 GUID 必須是登錄格式，以大括弧完成。</span><span class="sxs-lookup"><span data-stu-id="ce848-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="ce848-139">格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="ce848-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="ce848-140">*CustomInterfaceName*</span><span class="sxs-lookup"><span data-stu-id="ce848-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="ce848-141">DSP 外掛程式所執行之自訂介面的名稱。範例： "IProsewareDsp"</span><span class="sxs-lookup"><span data-stu-id="ce848-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="ce848-142">*NumberOfMethods*</span><span class="sxs-lookup"><span data-stu-id="ce848-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="ce848-143">自訂介面所定義之方法的數目，包括繼承的方法。範例： "5"</span><span class="sxs-lookup"><span data-stu-id="ce848-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="ce848-144">如果您的 DSP 外掛程式提供屬性頁，您必須在使用者的電腦上建立下列登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="ce848-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="ce848-145">在上述的登錄語法中，斜體的符號是 (Guid 外掛程式專屬的 Guid) 的名稱和全域唯一識別碼的預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce848-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="ce848-146">下表描述這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="ce848-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="ce848-147">預留位置</span><span class="sxs-lookup"><span data-stu-id="ce848-147">Placeholder</span></span>                 | <span data-ttu-id="ce848-148">描述</span><span class="sxs-lookup"><span data-stu-id="ce848-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce848-149">*PropPageClsid*</span><span class="sxs-lookup"><span data-stu-id="ce848-149">*PropPageClsid*</span></span>             | <span data-ttu-id="ce848-150">GUID，這是 DSP 外掛程式所提供之屬性頁類別的類別識別碼。此 GUID 必須是登錄格式，以大括弧完成。</span><span class="sxs-lookup"><span data-stu-id="ce848-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="ce848-151">格式： {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}。</span><span class="sxs-lookup"><span data-stu-id="ce848-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="ce848-152">*PropPageClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="ce848-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="ce848-153">屬性頁類別的易記名稱。範例： "ProsewareDSP Property Page Class"</span><span class="sxs-lookup"><span data-stu-id="ce848-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="ce848-154">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="ce848-154">*PluginModuleName*</span></span>          | <span data-ttu-id="ce848-155">執行 DSP 外掛程式之 DLL 的完整路徑。範例： "C： \\ Program Files \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="ce848-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="ce848-156">**呼叫 IWMPPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="ce848-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="ce848-157">除了上述清單和資料表中所述的登錄子機碼和專案以外，您還必須呼叫 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin)來建立一些登錄機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="ce848-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="ce848-158">這個方法會執行必要的註冊，讓 Windows Media Player 辨識您的外掛程式，並將其顯示為使用者的選項。</span><span class="sxs-lookup"><span data-stu-id="ce848-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="ce848-159">在外掛程式的 **DllRegisterServer** 函式中呼叫 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** ，然後在外掛程式的 **WMPUnRegisterPlayerPlugin** 函數中呼叫 [IWMPMediaPluginRegistrar：： DllUnregisterServer](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) 。</span><span class="sxs-lookup"><span data-stu-id="ce848-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="ce848-160">若要取得 **IWMPMediaPluginRegistrar** 介面的指標，請呼叫 **COCREATEINSTANCE**，將 CLSID \_ WMPMediaPluginRegistrar 傳遞為類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce848-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="ce848-161">常數 CLSID \_ WMPMediaPluginRegistrar 是在 wmpservices 中定義。</span><span class="sxs-lookup"><span data-stu-id="ce848-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="ce848-162">**在 DSP 外掛程式嚮導中註冊**</span><span class="sxs-lookup"><span data-stu-id="ce848-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="ce848-163">Windows SDK 中包含的 DSP 外掛程式 wizard 會根據 Active Template Library (ATL) 產生範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce848-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="ce848-164">範例外掛程式的 **DllRegisterServer** 函式會呼叫 ATL 的 **RegisterServer** 函式，此函式會根據 Visual Studio 專案中的兩個登入指令檔檔，建立登錄子機碼和專案。</span><span class="sxs-lookup"><span data-stu-id="ce848-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="ce848-165">檔案 *名稱* 為 .rgs 包含用來註冊外掛程式主要類別的腳本，而檔案 *專案名稱* PropPage 則包含用來註冊外掛程式屬性頁類別的腳本。</span><span class="sxs-lookup"><span data-stu-id="ce848-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="ce848-166">範例外掛程式的 **DllRegisterServer** 函數也會呼叫 **IWMPPluginRegistrar：： WMPRegisterPlayerPlugin**。</span><span class="sxs-lookup"><span data-stu-id="ce848-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="ce848-167">DSP 外掛程式 wizard 也會產生自我註冊 .dll 檔案之 proxy 存根元件的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce848-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="ce848-168">該檔案的註冊碼位於 dlldata.c .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="ce848-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="ce848-169">宏 **Dlldata.c \_ 常式** 會展開以包含 **DllRegisterServer** 的執行。</span><span class="sxs-lookup"><span data-stu-id="ce848-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce848-170">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce848-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce848-171">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="ce848-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="ce848-172">**IWMPMediaPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="ce848-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





