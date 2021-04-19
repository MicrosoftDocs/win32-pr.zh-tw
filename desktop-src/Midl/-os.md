---
title: /Os 參數
description: /Os 參數會指定混合模式方法，以封送處理在用戶端與伺服器之間傳遞的存根程式碼。
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /Os 參數 MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967860"
---
# <a name="os-switch"></a><span data-ttu-id="0919a-104">/Os 參數</span><span class="sxs-lookup"><span data-stu-id="0919a-104">/Os switch</span></span>

<span data-ttu-id="0919a-105">**/Os** 參數會指定混合模式方法，以封送處理在用戶端與伺服器之間傳遞的存根程式碼。</span><span class="sxs-lookup"><span data-stu-id="0919a-105">The **/Os** switch specifies the mixed-mode method to marshal stub code passed between client and server.</span></span>

``` syntax
midl /Os
```

## <a name="switch-options"></a><span data-ttu-id="0919a-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="0919a-106">Switch Options</span></span>

<span data-ttu-id="0919a-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0919a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0919a-108">備註</span><span class="sxs-lookup"><span data-stu-id="0919a-108">Remarks</span></span>

<span data-ttu-id="0919a-109">在決定封送處理常式代碼的方法之前，必須考慮一些重要的問題。</span><span class="sxs-lookup"><span data-stu-id="0919a-109">There are important issues to consider before deciding on the method for marshaling code.</span></span> <span data-ttu-id="0919a-110">這些問題的大小和效能都有問題。</span><span class="sxs-lookup"><span data-stu-id="0919a-110">These issues concern size and performance.</span></span> <span data-ttu-id="0919a-111">MIDL 編譯器提供兩種方法來封送處理常式代碼：混合模式 (**/os**) 和完整解釋 ([**/Oi**](-oi.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0919a-111">The MIDL compiler provides two methods for marshaling code: mixed-mode (**/Os**) and fully-interpreted ([**/Oi**](-oi.md)).</span></span> <span data-ttu-id="0919a-112">完全解讀的方法會完全離線地封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="0919a-112">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="0919a-113">這會大幅減少存根程式碼的大小，但它也會導致效能降低。</span><span class="sxs-lookup"><span data-stu-id="0919a-113">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span>

<span data-ttu-id="0919a-114">針對回溯相容性以外的所有用途，請使用 MIDL 預設模式 **/Oicf** /robust。</span><span class="sxs-lookup"><span data-stu-id="0919a-114">Use MIDL default mode **/Oicf** /robust for all purposes other than backward compatibility.</span></span> <span data-ttu-id="0919a-115">此模式是 MIDL 編譯器的安全標準模式;任何其他模式都應該只在仔細考慮安全性隱含的考慮之後才使用，以瞭解未來的延伸模組只會針對預設模式執行。</span><span class="sxs-lookup"><span data-stu-id="0919a-115">This mode is the secure standard mode of MIDL compiler; any other mode should be used only after careful consideration to the security implication, realizing that future extensions will only be implemented for default mode.</span></span> <span data-ttu-id="0919a-116">在混合模式中，編譯器會封送處理產生的存根中內嵌的一些參數。</span><span class="sxs-lookup"><span data-stu-id="0919a-116">In mixed mode, the compiler marshals some parameters inline in the generated stubs.</span></span> <span data-ttu-id="0919a-117">雖然這會產生較大的存根大小，但它也可能會提供更高的效能。</span><span class="sxs-lookup"><span data-stu-id="0919a-117">While this results in larger stub size, it also may offer increased performance.</span></span>

<span data-ttu-id="0919a-118">MIDL 只會在 [**/Oicf**](-oi.md) 模式中提供多維陣列和多維度大小指標的完整支援。</span><span class="sxs-lookup"><span data-stu-id="0919a-118">MIDL provides full support for multidimensional arrays and multidimensional-sized pointers only in [**/Oicf**](-oi.md) mode.</span></span> <span data-ttu-id="0919a-119">在 **/os** 和 **/Oi** 模式中，編譯器支援簡單的案例，例如固定大小的陣列。</span><span class="sxs-lookup"><span data-stu-id="0919a-119">In **/Os** and **/Oi** modes, the compiler supports simple cases, such as fixed-size arrays.</span></span> <span data-ttu-id="0919a-120">在 **/os** 或 **/Oi** 模式中使用多維陣列可能會導致未正確封送處理的參數。</span><span class="sxs-lookup"><span data-stu-id="0919a-120">Using multidimensional arrays in **/Os** or **/Oi** modes can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="0919a-121">當您的介面定義的參數是多維陣列或多維度大小的指標時，Microsoft 建議您使用 **/Oicf** 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="0919a-121">Microsoft recommends that you use the **/Oicf** command line switch when your interface defines parameters that are multidimensional arrays or multidimensional-sized pointers.</span></span>

<span data-ttu-id="0919a-122">為了進一步定義資料的封送處理方式層級，這個版本的 RPC 會提供 \[ [**optimize**](optimize.md) \] 屬性。</span><span class="sxs-lookup"><span data-stu-id="0919a-122">To further define the level of gradation in how data is marshaled, this version of RPC provides an \[[**optimize**](optimize.md)\] attribute.</span></span> <span data-ttu-id="0919a-123">這個屬性是用來做為 ACF 介面屬性或 operation 屬性，以選取封送處理模式。</span><span class="sxs-lookup"><span data-stu-id="0919a-123">This attribute is used as an ACF interface attribute or operation attribute to select the marshaling mode.</span></span>

## <a name="examples"></a><span data-ttu-id="0919a-124">範例</span><span class="sxs-lookup"><span data-stu-id="0919a-124">Examples</span></span>

<span data-ttu-id="0919a-125">**midl/Os 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="0919a-125">**midl /Os filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0919a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0919a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0919a-127">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="0919a-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0919a-128">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="0919a-128">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="0919a-129">**優化**</span><span class="sxs-lookup"><span data-stu-id="0919a-129">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="0919a-130">**/no \_ 格式 \_ 選擇**</span><span class="sxs-lookup"><span data-stu-id="0919a-130">**/no\_format\_opt**</span></span>](-no-format-opt.md)
</dt> </dl>

 

 




