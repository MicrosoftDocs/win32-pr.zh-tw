---
title: MIDL 與 Mktyplib.exe 之間的差異
description: MIDL 與 Mktyplib.exe 之間的差異
ms.assetid: 86abd70b-7238-49a6-a996-2c8906a14449
keywords:
- Midl 和 ODL MIDL，MIDL 與 Mktyplib.exe 之間的差異
- Mktyplib.exe MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a54b6103cc230e1c5e6700b0ddc93312c767f9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022089"
---
# <a name="differences-between-midl-and-mktyplib"></a><span data-ttu-id="0d21e-105">MIDL 與 Mktyplib.exe 之間的差異</span><span class="sxs-lookup"><span data-stu-id="0d21e-105">Differences Between MIDL and MkTypLib</span></span>

> [!Note]  
> <span data-ttu-id="0d21e-106">Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="0d21e-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="0d21e-107">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="0d21e-107">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="0d21e-108">MIDL 編譯器與 Mktyplib.exe 有幾個重要區域。</span><span class="sxs-lookup"><span data-stu-id="0d21e-108">There are a few key areas in which the MIDL compiler differs from MkTypLib.</span></span> <span data-ttu-id="0d21e-109">因為 MIDL 的方向比 Mktyplib.exe 更接近 C 語法，所以會發生這些差異。</span><span class="sxs-lookup"><span data-stu-id="0d21e-109">Most of these differences arise because MIDL is oriented more toward C-syntax than MkTypLib.</span></span>

<span data-ttu-id="0d21e-110">一般而言，您會想要在 IDL 檔案中使用 MIDL 語法。</span><span class="sxs-lookup"><span data-stu-id="0d21e-110">In general, you will want to use the MIDL syntax in your IDL files.</span></span> <span data-ttu-id="0d21e-111">但是，如果您需要編譯現有的 ODL 檔案，或維持與 Mktyplib.exe 的相容性，請使用 [**/Mktyplib203**](-mktyplib203.md) midl 編譯器選項強制 MIDL 的行為，就像 Mkktyplib.exe，version 2.03 一樣。</span><span class="sxs-lookup"><span data-stu-id="0d21e-111">However, if you need to compile an existing ODL file, or otherwise maintain compatibility with MkTypLib, use the [**/mktyplib203**](-mktyplib203.md) MIDL compiler option to force MIDL to behave like Mkktyplib.exe, version 2.03.</span></span> <span data-ttu-id="0d21e-112"> (這是 Mktyplib.exe 工具的最後一個版本。 ) 具體而言， **/mktyplib203** 選項會解決這些差異：</span><span class="sxs-lookup"><span data-stu-id="0d21e-112">(This is the last release of the MkTypLib tool.) Specifically, the **/mktyplib203** option resolves these differences:</span></span>

