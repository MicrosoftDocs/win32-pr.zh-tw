---
title: /ms_ext 參數
description: 自 MIDL 3.0 版起，ms ext 參數所啟用的功能 \_ 現在是 midl 編譯器的預設模式。
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext switch MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023332"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="28774-104">/ms \_ ext 參數</span><span class="sxs-lookup"><span data-stu-id="28774-104">/ms\_ext switch</span></span>

<span data-ttu-id="28774-105">自 MIDL 3.0 版起， **ms \_ ext** 參數所啟用的功能現在是 midl 編譯器的預設模式。</span><span class="sxs-lookup"><span data-stu-id="28774-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="28774-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="28774-106">Switch Options</span></span>

<span data-ttu-id="28774-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="28774-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="28774-108">備註</span><span class="sxs-lookup"><span data-stu-id="28774-108">Remarks</span></span>

<span data-ttu-id="28774-109">使用參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對 **/ms \_ ext** 或 [**/c \_ ext**](-c-ext.md) 的參考。</span><span class="sxs-lookup"><span data-stu-id="28774-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="28774-110">下列適用于憑證 DCE 的 Microsoft 擴充功能現在預設為可用：</span><span class="sxs-lookup"><span data-stu-id="28774-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="28774-111">OLE 物件的介面定義。</span><span class="sxs-lookup"><span data-stu-id="28774-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="28774-112">如需針對 OLE 介面產生之檔案的詳細資訊，請參閱[針對 COM 介面產生](files-generated-for-a-com-interface.md)的檔案。</span><span class="sxs-lookup"><span data-stu-id="28774-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="28774-113">在用戶端上指定靜態回呼函數的 [**\[ 回呼 \]**](callback.md)屬性</span><span class="sxs-lookup"><span data-stu-id="28774-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="28774-114"> (加上 *引號的 \_ 字串*) 和 [**\# pragma midl \_ echo**](pragma.md)的 [**cpp \_ 引號**](cpp-quote.md)</span><span class="sxs-lookup"><span data-stu-id="28774-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="28774-115">[**wchar \_ t**](wchar-t.md) 寬字元類型、常數和字串</span><span class="sxs-lookup"><span data-stu-id="28774-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="28774-116"> (稀疏枚舉器的 [**列舉初始化**](enum.md)) </span><span class="sxs-lookup"><span data-stu-id="28774-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="28774-117">作為大小和鑒別子規范的運算式</span><span class="sxs-lookup"><span data-stu-id="28774-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="28774-118">處理延伸模組</span><span class="sxs-lookup"><span data-stu-id="28774-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="28774-119">指標屬性類型繼承</span><span class="sxs-lookup"><span data-stu-id="28774-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="28774-120">多個介面</span><span class="sxs-lookup"><span data-stu-id="28774-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="28774-121">介面區塊外部的定義</span><span class="sxs-lookup"><span data-stu-id="28774-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="28774-122">您可以省略 [](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**中的**](in.md)方向屬性 [](out-idl.md) ，放大\]</span><span class="sxs-lookup"><span data-stu-id="28774-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="28774-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28774-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28774-124">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="28774-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="28774-125">指標屬性類型繼承</span><span class="sxs-lookup"><span data-stu-id="28774-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="28774-126">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="28774-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="28774-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="28774-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 