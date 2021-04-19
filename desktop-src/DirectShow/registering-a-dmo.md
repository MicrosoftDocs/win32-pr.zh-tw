---
description: 註冊 SQL-DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: 註冊 SQL-DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973538"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="e08f4-103">註冊 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="e08f4-103">Registering a DMO</span></span>

<span data-ttu-id="e08f4-104">為了讓用戶端使用您的，必須在使用者的系統上註冊 CLSID。</span><span class="sxs-lookup"><span data-stu-id="e08f4-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="e08f4-105">這是透過 DLL 的 **DllRegisterServer** 函式來完成。</span><span class="sxs-lookup"><span data-stu-id="e08f4-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="e08f4-106">如果您使用 Active Template Library (ATL) ，則 ATL wizard 會自動產生此函數。</span><span class="sxs-lookup"><span data-stu-id="e08f4-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="e08f4-107">您也可以在一或多個標準的 SQL-DMO 類別下註冊您的。</span><span class="sxs-lookup"><span data-stu-id="e08f4-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="e08f4-108">這可讓用戶端使用 [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) 函數探索您的。</span><span class="sxs-lookup"><span data-stu-id="e08f4-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="e08f4-109">類別目錄是由 GUID 所定義，而且會列在第一節的 [guid](dmo-guids.md)中。</span><span class="sxs-lookup"><span data-stu-id="e08f4-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="e08f4-110">在類別目錄下註冊的是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e08f4-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="e08f4-111">若要這樣做，請呼叫 [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) 函式，並指定該名稱、CLSID 和分類的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="e08f4-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="e08f4-112">（選擇性）您也可以註冊 DMOs 支援的一組媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e08f4-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="e08f4-113">如需詳細資訊，請參閱 [Sql-dmo 媒體類型](dmo-media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="e08f4-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="e08f4-114">下列範例顯示如何註冊支援 PCM 音訊輸入和輸出的音訊效果。</span><span class="sxs-lookup"><span data-stu-id="e08f4-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="e08f4-115">在此情況下，輸入類型和輸出類型都相同。</span><span class="sxs-lookup"><span data-stu-id="e08f4-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="e08f4-116">此範例假設使用 ATL 建立專案;函式的最後一行會呼叫標準 ATL 方法來註冊 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="e08f4-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="e08f4-117">如果您不是使用 ATL，則您的函式看起來會不同。</span><span class="sxs-lookup"><span data-stu-id="e08f4-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="e08f4-118">**取消註冊**</span><span class="sxs-lookup"><span data-stu-id="e08f4-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="e08f4-119">**DllUnregisterServer** 函數必須移除 **DllRegisterServer** 函數所建立的任何登錄專案。</span><span class="sxs-lookup"><span data-stu-id="e08f4-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="e08f4-120">如果您在註冊時呼叫 **DMORegister** ，則必須在取消註冊時使用相同的類別 [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) 。</span><span class="sxs-lookup"><span data-stu-id="e08f4-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="e08f4-121">下列範例會移除在上述範例中建立的登錄專案：</span><span class="sxs-lookup"><span data-stu-id="e08f4-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="e08f4-122">**DirectShow 業績值**</span><span class="sxs-lookup"><span data-stu-id="e08f4-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="e08f4-123">基於建立篩選圖形的目的，DirectShow 會將預設的業績值指派給 DMOs。</span><span class="sxs-lookup"><span data-stu-id="e08f4-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="e08f4-124">您可以藉由將登錄專案新增至 HKEY \_ 類別根目錄 CLSID 中的 sql-dmo 登錄機碼來覆寫此值 \_ \\ 。</span><span class="sxs-lookup"><span data-stu-id="e08f4-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="e08f4-125">包含名為的 **DWORD** 值 `Merit` ，其值會指定其值。</span><span class="sxs-lookup"><span data-stu-id="e08f4-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e08f4-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="e08f4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e08f4-127">撰寫 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="e08f4-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