-   <span data-ttu-id="0d21e-113">複雜資料類型的 typedef 語法</span><span class="sxs-lookup"><span data-stu-id="0d21e-113">typedef syntax for complex data types</span></span>

    <span data-ttu-id="0d21e-114">在 Mktyplib.exe 中，下列兩個定義都會產生 \_ \_ 類型程式庫中 "this struct" 的 TKIND 記錄。</span><span class="sxs-lookup"><span data-stu-id="0d21e-114">In MkTypLib, both of the following definitions generate a TKIND\_RECORD for "this\_struct" in the type library.</span></span> <span data-ttu-id="0d21e-115">標記「結構標籤」 \_ 是選擇性的，如果已使用，將不會顯示在類型程式庫中。</span><span class="sxs-lookup"><span data-stu-id="0d21e-115">The tag "struct\_tag" is optional and, if used, will not show up in the type library.</span></span>

    ``` syntax
    typedef struct struct_tag { ... } this_struct;
    typedef struct { ... } that_struct;
    ```

    <span data-ttu-id="0d21e-116">如果省略了選擇性標記，MIDL 將會產生它，有效地將標籤新增至使用者提供的定義。</span><span class="sxs-lookup"><span data-stu-id="0d21e-116">If an optional tag is missing, MIDL will generate it, effectively adding a tag to the definition supplied by the user.</span></span> <span data-ttu-id="0d21e-117">由於第一個定義具有標記，因此 MIDL 會產生 \_ "this struct" 的 TKIND \_ 記錄和 \_ "this STRUCT" 的 TKIND 別名 \_ (將 "this \_ struct" 定義為 "struct \_ tag" ) 的別名。</span><span class="sxs-lookup"><span data-stu-id="0d21e-117">Since the first definition has a tag, MIDL will generate a TKIND\_RECORD for "this\_struct" and a TKIND\_ALIAS for "this\_struct" (defining "this\_struct" as an alias for "struct\_tag").</span></span> <span data-ttu-id="0d21e-118">因為第二個定義中遺漏了標記，所以 MIDL 會產生對 \_ 使用者而言不具意義之名稱的 TKIND 記錄，以及「該結構」的 TKIND \_ 別名 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0d21e-118">Because the tag is missing in the second definition, MIDL will generate a TKIND\_RECORD for a mangled name, internal to MIDL, that is not meaningful to the user and a TKIND\_ALIAS for "that\_struct".</span></span>

    <span data-ttu-id="0d21e-119">這對於在其使用者介面中顯示記錄名稱的類型程式庫瀏覽器有潛在的影響。</span><span class="sxs-lookup"><span data-stu-id="0d21e-119">This has potential implications for type library browsers that simply show the name of a record in their user interface.</span></span> <span data-ttu-id="0d21e-120">如果您預期 TKIND \_ 記錄有實際名稱，則使用者介面可能會出現無法辨識的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d21e-120">If you expect a TKIND\_RECORD to have a real name, unrecognizable names could appear in the user interface.</span></span> <span data-ttu-id="0d21e-121">此行為也適用于 [**union**](union.md) 和 [**enum**](enum.md) 定義，而 MIDL 編譯器會分別產生 TKIND 聯集 \_ 和 TKIND 列舉 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0d21e-121">This behavior also applies to [**union**](union.md) and [**enum**](enum.md) definitions, with the MIDL compiler generating TKIND\_UNIONs and TKIND\_ENUMs, respectively.</span></span>

    <span data-ttu-id="0d21e-122">MIDL 也允許 C 樣式的 [**結構**](struct.md)、 [**等**](union.md)位和 [**列舉**](enum.md) 定義。</span><span class="sxs-lookup"><span data-stu-id="0d21e-122">MIDL also allows C-style [**struct**](struct.md), [**union**](union.md), and [**enum**](enum.md) definitions.</span></span> <span data-ttu-id="0d21e-123">例如，下列定義在 MIDL 中是合法的：</span><span class="sxs-lookup"><span data-stu-id="0d21e-123">For example, the following definition is legal in MIDL:</span></span>

    ``` syntax
    struct my_struct { ... };
    typedef struct my_struct your_struct;
    ```

-   <span data-ttu-id="0d21e-124">Boolean 資料類型</span><span class="sxs-lookup"><span data-stu-id="0d21e-124">Boolean data types</span></span>

    <span data-ttu-id="0d21e-125">在 Mktyplib.exe 中， [**布林值**](boolean.md) 基底類型和 mktyplib.exe 資料類型 BOOL 等於 VT \_ bool，它會對應至 VARIANT \_ bool，且定義為 [**簡短**](short.md)。</span><span class="sxs-lookup"><span data-stu-id="0d21e-125">In MkTypLib, the [**Boolean**](boolean.md) base type and the MkTypLib data type BOOL equate to VT\_BOOL, which maps to VARIANT\_BOOL, and which is defined as a [**short**](short.md).</span></span> <span data-ttu-id="0d21e-126">在 MIDL 中， **布林值** 基底類型相當於 VT \_ UI1 （定義為不 [**帶正負**](unsigned.md)號的字元），而 BOOL 資料類型定義為 [**long**](long.md)。</span><span class="sxs-lookup"><span data-stu-id="0d21e-126">In MIDL, the **Boolean** base type is equivalent to VT\_UI1, which is defined as an [**unsigned char**](unsigned.md), and the BOOL data type is defined as a [**long**](long.md).</span></span> <span data-ttu-id="0d21e-127">如果您在同一個檔案中混搭了 IDL 語法和 ODL 語法，同時仍在嘗試維持與 Mktyplib.exe 的相容性，這會導致問題。</span><span class="sxs-lookup"><span data-stu-id="0d21e-127">This leads to difficulties if you mix IDL syntax and ODL syntax in the same file while still trying to maintain compatibility with MkTypLib.</span></span> <span data-ttu-id="0d21e-128">由於資料類型的大小不同，因此封送處理常式代碼不會符合類型資訊中所描述的內容。</span><span class="sxs-lookup"><span data-stu-id="0d21e-128">Because the data types are different sizes, the marshaling code will not match what is described in the type information.</span></span> <span data-ttu-id="0d21e-129">如果您想要 \_ 在類型程式庫中使用 VT bool，則應該使用 VARIANT \_ bool 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0d21e-129">If you want a VT\_BOOL in your type library, you should use the VARIANT\_BOOL data type.</span></span>

