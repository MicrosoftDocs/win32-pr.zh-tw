---
title: RPC 等位
description: 封裝和 nonencapsulated 等位及其格式搭配遠端程序呼叫， (RPC) 。
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463168"
---
# <a name="rpc-unions"></a><span data-ttu-id="734c1-103">RPC 等位</span><span class="sxs-lookup"><span data-stu-id="734c1-103">RPC unions</span></span>

<span data-ttu-id="734c1-104">封裝和 nonencapsulated 等位都會共用通用聯集 \_ arm \_ 選取器<> 格式：</span><span class="sxs-lookup"><span data-stu-id="734c1-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="734c1-105">Union \_ arm<2> 欄位包含兩個部分。</span><span class="sxs-lookup"><span data-stu-id="734c1-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="734c1-106">如果等位是 MIDL 1.0 樣式聯集，則上層4位會包含與最大對齊 arm) 的聯集 arm (對齊。</span><span class="sxs-lookup"><span data-stu-id="734c1-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="734c1-107">否則，上層4位為零。</span><span class="sxs-lookup"><span data-stu-id="734c1-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="734c1-108">較低的12個位包含聯集內的 arm 數目。</span><span class="sxs-lookup"><span data-stu-id="734c1-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="734c1-109">換句話說：</span><span class="sxs-lookup"><span data-stu-id="734c1-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="734c1-110">\_ \_ Arm \_ 描述<2> 欄位包含 arm 型別描述的相對帶正負號位移。</span><span class="sxs-lookup"><span data-stu-id="734c1-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="734c1-111">不過，此欄位會使用簡單類型的優化進行多載。</span><span class="sxs-lookup"><span data-stu-id="734c1-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="734c1-112">在這些情況下，此位移欄位的上層位元組是 FC \_ 魔術 \_ UNION \_ byte (0x80) ，而 short 的下限是 arm 的實際格式字元類型。</span><span class="sxs-lookup"><span data-stu-id="734c1-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="734c1-113">因此，位移值有兩個範圍：「80 *xx*」表示 *xx* 是一種類型格式字串;以及範圍內的其他內容 (80 FF。</span><span class="sxs-lookup"><span data-stu-id="734c1-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="734c1-114">7f FF) 表示實際的位移。</span><span class="sxs-lookup"><span data-stu-id="734c1-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="734c1-115">這會從範圍 <80 00 進行位移。</span><span class="sxs-lookup"><span data-stu-id="734c1-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="734c1-116">80 FF > 無法作為位移。</span><span class="sxs-lookup"><span data-stu-id="734c1-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="734c1-117">編譯器會檢查是否有 MIDL 版本5.1.164。</span><span class="sxs-lookup"><span data-stu-id="734c1-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="734c1-118">預設 arm \_ \_ 描述<2> 欄位表示預設 arm 的聯集 arm 類型（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="734c1-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="734c1-119">如果沒有為聯集指定預設 arm，則預設 \_ arm \_ 描述<2> 欄位為0xffff，如果參數的 \_ 值與任何 arm 案例值不符，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="734c1-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="734c1-120">如果指定了預設 arm，但卻是空的，則預設的 \_ arm \_ 描述<2> 欄位為零。</span><span class="sxs-lookup"><span data-stu-id="734c1-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="734c1-121">否則，預設的 \_ arm \_ 描述<2> 欄位與 \_ arm 描述的位移 \_ \_<2> 欄位具有相同的語義。</span><span class="sxs-lookup"><span data-stu-id="734c1-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="734c1-122">以下是摘要：</span><span class="sxs-lookup"><span data-stu-id="734c1-122">The following is a summary:</span></span>

-   <span data-ttu-id="734c1-123">0-空的預設值</span><span class="sxs-lookup"><span data-stu-id="734c1-123">0 - empty default</span></span>
-   <span data-ttu-id="734c1-124">FFFF-沒有預設值</span><span class="sxs-lookup"><span data-stu-id="734c1-124">FFFF - no default</span></span>
-   <span data-ttu-id="734c1-125">80xx-簡單類型</span><span class="sxs-lookup"><span data-stu-id="734c1-125">80xx - simple type</span></span>
-   <span data-ttu-id="734c1-126">其他相對位移</span><span class="sxs-lookup"><span data-stu-id="734c1-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="734c1-127">封裝聯集</span><span class="sxs-lookup"><span data-stu-id="734c1-127">Encapsulated Unions</span></span>

<span data-ttu-id="734c1-128">封裝聯集是來自 IDL 中的特殊聯集語法。</span><span class="sxs-lookup"><span data-stu-id="734c1-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="734c1-129">實際上，封裝的等位是一種組合結構，其中的判別欄位位於結構的開頭，而聯集則是唯一的另一個成員。</span><span class="sxs-lookup"><span data-stu-id="734c1-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="734c1-130">封裝聯集的參數 \_ 類型<1> 欄位有兩個部分。</span><span class="sxs-lookup"><span data-stu-id="734c1-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="734c1-131">較低的半值會提供實際的 switch 型別，而上半個位元組會提供不進入的記憶體增量，也就是記憶體指標必須遞增以跳過 switch \_ 為欄位的數量，其中包含切換 \_ 為存根架構結構的 () 欄位和實際聯集欄位之間的任何填補。</span><span class="sxs-lookup"><span data-stu-id="734c1-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="734c1-132">記憶體 \_ 大小<2> 欄位為聯集的大小，與 nonencapsulated 聯集相同。</span><span class="sxs-lookup"><span data-stu-id="734c1-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="734c1-133">若要取得包含聯集之結構的總大小，請將記憶體 \_ 大小<2> 增加至記憶體增量，也就是切換類型<1> 欄位的上半部半形， \_ 然後對齊相對於增量的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="734c1-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="734c1-134">Nonencapsulated 聯集</span><span class="sxs-lookup"><span data-stu-id="734c1-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="734c1-135">Nonencapsulated 聯集是一般情況，其中 union 是一個引數或欄位，而參數分別是另一個引數或欄位。</span><span class="sxs-lookup"><span data-stu-id="734c1-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="734c1-136">其中：</span><span class="sxs-lookup"><span data-stu-id="734c1-136">Where:</span></span>

<span data-ttu-id="734c1-137">參數 \_ 類型<1> 欄位是判別的格式字元。</span><span class="sxs-lookup"><span data-stu-id="734c1-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="734c1-138">參數 \_ 是 \_ 描述項<> 欄位是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。</span><span class="sxs-lookup"><span data-stu-id="734c1-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="734c1-139">不過，針對參數的 \_ \_ 描述<>，如果等位內嵌在結構中，參數的位移欄位 \_ 就是 \_ 描述<> 是 \_ 從結構中聯集位置的欄位 (而不是從結構) 的開頭。</span><span class="sxs-lookup"><span data-stu-id="734c1-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="734c1-140">[大小] 和 [arm 描述] 的 [位移] \_ \_ \_ \_ \_<2> 欄位提供聯集大小和 arm 描述的位移，這與封裝聯集的大小和 arm 描述完全相同，而且會由相同類型的所有 nonencapsulated 聯集共用：</span><span class="sxs-lookup"><span data-stu-id="734c1-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 