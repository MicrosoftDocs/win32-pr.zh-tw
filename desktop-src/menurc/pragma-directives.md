---
title: Pragma 指示詞
description: RC 不支援 C/c + + 編譯器所支援的 pragma 指示詞。
ms.assetid: c7a944c0-a3d4-4568-a9ac-c338f0eaa427
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0c92136ba5e00d5b821d35ea05a337e7d6abe7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023453"
---
# <a name="pragma-directives"></a><span data-ttu-id="6e445-103">Pragma 指示詞</span><span class="sxs-lookup"><span data-stu-id="6e445-103">Pragma Directives</span></span>

<span data-ttu-id="6e445-104">RC 不支援 C/c + + 編譯器所支援的 pragma 指示詞。</span><span class="sxs-lookup"><span data-stu-id="6e445-104">RC does not support the pragma directives supported by the C/C++ compiler.</span></span> <span data-ttu-id="6e445-105">不過，RC 支援下列 pragma 指示詞來變更字碼頁：</span><span class="sxs-lookup"><span data-stu-id="6e445-105">However, RC does support the following pragma directive for changing the code page:</span></span>

``` syntax
#pragma code_page( [ DEFAULT | CodePageNum ] )
```

<span data-ttu-id="6e445-106"> ( .rc) 包含的資源檔中不支援這個 pragma。</span><span class="sxs-lookup"><span data-stu-id="6e445-106">This pragma is not supported in an included resource file (.rc).</span></span> <span data-ttu-id="6e445-107">因此，如果您有一個上層 .rc 檔案，且其中包含適用于多種語言的 .rc 檔，請在包含另一個 .rc 檔之前使用此 pragma，而不是在包含的 .rc 檔本身中使用它。</span><span class="sxs-lookup"><span data-stu-id="6e445-107">Therefore, if you have a parent .rc file and it includes .rc files for multiple languages, use this pragma before including another .rc file rather than using it in the included .rc file itself.</span></span> <span data-ttu-id="6e445-108">下列範例就將此進行示範。</span><span class="sxs-lookup"><span data-stu-id="6e445-108">This is demonstrated in the following example.</span></span>

``` syntax
#include "English.rc"
#pragma code_page(932)
#include "Japanese.rc"
```

<span data-ttu-id="6e445-109">如需 CodePageNum 的值清單，請參閱 [字碼頁識別碼](../intl/code-page-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="6e445-109">For a list of values for CodePageNum, see [Code Page Identifiers](../intl/code-page-identifiers.md).</span></span>

 

 