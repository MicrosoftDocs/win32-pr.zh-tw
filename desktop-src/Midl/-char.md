---
title: /char 參數
description: /Char 參數有助於確保 MIDL 編譯器和 C 編譯器都能正確地針對所有 char 和 small 類型運作。
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char 參數 MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678668"
---
# <a name="char-switch"></a><span data-ttu-id="df962-104">/char 參數</span><span class="sxs-lookup"><span data-stu-id="df962-104">/char switch</span></span>

<span data-ttu-id="df962-105">**/Char** 參數有助於確保 MIDL 編譯器和 C 編譯器都能正確地針對所有 [**char**](char-idl.md)和 [**small**](small.md)類型運作。</span><span class="sxs-lookup"><span data-stu-id="df962-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="df962-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="df962-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="df962-107"><span id="signed"></span><span id="SIGNED"></span>已簽署 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="df962-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="df962-108">指定 [**char**](char-idl.md) 的預設 C 編譯器類型已簽署。</span><span class="sxs-lookup"><span data-stu-id="df962-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="df962-109">不帶正負號規格的所有 **字元** 都是以不帶正負號的字元產生。</span><span class="sxs-lookup"><span data-stu-id="df962-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="df962-110"><span id="unsigned"></span><span id="UNSIGNED"></span>未簽署 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="df962-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="df962-111">指定 [**char**](char-idl.md) 的預設 C 編譯器類型不帶正負號。</span><span class="sxs-lookup"><span data-stu-id="df962-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="df962-112">所有不帶正負號規格的使用都會產生為帶正負 [**號的小型**](small.md) 。</span><span class="sxs-lookup"><span data-stu-id="df962-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="df962-113"><span id="ascii7"></span><span id="ASCII7"></span>ascii7\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="df962-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="df962-114">指定所有 [**char**](char-idl.md) 值都必須傳遞至產生的檔案，但不含特定的 sign 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="df962-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="df962-115">所有 [**不帶**](small.md) 正負號規格的使用都是以 **較小** 的方式產生。</span><span class="sxs-lookup"><span data-stu-id="df962-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df962-116">備註</span><span class="sxs-lookup"><span data-stu-id="df962-116">Remarks</span></span>

<span data-ttu-id="df962-117">根據定義，MIDL [**char**](char-idl.md) 不帶正負號。</span><span class="sxs-lookup"><span data-stu-id="df962-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="df962-118">"Small" 是以 **char** 定義 \# ， (定義 Small char) ，而且 MIDL [**small**](small.md) 會經過簽署。</span><span class="sxs-lookup"><span data-stu-id="df962-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="df962-119">當 C 編譯器簽署宣告與該型別的 MIDL 預設衝突時， **/char** 參數會指示 MIDL 編譯器在產生的檔案中指定明確 [**帶**](signed.md) 正負號或不 [**帶正負**](unsigned.md) 號聲明。</span><span class="sxs-lookup"><span data-stu-id="df962-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="df962-120">請記住，MIDL 編譯器會以 C 原始程式碼形式產生存根，您必須將它編譯為用戶端和伺服器程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="df962-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="df962-121">某些編譯器會在原始程式碼中指定 [**字元**](char-idl.md)資料的任何地方使用 **帶正負** 號的字元。</span><span class="sxs-lookup"><span data-stu-id="df962-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="df962-122">MIDL 編譯器產生的存根原始程式碼會將所有 **char** 資料視為不 **帶正負** 號的 char。</span><span class="sxs-lookup"><span data-stu-id="df962-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="df962-123">如果 MIDL 編譯器只是將 IDL 檔案中的所有 **char** 資料產生為存根中的 **char** 資料，則使用 **帶正負** 號 char **資料的** 編譯器會在存根原始程式碼中造成衝突。</span><span class="sxs-lookup"><span data-stu-id="df962-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="df962-124">**/Char** 命令列參數的目的是要解決這些潛在衝突。</span><span class="sxs-lookup"><span data-stu-id="df962-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="df962-125">它會將 IDL 檔案中指定為 [**char**](char-idl.md) 的所有資料保留為存根原始程式碼中的不 **帶正負號字元** 。</span><span class="sxs-lookup"><span data-stu-id="df962-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="df962-126">它也會將 [**小型**](small.md) 資料維護為已簽署。</span><span class="sxs-lookup"><span data-stu-id="df962-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="df962-127">下表摘要說明產生的類型。</span><span class="sxs-lookup"><span data-stu-id="df962-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="df962-128">midl/char 選項</span><span class="sxs-lookup"><span data-stu-id="df962-128">midl /char option</span></span>       | <span data-ttu-id="df962-129">產生的 char 類型</span><span class="sxs-lookup"><span data-stu-id="df962-129">Generated char type</span></span> | <span data-ttu-id="df962-130">產生的小型類型</span><span class="sxs-lookup"><span data-stu-id="df962-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="df962-131">**midl/char 已簽署**</span><span class="sxs-lookup"><span data-stu-id="df962-131">**midl /char signed**</span></span>   | <span data-ttu-id="df962-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="df962-132">**unsigned char**</span></span>   | <span data-ttu-id="df962-133">**small**</span><span class="sxs-lookup"><span data-stu-id="df962-133">**small**</span></span>            |
| <span data-ttu-id="df962-134">**midl/char 未簽署**</span><span class="sxs-lookup"><span data-stu-id="df962-134">**midl /char unsigned**</span></span> | <span data-ttu-id="df962-135">**char**</span><span class="sxs-lookup"><span data-stu-id="df962-135">**char**</span></span>            | <span data-ttu-id="df962-136">**帶正負號**</span><span class="sxs-lookup"><span data-stu-id="df962-136">**signed small**</span></span>     |
| <span data-ttu-id="df962-137">**midl/char ascii7**</span><span class="sxs-lookup"><span data-stu-id="df962-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="df962-138">**char**</span><span class="sxs-lookup"><span data-stu-id="df962-138">**char**</span></span>            | <span data-ttu-id="df962-139">**small**</span><span class="sxs-lookup"><span data-stu-id="df962-139">**small**</span></span>            |



 

