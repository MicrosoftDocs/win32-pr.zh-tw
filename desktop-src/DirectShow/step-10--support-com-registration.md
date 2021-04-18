---
description: 步驟 10：
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: 步驟 10： 支援 COM 註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971477"
---
# <a name="step-10-support-com-registration"></a><span data-ttu-id="8fc3b-104">步驟 10：</span><span class="sxs-lookup"><span data-stu-id="8fc3b-104">Step 10.</span></span> <span data-ttu-id="8fc3b-105">支援 COM 註冊</span><span class="sxs-lookup"><span data-stu-id="8fc3b-105">Support COM Registration</span></span>

<span data-ttu-id="8fc3b-106">最後一項工作是支援 COM 註冊，讓屬性框架可以建立您屬性頁的新實例。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="8fc3b-107">將另一個 [**CFactoryTemplate**](cfactorytemplate.md) 專案加入至全域 *g \_ 範本* 陣列，用來註冊 DLL 中的所有 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="8fc3b-108">請勿包含屬性頁的任何篩選設定資訊。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-108">Do not include any filter set-up information for the property page.</span></span>


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



<span data-ttu-id="8fc3b-109">如果您如下列程式碼所示宣告 *g \_ cTemplates* ，則它會根據陣列大小自動具有正確的值：</span><span class="sxs-lookup"><span data-stu-id="8fc3b-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="8fc3b-110">此外，將靜態 `CreateInstance` 方法加入至屬性頁類別。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="8fc3b-111">您可以為方法命名任何您偏好的名稱，但簽章必須符合下列範例所示的內容：</span><span class="sxs-lookup"><span data-stu-id="8fc3b-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



<span data-ttu-id="8fc3b-112">若要測試屬性頁，請註冊 DLL，然後在 GraphEdit 中載入篩選。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="8fc3b-113">以滑鼠右鍵按一下篩選器，然後選取 [ **篩選屬性**]。</span><span class="sxs-lookup"><span data-stu-id="8fc3b-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fc3b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fc3b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc3b-115">建立篩選屬性頁</span><span class="sxs-lookup"><span data-stu-id="8fc3b-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="8fc3b-116">如何建立 DirectShow 篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="8fc3b-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



