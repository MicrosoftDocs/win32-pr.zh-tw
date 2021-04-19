---
title: /c_ext 參數
description: 此參數已從 MIDL 編譯器的3.0 版淘汰。 不過，使用 c \_ ext 參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對/ms \_ ext 或/c \_ ext 的參考。
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext switch MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967232"
---
# <a name="c_ext-switch"></a><span data-ttu-id="3c89a-105">/c \_ ext 參數</span><span class="sxs-lookup"><span data-stu-id="3c89a-105">/c\_ext switch</span></span>

<span data-ttu-id="3c89a-106">此參數已從 MIDL 編譯器的3.0 版淘汰。</span><span class="sxs-lookup"><span data-stu-id="3c89a-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="3c89a-107">不過，使用 **c \_ ext** 參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對 [**/ms \_ ext**](-ms-ext.md) 或 **/c \_ ext** 的參考。</span><span class="sxs-lookup"><span data-stu-id="3c89a-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="3c89a-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="3c89a-108">Switch Options</span></span>

<span data-ttu-id="3c89a-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3c89a-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c89a-110">備註</span><span class="sxs-lookup"><span data-stu-id="3c89a-110">Remarks</span></span>

<span data-ttu-id="3c89a-111">下列功能現在預設為可用：</span><span class="sxs-lookup"><span data-stu-id="3c89a-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="3c89a-112">許多現有的標頭檔會使用不屬於 DCE IDL 的限定詞來定義具有辨識符號的類型，例如 **遠** 和 **stdcall**。</span><span class="sxs-lookup"><span data-stu-id="3c89a-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="3c89a-113">這些編譯器 (，而在 DCE 相容性模式中，MIDL 編譯器) 在嘗試處理這些限定詞時產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c89a-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="3c89a-114">MIDL 編譯器可讓您編譯包含這些限定詞的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c89a-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="3c89a-115">類型限定詞不會影響資料在網路上的傳輸方式。</span><span class="sxs-lookup"><span data-stu-id="3c89a-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="3c89a-116">您可以省略方向屬性，例如 [**\[ in \]**](in.md)或 [**\[ out \]**](out-idl.md)。</span><span class="sxs-lookup"><span data-stu-id="3c89a-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="3c89a-117">預設模式支援下列 C 語言延伸模組：</span><span class="sxs-lookup"><span data-stu-id="3c89a-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="3c89a-118">結構和等位中的位欄位</span><span class="sxs-lookup"><span data-stu-id="3c89a-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="3c89a-119">以兩個斜線字元開頭的批註 (//) </span><span class="sxs-lookup"><span data-stu-id="3c89a-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="3c89a-120">外部宣告</span><span class="sxs-lookup"><span data-stu-id="3c89a-120">External declarations</span></span>
-   <span data-ttu-id="3c89a-121">參數清單中有省略號的程式 ( ... ) </span><span class="sxs-lookup"><span data-stu-id="3c89a-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="3c89a-122">在32位平臺上， [**int**](int.md) 是原生32位基底類型;在16位平臺上，可辨識 **int** 但不是可遠端處理的類型</span><span class="sxs-lookup"><span data-stu-id="3c89a-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="3c89a-123">未在遠端作業中使用的類型 [**void \***](void.md)</span><span class="sxs-lookup"><span data-stu-id="3c89a-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="3c89a-124">類型限定詞（包括具有 ANSI 一致前置詞的表單）包含兩個底線字元 **： cdecl**、 **\_ \_ cdecl**、 [**const**](const.md)、 **\_ \_ const**、 **export**、 **\_ \_ export**、 **far**、 **\_ \_ far**、 **loadds**、 **\_ \_ loadds**、 **near**、 **\_ \_ near**、 **pascal**、 **\_ \_ pascal**、 **stdcall**、 **\_ \_ stdcall**、 **volatile** 和 **\_ \_ volatile**。</span><span class="sxs-lookup"><span data-stu-id="3c89a-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="3c89a-125">如需宣告限定詞的詳細資訊，請參閱 Microsoft C/c + + 檔。</span><span class="sxs-lookup"><span data-stu-id="3c89a-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c89a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c89a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c89a-127">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="3c89a-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="3c89a-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="3c89a-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="3c89a-129">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="3c89a-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




