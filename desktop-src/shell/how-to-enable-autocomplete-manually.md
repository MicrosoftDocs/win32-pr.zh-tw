---
description: 若要取得更詳細的自動完成行為控制，或加入自動完成字串的自訂來源，您必須自行管理自動完成物件。
ms.assetid: E1A7B1B0-2879-452E-9EBB-73F02B932200
title: 如何手動啟用自動完成
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee4b327c6ccdd62fd921c56cfb046edb8527bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973157"
---
# <a name="how-to-enable-autocomplete-manually"></a><span data-ttu-id="3cf3a-103">如何手動啟用自動完成</span><span class="sxs-lookup"><span data-stu-id="3cf3a-103">How to Enable Autocomplete Manually</span></span>

<span data-ttu-id="3cf3a-104">若要取得更詳細的自動完成行為控制，或加入自動完成字串的自訂來源，您必須自行管理自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-104">To gain more detailed control over the autocomplete behavior, or to add a custom source of autocomplete strings, you must manage the autocomplete object yourself.</span></span> <span data-ttu-id="3cf3a-105">您可以透過下列方式手動啟用自動完成。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-105">You can enable autocomplete manually in the following ways.</span></span>

## <a name="instructions"></a><span data-ttu-id="3cf3a-106">指示</span><span class="sxs-lookup"><span data-stu-id="3cf3a-106">Instructions</span></span>

### <a name="creating-a-simple-autocomplete-object"></a><span data-ttu-id="3cf3a-107">建立簡單的自動完成物件</span><span class="sxs-lookup"><span data-stu-id="3cf3a-107">Creating a Simple Autocomplete Object</span></span>

<span data-ttu-id="3cf3a-108">下列步驟說明如何建立和初始化簡單的自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-108">The following steps show how to create and initialize a simple autocomplete object.</span></span> <span data-ttu-id="3cf3a-109">簡單的自動完成物件會從單一來源完成字串。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-109">A simple autocomplete object completes strings from a single source.</span></span> <span data-ttu-id="3cf3a-110">在此範例中，已刻意省略錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-110">Error checking has been intentionally omitted in this example.</span></span>

1.  <span data-ttu-id="3cf3a-111">建立自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-111">Create the autocomplete object.</span></span>

    ```C++
    IAutoComplete *pac;

    HRESULT hr = CoCreateInstance(CLSID_AutoComplete, 
                                    NULL, 
                                  CLSCTX_INPROC_SERVER,
                                  IID_PPV_ARGS(&pac));
    ```

    

2.  <span data-ttu-id="3cf3a-112">建立自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-112">Create the autocomplete source.</span></span> <span data-ttu-id="3cf3a-113">您可以使用 [預先定義的自動完成來源](ac-ovw.md) ，也可以撰寫自己的自訂來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-113">You can use a [predefined autocomplete source](ac-ovw.md) or you can write your own custom source.</span></span>

    <span data-ttu-id="3cf3a-114">下列程式碼會使用其中一個預先定義的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-114">The following code uses one of the predefined autocomplete sources.</span></span>

    ```C++
    IUnknown *punkSource;

    hr = CoCreateInstance(CLSID_ACListISF, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&punkSource));
    ```

    

    <span data-ttu-id="3cf3a-115">下列程式碼會使用自訂的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-115">The following code uses a custom autocomplete source.</span></span> <span data-ttu-id="3cf3a-116">您可以藉由執行公開 [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) 介面的物件來撰寫自己的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-116">You can write your own autocomplete source by implementing an object that exposes the [**IEnumString**](/windows/win32/api/objidlbase/nn-objidlbase-ienumstring) interface.</span></span> <span data-ttu-id="3cf3a-117">物件也可以選擇性地執行 [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) 和 [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) 介面。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-117">The object can also optionally implement the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) and [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interfaces.</span></span>

    ```C++
    CCustomAutoCompleteSource *pcacs = new CCustomAutoCompleteSource();

    hr = pcacs->QueryInterface(IID_PPV_ARGS(&punkSource));
    if(SUCCEEDED(hr))
    {
        // ...
    }

    pcacs->Release();
    ```

    

