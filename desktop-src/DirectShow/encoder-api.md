---
description: 編碼器 API
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: 編碼器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385781"
---
# <a name="encoder-api"></a><span data-ttu-id="5b90b-103">編碼器 API</span><span class="sxs-lookup"><span data-stu-id="5b90b-103">Encoder API</span></span>

<span data-ttu-id="5b90b-104">編碼器 API 提供統一的介面來設定軟體和硬體編碼器。</span><span class="sxs-lookup"><span data-stu-id="5b90b-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="5b90b-105">應用程式可以使用編碼器 API 來設定編碼器和儲存設定。</span><span class="sxs-lookup"><span data-stu-id="5b90b-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="5b90b-106">編碼器廠商可使用編碼器 API 來公開編碼器的功能。</span><span class="sxs-lookup"><span data-stu-id="5b90b-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="5b90b-107">雖然編碼器 API 主要是針對編碼器所設計，但它通常也足以支援它。</span><span class="sxs-lookup"><span data-stu-id="5b90b-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="5b90b-108">編碼器 API 會透過 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面（由編碼器篩選器公開）公開給應用程式。</span><span class="sxs-lookup"><span data-stu-id="5b90b-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="5b90b-109">編碼器篩選器可能是原生的 DirectShow 篩選器、硬體編碼器或 DirectX 媒體物件 (SQL-DMO) 。</span><span class="sxs-lookup"><span data-stu-id="5b90b-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="5b90b-110">軟體篩選：實作為原生 DirectShow 篩選器的編碼器應該直接公開 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 。</span><span class="sxs-lookup"><span data-stu-id="5b90b-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="5b90b-111">硬體編碼器：編碼裝置會透過一或多個 AVStream minidrivers 公開，KSProxy 會在使用者模式中表示。</span><span class="sxs-lookup"><span data-stu-id="5b90b-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="5b90b-112">KSProxy 會將 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 方法呼叫轉譯為 KS 屬性集。</span><span class="sxs-lookup"><span data-stu-id="5b90b-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="5b90b-113">如需詳細資訊，請參閱 DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="5b90b-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="5b90b-114">DMOs： SQL-DMO 應該公開 [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) 介面。</span><span class="sxs-lookup"><span data-stu-id="5b90b-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="5b90b-115">DirectShow 應用程式可以查詢 SQL-DMO 包裝函式篩選器，此篩選器會藉由匯總來公開介面。</span><span class="sxs-lookup"><span data-stu-id="5b90b-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="5b90b-116">以 DirectShow 為基礎的應用程式可以直接查詢 SQL-DMO。</span><span class="sxs-lookup"><span data-stu-id="5b90b-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="5b90b-117">編碼器功能</span><span class="sxs-lookup"><span data-stu-id="5b90b-117">Encoder Capabilties</span></span>

