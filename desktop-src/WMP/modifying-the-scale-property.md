---
title: 修改尺規屬性
description: 修改尺規屬性
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，小數位數屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd91e2315db9d0d1e14d2aec55f79a8b05c442ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968219"
---
# <a name="modifying-the-scale-property"></a><span data-ttu-id="1484d-108">修改尺規屬性</span><span class="sxs-lookup"><span data-stu-id="1484d-108">Modifying the Scale Property</span></span>

<span data-ttu-id="1484d-109">預設的 wizard 執行會公開 scale 屬性。</span><span class="sxs-lookup"><span data-stu-id="1484d-109">The default wizard implementation exposes the scale property.</span></span> <span data-ttu-id="1484d-110">您可以變更現有的實作為，改為公開 [延遲時間] 屬性。</span><span class="sxs-lookup"><span data-stu-id="1484d-110">You can change the existing implementation to expose the delay time property instead.</span></span>

<span data-ttu-id="1484d-111">首先，使用下列範例來變更 \_ 在 Echo 中取得尺規和 put 縮放的函式原型 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1484d-111">First, use the following example to change the function prototypes for get\_scale and put\_scale in Echo.h.</span></span> <span data-ttu-id="1484d-112">變更方法的名稱和參數的資料類型：</span><span class="sxs-lookup"><span data-stu-id="1484d-112">Change the name of the methods and the data types for the parameters:</span></span>


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



<span data-ttu-id="1484d-113">接下來， \_ 在 Echo 中變更取得規模和 put \_ 調整方法的執行。</span><span class="sxs-lookup"><span data-stu-id="1484d-113">Next, change the implementations of the get\_scale and put\_scale methods in Echo.cpp.</span></span> <span data-ttu-id="1484d-114">使程式碼符合下列範例：</span><span class="sxs-lookup"><span data-stu-id="1484d-114">Make the code match the following examples:</span></span>


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



<span data-ttu-id="1484d-115">上述範例程式碼會變更方法名稱和參數資料類型。</span><span class="sxs-lookup"><span data-stu-id="1484d-115">The preceding example code changes the method names and the parameter data types.</span></span> <span data-ttu-id="1484d-116">成員變數名稱先前應該已經變更。</span><span class="sxs-lookup"><span data-stu-id="1484d-116">The member variable name should have been changed previously.</span></span> <span data-ttu-id="1484d-117">也請記得變更引進每個方法的批註。</span><span class="sxs-lookup"><span data-stu-id="1484d-117">Remember to change the comments that introduce each method as well.</span></span>

<span data-ttu-id="1484d-118">現在，變更介面定義。</span><span class="sxs-lookup"><span data-stu-id="1484d-118">Now, change the interface definition.</span></span> <span data-ttu-id="1484d-119">下列程式碼會取代 Echo 中 IEcho 介面宣告中的程式碼：</span><span class="sxs-lookup"><span data-stu-id="1484d-119">The following code replaces the code in the IEcho interface declaration in Echo.idl:</span></span>


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a><span data-ttu-id="1484d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1484d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1484d-121">**Echo 範例屬性**</span><span class="sxs-lookup"><span data-stu-id="1484d-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