3.  <span data-ttu-id="3cf3a-118">設定自動完成來源 (選用) 的選項。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-118">Set the options on the autocomplete source (optional).</span></span>

    <span data-ttu-id="3cf3a-119">如果來源公開 [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) 介面，您可以藉由設定自動完成來源的行為，藉此自訂。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-119">You can customize the behavior of the autocomplete source by setting its options if the source exposes the [**IACList2**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2) interface.</span></span> <span data-ttu-id="3cf3a-120">使用預先定義的自動完成來源時，只有 CLSID \_ ACListISF 會匯出 **IACList2**。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-120">When using the predefined autocomplete sources, only CLSID\_ACListISF exports **IACList2**.</span></span> <span data-ttu-id="3cf3a-121">如需選項及其值的完整清單，請參閱 [**IACList2：： >setoptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-121">For a complete list of options and their values, see [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IACList2 *pal2;

    hr = punkSource->QueryInterface(IID_PPV_ARGS(&pal2));
    if (SUCCEEDED(hr))
    {
        hr = pal2->SetOptions(ACLO_FILESYSONLY);
        pal2->Release();
    }
    ```

    

4.  <span data-ttu-id="3cf3a-122">初始化自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-122">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="3cf3a-123">在此範例中， **hwndEdit** 是 [編輯] 控制項視窗的控制碼，可啟用自動完成。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-123">In this example, **hwndEdit** is the handle of the edit control window for which autocomplete is to be enabled.</span></span> <span data-ttu-id="3cf3a-124">如需最後兩個未使用參數的描述，請參閱 [**IAutoComplete：： Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) 。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-124">See [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init) for a description of the final two unused parameters.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, punkSource, NULL, NULL);
    ```

    

5.  <span data-ttu-id="3cf3a-125">將 [自動完成] 物件的選項設定 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-125">Set the options of the autocomplete object (optional).</span></span>

    <span data-ttu-id="3cf3a-126">您可以藉由設定 [自動完成] 物件的選項來自訂其行為。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-126">You can customize the behavior of the autocomplete object by setting its options.</span></span> <span data-ttu-id="3cf3a-127">如需選項及其值的完整清單，請參閱 [**IACList2：： >setoptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions)的檔。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-127">For a complete list of options and their values, see the documentation for [**IACList2::SetOptions**](/windows/win32/api/shlobj_core/nf-shlobj_core-iaclist2-setoptions).</span></span>

    ```C++
    IAutoComplete2 *pac2;

    hr = pac->QueryInterface(IID_PPV_ARGS(&pac2));

    if (SUCCEEDED(hr))
    {
        hr = pac2->SetOptions(ACO_AUTOSUGGEST);
        pac2->Release();
    }
    ```

    

6.  <span data-ttu-id="3cf3a-128">釋放物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-128">Release the objects.</span></span>

    > [!Note]  
    > <span data-ttu-id="3cf3a-129">即使在您發行之後，自動完成物件仍會附加至編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-129">The autocomplete object remains attached to the edit control even after you release it.</span></span> <span data-ttu-id="3cf3a-130">如果您未來需要存取這些物件-如果您想要在稍後變更自動完成選項（例如），則不需要在此時釋放。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-130">If you foresee a need to access these objects later—if you want to change the autocomplete options at a later time, for example—it is not required that you release them at this point.</span></span>

     

    ```C++
    punkSource->Release();
    pac->Release();
    ```

    

### <a name="creating-a-compound-autocomplete-object"></a><span data-ttu-id="3cf3a-131">建立複合自動完成物件</span><span class="sxs-lookup"><span data-stu-id="3cf3a-131">Creating a Compound Autocomplete Object</span></span>

<span data-ttu-id="3cf3a-132">複合自動完成物件會與多個來源的字串相符。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-132">A compound autocomplete object matches against strings from multiple sources.</span></span> <span data-ttu-id="3cf3a-133">例如，Windows Internet Explorer 網址列會使用複合自動完成物件，因為使用者可能會開始輸入檔案或 URL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-133">For example, the Windows Internet Explorer Address bar uses a compound autocomplete object because the user might begin typing the name of a file or a URL.</span></span> <span data-ttu-id="3cf3a-134">建立複合自動完成物件所涉及的大部分步驟，與「建立簡單的自動完成物件」中的步驟相同。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-134">Most of the steps involved in creating a compound autocomplete object are identical to the steps in "Creating a Simple Autocomplete Object."</span></span> <span data-ttu-id="3cf3a-135">這些步驟會以這樣的方式表示。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-135">Those steps are indicated as such.</span></span>

1.  <span data-ttu-id="3cf3a-136">建立自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-136">Create the autocomplete object.</span></span> <span data-ttu-id="3cf3a-137">這與上述步驟1相同。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-137">This is the same as step 1 above.</span></span>

2.  <span data-ttu-id="3cf3a-138">建立自動完成複合來源物件管理員。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-138">Create the autocomplete compound source object manager.</span></span>

    <span data-ttu-id="3cf3a-139">自動完成複合來源物件可將多個自動完成來源合併成單一的自動完成來源。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-139">The autocomplete compound source object allows multiple autocomplete sources to be combined into a single autocomplete source.</span></span>

    ```C++
    IObjMgr *pom;

    hr = CoCreateInstance(CLSID_ACLMulti, 
                          NULL, 
                          CLSCTX_INPROC_SERVER,
                          IID_PPV_ARGS(&pom));
    ```

    

3.  <span data-ttu-id="3cf3a-140">建立並設定每個自動完成來源的選項。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-140">Create and set options for each of the autocomplete sources.</span></span> <span data-ttu-id="3cf3a-141">針對每個來源重複上述步驟2和3。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-141">Repeat steps 2 and 3 above for each source.</span></span>

4.  <span data-ttu-id="3cf3a-142">將每個自動完成來源附加至來源物件管理員。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-142">Attach each autocomplete source to the source object manager.</span></span>

    ```C++
    hr = pom->Append(punkSource1);
    hr = pom->Append(punkSource2);
    ```

    

5.  <span data-ttu-id="3cf3a-143">初始化自動完成物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-143">Initialize the autocomplete object.</span></span>

    <span data-ttu-id="3cf3a-144">這與上述步驟4相同，不同之處在于，您可以傳遞複合來源物件管理員，而不是將簡單的自動完成來源傳遞至 [**IAutoComplete：： Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init)。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-144">This is the same as step 4 above, except that instead of passing the simple autocomplete source to [**IAutoComplete::Init**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete-init), you pass the compound source object manager.</span></span>

    ```C++
    hr = pac->Init(hwndEdit, pom, NULL, NULL);
    ```

    

6.  <span data-ttu-id="3cf3a-145">設定自動完成物件的選項。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-145">Set the options of the autocomplete object.</span></span> <span data-ttu-id="3cf3a-146">這與上述步驟5相同。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-146">This is the same as step 5 above.</span></span>

7.  <span data-ttu-id="3cf3a-147">釋放物件。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-147">Release the objects.</span></span>

    <span data-ttu-id="3cf3a-148">在簡單的情況下，您可以在使用完畢後立即釋出物件，但是您也可以在稍後保留它們來變更選項。</span><span class="sxs-lookup"><span data-stu-id="3cf3a-148">As in the simple case, you can release the objects as soon as you are finished using them, but you can also retain them to change options later.</span></span>

    ```C++
    pac->Release();
    pom->Release();

    // Release each individual source.
    punkSource1->Release(); 
    punkSource2->Release();
    ```

    

 

 