<span data-ttu-id="5b90b-118">編碼器可以將高階功能的清單儲存在系統登錄中，以註冊它們。</span><span class="sxs-lookup"><span data-stu-id="5b90b-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="5b90b-119">每項功能都是由 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="5b90b-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="5b90b-120">若要列舉特定編碼器的功能，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5b90b-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="5b90b-121">建立代表編碼器篩選器的標記。</span><span class="sxs-lookup"><span data-stu-id="5b90b-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="5b90b-122"> (參閱 [使用系統裝置列舉](using-the-system-device-enumerator.md)值。 ) </span><span class="sxs-lookup"><span data-stu-id="5b90b-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="5b90b-123">查詢 [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) 介面的篩選準則標記。</span><span class="sxs-lookup"><span data-stu-id="5b90b-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="5b90b-124">呼叫 [**IGetCapabilitiesKey：： GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey)。</span><span class="sxs-lookup"><span data-stu-id="5b90b-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="5b90b-125">方法會將控制碼傳回至包含篩選功能清單的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="5b90b-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="5b90b-126">呼叫 **RegEnumValue** 函式來列舉傳回索引鍵的值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="5b90b-127">如果您要開發編碼器，請在註冊篩選器時建立這些功能的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="5b90b-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="5b90b-128">針對軟體篩選器，請建立名為「 **功能** 」的金鑰，該金鑰與 **FilterData** 和 **FriendlyName** 金鑰相鄰。</span><span class="sxs-lookup"><span data-stu-id="5b90b-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="5b90b-129">一般而言，您會在呼叫 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 之後加入這項資訊，以註冊標準篩選資料。</span><span class="sxs-lookup"><span data-stu-id="5b90b-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="5b90b-130">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="5b90b-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="5b90b-131">或者，您可以建立 **CapabilitiesLocation** 索引鍵，其中包含的字串可提供登錄中的 **功能** 金鑰位置。</span><span class="sxs-lookup"><span data-stu-id="5b90b-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="5b90b-132">字串的開頭應該是 "HKLM \\ "、"HKCR \\ " 或 "HKCU \\ "，以表示登錄子樹。</span><span class="sxs-lookup"><span data-stu-id="5b90b-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="5b90b-133">針對隨插即用裝置，驅動程式的安裝檔應該建立與篩選的 **FriendlyName** 金鑰連續的 **功能** 金鑰，也可以使用 **CapabilitiesLocation** 金鑰，如軟體篩選器所述。</span><span class="sxs-lookup"><span data-stu-id="5b90b-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="5b90b-134">建立 **功能** 金鑰之後，請為每個功能 GUID 建立一個值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="5b90b-135">值的名稱應該是 GUID 的字串格式，格式為 `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` 。</span><span class="sxs-lookup"><span data-stu-id="5b90b-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="5b90b-136">每個實值型別都應該是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="5b90b-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="5b90b-137">單一數值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-137">Single numerical value.</span></span> <span data-ttu-id="5b90b-138">使用 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="5b90b-139">GUID。</span><span class="sxs-lookup"><span data-stu-id="5b90b-139">GUID.</span></span> <span data-ttu-id="5b90b-140">使用 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="5b90b-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="5b90b-141">數值配對。</span><span class="sxs-lookup"><span data-stu-id="5b90b-141">Numeric pairs.</span></span> <span data-ttu-id="5b90b-142">使用格式為 "a，b" 的字串來代表值的配對，例如寬度和高度，或分數的分子和分母。</span><span class="sxs-lookup"><span data-stu-id="5b90b-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="5b90b-143">值的陣列。</span><span class="sxs-lookup"><span data-stu-id="5b90b-143">Arrays of values.</span></span> <span data-ttu-id="5b90b-144">使用多字串 (**REG \_ SZ \_ 多重**) 來代表一個以上的值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="5b90b-145">下列範例顯示軟體篩選器的登錄配置：</span><span class="sxs-lookup"><span data-stu-id="5b90b-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="5b90b-146">編碼器設定檔</span><span class="sxs-lookup"><span data-stu-id="5b90b-146">Encoder Profiles</span></span>

<span data-ttu-id="5b90b-147">*編碼器設定檔* 是固定的設定值清單，可在執行時間套用至編碼器。</span><span class="sxs-lookup"><span data-stu-id="5b90b-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="5b90b-148">設定檔與編碼器無關;應用程式可以選取編碼器，然後選取設定檔並將設定檔設定套用至編碼器。</span><span class="sxs-lookup"><span data-stu-id="5b90b-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="5b90b-149">設定檔是由 GUID 識別，且應儲存在登錄中的下列位置：</span><span class="sxs-lookup"><span data-stu-id="5b90b-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="5b90b-150">*設定檔 GUID*</span><span class="sxs-lookup"><span data-stu-id="5b90b-150">where *Profile GUID*</span></span>

<span data-ttu-id="5b90b-151">這是識別設定檔的 GUID 字串形式。</span><span class="sxs-lookup"><span data-stu-id="5b90b-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="5b90b-152">建立每個設定的值。</span><span class="sxs-lookup"><span data-stu-id="5b90b-152">Create values for each setting.</span></span> <span data-ttu-id="5b90b-153">此外，請建立名為 "FriendlyName" 的字串值，其資料會識別設定檔 (例如 "LowBandwidthVideo" ) 。</span><span class="sxs-lookup"><span data-stu-id="5b90b-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b90b-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b90b-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b90b-155">編碼器和解碼器開發</span><span class="sxs-lookup"><span data-stu-id="5b90b-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