-   <span data-ttu-id="0d21e-130">標頭檔中的 GUID 定義</span><span class="sxs-lookup"><span data-stu-id="0d21e-130">GUID definitions in header files</span></span>

    <span data-ttu-id="0d21e-131">在 Mktyplib.exe 中，Guid 會定義在標頭檔中，並具有可有條件地編譯的宏，以產生 GUID predefinition 或具現化的 GUID。</span><span class="sxs-lookup"><span data-stu-id="0d21e-131">In MkTypLib, GUIDs are defined in the header file with a macro that can be conditionally compiled to generate either a GUID predefinition or an instantiated GUID.</span></span> <span data-ttu-id="0d21e-132">MIDL 通常會將 GUID predefinitions 放在其產生的標頭檔中，而 GUID 只會在 [**/iid**](-iid.md) 參數所產生的檔案中使用 guid 具現化。</span><span class="sxs-lookup"><span data-stu-id="0d21e-132">MIDL normally puts GUID predefinitions in its generated header files and GUID instantiations only in the file generated by the [**/iid**](-iid.md) switch.</span></span>

<span data-ttu-id="0d21e-133">使用 [**/mktyplib203**](-mktyplib203.md) 參數無法解決下列行為差異：</span><span class="sxs-lookup"><span data-stu-id="0d21e-133">The following differences in behavior cannot be resolved by using the [**/mktyplib203**](-mktyplib203.md) switch:</span></span>

-   <span data-ttu-id="0d21e-134">區分大小寫</span><span class="sxs-lookup"><span data-stu-id="0d21e-134">Case sensitivity</span></span>

    <span data-ttu-id="0d21e-135">MIDL 會區分大小寫，而 OLE Automation 則否。</span><span class="sxs-lookup"><span data-stu-id="0d21e-135">MIDL is case sensitive, OLE Automation is not.</span></span>

-   <span data-ttu-id="0d21e-136">列舉宣告中的符號範圍</span><span class="sxs-lookup"><span data-stu-id="0d21e-136">Scope of symbols in an enum declaration</span></span>

    <span data-ttu-id="0d21e-137">在 Mktyplib.exe 中，列舉的符號範圍是本機的。</span><span class="sxs-lookup"><span data-stu-id="0d21e-137">In MkTypLib the scope of symbols in an enum is local.</span></span> <span data-ttu-id="0d21e-138">在 MIDL 中，列舉中的符號範圍是全域的，因為它是在 C 中。例如，下列程式碼會在 Mktyplib.exe 中編譯，但會在 MIDL 中產生重複的名稱錯誤：</span><span class="sxs-lookup"><span data-stu-id="0d21e-138">In MIDL, the scope of symbols in an enum is global, as it is in C. For example, the following code will compile in MkTypLib, but will generate a duplicate name error in MIDL:</span></span>

    ``` syntax
    typedef struct { ... } a;
    enum {a=1, b=2, c=3};
    ```

-   <span data-ttu-id="0d21e-139">公用屬性的範圍</span><span class="sxs-lookup"><span data-stu-id="0d21e-139">Scope of public attribute</span></span>

    <span data-ttu-id="0d21e-140">如果您將 [**公用**](public.md) 屬性套用至介面區塊，mktyplib.exe 會將該介面區塊內的每個 typedef 視為公用。</span><span class="sxs-lookup"><span data-stu-id="0d21e-140">If you apply the [**public**](public.md) attribute to an interface block, MkTypLib treats every typedef inside that interface block as public.</span></span> <span data-ttu-id="0d21e-141">MIDL 要求您明確地將 **公用** 屬性套用至您想要公開的 typedef。</span><span class="sxs-lookup"><span data-stu-id="0d21e-141">MIDL requires that you explicitly apply the **public** attribute to those typedefs that you want public.</span></span>

