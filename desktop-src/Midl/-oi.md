---
title: /Oi 參數
description: /Oi 和/Oic 參數會將 MIDL 編譯器導向，以使用完整解讀的封送處理方法。 /Oicf 參數可提供額外的效能增強功能。
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi 參數 MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185614"
---
# <a name="oi-switch"></a><span data-ttu-id="f8824-105">/Oi 參數</span><span class="sxs-lookup"><span data-stu-id="f8824-105">/Oi switch</span></span>

<span data-ttu-id="f8824-106">**/Oi** 和 **/Oic** 參數會將 MIDL 編譯器導向，以使用完整解讀的封送處理方法。</span><span class="sxs-lookup"><span data-stu-id="f8824-106">The **/Oi** and **/Oic** switches direct the MIDL compiler to use a fully-interpreted marshaling method.</span></span> <span data-ttu-id="f8824-107">**/Oicf** 參數可提供額外的效能增強功能。</span><span class="sxs-lookup"><span data-stu-id="f8824-107">The **/Oicf** switch provides additional performance enhancements.</span></span>

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a><span data-ttu-id="f8824-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="f8824-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="f8824-109">*Oi*</span><span class="sxs-lookup"><span data-stu-id="f8824-109">*Oi*</span></span> 
</dt> <dd>

<span data-ttu-id="f8824-110">針對在用戶端與伺服器之間傳遞的 stub 程式碼，指定完整解釋的方法。</span><span class="sxs-lookup"><span data-stu-id="f8824-110">Specifies the fully-interpreted method for marshaling stub code passed between client and server.</span></span>

> [!Note]  
> <span data-ttu-id="f8824-111">此參數已淘汰。</span><span class="sxs-lookup"><span data-stu-id="f8824-111">This switch is obsolete.</span></span> <span data-ttu-id="f8824-112">建議您在其位置使用 **/Oicf** 參數。</span><span class="sxs-lookup"><span data-stu-id="f8824-112">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8824-113">*Oic*</span><span class="sxs-lookup"><span data-stu-id="f8824-113">*Oic*</span></span> 
</dt> <dd>

<span data-ttu-id="f8824-114">指定封送處理的無程式碼 proxy 方法，提供 **/Oi** 的所有功能，同時也可進一步減少物件介面的用戶端 stub 程式碼大小。</span><span class="sxs-lookup"><span data-stu-id="f8824-114">Specifies the codeless proxy method of marshaling that provides all the features of **/Oi** and also further reduces the size of the client stub code for object interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="f8824-115">此參數已淘汰。</span><span class="sxs-lookup"><span data-stu-id="f8824-115">This switch is obsolete.</span></span> <span data-ttu-id="f8824-116">建議您在其位置使用 **/Oicf** 參數。</span><span class="sxs-lookup"><span data-stu-id="f8824-116">It is recommended that the **/Oicf** switch be used in its place.</span></span>

 

</dd> <dt>

<span data-ttu-id="f8824-117">*Oif 或 Oicf*</span><span class="sxs-lookup"><span data-stu-id="f8824-117">*Oif or Oicf*</span></span> 
</dt> <dd>

<span data-ttu-id="f8824-118">指定封送處理的無程式碼 proxy 方法，其中包含 **/Oi** 和 **/Oic** 提供的所有功能，但使用新的解譯器 (快速格式字串，) 提供比 **/Oi** 或 **/Oic** 更好的效能。</span><span class="sxs-lookup"><span data-stu-id="f8824-118">Specifies the codeless proxy method of marshaling that includes all the features provided by **/Oi** and **/Oic** but uses a new interpreter (fast format strings) that provides better performance than **/Oi** or **/Oic**.</span></span> <span data-ttu-id="f8824-119">此參數包含最近的 RPC 增強功能，建議用於新式 RPC 案例。</span><span class="sxs-lookup"><span data-stu-id="f8824-119">This switch includes recent RPC enhancements and is recommended for modern RPC scenarios.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8824-120">備註</span><span class="sxs-lookup"><span data-stu-id="f8824-120">Remarks</span></span>

