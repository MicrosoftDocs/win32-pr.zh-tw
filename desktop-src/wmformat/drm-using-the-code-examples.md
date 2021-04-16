---
title: 使用 Microsoft Windows Media DRM 用戶端程式代碼範例
description: 使用 Microsoft Windows Media DRM 用戶端程式代碼範例
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK，程式碼範例
- Windows Media Format SDK，範例程式碼
- Windows Media Format SDK，DRM 程式碼範例
- 數位版權管理 (DRM) ，程式碼範例
- DRM (數位版權管理) ，程式碼範例
- 數位版權管理 (DRM) ，範例程式碼
- DRM (數位版權管理) ，範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383545"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="9239d-110">使用 Microsoft Windows Media DRM 用戶端程式代碼範例</span><span class="sxs-lookup"><span data-stu-id="9239d-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="9239d-111">本檔中包含程式碼範例，以說明元件的使用方式。</span><span class="sxs-lookup"><span data-stu-id="9239d-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="9239d-112">這些範例會盡可能清楚且簡潔地撰寫。</span><span class="sxs-lookup"><span data-stu-id="9239d-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="9239d-113">閱讀範例時，您應該注意下列慣例。</span><span class="sxs-lookup"><span data-stu-id="9239d-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="9239d-114">所有範例都假設為包含 windows .h 和 wmdrmsdk .h。</span><span class="sxs-lookup"><span data-stu-id="9239d-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="9239d-115">如果需要其他標頭才能進行編譯，此範例將包含附注。</span><span class="sxs-lookup"><span data-stu-id="9239d-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="9239d-116">如果發生錯誤，則錯誤檢查已限制為無法中斷函數。</span><span class="sxs-lookup"><span data-stu-id="9239d-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="9239d-117">在應用程式中，您應該檢查特定的錯誤碼，並提供某種類型的錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="9239d-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="9239d-118">在程式碼範例中，會使用名為 SAFE \_ RELEASE 和 safe \_ ARRAY DELETE 的宏來釋放介面和記憶體 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9239d-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="9239d-119">這些宏會在下列程式碼中定義：</span><span class="sxs-lookup"><span data-stu-id="9239d-119">These macros are defined in the following code:</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="9239d-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9239d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9239d-121">**開始使用**</span><span class="sxs-lookup"><span data-stu-id="9239d-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




