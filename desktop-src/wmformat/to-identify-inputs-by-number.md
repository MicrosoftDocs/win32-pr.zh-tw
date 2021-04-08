---
title: 依數位識別輸入
description: 依數位識別輸入
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF) ，以數位識別輸入
- ASF (Advanced Systems Format) ，依數位識別輸入
- 設定檔，依編號識別輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023031"
---
# <a name="to-identify-inputs-by-number"></a><span data-ttu-id="b4b47-106">依數位識別輸入</span><span class="sxs-lookup"><span data-stu-id="b4b47-106">To Identify Inputs By Number</span></span>

<span data-ttu-id="b4b47-107">您傳遞給寫入器的每個範例都必須與輸入編號相關聯。</span><span class="sxs-lookup"><span data-stu-id="b4b47-107">Every sample you pass to the writer must be associated with an input number.</span></span> <span data-ttu-id="b4b47-108">每個輸入號碼都會對應到寫入器用來寫入檔案的設定檔中的一或多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="b4b47-108">Each input number corresponds to one or more streams in the profile that the writer is using to write the file.</span></span> <span data-ttu-id="b4b47-109">在設定檔中，媒體來源是以連接名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="b4b47-109">In a profile, media sources are identified by a connection name.</span></span> <span data-ttu-id="b4b47-110">當您設定寫入器的設定檔時，寫入器會將輸入編號與每個連接名稱產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b4b47-110">The writer associates an input number with each connection name when you set the profile for the writer.</span></span> <span data-ttu-id="b4b47-111">在您可以將範例傳遞給寫入器之前，您必須決定每個輸入所預期的資料。</span><span class="sxs-lookup"><span data-stu-id="b4b47-111">Before you can pass samples to the writer, you must determine what data each input is expecting.</span></span> <span data-ttu-id="b4b47-112">您無法假設輸入的順序與設定檔中的資料流程相同，即使通常是如此。</span><span class="sxs-lookup"><span data-stu-id="b4b47-112">You cannot assume that the inputs will be in the same order as the streams in a profile, even if this is often the case.</span></span> <span data-ttu-id="b4b47-113">因此，將輸入與資料流程相符的唯一可靠方式是將輸入的連接名稱與資料流程的連接名稱進行比較。</span><span class="sxs-lookup"><span data-stu-id="b4b47-113">Therefore, the only reliable way to match inputs with streams is to compare the connection name of the input with the connection name of the stream.</span></span>

<span data-ttu-id="b4b47-114">若要識別已載入設定檔的連線名稱和對應的輸入編號，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b4b47-114">To identify the connection names and corresponding input numbers for a loaded profile, perform the following steps:</span></span>

1.  <span data-ttu-id="b4b47-115">建立寫入器物件，並設定要使用的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b4b47-115">Create a writer object and set a profile to use.</span></span> <span data-ttu-id="b4b47-116">如需在寫入器中設定設定檔的詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="b4b47-116">For more information about setting profiles in the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="b4b47-117">您應該知道設定檔中的資料流程所使用的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b47-117">You should know the connection names used for the streams in the profile.</span></span> <span data-ttu-id="b4b47-118">您可以取得每個資料流程的串流設定物件，並呼叫 [**IWMStreamConfig：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname)，以從設定檔中取得連接名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b47-118">You can get the connection name from within the profile by getting the stream configuration object for each stream and calling [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname).</span></span> <span data-ttu-id="b4b47-119">如需設定檔和串流設定物件的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。</span><span class="sxs-lookup"><span data-stu-id="b4b47-119">For more information about profiles and stream configuration objects, see [Working with Profiles](working-with-profiles.md).</span></span>
2.  <span data-ttu-id="b4b47-120">藉由呼叫 [**IWMWriter：： GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount)來取出輸入總數。</span><span class="sxs-lookup"><span data-stu-id="b4b47-120">Retrieve the total number of inputs by calling [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount).</span></span>
3.  <span data-ttu-id="b4b47-121">迴圈執行所有輸入，為每個輸入執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="b4b47-121">Loop through all of the inputs, performing the following steps for each.</span></span>
    -   <span data-ttu-id="b4b47-122">藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)，來取得輸入的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="b4b47-122">Retrieve the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
    -   <span data-ttu-id="b4b47-123">藉由呼叫 [**IWMInputMediaProps：： GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname)，以抓取與輸入編號對應的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b47-123">Retrieve the connection name that corresponds to the input number by calling [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname).</span></span> <span data-ttu-id="b4b47-124">連接名稱之後，您就知道與寫入器指派的輸入編號相關聯的資料流程。</span><span class="sxs-lookup"><span data-stu-id="b4b47-124">After you have the connection name, you know the streams that are associated with the input numbers assigned by the writer.</span></span>

<span data-ttu-id="b4b47-125">下列程式碼範例會顯示每個輸入的連接名稱。</span><span class="sxs-lookup"><span data-stu-id="b4b47-125">The following example code displays the connection name for each input.</span></span> <span data-ttu-id="b4b47-126">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="b4b47-126">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="b4b47-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4b47-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4b47-128">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="b4b47-128">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="b4b47-129">**寫入 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="b4b47-129">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




