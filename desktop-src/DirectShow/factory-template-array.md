---
description: Factory 範本陣列
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Factory 範本陣列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109900"
---
# <a name="factory-template-array"></a><span data-ttu-id="5aacb-103">Factory 範本陣列</span><span class="sxs-lookup"><span data-stu-id="5aacb-103">Factory Template Array</span></span>

<span data-ttu-id="5aacb-104">Factory 範本包含下列公用成員變數：</span><span class="sxs-lookup"><span data-stu-id="5aacb-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="5aacb-105">這兩個函式指標（ [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) 和 [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md)）使用下列型別定義：</span><span class="sxs-lookup"><span data-stu-id="5aacb-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="5aacb-106">第一個是元件的具現化函數。</span><span class="sxs-lookup"><span data-stu-id="5aacb-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="5aacb-107">第二個是選擇性的初始化函數。</span><span class="sxs-lookup"><span data-stu-id="5aacb-107">The second is an optional initialization function.</span></span> <span data-ttu-id="5aacb-108">如果您提供初始化函式，它會從 DLL 進入點函數內部呼叫。</span><span class="sxs-lookup"><span data-stu-id="5aacb-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="5aacb-109">本文稍後將討論 DLL 進入點函數 (。 ) </span><span class="sxs-lookup"><span data-stu-id="5aacb-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="5aacb-110">假設您要建立一個 DLL，其中包含名為 CMyComponent 的元件，而該元件繼承自 [**CUnknown**](cunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="5aacb-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="5aacb-111">您必須在 DLL 中提供下列專案：</span><span class="sxs-lookup"><span data-stu-id="5aacb-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="5aacb-112">初始化函式，這個公用方法會傳回 CMyComponent 的新實例。</span><span class="sxs-lookup"><span data-stu-id="5aacb-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="5aacb-113">名為 *g \_ 範本* 的原廠範本的全域陣列。</span><span class="sxs-lookup"><span data-stu-id="5aacb-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="5aacb-114">此陣列包含 CMyComponent 的 factory 範本。</span><span class="sxs-lookup"><span data-stu-id="5aacb-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="5aacb-115">名為 *g \_ cTemplates* 的全域變數，可指定陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="5aacb-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="5aacb-116">下列範例顯示如何宣告這些專案：</span><span class="sxs-lookup"><span data-stu-id="5aacb-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="5aacb-117">`CreateInstance`方法會呼叫類別的函式，並將指標傳回至新的類別實例。</span><span class="sxs-lookup"><span data-stu-id="5aacb-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="5aacb-118">參數 *pUnk* 是匯總 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)的指標。</span><span class="sxs-lookup"><span data-stu-id="5aacb-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="5aacb-119">您可以直接將此參數傳遞至類別的函式。</span><span class="sxs-lookup"><span data-stu-id="5aacb-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="5aacb-120">參數 *pHr* 是 HRESULT 值的指標。</span><span class="sxs-lookup"><span data-stu-id="5aacb-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="5aacb-121">類別的函式會將此值設定為適當的值，但如果此函式失敗，請將值設定為 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="5aacb-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="5aacb-122">[**NAME**](name.md)宏會在 debug 組建中產生字串，但會在零售組建中解析為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5aacb-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="5aacb-123">在此範例中，會使用它來提供元件名稱，此名稱會出現在偵錯工具記錄檔中，但不會在最終版本中佔用記憶體。</span><span class="sxs-lookup"><span data-stu-id="5aacb-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="5aacb-124">`CreateInstance`方法可以有任何名稱，因為 class factory 參考 factory 範本中的函式指標。</span><span class="sxs-lookup"><span data-stu-id="5aacb-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="5aacb-125">但是， *g \_ 範本* 和 *g \_ cTemplates* 是 class factory 預期要尋找的全域變數，因此它們必須正好具有這些名稱。</span><span class="sxs-lookup"><span data-stu-id="5aacb-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aacb-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="5aacb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aacb-127">如何建立 DirectShow 篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="5aacb-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
