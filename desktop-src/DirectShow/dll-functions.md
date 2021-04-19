---
description: 本主題說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: DLL 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991585"
---
# <a name="dll-functions"></a><span data-ttu-id="82eb6-103">DLL 函數</span><span class="sxs-lookup"><span data-stu-id="82eb6-103">DLL Functions</span></span>

<span data-ttu-id="82eb6-104">本主題說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="82eb6-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="82eb6-105">DLL 必須執行下列函式，才能註冊、取消註冊，並將其載入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="82eb6-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="82eb6-106">[*DllMain*](/windows/desktop/Dlls/dllmain)： DLL 進入點。</span><span class="sxs-lookup"><span data-stu-id="82eb6-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="82eb6-107">名稱 *DllMain* 是程式庫定義函數名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="82eb6-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="82eb6-108">DirectShow 執行會使用名稱 **DllEntryPoint**。</span><span class="sxs-lookup"><span data-stu-id="82eb6-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="82eb6-109">如需詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="82eb6-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="82eb6-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)：建立 class factory 實例。</span><span class="sxs-lookup"><span data-stu-id="82eb6-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="82eb6-111">如上一節所述。</span><span class="sxs-lookup"><span data-stu-id="82eb6-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="82eb6-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)：查詢是否可以安全地卸載 DLL。</span><span class="sxs-lookup"><span data-stu-id="82eb6-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="82eb6-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)：建立 DLL 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="82eb6-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="82eb6-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)：移除 DLL 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="82eb6-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="82eb6-115">其中，前三個是由 DirectShow 所執行。</span><span class="sxs-lookup"><span data-stu-id="82eb6-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="82eb6-116">如果您的 factory 範本在 [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) 成員變數中提供初始化函式，則會從 DLL 進入點函數內部呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="82eb6-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="82eb6-117">如需有關系統何時呼叫 DLL 進入點函數的詳細資訊，請參閱 [*DllMain*](/windows/desktop/Dlls/dllmain)。</span><span class="sxs-lookup"><span data-stu-id="82eb6-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="82eb6-118">您必須執行 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)，但 DirectShow 提供了一個名為 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 的函式，它會執行必要的工作。</span><span class="sxs-lookup"><span data-stu-id="82eb6-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="82eb6-119">您的元件可以直接包裝此函式，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="82eb6-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="82eb6-120">不過，在 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) 中，您可以視需要自訂註冊程式。</span><span class="sxs-lookup"><span data-stu-id="82eb6-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="82eb6-121">如果您的 DLL 包含篩選器，您可能需要執行一些額外的工作。</span><span class="sxs-lookup"><span data-stu-id="82eb6-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="82eb6-122">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="82eb6-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="82eb6-123">在模組定義中 ( .def) 檔案中，匯出所有 DLL 函式，但不包括進入點函數。</span><span class="sxs-lookup"><span data-stu-id="82eb6-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="82eb6-124">以下是 .def 檔案的範例：</span><span class="sxs-lookup"><span data-stu-id="82eb6-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="82eb6-125">您可以使用 Regsvr32.exe 公用程式來註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="82eb6-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82eb6-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="82eb6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82eb6-127">如何建立 DirectShow 篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="82eb6-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
