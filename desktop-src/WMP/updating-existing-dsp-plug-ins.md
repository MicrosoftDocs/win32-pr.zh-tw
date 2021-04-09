---
title: 更新現有的 DSP 外掛程式
description: 更新現有的 DSP 外掛程式
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- 'Windows Media Player 外掛程式、數位信號處理 (DSP) '
- '外掛程式，數位信號處理 (DSP) '
- 數位信號處理外掛程式，更新
- DSP 外掛程式，更新
- Windows Media Player、DSP 外掛程式的版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681402"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="7b2d1-108">更新現有的 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="7b2d1-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="7b2d1-109">在 Windows Media Player 11 SDK 發行之前建立的 DSP 外掛程式，可能無法如預期般運作，因為在 Windows Vista 上執行的 Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="7b2d1-110">為了確保在 Windows Vista 上執行 Windows Media Player 11 的客戶可以使用您的外掛程式，您必須對您的 DSP 外掛程式程式碼進行一些變更、重新編譯您的專案，然後將更新的外掛程式散發給您的客戶。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="7b2d1-111">使用最新版 Windows Media Player 外掛程式 wizard 建立的專案將包含必要的更新。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="7b2d1-112">請參閱 [Windows Media Player 11 的 DSP 外掛程式 Wizard 更新](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="7b2d1-113"> (建議您執行 wizard 來建立新的範例專案，然後使用 Visual Studio 所隨附的 Windiff.exe 工具，來檢查範例程式碼與您的實際執行程式碼之間的差異。 ) </span><span class="sxs-lookup"><span data-stu-id="7b2d1-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="7b2d1-114">您必須對任何現有的 DSP 外掛程式進行三項主要變更：</span><span class="sxs-lookup"><span data-stu-id="7b2d1-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="7b2d1-115">變更外掛程式註冊的方式。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="7b2d1-116">您現有的外掛程式可能會將執行緒模型註冊為「單元」。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="7b2d1-117">在 Windows Vista 上執行的 Windows Media Player 11 需要 DSP 外掛程式將執行緒模型註冊為「兩者」。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="7b2d1-118">您可以藉由變更 *專案名稱*.rgs 檔中的執行緒模型值來修正此問題，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7b2d1-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="7b2d1-119">將執行緒模型指定為「兩者」會移除 COM 針對自訂介面的呼叫所提供的任何序列化。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="7b2d1-120">如果您從多個執行緒呼叫自訂介面，就必須自行提供此序列化。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="7b2d1-121">Windows Media Player 11 可確保對 SQL-DMO 介面的呼叫已正確序列化。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="7b2d1-122">使用新的外掛程式類型，將呼叫新增至 [IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) 和 [IWMPMediaPluginRegistrar：： WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) ，並將 PLUGINTYPE 和 OUTOFPROC 中的 WMP DllRegisterServer DSP DllUnregisterServer 用於 \_ \_ \_ *projectnamedll*.cpp 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="7b2d1-123">如需詳細資訊，請參閱這些方法的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="7b2d1-124">建立並散發 proxy/stub DLL，以啟用任何自訂介面的 COM 封送處理，該介面是由外掛程式類別所執行或建立。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="7b2d1-125">自訂介面是您定義和執行的任何專屬介面，可供外掛程式物件使用。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="7b2d1-126">這包括您的屬性頁所使用的自訂介面（如果您有提供的話），但也可能包含連接至 UI 外掛程式的介面（例如）。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="7b2d1-127">外掛程式嚮導所建立的自訂介面範例是 *Iprojectname*。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="7b2d1-128">非自訂介面的介面範例包括 **IMediaObject** 和 **IWMPPluginEnable**。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="7b2d1-129">如果您的 DSP 外掛程式處理音訊，您也必須新增下列新音訊格式的支援：</span><span class="sxs-lookup"><span data-stu-id="7b2d1-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="7b2d1-130">WAVE \_ 格式 \_ IEEE \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="7b2d1-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="7b2d1-131">WAVE \_ 格式可延伸 \_ 的 subformat KSDATAFORMAT \_ 子類型 \_ IEEE \_ FLOAT。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="7b2d1-132">如果您的 DSP 外掛程式處理影片，您必須新增 NV12 影片格式的支援。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="7b2d1-133">請參閱嚮導所建立的範例音訊或影片 DSP 外掛程式，以取得如何處理這些格式類型的範例。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="7b2d1-134">關於 Proxy/Stub 專案</span><span class="sxs-lookup"><span data-stu-id="7b2d1-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="7b2d1-135">若要為您的 DSP 外掛程式建立 proxy/存根 DLL 專案，最簡單的方式就是執行 DSP 外掛程式 wizard。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="7b2d1-136">這會建立範例 proxy/stub 專案，讓您可以修改以使用現有的程式碼。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="7b2d1-137">您將需要進行下列變更：</span><span class="sxs-lookup"><span data-stu-id="7b2d1-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="7b2d1-138">從程式碼中移除自訂介面的任何現有定義。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="7b2d1-139">例如，來自 Windows Media Player 10 SDK 的 DSP 外掛程式 wizard 會使用 **interface** 關鍵字，在 *專案名稱*.H 檔案中建立 *Iprojectname* 介面定義。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="7b2d1-140">在 proxy/stub 專案的 IDL 檔案中定義您的自訂介面。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="7b2d1-141">在您的主要專案之前，建立 proxy/stub 專案。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="7b2d1-142">如果兩個專案都是相同方案的一部分，您可以設定 Visual Studio 自動完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="7b2d1-143">MIDL 編譯器會建立新的標頭檔，其名稱格式為專案名稱 \_ h.h。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="7b2d1-144">您必須將此標頭包含在主要專案 (的專案 *名稱*.h) 中。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="7b2d1-145">它包含自訂介面的定義。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="7b2d1-146">發佈更新的外掛程式</span><span class="sxs-lookup"><span data-stu-id="7b2d1-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="7b2d1-147">您可以將更新的外掛程式安裝在使用者電腦上，就像過去一樣。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="7b2d1-148">不過，您現在也必須散發並註冊 proxy/stub DLL。</span><span class="sxs-lookup"><span data-stu-id="7b2d1-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b2d1-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b2d1-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2d1-150">**DSP 外掛程式開發人員總覽**</span><span class="sxs-lookup"><span data-stu-id="7b2d1-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