-   <span data-ttu-id="0d21e-142">Importlib 搜尋順序</span><span class="sxs-lookup"><span data-stu-id="0d21e-142">Importlib search order</span></span>

    <span data-ttu-id="0d21e-143">如果您匯入多個類型程式庫，而且這些程式庫包含重複的參考，則 Mktyplib.exe 會使用它所找到的第一個參考來解析此項。</span><span class="sxs-lookup"><span data-stu-id="0d21e-143">If you import more than one type library, and if these libraries contain duplicate references, MkTypLib resolves this by using the first reference that it finds.</span></span> <span data-ttu-id="0d21e-144">MIDL 會使用它所找到的最後一個參考。</span><span class="sxs-lookup"><span data-stu-id="0d21e-144">MIDL will use the last reference that it finds.</span></span> <span data-ttu-id="0d21e-145">例如，假設有下列 ODL 語法，當您使用 Mktyplib.exe 編譯時，程式庫 C 將會從程式庫 A 使用 MOO typedef，如果您使用 MIDL 進行編譯，則會從程式庫 B 使用 MOO typedef：</span><span class="sxs-lookup"><span data-stu-id="0d21e-145">For example, given the following ODL syntax, library C will use the MOO typedef from library A if you compile with MkTypLib, and the MOO typedef from library B if you compile with MIDL:</span></span>

    ``` syntax
    [...]library A
    {
        typedef struct tagMOO
        {...}MOO
    }

    [...]library B
    {
        typedef struct tagMOO
        {...} MOO
    }

    [...]library C
    {
        importlib (A.TLB)
        importlib (B.TLB)
        typedef struct tagBAA
        {MOO y;}BAA
    }
    ```

    <span data-ttu-id="0d21e-146">適當的解決方法是使用正確的匯入程式庫名稱來限定每個這類參考，如下所示：</span><span class="sxs-lookup"><span data-stu-id="0d21e-146">The appropriate workaround for this is to qualify each such reference with the correct import library name, like this:</span></span>

    ``` syntax
    typedef struct tagBAA
        {A.MOO y;}BAA
    ```

-   <span data-ttu-id="0d21e-147">無法辨識 VOID 資料類型</span><span class="sxs-lookup"><span data-stu-id="0d21e-147">VOID data type not recognized</span></span>

    <span data-ttu-id="0d21e-148">MIDL 可識別 C 語言 [**void**](void.md) 資料類型，而且無法辨識 OLE Automation void 資料類型。</span><span class="sxs-lookup"><span data-stu-id="0d21e-148">MIDL recognizes the C-language [**void**](void.md) data type and does not recognize the OLE Automation VOID data type.</span></span> <span data-ttu-id="0d21e-149">如果您有使用 VOID 的 ODL 檔案，請將此定義放在檔案的頂端：</span><span class="sxs-lookup"><span data-stu-id="0d21e-149">If you have an ODL file that uses VOID, place this definition at the top of the file:</span></span>

    ``` syntax
#define VOID void
    ```

-   <span data-ttu-id="0d21e-150">指數標記法</span><span class="sxs-lookup"><span data-stu-id="0d21e-150">Exponential notation</span></span>

    <span data-ttu-id="0d21e-151">MIDL 要求以指數標記法表示的值必須包含在引號中。</span><span class="sxs-lookup"><span data-stu-id="0d21e-151">MIDL requires that values expressed in exponential notation be contained within quotation marks.</span></span> <span data-ttu-id="0d21e-152">例如，"-2.5 E + 3"</span><span class="sxs-lookup"><span data-stu-id="0d21e-152">For example, "-2.5E+3"</span></span>

-   <span data-ttu-id="0d21e-153">LCID 值和常數</span><span class="sxs-lookup"><span data-stu-id="0d21e-153">LCID values and constants</span></span>

    <span data-ttu-id="0d21e-154">在剖析檔案時，MIDL 通常不會考慮 LCID。</span><span class="sxs-lookup"><span data-stu-id="0d21e-154">Normally MIDL does not consider the LCID when parsing files.</span></span> <span data-ttu-id="0d21e-155">若要強制執行此行為的值，或如果您在定義常數時需要使用地區設定特有的標記法，請用引號括住值或常數。</span><span class="sxs-lookup"><span data-stu-id="0d21e-155">To force this behavior for a value, or if you need to use locale-specific notation when defining a constant, enclose the value or constant in quotation marks.</span></span>

<span data-ttu-id="0d21e-156">如需詳細資訊，請參閱 [**/mktyplib203**](-mktyplib203.md)、 [**/Iid**](-iid.md)和 [封送處理 OLE 資料類型](marshaling-ole-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0d21e-156">For more information, see [**/mktyplib203**](-mktyplib203.md), [**/iid**](-iid.md), and [Marshaling OLE Data Types](marshaling-ole-data-types.md).</span></span>

 

 




