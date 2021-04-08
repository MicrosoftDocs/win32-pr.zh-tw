---
title: /osf 參數
description: /Osf 交換器會強制與憑證 DCE 具有嚴格的相容性。
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- /osf 參數 MIDL
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2936401d59bb8c2c2bcfdcffce27ba9ed978d506
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023361"
---
# <a name="osf-switch"></a><span data-ttu-id="edbdf-104">/osf 參數</span><span class="sxs-lookup"><span data-stu-id="edbdf-104">/osf switch</span></span>

<span data-ttu-id="edbdf-105">**/Osf** 交換器會強制與憑證 DCE 具有嚴格的相容性。</span><span class="sxs-lookup"><span data-stu-id="edbdf-105">The **/osf** switch forces strict compatibility with OSF DCE.</span></span>

``` syntax
midl /osf
```

## <a name="switch-options"></a><span data-ttu-id="edbdf-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="edbdf-106">Switch Options</span></span>

<span data-ttu-id="edbdf-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="edbdf-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="edbdf-108">備註</span><span class="sxs-lookup"><span data-stu-id="edbdf-108">Remarks</span></span>

<span data-ttu-id="edbdf-109">如果您的應用程式需要與憑證 DCE 的嚴格相容性，以提供可攜性的原因。</span><span class="sxs-lookup"><span data-stu-id="edbdf-109">Use this switch if your application requires strict compatibility with OSF DCE for portability reasons.</span></span>

<span data-ttu-id="edbdf-110">在 **/osf** 模式中，當您使用完整指標、引數需要記憶體配置，或當您使用 [ [**啟用 \_ 配置**](enable-allocate.md) ] 屬性時，便會自動啟用 RpcSs 套件。</span><span class="sxs-lookup"><span data-stu-id="edbdf-110">In **/osf** mode, the RpcSs package is automatically enabled when you use full pointers, the arguments require memory allocation, or when you use the [**enable\_allocate**](enable-allocate.md) attribute.</span></span> <span data-ttu-id="edbdf-111">這表示您不需要在用戶端和伺服器應用程式中提供 [**midl \_ 使用者 \_ 配置**](/windows/desktop/Rpc/the-midl-user-allocate-function) 和 [**midl \_ 使用者 \_ 免費**](/windows/desktop/Rpc/the-midl-user-free-function) 函數。</span><span class="sxs-lookup"><span data-stu-id="edbdf-111">This means that you do not have to supply the [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) functions in your client and server application.</span></span>

