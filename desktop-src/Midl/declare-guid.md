---
title: declare_guid 關鍵字
description: Declare \_ guid 關鍵字會指示 MIDL 將 guid 變數發出至產生的標頭檔。
keywords:
- declare_guid 關鍵字 MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106992226"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="a14a9-104">declare \_ guid 關鍵字</span><span class="sxs-lookup"><span data-stu-id="a14a9-104">declare\_guid keyword</span></span>

<span data-ttu-id="a14a9-105">**Declare \_ guid** 關鍵字會指示 MIDL 將 guid 變數發出至產生的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="a14a9-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="a14a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="a14a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a14a9-107">*變數名稱*</span><span class="sxs-lookup"><span data-stu-id="a14a9-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a14a9-108">在產生的標頭檔中指定識別碼的變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a14a9-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="a14a9-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="a14a9-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="a14a9-110">指定將套用至所產生標頭檔中變數名稱的 [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 。</span><span class="sxs-lookup"><span data-stu-id="a14a9-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a14a9-111">範例</span><span class="sxs-lookup"><span data-stu-id="a14a9-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="a14a9-112">備註</span><span class="sxs-lookup"><span data-stu-id="a14a9-112">Remarks</span></span>

<span data-ttu-id="a14a9-113">使用 `declare_guid` 相當於使用 `cpp_quote` 來產生宏的調用 `EXTERN_GUID` 。</span><span class="sxs-lookup"><span data-stu-id="a14a9-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="a14a9-114">上述範例會產生下列輸出：</span><span class="sxs-lookup"><span data-stu-id="a14a9-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="a14a9-115">`declare_guid`提供語句是為了方便起見。</span><span class="sxs-lookup"><span data-stu-id="a14a9-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="a14a9-116">它的優點是使用與[ `uuid` 屬性](uuid.md)相同的 GUID 語法。</span><span class="sxs-lookup"><span data-stu-id="a14a9-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a14a9-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a14a9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14a9-118"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="a14a9-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a14a9-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="a14a9-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="a14a9-120">**uuid 屬性**</span><span class="sxs-lookup"><span data-stu-id="a14a9-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="a14a9-121">**GUID 結構**</span><span class="sxs-lookup"><span data-stu-id="a14a9-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
