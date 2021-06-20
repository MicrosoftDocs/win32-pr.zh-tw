---
description: 在建立自訂 DirectShow 篩選準則的篩選屬性頁時，定義用來設定屬性的機制。
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: 步驟 1： 定義用來設定屬性的機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410071"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="1598d-104">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="1598d-104">Step 1.</span></span> <span data-ttu-id="1598d-105">定義用來設定屬性的機制</span><span class="sxs-lookup"><span data-stu-id="1598d-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="1598d-106">篩選準則必須支援屬性頁面與其通訊的方式，讓屬性頁可以設定和抓取篩選的屬性。</span><span class="sxs-lookup"><span data-stu-id="1598d-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="1598d-107">可能的機制包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="1598d-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="1598d-108">公開自訂 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="1598d-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="1598d-109">透過 **IDispatch** 支援 Automation 屬性。</span><span class="sxs-lookup"><span data-stu-id="1598d-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="1598d-110">公開 **IPropertyBag** 介面，並定義一組命名屬性。</span><span class="sxs-lookup"><span data-stu-id="1598d-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="1598d-111">這個範例會使用名為 ISaturation 的自訂 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="1598d-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="1598d-112">這不是實際的 DirectShow 介面;它只會在此範例中定義。</span><span class="sxs-lookup"><span data-stu-id="1598d-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="1598d-113">首先，在標頭檔中宣告介面，以及 (IID) 的介面識別碼：</span><span class="sxs-lookup"><span data-stu-id="1598d-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="1598d-114">您也可以使用 IDL 定義介面，並使用 MIDL 編譯器來建立標頭檔。</span><span class="sxs-lookup"><span data-stu-id="1598d-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="1598d-115">接下來，在篩選中執行自訂介面。</span><span class="sxs-lookup"><span data-stu-id="1598d-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="1598d-116">此範例會使用 "Get" 和 "Set" 方法做為篩選的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="1598d-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="1598d-117">請注意，這兩種方法都可保護 m \_ lSaturation 成員的重要區段。</span><span class="sxs-lookup"><span data-stu-id="1598d-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="1598d-118">當然，您自己的實作為詳細資料將與此處所示的範例不同。</span><span class="sxs-lookup"><span data-stu-id="1598d-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="1598d-119">下一 [步：步驟2。執行 ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)。</span><span class="sxs-lookup"><span data-stu-id="1598d-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1598d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="1598d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1598d-121">**CCritSec 類別**</span><span class="sxs-lookup"><span data-stu-id="1598d-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="1598d-122">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="1598d-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



