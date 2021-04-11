---
description: 執行 DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: 執行 DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109525"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="c8fd2-103">執行 DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="c8fd2-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="c8fd2-104">最後一個步驟是執行 **DllRegisterServer** 函數。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="c8fd2-105">包含元件的 DLL 必須匯出此函數。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="c8fd2-106">設定應用程式或使用者執行 Regsvr32.exe 工具時，會呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="c8fd2-107">下列範例顯示最基本的 **DlLRegisterServer** 執行：</span><span class="sxs-lookup"><span data-stu-id="c8fd2-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="c8fd2-108">[**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式會為每個元件建立登錄專案。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="c8fd2-109">陣列。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-109">array.</span></span> <span data-ttu-id="c8fd2-110">不過，此函數有一些限制。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-110">However, this function has some limitations.</span></span> <span data-ttu-id="c8fd2-111">首先，它會將每個篩選指派給「DirectShow 篩選」類別 (CLSID \_ LegacyAmFilterCategory) ，但並非每個篩選都屬於此類別。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="c8fd2-112">例如，「捕獲篩選準則」和「壓縮」篩選器都有自己的類別。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="c8fd2-113">其次，如果您的篩選器支援硬體裝置，您可能需要註冊兩項額外的資訊， **AMovieDLLRegisterServer2** 不會處理這些資訊： *媒體* 和 *pin 類別*。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="c8fd2-114">媒體定義了硬體裝置（例如匯流排）的通訊方法。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="c8fd2-115">Pin 類別會定義 pin 的功能。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="c8fd2-116">如需有關媒體的資訊，請參閱 \_ Microsoft Windows 驅動程式開發工具組中的 "KSPIN MEDIUM" (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="c8fd2-117">如需 pin 類別的清單，請參閱 [釘選屬性集](pin-property-set.md)。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="c8fd2-118">如果您想要指定篩選類別、媒體或釘選類別，請從 **DllRegisterServer** 內呼叫 [**IFilterMapper2：： RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter)方法。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="c8fd2-119">這個方法會採用 [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) 結構的指標，此結構會指定篩選的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="c8fd2-120">為了讓事情稍微複雜一點， **REGFILTER2** 結構支援兩種不同的格式來註冊 pin。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="c8fd2-121">**DwVersion** 成員會指定格式：</span><span class="sxs-lookup"><span data-stu-id="c8fd2-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="c8fd2-122">如果 **dwVersion** 是1，則 pin 格式為 **AMOVIESETUP \_ pin** (先前) 所述。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="c8fd2-123">如果 **dwVersion** 為2，則會 [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2)pin 格式。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="c8fd2-124">**REGFILTERPINS2** 結構包含 pin 媒體和 pin 類別目錄的專案。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="c8fd2-125">此外，針對 **AMOVIESETUP \_ 釘** 選為布林值的某些專案，它會使用位旗標。</span><span class="sxs-lookup"><span data-stu-id="c8fd2-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="c8fd2-126">下列範例顯示如何從 **DllRegisterServer** 內部呼叫 **IFilterMapper2：： RegisterFilter** ：</span><span class="sxs-lookup"><span data-stu-id="c8fd2-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