<span data-ttu-id="f8824-121">請注意與支援平臺相關的限制。</span><span class="sxs-lookup"><span data-stu-id="f8824-121">Please note the restrictions related to supporting platforms.</span></span>

<span data-ttu-id="f8824-122">MIDL 3.0 編譯器提供兩種方法來封送處理常式代碼：完全解讀的 ( **/Oi**、 **/Oic** 和 **/Oicf**) 和混合模式 ( [**/os**](-os.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f8824-122">The MIDL 3.0 compiler provides two methods for marshaling code: fully-interpreted ( **/Oi**, **/Oic** and **/Oicf**) and mixed-mode ( [**/Os**](-os.md)).</span></span> <span data-ttu-id="f8824-123">從 MIDL 版本6.0.359 開始，MIDL 編譯器預設會產生 **/Oicf** 的  [**/robust**](-robust.md) 存根。</span><span class="sxs-lookup"><span data-stu-id="f8824-123">Starting with MIDL version 6.0.359, the MIDL compiler generates **/Oicf** Â  [**/robust**](-robust.md) stubs by default.</span></span> <span data-ttu-id="f8824-124">某些模式不支援某些語言功能。</span><span class="sxs-lookup"><span data-stu-id="f8824-124">Some language features are not supported in some modes.</span></span> <span data-ttu-id="f8824-125">在此情況下，編譯器會自動切換至適當的模式，併發出警告。</span><span class="sxs-lookup"><span data-stu-id="f8824-125">In this case, the compiler automatically switches to the appropriate mode and issues a warning.</span></span>

<span data-ttu-id="f8824-126">如果有問題，混合模式 ( [**/os**](-os.md)) 方法可能是最好的方法。</span><span class="sxs-lookup"><span data-stu-id="f8824-126">If performance is a concern, the mixed-mode ( [**/Os**](-os.md)) method can be the best approach.</span></span> <span data-ttu-id="f8824-127">在此模式中，編譯器會選擇封送處理產生的存根中內嵌的一些參數。</span><span class="sxs-lookup"><span data-stu-id="f8824-127">In this mode, the compiler chooses to marshal some parameters inline in the generated stubs.</span></span> <span data-ttu-id="f8824-128">雖然這會產生較大的存根大小，但它可提供更高的效能。</span><span class="sxs-lookup"><span data-stu-id="f8824-128">While this results in larger stub size, it offers increased performance.</span></span>

<span data-ttu-id="f8824-129">完全解讀的方法會完全離線地封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="f8824-129">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="f8824-130">這可大幅減少存根程式碼的大小，但會導致效能降低。</span><span class="sxs-lookup"><span data-stu-id="f8824-130">This considerably reduces the size of the stub code, but results in decreased performance.</span></span> <span data-ttu-id="f8824-131">此外，使用完整解釋的方法時，每個程式都有16個參數的限制。</span><span class="sxs-lookup"><span data-stu-id="f8824-131">Also, with the fully-interpreted method, there is a limit of 16 parameters for each procedure.</span></span> <span data-ttu-id="f8824-132">任何包含16個以上參數的程式，將會自動以 [**/os**](-os.md) 模式處理。</span><span class="sxs-lookup"><span data-stu-id="f8824-132">Any procedure containing more than 16 parameters will automatically be processed in [**/Os**](-os.md) mode.</span></span> <span data-ttu-id="f8824-133">**/Oicf** 可提供最佳的效能，而 **/Oi** 則提供最佳的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="f8824-133">Among the interpreted modes, **/Oicf** offers the best performance and **/Oi** offers the best backward compatibility.</span></span>

<span data-ttu-id="f8824-134">如果您的應用程式使用 midl 3.0 所引進的 midl 功能（例如， \[ [**網路 \_ 封送**](wire-marshal.md)處理 \] 和 \[ [**使用者 \_ 封送**](user-marshal.md)處理屬性），您可能會想要使用/Oif 選項 \] 。</span><span class="sxs-lookup"><span data-stu-id="f8824-134">You may want to use the **/Oif** option if your application uses MIDL features that were introduced with MIDL 3.0, such as the \[[**wire\_marshal**](wire-marshal.md)\] and \[[**user\_marshal**](user-marshal.md)\] attributes.</span></span> <span data-ttu-id="f8824-135">如果您的應用程式使用 [管道](/windows/desktop/Rpc/pipes) ，則必須使用 **/Oif** 選項;如果您指定另一個模式，MIDL 編譯器將切換至 **/Oif**。</span><span class="sxs-lookup"><span data-stu-id="f8824-135">If your application uses [pipes](/windows/desktop/Rpc/pipes) you must use the **/Oif** option; if you specify another mode, the MIDL compiler will switch to **/Oif**.</span></span>

<span data-ttu-id="f8824-136">為了微調存根程式碼的封送處理方式，Microsoft RPC 提供 ACF \[ [**optimize**](optimize.md) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="f8824-136">To fine-tune the way your stub code is marshaled, Microsoft RPC provides an ACF \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="f8824-137">這個屬性是用來做為介面屬性或 operation 屬性，以選取個別介面或個別作業的封送處理模式。</span><span class="sxs-lookup"><span data-stu-id="f8824-137">This attribute is used as an interface attribute or operation attribute to select the marshaling mode for individual interfaces or for individual operations.</span></span>

### <a name="calling-conventions"></a><span data-ttu-id="f8824-138">呼叫慣例</span><span class="sxs-lookup"><span data-stu-id="f8824-138">Calling Conventions</span></span>

<span data-ttu-id="f8824-139">在使用 **/Oi**、 **/Oic** 或 **/Oif** 參數的解讀方法中，MIDL 編譯器所產生的存根，在 C 編譯期間必須編譯為 stdcall 或 cdecl 程式。</span><span class="sxs-lookup"><span data-stu-id="f8824-139">Stubs generated by the MIDL compiler in the interpreted method using the **/Oi**, **/Oic**, or **/Oif** switches must be compiled as either a stdcall or a cdecl procedure during the C compilation.</span></span> <span data-ttu-id="f8824-140">PASCAL 或 Fastcall 呼叫慣例將無法運作。</span><span class="sxs-lookup"><span data-stu-id="f8824-140">A PASCAL or Fastcall calling convention will not work.</span></span> <span data-ttu-id="f8824-141">此外，伺服器 stub 必須編譯為 stdcall。</span><span class="sxs-lookup"><span data-stu-id="f8824-141">Additionally, the server stub must be compiled as stdcall.</span></span>

## <a name="examples"></a><span data-ttu-id="f8824-142">範例</span><span class="sxs-lookup"><span data-stu-id="f8824-142">Examples</span></span>

<span data-ttu-id="f8824-143">**midl/Oi 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="f8824-143">**midl /Oi filename.idl**</span></span>

<span data-ttu-id="f8824-144">**midl/Oic 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="f8824-144">**midl /Oic filename.idl**</span></span>

<span data-ttu-id="f8824-145">**midl/Oif 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="f8824-145">**midl /Oif filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f8824-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8824-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8824-147">**/robust**</span><span class="sxs-lookup"><span data-stu-id="f8824-147">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="f8824-148">**/no \_ 健全**</span><span class="sxs-lookup"><span data-stu-id="f8824-148">**/no\_robust**</span></span>](-no-robust.md)
</dt> <dt>

[<span data-ttu-id="f8824-149">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="f8824-149">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f8824-150">**/Os**</span><span class="sxs-lookup"><span data-stu-id="f8824-150">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="f8824-151">**優化**</span><span class="sxs-lookup"><span data-stu-id="f8824-151">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="f8824-152">**/no \_ 格式 \_ 選擇**</span><span class="sxs-lookup"><span data-stu-id="f8824-152">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 