<span data-ttu-id="edbdf-112">當您使用 **/osf** 參數進行編譯時，無法使用下列 Microsoft 擴充功能：</span><span class="sxs-lookup"><span data-stu-id="edbdf-112">The following Microsoft-extended features are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="edbdf-113">在 IDL 檔案中)  (未具名引數的抽象宣告子。</span><span class="sxs-lookup"><span data-stu-id="edbdf-113">Abstract declarators (unnamed parameters) in the IDL file.</span></span>
-   <span data-ttu-id="edbdf-114">COM 物件的介面定義。</span><span class="sxs-lookup"><span data-stu-id="edbdf-114">Interface definitions for COM objects.</span></span>
-   <span data-ttu-id="edbdf-115">具有超過17個字元的介面名稱。</span><span class="sxs-lookup"><span data-stu-id="edbdf-115">Interface names with more than 17 characters.</span></span>
-   <span data-ttu-id="edbdf-116">僅限 MIDL 屬性（例如， [**電傳 \_ 封送**](wire-marshal.md)處理、 [**使用者 \_ 封送**](user-marshal.md)處理和 typelib） (ODL) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="edbdf-116">MIDL-only attributes, such as [**wire\_marshal**](wire-marshal.md), [**user\_marshal**](user-marshal.md), and the typelib (ODL)extensions.</span></span>
-   <span data-ttu-id="edbdf-117">在 IDL 檔案中使用 ACF 關鍵字 (MIDL **/app \_ config** 選項) 。</span><span class="sxs-lookup"><span data-stu-id="edbdf-117">Using ACF keywords in an IDL file (the MIDL **/app\_config** option).</span></span>
-   <span data-ttu-id="edbdf-118">用戶端上的靜態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="edbdf-118">Static callback functions on the client.</span></span>
-   <span data-ttu-id="edbdf-119">[**Async**](async.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="edbdf-119">The [**async**](async.md) attribute.</span></span>
-   <span data-ttu-id="edbdf-120">[**.cpp \_ 引號**](cpp-quote.md)和 **\# pragma midl \_ echo**。</span><span class="sxs-lookup"><span data-stu-id="edbdf-120">[**cpp\_quote**](cpp-quote.md) and **\#pragma midl\_echo**.</span></span>
-   <span data-ttu-id="edbdf-121">[**wchar \_ t**](wchar-t.md) 寬字元類型、常數和字串。</span><span class="sxs-lookup"><span data-stu-id="edbdf-121">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings.</span></span>
-   <span data-ttu-id="edbdf-122">[**列舉**](enum.md) 初始化 (稀疏列舉值) 。</span><span class="sxs-lookup"><span data-stu-id="edbdf-122">[**enum**](enum.md) initialization (sparse enumerators).</span></span>
-   <span data-ttu-id="edbdf-123">僅限 [**輸出**](out-idl.md)大小的規格。</span><span class="sxs-lookup"><span data-stu-id="edbdf-123">[**out**](out-idl.md)-only size specification.</span></span>
-   <span data-ttu-id="edbdf-124">混合大小的指標和大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="edbdf-124">Mixed sized-pointers and sized arrays.</span></span>
-   <span data-ttu-id="edbdf-125">用於大小和鑒別子規范的運算式。</span><span class="sxs-lookup"><span data-stu-id="edbdf-125">Expressions used for size and discriminator specifiers.</span></span>
-   <span data-ttu-id="edbdf-126">引數清單中任何位置的明確控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="edbdf-126">Explicit handle parameters in any position in the argument list.</span></span> <span data-ttu-id="edbdf-127">在 **/osf** 模式中，MIDL 編譯器會尋找明確的系結控制碼做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="edbdf-127">In **/osf** mode, the MIDL compiler looks for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="edbdf-128">當第一個參數不是系結控制碼，且指定了一個或多個內容控制碼時，會使用最左邊的內容控制碼作為系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="edbdf-128">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="edbdf-129">當第一個參數不是控制碼，而且沒有內容控制碼時，程式會使用 ACF 屬性 [**隱含 \_ 控制碼**](implicit-handle.md) 或 [**自動 \_ 控制碼**](auto-handle.md)來使用隱含系結。</span><span class="sxs-lookup"><span data-stu-id="edbdf-129">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute [**implicit\_handle**](implicit-handle.md) or [**auto\_handle**](auto-handle.md).</span></span>
-   <span data-ttu-id="edbdf-130">指標屬性型別繼承。</span><span class="sxs-lookup"><span data-stu-id="edbdf-130">Pointer-attribute type inheritance.</span></span> <span data-ttu-id="edbdf-131">憑證 DCE 不允許未歸屬指標。</span><span class="sxs-lookup"><span data-stu-id="edbdf-131">OSF DCE does not allow unattributed pointers.</span></span> <span data-ttu-id="edbdf-132">因此，在 **/osf** 模式中，每個 IDL 檔案都必須定義其指標的屬性。</span><span class="sxs-lookup"><span data-stu-id="edbdf-132">Therefore, in **/osf** mode each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="edbdf-133">如果有任何指標沒有明確的屬性，則 IDL 檔案必須具有 [**指標 \_ 預設**](pointer-default.md) 規格，才能設定指標類型。</span><span class="sxs-lookup"><span data-stu-id="edbdf-133">If any pointer does not have an explicit attribute, the IDL file must have a [**pointer\_default**](pointer-default.md) specification to set the pointer type.</span></span>
-   <span data-ttu-id="edbdf-134">IDL 檔案中的多個介面。</span><span class="sxs-lookup"><span data-stu-id="edbdf-134">Multiple interfaces in an IDL file.</span></span>
-   <span data-ttu-id="edbdf-135">介面區塊外部的定義。</span><span class="sxs-lookup"><span data-stu-id="edbdf-135">Definitions outside of the interface block.</span></span>
-   <span data-ttu-id="edbdf-136">類型限定詞，例如 **遠** 和 **stdcall**。</span><span class="sxs-lookup"><span data-stu-id="edbdf-136">Type qualifiers such as **far** and **stdcall**.</span></span>
-   <span data-ttu-id="edbdf-137">省略方向屬性。</span><span class="sxs-lookup"><span data-stu-id="edbdf-137">Omitting directional attributes.</span></span>

<span data-ttu-id="edbdf-138">當您使用 **/osf** 參數編譯時，無法使用下列 C/c + + 語言延伸模組：</span><span class="sxs-lookup"><span data-stu-id="edbdf-138">The following C/C++ language extensions are not available when you compile with the **/osf** switch:</span></span>

-   <span data-ttu-id="edbdf-139">結構和等位中的位欄位。</span><span class="sxs-lookup"><span data-stu-id="edbdf-139">Bit fields in structures and unions.</span></span>
-   <span data-ttu-id="edbdf-140">以兩個斜線字元分隔的單行批註 (//) 。</span><span class="sxs-lookup"><span data-stu-id="edbdf-140">Single line comments delimited with two slash characters (//).</span></span>
-   <span data-ttu-id="edbdf-141">外部宣告。</span><span class="sxs-lookup"><span data-stu-id="edbdf-141">External declarations.</span></span>
-   <span data-ttu-id="edbdf-142">參數清單中有省略號的程式。</span><span class="sxs-lookup"><span data-stu-id="edbdf-142">Procedures with ellipses in the parameter list.</span></span>
-   <span data-ttu-id="edbdf-143">輸入 [**int**](int.md)。</span><span class="sxs-lookup"><span data-stu-id="edbdf-143">Type [**int**](int.md).</span></span>
-   <span data-ttu-id="edbdf-144">輸入 **void \*** (，但 [**內容 \_ 控制碼**](context-handle.md)屬性) 除外。</span><span class="sxs-lookup"><span data-stu-id="edbdf-144">Type **void \*** (except with the [**context\_handle**](context-handle.md) attribute).</span></span>
-   <span data-ttu-id="edbdf-145">類型限定詞，包括具有 ANSI 一致前置詞的表單，其中包含兩個底線字元： **\_ \_ cdecl**、 **cdecl**、 [**const**](const.md)、 **const**、 **\_ \_ export**、 **export**、 **\_ \_ far**、 **far**、 **\_ \_ loadds**、 **loadds**、 **\_ \_ near**、 **near**、 **\_ \_ pascal**、 **pascal**、 **\_ \_ stdcall**、 **stdcall**、 **\_ \_ volatile** 和 **volatile**。</span><span class="sxs-lookup"><span data-stu-id="edbdf-145">Type qualifiers, including the form with the ANSI-conformant prefix, contain two underscore characters: **\_\_cdecl**, **cdecl**, [**const**](const.md), **const**, **\_\_export**, **export**, **\_\_far**, **far**, **\_\_loadds**, **loadds**, **\_\_near**, **near**, **\_\_pascal**, **pascal**, **\_\_stdcall**, **stdcall**, **\_\_volatile**, and **volatile**.</span></span>
-   <span data-ttu-id="edbdf-146">任何 \# [**pragma**](pragma.md)警告或 **\# pragma** 批註。</span><span class="sxs-lookup"><span data-stu-id="edbdf-146">Any \# [**pragma**](pragma.md) warning or **\#pragma** comment.</span></span>
-   <span data-ttu-id="edbdf-147">類型序列化。</span><span class="sxs-lookup"><span data-stu-id="edbdf-147">Type serialization.</span></span>
-   <span data-ttu-id="edbdf-148">[**\_ \_ Int3264**](--int3264.md)資料類型。</span><span class="sxs-lookup"><span data-stu-id="edbdf-148">The [**\_\_int3264**](--int3264.md) data type.</span></span>
-   <span data-ttu-id="edbdf-149">[**/Protocol**](-protocol.md)參數和 ndr64 傳輸語法。</span><span class="sxs-lookup"><span data-stu-id="edbdf-149">The [**/protocol**](-protocol.md) switch, and ndr64 transfer syntax.</span></span>

## <a name="examples"></a><span data-ttu-id="edbdf-150">範例</span><span class="sxs-lookup"><span data-stu-id="edbdf-150">Examples</span></span>

<span data-ttu-id="edbdf-151">**midl/osf 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="edbdf-151">**midl /osf filename.idl**</span></span>

<span data-ttu-id="edbdf-152">**midl/osf/app \_ config 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="edbdf-152">**midl /osf /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="edbdf-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edbdf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbdf-154">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="edbdf-154">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="edbdf-155">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="edbdf-155">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="edbdf-156">**/ms \_ ext**</span><span class="sxs-lookup"><span data-stu-id="edbdf-156">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="edbdf-157">Rpcss 記憶體管理套件</span><span class="sxs-lookup"><span data-stu-id="edbdf-157">Rpcss Memory Management Package</span></span>](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 