<span data-ttu-id="df962-140">**/Char** 帶正負號選項表示 C 編譯器字元和小型類型已簽署。</span><span class="sxs-lookup"><span data-stu-id="df962-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="df962-141">若要比對 **char** 的 midl 預設值，MIDL 編譯器必須將未伴隨正負號規格之 **char** 的所有用法轉換成不帶正負號的 **char**。</span><span class="sxs-lookup"><span data-stu-id="df962-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="df962-142">因為這個 C 編譯器預設值符合 **small** 的 MIDL 預設值，所以不會修改 [**small**](small.md)型別。</span><span class="sxs-lookup"><span data-stu-id="df962-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="df962-143">**/Char** 未簽署選項表示 C 編譯器 [**char**](char-idl.md)類型未簽署。</span><span class="sxs-lookup"><span data-stu-id="df962-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="df962-144">MIDL 編譯器會將 [**small**](small.md) 未伴隨正負號規格的所有用法轉換成 **帶正負** 號的 **小**。</span><span class="sxs-lookup"><span data-stu-id="df962-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="df962-145">Ascii7 選項表示不會將明確的正負號規格新增至 [**char**](char-idl.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="df962-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="df962-146">[**Small**](small.md)類型會產生為 **small**。</span><span class="sxs-lookup"><span data-stu-id="df962-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="df962-147">為了避免混淆，您應該盡可能在 IDL 檔案中使用 [**char**](char-idl.md) 和 small 類型的明確簽署規格。</span><span class="sxs-lookup"><span data-stu-id="df962-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="df962-148">請注意，DCE IDL 不支援在 IDL 檔案中使用明確簽署的 **char** 類型。</span><span class="sxs-lookup"><span data-stu-id="df962-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="df962-149">因此，當您使用 MIDL [**/osf**](-osf.md) 參數進行編譯時，就無法使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="df962-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="df962-150">如需 **/char** 的相關資訊，請參閱 [**small**](small.md)。</span><span class="sxs-lookup"><span data-stu-id="df962-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="df962-151">範例</span><span class="sxs-lookup"><span data-stu-id="df962-151">Examples</span></span>

<span data-ttu-id="df962-152">**midl/char 簽署的檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="df962-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="df962-153">**midl/char 不帶正負號的檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="df962-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="df962-154">**midl/char ascii7 filename .idl**</span><span class="sxs-lookup"><span data-stu-id="df962-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="df962-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df962-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df962-156">**字元**</span><span class="sxs-lookup"><span data-stu-id="df962-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="df962-157">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="df962-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="df962-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="df962-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="df962-159">**小**</span><span class="sxs-lookup"><span data-stu-id="df962-159">**small**</span></span>](small.md)
</dt> </dl>

 

 




