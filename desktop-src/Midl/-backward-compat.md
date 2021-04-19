---
title: /backward_compat 參數
description: /Backward \_ 相容性參數會指示 MIDL 編譯器在產生 RPC/COM 存根時關閉一些 advanced 功能。
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968021"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="0d2b7-103">/backward \_ 相容性參數</span><span class="sxs-lookup"><span data-stu-id="0d2b7-103">/backward\_compat Switch</span></span>

<span data-ttu-id="0d2b7-104">/Backward \_ 相容性參數會指示 MIDL 編譯器在產生 RPC/COM 存根時關閉一些 advanced 功能。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="0d2b7-105">切換選項</span><span class="sxs-lookup"><span data-stu-id="0d2b7-105">Switch Options</span></span>

<span data-ttu-id="0d2b7-106">*maybenull \_ sizeis*</span><span class="sxs-lookup"><span data-stu-id="0d2b7-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="0d2b7-107">將[ \[ 停用 \_ 一致性 \_ 檢查 \] ](disable-consistence-check.md)屬性套用至整個 MIDL 編譯。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="0d2b7-108">*zeroout \_ alignmentgap*</span><span class="sxs-lookup"><span data-stu-id="0d2b7-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="0d2b7-109">關閉已封送處理之緩衝區中的清空間距。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="0d2b7-110">*BSTR \_ byvalue \_ 轉義*</span><span class="sxs-lookup"><span data-stu-id="0d2b7-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="0d2b7-111">指示 MIDL 編譯器接受 escape 序列，例如 \\ bstr 中的̃ nâ€™或̃ \\ tâ€™。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="0d2b7-112">*字串 \_ defaultvalue*</span><span class="sxs-lookup"><span data-stu-id="0d2b7-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="0d2b7-113">強制 MIDL 編譯器將 [**\[ defaultvalue \]**](defaultvalue.md)屬性中的字串強制轉換成 VARIANT。VT \_ I4 型別，請先將值強制轉換成正確的型別。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="0d2b7-114">*簽署的 \_ wchar \_ t*</span><span class="sxs-lookup"><span data-stu-id="0d2b7-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="0d2b7-115">指示 MIDL 將 wchar \_ t 類型視為已簽署，以提供 Visual Basic 的相容性。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="0d2b7-116">備註</span><span class="sxs-lookup"><span data-stu-id="0d2b7-116">Remarks</span></span>

-   <span data-ttu-id="0d2b7-117">*maybenull \_ sizeis*：請參閱 \[ 停用 \_ 一致性 \_ 檢查 \] 。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="0d2b7-118">*zeroout \_ alignmentgap*：當 idl 是以「目標 NT60」或更高版本編譯時，MIDL 將會建立存根，使其在連線緩衝區內的成員或結構之間有任何對齊間距。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="0d2b7-119">命令列參數 */backward \_ 相容性 zeroout \_ alignmentgap* 指示 MIDL 停用此功能。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="0d2b7-120">在下列範例結構中，網路緩衝區包含7個位元組對齊間距，以將超成員對齊 char 成員之後的8個。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="0d2b7-121">使用「目標 NT60 或更高版本時，MIDL 將會零出該間距，除非使用參數。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="0d2b7-122">IDL 檔案：</span><span class="sxs-lookup"><span data-stu-id="0d2b7-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="0d2b7-123">此參數可讓洩漏的風險大幅增加，進而大幅改善效能。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="0d2b7-124">*BSTR \_ byvalue \_* escape：根據預設，MIDL 編譯器不會 \\ \\ 在將字串常數轉換成類型 vt \_ TÂ或 vt LPSTR 時，處理 OLE Automation 的字串常數中的 escape 序列，例如̃ nâ€™或€̃ LPWSTR €™ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="0d2b7-125">使用這個回溯相容性切換選項，就會評估 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="0d2b7-126">*字串 \_ defaultvalue*：強制 MIDL 編譯器將 [**\[ \] defaultvalue**](defaultvalue.md)屬性中的數值字串強制轉換成 VARIANT。VT \_ I4 型別，請先將值強制轉換成正確的型別。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="0d2b7-127">這可能會導致在某些情況下遺失精確度，因此不建議使用此切換選項。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="0d2b7-128">*帶正負號的 \_ wchar \_ t*：指示 MIDL 將 wchar \_ t 類型視為已簽署，以提供 Visual Basic 的相容性。</span><span class="sxs-lookup"><span data-stu-id="0d2b7-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




