---
title: ACF 主體
description: ACF 主體包含設定屬性，適用于在 IDL 檔案的介面主體中定義的類型和函式。
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104024241"
---
# <a name="the-acf-body"></a><span data-ttu-id="ccfb5-103">ACF 主體</span><span class="sxs-lookup"><span data-stu-id="ccfb5-103">The ACF Body</span></span>

<span data-ttu-id="ccfb5-104">ACF 主體包含設定屬性，適用于在 IDL 檔案的介面主體中定義的類型和函式。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="ccfb5-105">ACF 的主體可以是空的，也可以包含 ACF [**include**](/windows/desktop/Midl/include)、 [**typedef**](/windows/desktop/Midl/typedef)、function 和 parameter 屬性。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="ccfb5-106">所有這些專案都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-106">All of these items are optional.</span></span> <span data-ttu-id="ccfb5-107">套用至 ACF 主體中個別類型和函式的屬性會覆寫 ACF 標頭中的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="ccfb5-108">ACF 會指定本機電腦上的行為，而且不會影響透過網路傳輸的資料。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="ccfb5-109">它是用來指定要產生的存根詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="ccfb5-110">在 DCE 相容性模式中 ([**/osf**](/windows/desktop/Midl/-osf)) ，此 ACF 不會影響存根之間的互動，而是在存根和應用程式程式碼之間的互動。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="ccfb5-111">在 ACF 中指定的參數必須是 IDL 檔案中指定的其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="ccfb5-112">ACF 中參數的規格順序並不重要，因為比對是依名稱，而不是依位置。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="ccfb5-113">ACF 中的參數清單可以是空的，即使對應的 IDL 簽章中的參數清單不 (，但) 不建議這樣做。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="ccfb5-114">在 IDL 檔案中)  (未具名引數的抽象宣告子，會導致 MIDL 編譯器在處理 ACF 時發生錯誤，因為找不到參數。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="ccfb5-115">ACF **include** 指示詞會指定在產生的標頭中顯示的標頭檔，作為標準 C 預處理器 **\# include** 語句的一部分。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="ccfb5-116">ACF 關鍵字 **包含** 不同于 **\# include** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="ccfb5-117">ACF 關鍵字 **包含** 會導致程式程式碼 "**\# include** *filename*" 出現在產生的標頭檔中，而 C 語言指示詞 "**\# include** *FILENAME*" 則會將該檔案的內容放在 ACF 中。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="ccfb5-118">ACF [**typedef**](/windows/desktop/Midl/typedef) 語句可讓您將 ACF 類型屬性套用至 IDL 檔案中先前定義的類型。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="ccfb5-119">ACF **typedef** 語法與 C **typedef** 語法不同。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="ccfb5-120">ACF 函數屬性可讓您指定套用至整個函數的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="ccfb5-121">如需詳細資訊，請參閱程式 **\[** [**代碼**](/windows/desktop/Midl/code) **\]** 、 **\[** [**優化**](/windows/desktop/Midl/optimize) **\]** 和 **\[** [**了 nocode**](/windows/desktop/Midl/nocode) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="ccfb5-122">ACF 參數屬性可讓您指定套用至函數之個別參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="ccfb5-123">如需詳細資訊，請參閱 **\[** [**位元組 \_ 計數**](/windows/desktop/Midl/byte-count) **\]** 。</span><span class="sxs-lookup"><span data-stu-id="ccfb5-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccfb5-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccfb5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfb5-125">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="ccfb5-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="ccfb5-127">[**\[自動 \_ 處理\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="ccfb5-128">[**\[代碼\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="ccfb5-129">[**\[明確 \_ 控制碼\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ccfb5-130">介面定義語言 (IDL) 檔</span><span class="sxs-lookup"><span data-stu-id="ccfb5-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="ccfb5-131">[**\[隱含 \_ 控制碼\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ccfb5-132">**包括**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="ccfb5-133">midl</span><span class="sxs-lookup"><span data-stu-id="ccfb5-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="ccfb5-134">[**\[了 nocode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="ccfb5-135">[**\[優化\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="ccfb5-136">[**\[表示 \_ 為\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="ccfb5-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ccfb5-137">**著**</span><span class="sxs-lookup"><span data-stu-id="ccfb5-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 