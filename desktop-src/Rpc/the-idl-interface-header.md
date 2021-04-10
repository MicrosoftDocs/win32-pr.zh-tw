---
title: IDL 介面標頭
description: IDL 介面標頭會指定整個介面的相關資訊。 不同于 ACF，介面標頭包含的屬性與平臺無關。
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093240"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="51c2d-104">IDL 介面標頭</span><span class="sxs-lookup"><span data-stu-id="51c2d-104">The IDL Interface Header</span></span>

<span data-ttu-id="51c2d-105">IDL 介面標頭會指定整個介面的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51c2d-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="51c2d-106">不同于 ACF，介面標頭包含的屬性與平臺無關。</span><span class="sxs-lookup"><span data-stu-id="51c2d-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="51c2d-107">介面標頭中的屬性是整個介面的通用屬性。</span><span class="sxs-lookup"><span data-stu-id="51c2d-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="51c2d-108">亦即，它們會套用至介面及其所有部分。</span><span class="sxs-lookup"><span data-stu-id="51c2d-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="51c2d-109">這些屬性會以方括弧括住介面定義的開頭。</span><span class="sxs-lookup"><span data-stu-id="51c2d-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="51c2d-110">下列介面定義中會顯示一個範例：</span><span class="sxs-lookup"><span data-stu-id="51c2d-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="51c2d-111">請注意，介面標頭包含 **\[** [**uuid**](/windows/desktop/Midl/uuid) **\]** 和 **\[** [**version**](/windows/desktop/Midl/version) **\]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="51c2d-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="51c2d-112">因為這些分別代表介面的 UUID 和版本號碼，所以它們是整個介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="51c2d-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="51c2d-113">介面主體也可以包含屬性。</span><span class="sxs-lookup"><span data-stu-id="51c2d-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="51c2d-114">不過，它們並不適用于整個介面。</span><span class="sxs-lookup"><span data-stu-id="51c2d-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="51c2d-115">它們參考介面中的特定專案，例如遠端過程參數。</span><span class="sxs-lookup"><span data-stu-id="51c2d-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="51c2d-116">如需 IDL 標頭屬性的完整討論，請參閱 [MIDL 語言參考](/windows/desktop/Midl/midl-language-reference)。</span><span class="sxs-lookup"><span data-stu-id="51c2d-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 