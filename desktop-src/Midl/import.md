---
title: import 屬性
description: 匯入指示詞會指定另一個 IDL、ODL 或標頭檔，其中包含您想要從主要 IDL 檔案參考的定義。
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- 匯入屬性 MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314767"
---
# <a name="import-attribute"></a><span data-ttu-id="00e20-104">import 屬性</span><span class="sxs-lookup"><span data-stu-id="00e20-104">import attribute</span></span>

<span data-ttu-id="00e20-105">匯 **入** 指示詞會指定另一個 IDL、ODL 或標頭檔，其中包含您想要從主要 IDL 檔案參考的定義。</span><span class="sxs-lookup"><span data-stu-id="00e20-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="00e20-106">參數</span><span class="sxs-lookup"><span data-stu-id="00e20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e20-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="00e20-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="00e20-108">指定要匯入之標頭、IDL 或 ODL 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="00e20-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00e20-109">備註</span><span class="sxs-lookup"><span data-stu-id="00e20-109">Remarks</span></span>

<span data-ttu-id="00e20-110">使用匯 **入** 指示詞時，匯入的檔案中的所有 IDL 語句（例如 typedef、常數宣告和介面定義）都會變成可供匯入。IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="00e20-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="00e20-111">匯入的檔案會分開處理 (這表示會從匯入 IDL 檔案) 獨立叫用 CPP 預處理器。</span><span class="sxs-lookup"><span data-stu-id="00e20-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="00e20-112">如此一來，預處理器指示詞（例如 \# define）不會將匯入的標頭或 IDL 檔案從匯入的 idl 檔案中執行。</span><span class="sxs-lookup"><span data-stu-id="00e20-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="00e20-113">如同 C 語言預處理器宏 **\# 在內**， **import** 指示詞會指示編譯器包含匯入的 IDL 檔案中所定義的資料類型。</span><span class="sxs-lookup"><span data-stu-id="00e20-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="00e20-114">和 **\# include** 指示詞不同，匯 **入** 指示詞會忽略程式原型，因為匯入檔案中的任何作業都不會產生任何 stub。</span><span class="sxs-lookup"><span data-stu-id="00e20-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="00e20-115">如需使用匯 **入** 將標頭檔併入 IDL 檔案的特定資訊，請參閱匯 [入系統標頭檔](importing-system-header-files.md)。</span><span class="sxs-lookup"><span data-stu-id="00e20-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="00e20-116">C 語言標頭 (。H) 針對介面產生的檔案不會直接包含匯入的型別，而是會針對對應至已匯入介面的標頭檔產生 **\# include** 指示詞。</span><span class="sxs-lookup"><span data-stu-id="00e20-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="00e20-117">例如，當您匯入基底時。IDL 至您衍生的。IDL，衍生產生的標頭檔。H 將包含指示詞， **\# 包含** BASE. H。</span><span class="sxs-lookup"><span data-stu-id="00e20-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="00e20-118">適用的規則如下：</span><span class="sxs-lookup"><span data-stu-id="00e20-118">The following rules apply:</span></span>

-   <span data-ttu-id="00e20-119">匯 **入** 關鍵字是選擇性的，而且可以在 IDL 檔案中出現零次或多次。</span><span class="sxs-lookup"><span data-stu-id="00e20-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="00e20-120">每個 **import** 關鍵字都可以與一個以上的檔案名相關聯。</span><span class="sxs-lookup"><span data-stu-id="00e20-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="00e20-121">以逗號分隔多個檔案名。</span><span class="sxs-lookup"><span data-stu-id="00e20-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="00e20-122">您必須將檔案名括在引號內，並以分號 ( 結束 import 語句，) 。</span><span class="sxs-lookup"><span data-stu-id="00e20-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="00e20-123">您可以將沒有屬性的介面匯入至另一個 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="00e20-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="00e20-124">不過，介面必須只包含資料類型;它不能包含任何程式。</span><span class="sxs-lookup"><span data-stu-id="00e20-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="00e20-125">如果匯入的介面中包含一個程式，您必須指定 [**本機**](local.md) 或 [**UUID**](uuid.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="00e20-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="00e20-126">匯 **入** 函式 idempotentÂ的是，一次匯入介面沒有額外的效果。</span><span class="sxs-lookup"><span data-stu-id="00e20-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="00e20-127">匯 **入** 指示詞的行為獨立于 MIDL 編譯器模式參數 [**/ms \_ ext**](-ms-ext.md) (預設) 、 [**/osf**](-osf.md)和 [**/app \_**](-app-config.md)設定。</span><span class="sxs-lookup"><span data-stu-id="00e20-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="00e20-128">不過，編譯器模式 (**/osf** 或 **/ms \_ ext**) 可能會影響匯入類型上的指標屬性裝飾。</span><span class="sxs-lookup"><span data-stu-id="00e20-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="00e20-129">如需詳細資訊，請參閱 [指標屬性類型繼承](/windows/desktop/Rpc/pointer-attribute-type-inheritance)。</span><span class="sxs-lookup"><span data-stu-id="00e20-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="00e20-130">範例</span><span class="sxs-lookup"><span data-stu-id="00e20-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="00e20-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00e20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e20-132">**/app \_ 設定**</span><span class="sxs-lookup"><span data-stu-id="00e20-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="00e20-133"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="00e20-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="00e20-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="00e20-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="00e20-135">**包括**</span><span class="sxs-lookup"><span data-stu-id="00e20-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="00e20-136">匯入系統標頭檔</span><span class="sxs-lookup"><span data-stu-id="00e20-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="00e20-137">匯入檔案和型別程式庫</span><span class="sxs-lookup"><span data-stu-id="00e20-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="00e20-138">**/ms \_ ext**</span><span class="sxs-lookup"><span data-stu-id="00e20-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="00e20-139">**/osf**</span><span class="sxs-lookup"><span data-stu-id="00e20-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 