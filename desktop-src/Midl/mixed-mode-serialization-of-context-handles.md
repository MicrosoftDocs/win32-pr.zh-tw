---
title: 內容控制碼的混合模式序列化
description: 在 Microsoft Windows XP 中，單一介面可以容納序列化和非序列化的內容控制碼，也就是所謂的混合模式序列化。
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL 語言參考 MIDL，內容控制碼的混合模式序列化
- 內容控制碼 MIDL
- 混合模式序列化 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839960"
---
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="1458a-106">內容控制碼的混合模式序列化</span><span class="sxs-lookup"><span data-stu-id="1458a-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="1458a-107">從 Windows XP 開始，單一介面可以容納序列化和非序列化的內容控制碼，在介面上啟用一種方法，以獨佔方式存取內容控制碼 (序列化) ，而其他方法則會在共用模式中存取該內容控制碼 (非序列化) 。</span><span class="sxs-lookup"><span data-stu-id="1458a-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="1458a-108">如需內容控制碼的詳細資訊，請參閱下列屬性：</span><span class="sxs-lookup"><span data-stu-id="1458a-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="1458a-109">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="1458a-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="1458a-110">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="1458a-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="1458a-111">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="1458a-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="1458a-112">序列化和共用模式存取功能相當於讀取/寫入鎖定機制;使用序列化內容控制碼的方法是 (寫入器) 的專屬使用者，而使用非序列化內容控制碼的方法則是 (讀取器) 的共用使用者。</span><span class="sxs-lookup"><span data-stu-id="1458a-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="1458a-113">損毀或修改內容控制碼狀態的方法必須序列化。</span><span class="sxs-lookup"><span data-stu-id="1458a-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="1458a-114">未修改內容控制碼狀態的方法（例如直接從內容控制碼讀取的方法）可以是非序列化的。</span><span class="sxs-lookup"><span data-stu-id="1458a-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="1458a-115">在混合模式中使用內容控制碼，可大幅改善伺服器的擴充性，特別是當多個執行緒同時呼叫相同的內容控制碼時。</span><span class="sxs-lookup"><span data-stu-id="1458a-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="1458a-116">RPC 不會在共用模式中使用內容控制碼在方法上強制執行「寫入鎖定」，這表示應用程式必須確保不會修改共用模式內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="1458a-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="1458a-117">修改共用模式所使用的內容控制碼可能會導致內容控制碼內容的微妙損毀，而這種情況可能無法進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="1458a-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="1458a-118">變更內容控制碼的序列化邏輯只會影響伺服器。</span><span class="sxs-lookup"><span data-stu-id="1458a-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="1458a-119">此外，變更內容控制碼的序列化邏輯並不會影響電傳格式，因此，對伺服器上序列化邏輯的變更不會影響現有用戶端與伺服器互動的功能。</span><span class="sxs-lookup"><span data-stu-id="1458a-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="1458a-120">不建議只使用非序列化的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="1458a-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="1458a-121">使用非序列化控制碼的伺服器應該針對關閉內容控制碼的方法切換至序列化存取。</span><span class="sxs-lookup"><span data-stu-id="1458a-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="1458a-122">僅限輸出的內容控制碼 \[ \] 通常會由建立方法使用，且不需要任何序列化。</span><span class="sxs-lookup"><span data-stu-id="1458a-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="1458a-123">因此， \[ \] RPC 會忽略套用至僅限輸出內容控制碼（例如 [**內容 \_ 控制碼 \_ 序列化**](context-handle-serialize.md) 或 [**內容 \_ 控制碼 \_ noserialize**](context-handle-noserialize.md)）的任何序列化屬性。</span><span class="sxs-lookup"><span data-stu-id="1458a-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="1458a-124">建立方法會以隱含方式序列化。</span><span class="sxs-lookup"><span data-stu-id="1458a-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1458a-125">範例</span><span class="sxs-lookup"><span data-stu-id="1458a-125">Examples</span></span>

<span data-ttu-id="1458a-126">下列兩個範例示範如何啟用內容控制碼的混合模式序列化。</span><span class="sxs-lookup"><span data-stu-id="1458a-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="1458a-127">第一個範例顯示如何在 IDL 檔案中執行此動作：</span><span class="sxs-lookup"><span data-stu-id="1458a-127">The first example shows how to do so in the IDL file:</span></span>

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

<span data-ttu-id="1458a-128">第二個範例顯示如何在 ACF 檔中啟用內容控制碼的混合模式序列化：</span><span class="sxs-lookup"><span data-stu-id="1458a-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="1458a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="1458a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1458a-130">**內容 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="1458a-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="1458a-131">**內容 \_ 控制碼 \_ 序列化**</span><span class="sxs-lookup"><span data-stu-id="1458a-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="1458a-132">**內容 \_ 控制碼 \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="1458a-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




