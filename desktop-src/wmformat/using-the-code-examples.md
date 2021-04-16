---
title: 使用 Windows Media Format SDK 程式碼範例
description: 使用 Windows Media Format SDK 程式碼範例
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK，程式碼範例
- Windows Media Format SDK，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383785"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="e617c-105">使用 Windows Media Format SDK 程式碼範例</span><span class="sxs-lookup"><span data-stu-id="e617c-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="e617c-106">此 SDK 的許多說明章節都包含程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="e617c-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="e617c-107">這些範例會盡可能清楚且簡潔地撰寫。</span><span class="sxs-lookup"><span data-stu-id="e617c-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="e617c-108">閱讀範例時，您應該注意下列慣例。</span><span class="sxs-lookup"><span data-stu-id="e617c-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="e617c-109">所有範例都假設為包含 windows .h 和 wmsdk .h。</span><span class="sxs-lookup"><span data-stu-id="e617c-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="e617c-110">解說文字中提及任何其他必要的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="e617c-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="e617c-111">如果發生錯誤，則錯誤檢查已限制為無法中斷函數。</span><span class="sxs-lookup"><span data-stu-id="e617c-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="e617c-112">在應用程式中，您應該檢查特定的錯誤碼，並提供某種類型的錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="e617c-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="e617c-113">檢查傳回 **HRESULT** 值的方法或函式傳回值時，您應該使用 **FAILED** 宏來探索傳回值是否指出失敗。</span><span class="sxs-lookup"><span data-stu-id="e617c-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="e617c-114">本檔中的許多範例都使用名為 GOTO EXIT 的宏 \_ \_ \_ （如果失敗），這是在下列程式碼中定義的。</span><span class="sxs-lookup"><span data-stu-id="e617c-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="e617c-115">這些範例函式每個都有一個名為 "Exit：" 的標記，之後會釋出函式中配置的所有介面和記憶體，並傳回錯誤碼（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e617c-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="e617c-116">在程式碼範例中，會使用名為 SAFE \_ RELEASE 和 safe \_ ARRAY DELETE 的宏來釋放介面和記憶體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e617c-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="e617c-117">這些宏會在下列程式碼中定義：</span><span class="sxs-lookup"><span data-stu-id="e617c-117">These macros are defined in the following code:</span></span>
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   <span data-ttu-id="e617c-118">通常，您必須在另一個範例中包含一個範例的邏輯，讓範例有意義。</span><span class="sxs-lookup"><span data-stu-id="e617c-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="e617c-119">在這些情況下，會包含 TODO 批註以及適當程式碼範例的參考。</span><span class="sxs-lookup"><span data-stu-id="e617c-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="e617c-120">為了讓程式碼更容易閱讀，本檔中的範例函式都不會驗證其輸入參數。</span><span class="sxs-lookup"><span data-stu-id="e617c-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="e617c-121">如果您將任何這些函式複製到您的程式碼中，您應該驗證任何輸入參數。</span><span class="sxs-lookup"><span data-stu-id="e617c-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e617c-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="e617c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e617c-123">**開始使用**</span><span class="sxs-lookup"><span data-stu-id="e617c-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




