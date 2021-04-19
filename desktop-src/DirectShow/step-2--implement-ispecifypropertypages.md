---
description: 步驟 2：
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: 步驟 2： 執行 ISpecifyPropertyPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983800"
---
# <a name="step-2-implement-ispecifypropertypages"></a><span data-ttu-id="afc08-104">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="afc08-104">Step 2.</span></span> <span data-ttu-id="afc08-105">執行 ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="afc08-105">Implement ISpecifyPropertyPages</span></span>

<span data-ttu-id="afc08-106">接下來，在篩選中執行 **ISpecifyPropertyPages** 介面。</span><span class="sxs-lookup"><span data-stu-id="afc08-106">Next, implement the **ISpecifyPropertyPages** interface in your filter.</span></span> <span data-ttu-id="afc08-107">這個介面具有單一方法 **GetPages**，它會針對篩選準則所支援的屬性頁傳回 clsid 的陣列。</span><span class="sxs-lookup"><span data-stu-id="afc08-107">This interface has a single method, **GetPages**, which returns an array of CLSIDs for the property pages that the filter supports.</span></span> <span data-ttu-id="afc08-108">在此範例中，篩選準則具有單一屬性頁。</span><span class="sxs-lookup"><span data-stu-id="afc08-108">In this example, the filter has a single property page.</span></span> <span data-ttu-id="afc08-109">從產生 CLSID 並在標頭檔中宣告它來開始：</span><span class="sxs-lookup"><span data-stu-id="afc08-109">Start by generating the CLSID and declaring it in your header file:</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



<span data-ttu-id="afc08-110">現在，請執行 **GetPages** 方法：</span><span class="sxs-lookup"><span data-stu-id="afc08-110">Now implement the **GetPages** method:</span></span>


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



<span data-ttu-id="afc08-111">使用 **CoTaskMemAlloc** 配置陣列的記憶體。</span><span class="sxs-lookup"><span data-stu-id="afc08-111">Allocate memory for the array using **CoTaskMemAlloc**.</span></span> <span data-ttu-id="afc08-112">呼叫端會釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="afc08-112">The caller will release the memory.</span></span>

<span data-ttu-id="afc08-113">下一 [步：步驟3。支援 QueryInterface](step-3--support-queryinterface.md)。</span><span class="sxs-lookup"><span data-stu-id="afc08-113">Next: [Step 3. Support QueryInterface](step-3--support-queryinterface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="afc08-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="afc08-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afc08-115">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="afc08-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



