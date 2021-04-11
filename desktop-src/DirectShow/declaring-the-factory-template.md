---
description: 宣告 Factory 範本
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: 宣告 Factory 範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108629"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="57d23-103">宣告 Factory 範本</span><span class="sxs-lookup"><span data-stu-id="57d23-103">Declaring the Factory Template</span></span>

<span data-ttu-id="57d23-104">下一步是宣告您篩選的 factory 範本。</span><span class="sxs-lookup"><span data-stu-id="57d23-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="57d23-105">Factory 範本是 c + + 類別，其中包含 class factory 的資訊。</span><span class="sxs-lookup"><span data-stu-id="57d23-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="57d23-106">在您的 DLL 中，宣告 [**CFactoryTemplate**](cfactorytemplate.md) 物件的全域陣列，也就是 dll 中每個篩選或 COM 元件的陣列。</span><span class="sxs-lookup"><span data-stu-id="57d23-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="57d23-107">陣列必須命名為 *g \_ Templates*。</span><span class="sxs-lookup"><span data-stu-id="57d23-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="57d23-108">如需工廠範本的詳細資訊，請參閱 [如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)。</span><span class="sxs-lookup"><span data-stu-id="57d23-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="57d23-109">Factory 範本的 **m \_ pAMovieSetup \_ 濾波器** 成員是先前所述之 [**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="57d23-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="57d23-110">下列範例會使用前一個範例中提供的結構來顯示 factory 範本：</span><span class="sxs-lookup"><span data-stu-id="57d23-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="57d23-111">如果您未宣告任何篩選資訊， **m \_ pAMoveSetup \_ 濾波器** 可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57d23-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57d23-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="57d23-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57d23-113">如何註冊 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="57d23-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



