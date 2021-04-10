---
title: Microsoft RPC Binding-Handle 擴充功能
description: IDL 語言的 Microsoft 擴充功能支援多個控制碼參數，這些參數會出現在第一個、最左邊的參數以外的位置。
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104024239"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="a8f1f-103">Microsoft RPC Binding-Handle 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a8f1f-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="a8f1f-104">IDL 語言的 Microsoft 擴充功能支援多個控制碼參數，這些參數會出現在第一個、最左邊的參數以外的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="a8f1f-105">下列步驟描述 MIDL 編譯器在 DCE 相容性模式中解析系結控制碼參數的順序 (/**憑證**) ，以及預設 (Microsoft 延伸的) 模式。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="a8f1f-106">DCE 相容模式</span><span class="sxs-lookup"><span data-stu-id="a8f1f-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="a8f1f-107">出現在第一個位置的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="a8f1f-108">\[[**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)參數 [**的最左邊**](/windows/desktop/Midl/in) \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="a8f1f-109">\[[**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)所指定的隱含系結控制碼 \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="a8f1f-110">如果沒有 ACF 存在，則預設為使用 \[ **auto \_ 控制碼** \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="a8f1f-111">預設模式</span><span class="sxs-lookup"><span data-stu-id="a8f1f-111">Default mode</span></span>

-   <span data-ttu-id="a8f1f-112">最左邊的明確系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="a8f1f-113">\[[**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)所指定的隱含系結控制碼 \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="a8f1f-114">如果沒有 ACF 存在，則預設為使用 \[ [**auto \_ 控制碼**](/windows/desktop/Midl/auto-handle) \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a8f1f-115">DCE IDL 編譯器會尋找明確的系結控制碼做為第一個參數。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="a8f1f-116">當第一個參數不是系結控制碼，且指定了一個或多個內容控制碼時，會使用最左邊的內容控制碼作為系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="a8f1f-117">當第一個參數不是控制碼，而且沒有內容控制碼時，程式會使用 ACF 屬性 \[ [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)來使用隱含系結 \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a8f1f-118">IDL 的 Microsoft 擴充功能允許系結控制碼位於第一個參數以外的位置。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="a8f1f-119">\[ [](/windows/desktop/Midl/in) \] 明確控制碼參數中最左邊的參數（不論是基本、程式設計人員定義或內容控制碼）是系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="a8f1f-120">如果沒有控制碼參數，程式會使用 ACF 屬性 \[ [**隱含 \_ 控制碼**](/windows/desktop/Midl/implicit-handle) \] 或 \[ [**自動 \_ 控制碼**](/windows/desktop/Midl/auto-handle)來使用隱含系結 \] 。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="a8f1f-121">下列規則適用于 DCE 相容性 (/osf) 模式和預設模式：</span><span class="sxs-lookup"><span data-stu-id="a8f1f-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="a8f1f-122">當沒有 ACF 存在時，會使用自動控制碼系結。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="a8f1f-123">明確 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**， [](/windows/desktop/Midl/out-idl) \] 個別函式的 out 控制碼會優先採用針對介面指定的任何隱含系結。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="a8f1f-124">不支援多個 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**、out \] 基本控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="a8f1f-125">中有多個 \[ [**in**](/windows/desktop/Midl/in) \] 或 \[ **in**， \] 可使用 out 明確的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="a8f1f-126">所有程式設計師定義的控制碼參數（系結控制碼參數除外）都會被視為 transmissible 資料。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="a8f1f-127">下表包含範例，並說明如何在每個編譯器模式中指派系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8f1f-128">範例</span><span class="sxs-lookup"><span data-stu-id="a8f1f-128">Example</span></span></th>
<th><span data-ttu-id="a8f1f-129">描述</span><span class="sxs-lookup"><span data-stu-id="a8f1f-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="a8f1f-130">未指定明確的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-130">No explicit handle is specified.</span></span> <span data-ttu-id="a8f1f-131">使用 [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] 或 [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>] 所指定的隱含系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="a8f1f-132">如果沒有 ACF 存在，則會使用自動控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="a8f1f-133">已指定 handle_t 類型的明確控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="a8f1f-134">參數 <em>H</em> 是程式的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="a8f1f-135">第一個參數不是控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-135">The first parameter is not a handle.</span></span> <span data-ttu-id="a8f1f-136">在預設模式中，最左邊的控制碼參數 <em>H</em>為系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="a8f1f-137">在/osf 模式中，會使用隱含系結。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="a8f1f-138">系統會報告錯誤，因為第二個參數應為 transmissible，而且 handle_t 無法傳輸。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="a8f1f-139">第一個參數不是控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-139">The first parameter is not a handle.</span></span> <span data-ttu-id="a8f1f-140">在預設模式中，最左邊的控制碼參數 <em>H</em>為系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="a8f1f-141">存根會呼叫使用者提供的常式 MY_HDL_bind 和 MY_HDL_unbind。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="a8f1f-142">在/憑證模式中，會使用隱含系結。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="a8f1f-143">程式設計師定義的控制碼參數 <em>H</em> 會視為 transmissible 資料。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="a8f1f-144">第一個參數是系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="a8f1f-145">參數 <em>H</em> 是系結控制碼參數。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="a8f1f-146">第二個程式設計師定義的控制碼參數會被視為 transmissible 資料。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="a8f1f-147">系結控制碼是一個內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-147">The binding handle is a context handle.</span></span> <span data-ttu-id="a8f1f-148">參數 <em>H</em> 是系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="a8f1f-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 