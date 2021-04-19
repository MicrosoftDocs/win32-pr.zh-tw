---
title: 將屬性新增至範例音訊 DSP 外掛程式
description: 將屬性新增至範例音訊 DSP 外掛程式
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊屬性
- DSP 外掛程式、音訊屬性
- 音訊 DSP 外掛程式，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969657"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a><span data-ttu-id="7c57f-108">將屬性新增至範例音訊 DSP 外掛程式</span><span class="sxs-lookup"><span data-stu-id="7c57f-108">Adding Properties to the Sample Audio DSP Plug-in</span></span>

<span data-ttu-id="7c57f-109">Windows Media Player 外掛程式 Wizard 產生的音訊 DSP 範例程式碼會使用代表音訊音量比例因數的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="7c57f-109">The audio DSP sample code that the Windows Media Player Plug-in Wizard generates uses a single property that represents the scale factor for the audio volume.</span></span> <span data-ttu-id="7c57f-110">您的外掛程式可能需要一個以上的屬性。</span><span class="sxs-lookup"><span data-stu-id="7c57f-110">Your plug-in may require more than one property.</span></span> <span data-ttu-id="7c57f-111">您可以使用下列步驟，在 Visual Studio 中輕鬆地將屬性新增至您的 DSP 外掛程式：</span><span class="sxs-lookup"><span data-stu-id="7c57f-111">You can easily add properties to your DSP plug-in in Visual Studio using the following steps:</span></span>

-   <span data-ttu-id="7c57f-112">在屬於 proxy 存根專案一部分的 IDL 檔案中，定義介面定義程式碼中的方法。</span><span class="sxs-lookup"><span data-stu-id="7c57f-112">Define the methods in the interface definition code in the IDL file that is part of the proxy-stub project.</span></span>
    -   <span data-ttu-id="7c57f-113">將方法執行程式新增至專案的主要 CPP 檔案：</span><span class="sxs-lookup"><span data-stu-id="7c57f-113">Add the method implementations to the project's main CPP file:</span></span>

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

<span data-ttu-id="7c57f-114">最後，為了讓使用者可以存取屬性，您會想要對屬性頁的執行進行變更。</span><span class="sxs-lookup"><span data-stu-id="7c57f-114">Finally, to make the properties accessible to the user, you'll want to make changes to the property page implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c57f-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="7c57f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c57f-116">**執行音訊 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="7c57f-116">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




