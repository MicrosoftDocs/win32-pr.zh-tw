---
title: ACF 標頭
description: ACF 標頭包含適用于整個介面的平臺特定屬性。 套用至 ACF 主體中個別類型和函式的屬性會覆寫 ACF 標頭中的屬性。 ACF 標頭中不需要任何屬性。
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023755"
---
# <a name="the-acf-header"></a><span data-ttu-id="c2b31-105">ACF 標頭</span><span class="sxs-lookup"><span data-stu-id="c2b31-105">The ACF Header</span></span>

<span data-ttu-id="c2b31-106">ACF 標頭包含適用于整個介面的平臺特定屬性。</span><span class="sxs-lookup"><span data-stu-id="c2b31-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="c2b31-107">套用至 ACF 主體中個別類型和函式的屬性會覆寫 ACF 標頭中的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2b31-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="c2b31-108">ACF 標頭中不需要任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c2b31-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="c2b31-109">ACF 標頭可以包含下列其中一個屬性： **\[** [**auto \_ 控制碼**](/windows/desktop/Midl/auto-handle) **\]** 、 **\[** [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) **\]** 或 [**明確 \_ 控制碼**](/windows/desktop/Midl/explicit-handle) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="c2b31-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="c2b31-110">如果使用 **\[ auto \_ 控制碼 \]** 或 **\[ 隱含 \_ 控制碼 \]** ，它會指定當遠端函式沒有明確的系結控制碼參數時，將用於系結的系結控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="c2b31-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="c2b31-111">當 ACF 不存在或未指定自動、隱含或明確的系結控制碼時，MIDL 會針對隱含系結使用 **\[ auto \_ 控制碼 \]** 。</span><span class="sxs-lookup"><span data-stu-id="c2b31-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="c2b31-112">程式 **\[** [**代碼**](/windows/desktop/Midl/code) **\]** 或 **\[** [**了 nocode**](/windows/desktop/Midl/nocode) **\]** 可以出現在介面標頭中，但您選擇的只會顯示一次。</span><span class="sxs-lookup"><span data-stu-id="c2b31-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="c2b31-113">當兩個屬性都不存在時，編譯器會使用程式 **\[ 代碼 \]** 做為預設值。</span><span class="sxs-lookup"><span data-stu-id="c2b31-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="c2b31-114">如需詳細資訊，請參閱 [ACF 屬性](/windows/desktop/Midl/acf-attributes)。</span><span class="sxs-lookup"><span data-stu-id="c2b31-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 