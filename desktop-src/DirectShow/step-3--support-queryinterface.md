---
description: 步驟 3：
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: 步驟 3： 支援 QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e3d44b67971e165b8586aa3a02cc65ab3ab05f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971574"
---
# <a name="step-3-support-queryinterface"></a><span data-ttu-id="49185-104">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="49185-104">Step 3.</span></span> <span data-ttu-id="49185-105">支援 QueryInterface</span><span class="sxs-lookup"><span data-stu-id="49185-105">Support QueryInterface</span></span>

<span data-ttu-id="49185-106">若要向用戶端公開篩選的新介面，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="49185-106">To expose the filter's new interfaces to clients, do the following:</span></span>

-   <span data-ttu-id="49185-107">在篩選準則的公用宣告區段中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 宏：</span><span class="sxs-lookup"><span data-stu-id="49185-107">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public declaration section of your filter:</span></span>
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   <span data-ttu-id="49185-108">覆寫 [**CUnknown：： NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) ，以檢查兩個介面的 iid：</span><span class="sxs-lookup"><span data-stu-id="49185-108">Override [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) to check for the IIDs of the two interfaces:</span></span>
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

    

<span data-ttu-id="49185-109">下一 [步：步驟4。建立屬性頁](step-4--create-the-property-page.md)。</span><span class="sxs-lookup"><span data-stu-id="49185-109">Next: [Step 4. Create the Property Page](step-4--create-the-property-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49185-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="49185-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49185-111">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="49185-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="49185-112">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="49185-112">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 



