---
description: 在建立自訂 DirectShow 篩選器的篩選屬性頁時，將篩選的新介面公開給用戶端。
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 步驟 3： 支援 QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410021"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="98682-104">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="98682-104">Step 3.</span></span> <span data-ttu-id="98682-105">支援 QueryInterface</span><span class="sxs-lookup"><span data-stu-id="98682-105">Support QueryInterface</span></span>

<span data-ttu-id="98682-106">若要向用戶端公開篩選的新介面，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="98682-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="98682-107">在篩選準則的公用宣告區段中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏：</span><span class="sxs-lookup"><span data-stu-id="98682-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="98682-108">覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) ，以檢查兩個介面的 iid：</span><span class="sxs-lookup"><span data-stu-id="98682-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

<span data-ttu-id="98682-109">下一 [步：步驟4。建立屬性頁](step-4--create-the-property-page.md)。</span><span class="sxs-lookup"><span data-stu-id="98682-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="98682-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="98682-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98682-111">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="98682-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="98682-112">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="98682-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



