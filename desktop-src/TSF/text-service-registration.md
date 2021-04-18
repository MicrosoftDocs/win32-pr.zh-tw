---
title: 文字服務註冊
description: 除了標準的 COM 同進程伺服器登錄專案之外，文字服務還必須向文字服務架構 (TSF) 登錄，才能讓它與應用程式搭配使用。
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- 文字服務架構 (TSF) ，註冊
- TSF (文字服務架構) ，註冊
- 文字服務，註冊
- 文字服務架構 (TSF) ，語言設定檔
- TSF (文字服務架構) ，語言設定檔
- 文字服務，語言設定檔
- 文字服務架構 (TSF) 、類別目錄
- TSF (文字服務架構) 、類別
- 文字服務、類別
- 註冊文字服務
- 註冊語言設定檔
- 註冊類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463400"
---
# <a name="text-service-registration"></a><span data-ttu-id="349f1-115">文字服務註冊</span><span class="sxs-lookup"><span data-stu-id="349f1-115">Text Service Registration</span></span>

<span data-ttu-id="349f1-116">除了標準的 COM 同進程伺服器登錄專案之外，文字服務還必須向文字服務架構 (TSF) 登錄，才能讓它與應用程式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="349f1-116">In addition to the standard COM in-proc server registry entries, a text service must register itself with the Text Services Framework (TSF) so that it can be available for use with an application.</span></span> <span data-ttu-id="349f1-117">TSF 會提供 [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) 和 [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) 介面，以簡化註冊程式。</span><span class="sxs-lookup"><span data-stu-id="349f1-117">TSF supplies the [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) and [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) interface to simplify the registration process.</span></span>

<span data-ttu-id="349f1-118">文字服務提供者也應提供數位簽章給其二進位可執行檔。</span><span class="sxs-lookup"><span data-stu-id="349f1-118">Text service providers should also provide digital signatures with their binary executables.</span></span> <span data-ttu-id="349f1-119">請參閱程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="349f1-119">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).</span></span>

## <a name="registering-the-text-service"></a><span data-ttu-id="349f1-120">註冊文字服務</span><span class="sxs-lookup"><span data-stu-id="349f1-120">Registering the Text Service</span></span>

<span data-ttu-id="349f1-121">文字服務會以文字服務的類別識別碼呼叫 [ITfInputProcessorProfiles：： Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) ，向 TSF 註冊本身。</span><span class="sxs-lookup"><span data-stu-id="349f1-121">A text service registers itself with TSF by calling [ITfInputProcessorProfiles::Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) with the class identifier of the text service.</span></span> <span data-ttu-id="349f1-122">**ITfInputProcessorProfiles** 介面的實例是藉由使用 CLSID TF InputProcessorProfiles 呼叫 **CoCreateInstance** 取得的 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="349f1-122">An instance of the **ITfInputProcessorProfiles** interface is obtained by calling **CoCreateInstance** with CLSID\_TF\_InputProcessorProfiles.</span></span>

<span data-ttu-id="349f1-123">下列範例示範如何建立 **ITfInputProcessorProfiles** 物件並註冊文字服務。</span><span class="sxs-lookup"><span data-stu-id="349f1-123">The following example demonstrates how to create an **ITfInputProcessorProfiles** object and register the text service.</span></span>


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[<span data-ttu-id="349f1-124">ITfInputProcessorProfiles：：取消註冊</span><span class="sxs-lookup"><span data-stu-id="349f1-124">ITfInputProcessorProfiles::Unregister</span></span>](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a><span data-ttu-id="349f1-125">註冊語言設定檔</span><span class="sxs-lookup"><span data-stu-id="349f1-125">Registering Language Profiles</span></span>

<span data-ttu-id="349f1-126">只有當應用程式具有焦點且在語言列中選取了適當的語言時，才可使用文字服務。</span><span class="sxs-lookup"><span data-stu-id="349f1-126">A text service is only available when an application has the focus and the proper language is selected in the language bar.</span></span> <span data-ttu-id="349f1-127">為了方便這項工作，TSF 需要文字服務為其支援的所有語言註冊本身。</span><span class="sxs-lookup"><span data-stu-id="349f1-127">To facilitate this, TSF requires that a text service register itself for all of the languages that it supports.</span></span> <span data-ttu-id="349f1-128">文字服務會藉由呼叫 [ITfInputProcessorProfiles：： AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) 與文字服務類別識別碼、設定檔的語言識別項，以及識別語言設定檔的文字服務定義 **GUID** ，來註冊其語言設定檔。</span><span class="sxs-lookup"><span data-stu-id="349f1-128">The text service registers its language profiles by calling [ITfInputProcessorProfiles::AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) with the text service class identifier, that language identifier of the profile, and a text service defined **GUID** that identifies the language profile.</span></span>

<span data-ttu-id="349f1-129">您可以藉由呼叫 [ITfInputProcessorProfiles：： RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile)來移除語言設定檔。</span><span class="sxs-lookup"><span data-stu-id="349f1-129">A language profile can be removed by calling [ITfInputProcessorProfiles::RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile).</span></span> <span data-ttu-id="349f1-130">**ITfInputProcessorProfiles：：取消註冊** 會移除文字服務的所有語言設定檔;當文字服務卸載時，需要移除個別的語言設定檔。</span><span class="sxs-lookup"><span data-stu-id="349f1-130">**ITfInputProcessorProfiles::Unregister** removes all language profiles for the text service; when a text service is uninstalled, it does require removal of the individual language profiles.</span></span>

## <a name="registering-categories"></a><span data-ttu-id="349f1-131">註冊類別</span><span class="sxs-lookup"><span data-stu-id="349f1-131">Registering Categories</span></span>

<span data-ttu-id="349f1-132">文字服務也必須註冊套用文字服務的類別。</span><span class="sxs-lookup"><span data-stu-id="349f1-132">A text service must also register the category that the text service applies to.</span></span> <span data-ttu-id="349f1-133">例如，如果文字服務提供顯示內容資訊，則必須透過呼叫 [ITfCategoryMgr：： RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) 與第一個參數的文字服務的類別識別碼、GUID TFCAT DISPLAYATTRIBUTEPROVIDER 做為第二個參數 \_ \_ 以及第三個參數的文字服務類別識別碼，將本身註冊為顯示內容提供者。</span><span class="sxs-lookup"><span data-stu-id="349f1-133">For example, if the text service supplies display attribute information, it must register itself as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span> <span data-ttu-id="349f1-134">可能的類別會列在 [預先定義的類別目錄值](predefined-category-values.md)底下。</span><span class="sxs-lookup"><span data-stu-id="349f1-134">The possible categories are listed under [Predefined Category Values](predefined-category-values.md).</span></span>

<span data-ttu-id="349f1-135">藉由呼叫 [ITfCategoryMgr：： UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory)來移除先前註冊的類別。</span><span class="sxs-lookup"><span data-stu-id="349f1-135">Remove previously registered categories by calling [ITfCategoryMgr::UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory).</span></span> <span data-ttu-id="349f1-136">ITfInputProcessorProfiles：：取消註冊會移除文字服務的所有類別;當文字服務卸載時，它必須移除個別類別。</span><span class="sxs-lookup"><span data-stu-id="349f1-136">ITfInputProcessorProfiles::Unregister removes all categories for the text service; when a text service is uninstalled, it must remove the individual categories.</span></span>

 

 