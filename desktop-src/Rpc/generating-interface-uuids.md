---
title: 產生介面 Uuid
description: " (Uuid) 和使用 Uuidgen.exe 產生介面通用唯一識別碼。"
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673003"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="da8d0-103">產生介面 Uuid</span><span class="sxs-lookup"><span data-stu-id="da8d0-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="da8d0-104">本節提供 (Uuid) 的通用唯一識別碼的相關資訊，以及下列主題中的 Uuidgen.exe 公用程式：</span><span class="sxs-lookup"><span data-stu-id="da8d0-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="da8d0-105">什麼是 UUID？</span><span class="sxs-lookup"><span data-stu-id="da8d0-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="da8d0-106">使用 Uuidgen.exe</span><span class="sxs-lookup"><span data-stu-id="da8d0-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="da8d0-107">什麼是 UUID？</span><span class="sxs-lookup"><span data-stu-id="da8d0-107">What is a UUID?</span></span>

<span data-ttu-id="da8d0-108">所有介面都必須在網路上唯一識別，讓用戶端可以找到它們。</span><span class="sxs-lookup"><span data-stu-id="da8d0-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="da8d0-109">在小型網路中，介面的名稱單獨可能就足以識別它。</span><span class="sxs-lookup"><span data-stu-id="da8d0-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="da8d0-110">不過，這在大型網路上通常不可行。</span><span class="sxs-lookup"><span data-stu-id="da8d0-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="da8d0-111">因此，開發人員通常會將通用唯一識別碼指派 (UUID、與詞彙 GUID 交換，或在每個介面) 全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="da8d0-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="da8d0-112">UUID 是包含一組十六進位數位的字串。</span><span class="sxs-lookup"><span data-stu-id="da8d0-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="da8d0-113">每個介面都有不同的 UUID。</span><span class="sxs-lookup"><span data-stu-id="da8d0-113">Each interface has a different UUID.</span></span> <span data-ttu-id="da8d0-114">如需詳細資訊，請參閱 [字串 UUID](string-uuid.md)。</span><span class="sxs-lookup"><span data-stu-id="da8d0-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="da8d0-115">UUID 的文字標記法是由8個十六進位數位後面接著連字號的字串所組成，後面接著三個以連字號分隔的4個十六進位數位，後面接著連字號和12個十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="da8d0-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="da8d0-116">下列範例是有效的 UUID 字串：</span><span class="sxs-lookup"><span data-stu-id="da8d0-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="da8d0-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="da8d0-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="da8d0-118">空白 Uuid 稱為「nil Uuid」，而不是 **Null** uuid。</span><span class="sxs-lookup"><span data-stu-id="da8d0-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="da8d0-119">Nil 一詞表示任何零、空白、空白或未初始化的值。</span><span class="sxs-lookup"><span data-stu-id="da8d0-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="da8d0-120">空字串、空的資料庫記錄或未初始化的 UUID 都是 nil 值的範例。</span><span class="sxs-lookup"><span data-stu-id="da8d0-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="da8d0-121">**Null** 值是特定的值零。</span><span class="sxs-lookup"><span data-stu-id="da8d0-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="da8d0-122">它通常用於 C 和 c + + 程式設計中搭配指標。</span><span class="sxs-lookup"><span data-stu-id="da8d0-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="da8d0-123">Nil 是比 **Null** 更常見的詞彙。</span><span class="sxs-lookup"><span data-stu-id="da8d0-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="da8d0-124">未初始化的物件介面 Uuid 應一律稱為「nil Uuid」（而非 **Null** uuid）。</span><span class="sxs-lookup"><span data-stu-id="da8d0-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="da8d0-125">使用 Uuidgen.exe</span><span class="sxs-lookup"><span data-stu-id="da8d0-125">Using Uuidgen</span></span>

<span data-ttu-id="da8d0-126">Microsoft 提供一個稱為 Uuidgen.exe 的公用程式來產生您的 Uuid。</span><span class="sxs-lookup"><span data-stu-id="da8d0-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="da8d0-127">Uuidgen.exe 公用程式會以 IDL 檔案格式或 C 語言格式產生 UUID。</span><span class="sxs-lookup"><span data-stu-id="da8d0-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="da8d0-128">當您從命令列執行 Uuidgen.exe 公用程式時，您可以使用下列命令參數。</span><span class="sxs-lookup"><span data-stu-id="da8d0-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="da8d0-129">Uuidgen.exe 參數</span><span class="sxs-lookup"><span data-stu-id="da8d0-129">Uuidgen switch</span></span>           | <span data-ttu-id="da8d0-130">Description</span><span class="sxs-lookup"><span data-stu-id="da8d0-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="da8d0-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="da8d0-131">**/I**</span></span>                   | <span data-ttu-id="da8d0-132">將 UUID 輸出至 IDL 介面範本。</span><span class="sxs-lookup"><span data-stu-id="da8d0-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="da8d0-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="da8d0-133">**/s**</span></span>                   | <span data-ttu-id="da8d0-134">將 UUID 輸出為初始化的 C 結構。</span><span class="sxs-lookup"><span data-stu-id="da8d0-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="da8d0-135">**/o** <*檔案名*></span><span class="sxs-lookup"><span data-stu-id="da8d0-135">**/o**<*filename*></span></span> | <span data-ttu-id="da8d0-136">將輸出重新導向至檔案;在 **/o** 參數之後立即指定。</span><span class="sxs-lookup"><span data-stu-id="da8d0-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="da8d0-137">**/n** <*數位*></span><span class="sxs-lookup"><span data-stu-id="da8d0-137">**/n**<*number*></span></span>   | <span data-ttu-id="da8d0-138">指定要產生的 Uuid 數目。</span><span class="sxs-lookup"><span data-stu-id="da8d0-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="da8d0-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="da8d0-139">**/v**</span></span>                   | <span data-ttu-id="da8d0-140">顯示有關 Uuidgen.exe 的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="da8d0-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="da8d0-141">**/h** 或 **？**</span><span class="sxs-lookup"><span data-stu-id="da8d0-141">**/h** or **?**</span></span>          | <span data-ttu-id="da8d0-142">顯示命令選項摘要。</span><span class="sxs-lookup"><span data-stu-id="da8d0-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="da8d0-143">一般而言，您會使用 Uuidgen.exe 公用程式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="da8d0-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="da8d0-144">**uuidgen.exe-i-oMyApp .idl**</span><span class="sxs-lookup"><span data-stu-id="da8d0-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="da8d0-145">此命令會產生 UUID，並將其儲存在可作為範本的 MIDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="da8d0-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="da8d0-146">執行上述命令時，MyApp 的內容如下所示：</span><span class="sxs-lookup"><span data-stu-id="da8d0-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="da8d0-147">下一步是使用您介面的實際名稱來取代預留位置名稱介面名稱。</span><span class="sxs-lookup"><span data-stu-id="da8d0-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




